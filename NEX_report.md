# NEX

**Generated** : 2026-08-27T21:43:41.974923+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €142.70  

> 🟡 **WAIT-FOR-DIP** — spot +6.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €142.70 (+6.9% vs entrée) · entrée €133.51 · stop €129.70 · T1 €136.88 · R/R 0.88  
> ↳ P(T1 av. stop) 64 % · EV/risk 0.152 · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.260 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €132.84–€134.19 (mid €133.51)
- Spot actuel : €142.70 (+6.9% au-dessus de la zone — repli à attendre)
- Stop : €129.70 (stop swing_plan-based (-9.11%))
- Targets : T1 €136.88 · R/R 0.88 | T2 €140.24 · R/R 1.77 | T3 €143.60 · R/R 2.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.70


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.11 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **0.486 pt plus bas** dans le cas TYPIQUE (médiane), 0.486 au p90, **0.486 au pire**
   - perte réelle **9.596 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 9.11 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0004 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0046** [0.0004 ; 0.0245] _(largeur 2.4 pt, n_eff 173.1)_
   - swing : **0.4558** [0.4039 ; 0.5085] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4348** [0.3833 ; 0.4874] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 13.9 observations effectives », dont la borne haute a 95 % vaut environ 21.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (48.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.25 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0127** (β de hausse 1.0945, asymétrie 0.9252) vs FCHI — 618 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 127.4429 sur atr_grid (4.0 ATR, 10.692 %) — p(stop avant cible) 0.1088 [0.08 ; 0.14], R/R 1.377, perte reelle 10.692 % (gap inclus), CVaR 10.692 %, EV 0.5879 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.009 %) — p(stop avant cible) 0.5506 [0.50 ; 0.60], R/R 2.278, perte reelle 6.462 % (gap inclus), EV -1.1422 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.551, borne haute 0.602 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 5.9 % x 14.72 % + P(rien) 39.0 % x 3.96 % ne couvrent pas P(stop) 55.1 % x 6.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.88 ATR (stop 6.38 %) — p(stop avant cible) 0.3542 [0.31 ; 0.41], R/R 1.812, perte reelle 8.124 % (gap inclus), EV -0.3357 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 5.9 % x 14.72 % + P(rien) 58.7 % x 2.85 % ne couvrent pas P(stop) 35.4 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 4.48 ATR (stop 13.332 %) — p(stop avant cible) 0.0463 [0.03 ; 0.07], R/R 1.104, perte reelle 13.332 % (gap inclus), EV 0.5758 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.33 % > budget 12.00 %
   - 🟢 support a 9.17 ATR (stop 25.867 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.569, perte reelle 25.867 % (gap inclus), EV 0.6716 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.87 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.668 %) — p(stop avant cible) 0.909 [0.88 ; 0.94], R/R 8.95, perte reelle 1.645 % (gap inclus), EV -0.789 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 8.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.909, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.79 %) : P(cible) 1.4 % x 14.72 % + P(rien) 7.7 % x 6.55 % ne couvrent pas P(stop) 90.9 % x 1.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.336 %) — p(stop avant cible) 0.8377 [0.80 ; 0.87], R/R 5.473, perte reelle 2.69 % (gap inclus), EV -1.1074 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.838, borne haute 0.874 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 2.1 % x 14.72 % + P(rien) 14.1 % x 5.91 % ne couvrent pas P(stop) 83.8 % x 2.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.005 %) — p(stop avant cible) 0.7476 [0.70 ; 0.79], R/R 3.928, perte reelle 3.748 % (gap inclus), EV -1.191 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.748, borne haute 0.791 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 3.2 % x 14.72 % + P(rien) 22.0 % x 5.16 % ne couvrent pas P(stop) 74.8 % x 3.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.673 %) — p(stop avant cible) 0.6836 [0.63 ; 0.73], R/R 3.275, perte reelle 4.496 % (gap inclus), EV -1.1815 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.684, borne haute 0.731 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 4.0 % x 14.72 % + P(rien) 27.6 % x 4.71 % ne couvrent pas P(stop) 68.4 % x 4.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.341 %) — p(stop avant cible) 0.6157 [0.56 ; 0.67], R/R 2.805, perte reelle 5.248 % (gap inclus), EV -1.0139 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.616, borne haute 0.666 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 5.2 % x 14.72 % + P(rien) 33.2 % x 4.37 % ne couvrent pas P(stop) 61.6 % x 5.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.88 ATR (stop 5.821 %) — p(stop avant cible) 0.4082 [0.36 ; 0.46], R/R 1.812, perte reelle 8.124 % (gap inclus), EV -0.7064 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 5.9 % x 14.72 % + P(rien) 53.3 % x 3.27 % ne couvrent pas P(stop) 40.8 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 7.351 %) — p(stop avant cible) 0.2673 [0.22 ; 0.32], R/R 1.767, perte reelle 8.333 % (gap inclus), EV 0.2235 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 8.019 %) — p(stop avant cible) 0.2218 [0.18 ; 0.27], R/R 1.718, perte reelle 8.571 % (gap inclus), EV 0.4571 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 9.355 %) — p(stop avant cible) 0.1601 [0.12 ; 0.20], R/R 1.534, perte reelle 9.596 % (gap inclus), EV 0.5383 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 10.692 %) — p(stop avant cible) 0.1088 [0.08 ; 0.14], R/R 1.377, perte reelle 10.692 % (gap inclus), EV 0.5879 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 4.48 ATR (stop 12.773 %) — p(stop avant cible) 0.0598 [0.04 ; 0.09], R/R 1.153, perte reelle 12.773 % (gap inclus), EV 0.5588 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.77 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 14.701 %) — p(stop avant cible) 0.0272 [0.01 ; 0.05], R/R 1.001, perte reelle 14.701 % (gap inclus), EV 0.6045 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.70 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 16.038 %) — p(stop avant cible) 0.0143 [0.01 ; 0.03], R/R 0.918, perte reelle 16.038 % (gap inclus), EV 0.623 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.04 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 17.374 %) — p(stop avant cible) 0.0098 [0.00 ; 0.02], R/R 0.847, perte reelle 17.374 % (gap inclus), EV 0.6334 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.37 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 18.711 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 0.787, perte reelle 18.711 % (gap inclus), EV 0.6597 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 20.047 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.734, perte reelle 20.047 % (gap inclus), EV 0.6669 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.05 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 21.384 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.689, perte reelle 21.384 % (gap inclus), EV 0.6688 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.38 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 142.7, ATR14 3.8143 (2.673 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.351 ATR = 0.938 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.134 % | 142.5093 | 87.94 % | 91.56 % | 93.32 % | 95.37 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.267 % | 142.3186 | 82.16 % | 87.83 % | 90.37 % | 93.21 % | 95.45 % | 97.0 % |
| 0.15 ATR | 0.401 % | 142.1279 | 75.49 % | 83.61 % | 86.94 % | 90.26 % | 93.97 % | 95.7 % |
| 0.2 ATR | 0.535 % | 141.9371 | 68.92 % | 78.61 % | 83.4 % | 88.29 % | 92.48 % | 95.0 % |
| 0.25 ATR | 0.668 % | 141.7464 | 62.35 % | 73.8 % | 79.27 % | 85.04 % | 90.41 % | 93.81 % |
| 0.35 ATR | 0.936 % | 141.365 | 50.1 % | 64.57 % | 72.0 % | 78.94 % | 86.45 % | 91.61 % |
| 0.5 ATR | 1.336 % | 140.7929 | 34.8 % | 52.8 % | 61.59 % | 70.77 % | 80.22 % | 87.61 % |
| 0.75 ATR | 2.005 % | 139.8393 | 20.29 % | 36.7 % | 47.74 % | 58.96 % | 70.33 % | 81.12 % |
| 1.0 ATR | 2.673 % | 138.8857 | 10.69 % | 24.53 % | 35.07 % | 48.62 % | 61.52 % | 74.53 % |
| 1.25 ATR | 3.341 % | 137.9321 | 4.9 % | 16.29 % | 25.15 % | 39.67 % | 54.6 % | 68.13 % |
| 1.5 ATR | 4.009 % | 136.9786 | 2.45 % | 11.09 % | 18.47 % | 30.71 % | 46.98 % | 60.74 % |
| 2.0 ATR | 5.346 % | 135.0714 | 0.78 % | 5.2 % | 10.02 % | 19.39 % | 35.51 % | 51.05 % |
| 2.5 ATR | 6.682 % | 133.1643 | 0.49 % | 2.65 % | 5.6 % | 11.42 % | 24.93 % | 39.26 % |
| 3.0 ATR | 8.019 % | 131.2571 | 0.2 % | 1.67 % | 3.24 % | 7.19 % | 17.71 % | 30.67 % |
| 4.0 ATR | 10.692 % | 127.4429 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.62 % | 18.08 % |
| 6.0 ATR | 16.038 % | 119.8143 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.14 ATR | 1.59 ATR | 2.04 ATR |
| **3 s.** | 0.31 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.26 ATR | 1.44 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.97 ATR | 1.10 ATR | 1.44 ATR | 1.75 ATR | 1.97 ATR | 2.67 ATR | 3.41 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.59 ATR | 2.12 ATR | 2.50 ATR | 2.84 ATR | 3.76 ATR | 4.84 ATR |
| **20 s.** | 0.98 ATR | 2.04 ATR | 2.26 ATR | 2.86 ATR | 3.45 ATR | 3.85 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.4–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (79.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.621–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.005 %, prix 139.8389), p(touche) 36.7 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.804–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.673 %, prix 138.8856), p(touche) 35.07 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.101–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.341 %, prix 137.9324), p(touche) 39.67 % (en stress 94.12 %)  ✅ optimum identifie (63.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.586–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.346 %, prix 135.0713), p(touche) 35.51 % (en stress 99.02 %)  ✅ optimum identifie (70.9 % des re-echantillons)
- **20 seance(s)** : plage utile 2.257–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (6.682 %, prix 133.1648), p(touche) 39.26 % (en stress 98.02 %)  ✅ optimum identifie (69.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.025 | EV/share : €0.097 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 27 % | T3 10 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.2 | bear 16.5 | side 73.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 428.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.924% → cible +1.126% / stop −8.0%, p_fill 21%, n_eff≈13.9) : P(cible|rempli) **47%** · **EV/risk +0.004** (×p_fill ; si rempli +0.14% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→64% · +1.0%→50% · +2.0%→24% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 3.0% (p90 4.72%) · excursion haute méd. +1.0% / basse méd. −1.43%
- Profil de vol intra : ouverture 1.747% vs midi 0.528% vs clôture 0.728% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; neutre — autocorr -0.028)_ ; drift intra méd. -0.4% ; recovery-V 18%
- **σ réalisé intraday** 2.084% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 71% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 141.89 (VA 141.33–142.87 ; dernier close 141.35)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 17% · rebond 56% · **stop −2.01%** sous le fill (sous le bruit) · cible +1.25% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.35% · baisse 33% (gap-down >1% 6% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.43% (p90 −1.93%) · haut méd +0.29% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −2.08%) · haut méd +0.44% · range méd 1.3%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −2.31%) · haut méd +0.57% · range méd 1.41%
- Excursion ouverture 60min (n=160) : bas méd −0.81% (p90 −2.58%) · haut méd +0.59% · range méd 1.57%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 141.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 63% (91/159) · gap 12% · délai 3.8min · rebond 46% (45/91) (MFE +0.78%)
   - −1.0% : fill 30min 28% · séance 55% (74/159) · gap 6% · délai 21.7min · rebond 46% (36/74) (MFE +0.86%)
   - −1.5% : fill 30min 17% · séance 42% (55/159) · gap 1% · délai 45.4min · rebond 44% (26/55) (MFE +0.8%)
   - −2.0% : fill 30min 12% · séance 28% (39/159) · gap 1% · délai 53.1min · rebond 54% (20/39) (MFE +1.14%)
   - −3.0% : fill 30min 4% · séance 17% (23/159) · gap 0% · délai 133.5min · rebond 56% (13/23) (MFE +1.25%)
   - −4.0% : fill 30min 0% · séance 6% (9/159) · gap 0% · délai 350.2min · rebond 11% (3/9) (MFE +0.48%)
   - −5.0% : fill 30min 0% · séance 2% (3/159) · gap 0% · délai 410.2min · rebond 42% (1/3) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.15%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.96%) → stop au-delà de −0.58% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.6%) → stop au-delà de −0.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=329 jambes) : jambe baissière méd −1.09% (p90 −2.42%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 80% (25/30) · rebond 55% (13/25)
      · −2.0% : fill 50% (16/30) · rebond 44% (7/16)
      · −3.0% : fill 32% (11/30) · rebond 44% (6/11)
      · −4.0% : fill 21% (6/30) · rebond 12% (2/6)
      · −5.0% : fill 12% (3/30) · rebond 42% (1/3)
   - **flat** (33 séances) :
      · −1.0% : fill 59% (20/33) · rebond 40% (9/20)
      · −2.0% : fill 30% (10/33) · rebond 38% (4/10)
      · −3.0% : fill 18% (6/33) · rebond 45% (3/6)
      · −4.0% : fill 8% (2/33) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/33) · rebond 0% (0/0)
   - **gap-up** (96 séances) :
      · −1.0% : fill 44% (29/96) · rebond 45% (14/29)
      · −2.0% : fill 20% (13/96) · rebond 76% (9/13)
      · −3.0% : fill 11% (6/96) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/96) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/96) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 68% si les 15 1res min sont vertes (86 cas) · 20% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **45min** → P(séance verte=clôture>ouverture) 75% si début vert vs 22% si rouge (base 46% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 249min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **75%** · continue >prix actuel 48% ; creux résiduel méd -0.83% (q20 -2.03%) → **SL/trailing à −2.03%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +1.63% → **scale +1.06% / runner +1.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 55%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.04%** (au-delà de la MAE q10 -3.04%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.01% .. +2.31%] · haut q95 +2.62% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.82% .. +2.66%] · haut q95 +2.83% · bas q05 -3.24%
   - 2h (n=160) : retour [-3.55% .. +2.56%] · haut q95 +2.94% · bas q05 -3.74%
   - 4h (n=160) : retour [-3.12% .. +2.74%] · haut q95 +3.04% · bas q05 -3.88%
   - 6h (n=160) : retour [-3.81% .. +3.51%] · haut q95 +3.91% · bas q05 -4.17%
   - session (n=160) : retour [-3.51% .. +2.88%] · haut q95 +4.18% · bas q05 -4.67%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 55.0  _(momentum haussier)_
- **ADX** : 13.7  _(pas de tendance nette)_
- **MACD** : hist 0.439  _(pas de croisement recent)_
- **BB** : %B 0.76 · largeur 10.9%
- **ATR** : 3.81 (34.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.258  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 65.4  _(marche en range (choppy))_
- **MA** : MA20 138.76 · MA50 138.39 · MA200 133.51  _(prix > MA20)_
- **Dist MA** : MA20 +2.8% · MA50 +3.1% · MA200 +6.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (859030 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
