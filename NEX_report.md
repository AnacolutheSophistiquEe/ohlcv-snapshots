# NEX

**Generated** : 2026-08-31T00:09:22.273348+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €143.50  

> 🟡 **WAIT-FOR-DIP** — spot +7.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €143.50 (+7.2% vs entrée) · entrée €133.87 · stop €130.09 · T1 €137.24 · R/R 0.89  
> ↳ P(T1 av. stop) 66 % · EV/risk 0.218 · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.190 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €133.20–€134.55 (mid €133.87)
- Spot actuel : €143.50 (+7.2% au-dessus de la zone — repli à attendre)
- Stop : €130.09 (stop swing_plan-based (-9.35%))
- Targets : T1 €137.24 · R/R 0.89 | T2 €140.61 · R/R 1.78 | T3 €143.98 · R/R 2.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €130.09


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.35 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **0.246 pt plus bas** dans le cas TYPIQUE (médiane), 0.246 au p90, **0.246 au pire**
   - perte réelle **9.596 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 9.35 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0002 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0045** [0.0004 ; 0.0243] _(largeur 2.4 pt, n_eff 173.1)_
   - swing : **0.4532** [0.4013 ; 0.5059] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4391** [0.3875 ; 0.4917] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 11.0 observations effectives », dont la borne haute a 95 % vaut environ 27.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (50.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.25 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0127** (β de hausse 1.0985, asymétrie 0.9219) vs FCHI — 618 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 128.3571 sur atr_grid (4.0 ATR, 10.553 %) — p(stop avant cible) 0.1175 [0.09 ; 0.15], R/R 1.335, perte reelle 10.553 % (gap inclus), CVaR 10.553 %, EV 0.5219 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.957 %) — p(stop avant cible) 0.5536 [0.50 ; 0.61], R/R 2.253, perte reelle 6.254 % (gap inclus), EV -1.0888 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.554, borne haute 0.605 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 6.3 % x 14.09 % + P(rien) 38.3 % x 3.87 % ne couvrent pas P(stop) 55.4 % x 6.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.1 ATR (stop 7.001 %) — p(stop avant cible) 0.3018 [0.26 ; 0.35], R/R 1.734, perte reelle 8.124 % (gap inclus), EV 0.0081 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 4.72 ATR (stop 13.916 %) — p(stop avant cible) 0.0386 [0.02 ; 0.06], R/R 1.013, perte reelle 13.916 % (gap inclus), EV 0.543 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.92 % > budget 12.00 %
   - 🟢 support a 9.45 ATR (stop 26.384 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.534, perte reelle 26.384 % (gap inclus), EV 0.6379 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.38 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.66 %) — p(stop avant cible) 0.9116 [0.88 ; 0.94], R/R 8.618, perte reelle 1.635 % (gap inclus), EV -0.8112 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 8.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.912, borne haute 0.938 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 1.4 % x 14.09 % + P(rien) 7.5 % x 6.51 % ne couvrent pas P(stop) 91.2 % x 1.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.319 %) — p(stop avant cible) 0.8422 [0.80 ; 0.88], R/R 5.238, perte reelle 2.69 % (gap inclus), EV -1.1471 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.842, borne haute 0.878 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 2.1 % x 14.09 % + P(rien) 13.6 % x 5.99 % ne couvrent pas P(stop) 84.2 % x 2.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 1.979 %) — p(stop avant cible) 0.7564 [0.71 ; 0.80], R/R 3.759, perte reelle 3.748 % (gap inclus), EV -1.3139 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.756, borne haute 0.799 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 3.2 % x 14.09 % + P(rien) 21.1 % x 5.06 % ne couvrent pas P(stop) 75.6 % x 3.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.638 %) — p(stop avant cible) 0.6873 [0.64 ; 0.73], R/R 3.134, perte reelle 4.496 % (gap inclus), EV -1.2326 % — **REFUSE**
      - refuse : cible atteinte seulement 4.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.687, borne haute 0.734 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.23 %) : P(cible) 4.4 % x 14.09 % + P(rien) 26.8 % x 4.60 % ne couvrent pas P(stop) 68.7 % x 4.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.298 %) — p(stop avant cible) 0.6191 [0.57 ; 0.67], R/R 2.735, perte reelle 5.152 % (gap inclus), EV -1.0193 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.619, borne haute 0.669 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 5.6 % x 14.09 % + P(rien) 32.5 % x 4.25 % ne couvrent pas P(stop) 61.9 % x 5.15 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 4.617 %) — p(stop avant cible) 0.4896 [0.44 ; 0.54], R/R 1.831, perte reelle 7.697 % (gap inclus), EV -1.2639 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 6.3 % x 14.09 % + P(rien) 44.7 % x 3.61 % ne couvrent pas P(stop) 49.0 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.1 ATR (stop 6.336 %) — p(stop avant cible) 0.3551 [0.31 ; 0.41], R/R 1.734, perte reelle 8.124 % (gap inclus), EV -0.388 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 6.3 % x 14.09 % + P(rien) 58.2 % x 2.76 % ne couvrent pas P(stop) 35.5 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 7.914 %) — p(stop avant cible) 0.2281 [0.19 ; 0.27], R/R 1.644, perte reelle 8.571 % (gap inclus), EV 0.3974 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 9.233 %) — p(stop avant cible) 0.1627 [0.13 ; 0.20], R/R 1.468, perte reelle 9.596 % (gap inclus), EV 0.4839 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 10.553 %) — p(stop avant cible) 0.1175 [0.09 ; 0.15], R/R 1.335, perte reelle 10.553 % (gap inclus), EV 0.5219 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 4.72 ATR (stop 13.252 %) — p(stop avant cible) 0.0512 [0.03 ; 0.08], R/R 1.063, perte reelle 13.252 % (gap inclus), EV 0.527 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.25 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 14.51 %) — p(stop avant cible) 0.0272 [0.01 ; 0.05], R/R 0.971, perte reelle 14.51 % (gap inclus), EV 0.5756 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.51 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 15.829 %) — p(stop avant cible) 0.0143 [0.01 ; 0.03], R/R 0.89, perte reelle 15.829 % (gap inclus), EV 0.5922 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.83 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 17.148 %) — p(stop avant cible) 0.0105 [0.00 ; 0.03], R/R 0.822, perte reelle 17.148 % (gap inclus), EV 0.591 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.15 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 18.467 %) — p(stop avant cible) 0.0057 [0.00 ; 0.02], R/R 0.763, perte reelle 18.467 % (gap inclus), EV 0.6152 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.47 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 19.786 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.712, perte reelle 19.786 % (gap inclus), EV 0.6345 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.79 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 21.105 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.668, perte reelle 21.105 % (gap inclus), EV 0.6361 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.10 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 143.5, ATR14 3.7857 (2.638 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.35 ATR = 0.923 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.132 % | 143.3107 | 87.84 % | 91.56 % | 93.22 % | 95.37 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.264 % | 143.1214 | 82.06 % | 87.83 % | 90.28 % | 93.21 % | 95.45 % | 97.0 % |
| 0.15 ATR | 0.396 % | 142.9321 | 75.39 % | 83.61 % | 86.84 % | 90.26 % | 93.97 % | 95.7 % |
| 0.2 ATR | 0.528 % | 142.7429 | 68.82 % | 78.51 % | 83.3 % | 88.29 % | 92.48 % | 95.0 % |
| 0.25 ATR | 0.66 % | 142.5536 | 62.25 % | 73.7 % | 79.17 % | 85.04 % | 90.41 % | 93.81 % |
| 0.35 ATR | 0.923 % | 142.175 | 50.0 % | 64.47 % | 71.91 % | 78.94 % | 86.45 % | 91.61 % |
| 0.5 ATR | 1.319 % | 141.6071 | 34.71 % | 52.7 % | 61.49 % | 70.67 % | 80.22 % | 87.61 % |
| 0.75 ATR | 1.979 % | 140.6607 | 20.29 % | 36.6 % | 47.64 % | 58.86 % | 70.33 % | 81.12 % |
| 1.0 ATR | 2.638 % | 139.7143 | 10.69 % | 24.53 % | 34.97 % | 48.52 % | 61.52 % | 74.53 % |
| 1.25 ATR | 3.298 % | 138.7679 | 4.9 % | 16.29 % | 25.05 % | 39.57 % | 54.5 % | 68.13 % |
| 1.5 ATR | 3.957 % | 137.8214 | 2.45 % | 11.09 % | 18.37 % | 30.61 % | 46.88 % | 60.64 % |
| 2.0 ATR | 5.276 % | 135.9286 | 0.78 % | 5.2 % | 9.92 % | 19.29 % | 35.41 % | 51.05 % |
| 2.5 ATR | 6.595 % | 134.0357 | 0.49 % | 2.65 % | 5.6 % | 11.42 % | 24.93 % | 39.26 % |
| 3.0 ATR | 7.914 % | 132.1429 | 0.2 % | 1.67 % | 3.24 % | 7.19 % | 17.71 % | 30.67 % |
| 4.0 ATR | 10.553 % | 128.3571 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.62 % | 18.08 % |
| 6.0 ATR | 15.829 % | 120.7857 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.29 % | 4.3 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.14 ATR | 1.59 ATR | 2.04 ATR |
| **3 s.** | 0.31 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.25 ATR | 1.44 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.10 ATR | 1.43 ATR | 1.75 ATR | 1.97 ATR | 2.67 ATR | 3.41 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.12 ATR | 2.50 ATR | 2.84 ATR | 3.76 ATR | 4.83 ATR |
| **20 s.** | 0.98 ATR | 2.04 ATR | 2.26 ATR | 2.86 ATR | 3.45 ATR | 3.85 ATR | 5.17 ATR | 5.90 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.399–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (78.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.62–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.979 %, prix 140.6601), p(touche) 36.6 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.802–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.638 %, prix 139.7145), p(touche) 34.97 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.098–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.298 %, prix 138.7674), p(touche) 39.57 % (en stress 94.12 %)  ✅ optimum identifie (62.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.582–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.276 %, prix 135.9289), p(touche) 35.41 % (en stress 98.04 %)  ✅ optimum identifie (71.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.257–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (6.595 %, prix 134.0362), p(touche) 39.26 % (en stress 98.02 %)  ✅ optimum identifie (69.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.02 | EV/share : €0.076 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 26 % | T3 10 %
- Kelly (position) : f* 0.028 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.0 | bear 16.6 | side 73.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 430.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.054% → cible +1.125% / stop −8.0%, p_fill 19%, n_eff≈11.0) : P(cible|rempli) **32%** · **EV/risk +0.001** (×p_fill ; si rempli +0.06% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→62% · +1.0%→50% · +2.0%→24% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 2.95% (p90 4.72%) · excursion haute méd. +1.0% / basse méd. −1.4%
- Profil de vol intra : ouverture 1.746% vs midi 0.516% vs clôture 0.715% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 46% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; neutre — autocorr -0.028)_ ; drift intra méd. -0.364% ; recovery-V 15%
- **σ réalisé intraday** 2.0% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 64% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 144.9706 (VA 144.0119–145.4131 ; dernier close 143.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 17% · rebond 50% · **stop −1.94%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 34% (gap-down >1% 5% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.49% (p90 −1.86%) · haut méd +0.24% · range méd 1.04%
- Excursion ouverture 15min (n=160) : bas méd −0.61% (p90 −1.97%) · haut méd +0.42% · range méd 1.29%
- Excursion ouverture 30min (n=160) : bas méd −0.74% (p90 −2.26%) · haut méd +0.55% · range méd 1.41%
- Excursion ouverture 60min (n=160) : bas méd −0.84% (p90 −2.5%) · haut méd +0.58% · range méd 1.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 143.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 44% · séance 59% (91/159) · gap 11% · délai 3.0min · rebond 44% (44/91) (MFE +0.74%)
   - −1.0% : fill 30min 27% · séance 52% (75/159) · gap 5% · délai 23.2min · rebond 44% (36/75) (MFE +0.83%)
   - −1.5% : fill 30min 16% · séance 40% (56/159) · gap 1% · délai 41.2min · rebond 42% (26/56) (MFE +0.74%)
   - −2.0% : fill 30min 11% · séance 28% (40/159) · gap 1% · délai 57.0min · rebond 51% (20/40) (MFE +1.02%)
   - −3.0% : fill 30min 4% · séance 17% (24/159) · gap 0% · délai 207.9min · rebond 50% (13/24) (MFE +1.05%)
   - −4.0% : fill 30min 0% · séance 6% (9/159) · gap 0% · délai 350.2min · rebond 11% (3/9) (MFE +0.48%)
   - −5.0% : fill 30min 0% · séance 2% (3/159) · gap 0% · délai 410.2min · rebond 42% (1/3) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.99%) → stop au-delà de −0.81% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.9%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −0.6%) → stop au-delà de −0.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=324 jambes) : jambe baissière méd −1.09% (p90 −2.39%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 80% (25/30) · rebond 55% (13/25)
      · −2.0% : fill 50% (16/30) · rebond 44% (7/16)
      · −3.0% : fill 32% (11/30) · rebond 44% (6/11)
      · −4.0% : fill 21% (6/30) · rebond 12% (2/6)
      · −5.0% : fill 12% (3/30) · rebond 42% (1/3)
   - **flat** (35 séances) :
      · −1.0% : fill 58% (21/35) · rebond 37% (9/21)
      · −2.0% : fill 32% (11/35) · rebond 32% (4/11)
      · −3.0% : fill 21% (7/35) · rebond 33% (3/7)
      · −4.0% : fill 7% (2/35) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/35) · rebond 0% (0/0)
   - **gap-up** (94 séances) :
      · −1.0% : fill 40% (29/94) · rebond 45% (14/29)
      · −2.0% : fill 18% (13/94) · rebond 76% (9/13)
      · −3.0% : fill 10% (6/94) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/94) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/94) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 70% si les 15 1res min sont vertes (85 cas) · 18% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 75% si début vert vs 21% si rouge (base 45% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 249min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **75%** · continue >prix actuel 50% ; creux résiduel méd -0.94% (q20 -1.96%) → **SL/trailing à −1.96%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +1.67% → **scale +1.18% / runner +1.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **21%** (continue à baisser 56%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.14%** (au-delà de la MAE q10 -3.14%), cible rebond +1.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.95% .. +2.23%] · haut q95 +2.55% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.81% .. +2.54%] · haut q95 +2.74% · bas q05 -3.24%
   - 2h (n=160) : retour [-3.45% .. +2.49%] · haut q95 +2.93% · bas q05 -3.73%
   - 4h (n=160) : retour [-2.92% .. +3.24%] · haut q95 +3.34% · bas q05 -3.82%
   - 6h (n=160) : retour [-3.72% .. +3.69%] · haut q95 +3.99% · bas q05 -4.15%
   - session (n=160) : retour [-3.45% .. +2.85%] · haut q95 +4.02% · bas q05 -4.66%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 59.4  _(momentum haussier)_
- **ADX** : 13.8  _(pas de tendance nette)_
- **MACD** : hist 0.519  _(pas de croisement recent)_
- **BB** : %B 0.79 · largeur 10.2%
- **ATR** : 3.79 (33.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.186  _(distribution)_
- **Vol ratio** : 0.34  _(volume atone)_
- **Choppiness** : 65.1  _(marche en range (choppy))_
- **MA** : MA20 139.34 · MA50 138.09 · MA200 133.63  _(prix > MA20)_
- **Dist MA** : MA20 +3.0% · MA50 +3.9% · MA200 +7.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (896524 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
