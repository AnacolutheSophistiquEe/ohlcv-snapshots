# NEX

**Generated** : 2026-09-01T21:43:50.042056+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €137.50  

> 🟡 **WAIT-FOR-DIP** — spot +4.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €137.50 (+4.7% vs entrée) · entrée €131.28 · stop €127.57 · T1 €134.53 · R/R 0.88  
> ↳ P(T1 av. stop) 70 % · EV/risk 0.052 · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.290 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €130.63–€131.93 (mid €131.28)
- Spot actuel : €137.50 (+4.7% au-dessus de la zone — repli à attendre)
- Stop : €127.57 (stop swing_plan-based (-7.22%))
- Targets : T1 €134.53 · R/R 0.88 | T2 €137.79 · R/R 1.75 | T3 €141.05 · R/R 2.63
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €127.57


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.22 %)** : le gap seul le franchit 0.391 % des séances (5 fois sur 1280).
   - exécution **1.047 pt plus bas** dans le cas TYPIQUE (médiane), 1.879 au p90, **2.376 au pire**
   - perte réelle **8.333 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 7.22 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0043 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0044** [0.0004 ; 0.0241] _(largeur 2.4 pt, n_eff 173.1)_
   - swing : **0.4535** [0.4016 ; 0.5062] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.435** [0.3835 ; 0.4876] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.9 observations effectives », dont la borne haute a 95 % vaut environ 17.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.25 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0139** (β de hausse 1.097, asymétrie 0.9242) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 122.6714 sur atr_grid (4.0 ATR, 10.784 %) — p(stop avant cible) 0.1009 [0.07 ; 0.14], R/R 1.77, perte reelle 10.784 % (gap inclus), CVaR 10.784 %, EV 0.6905 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.52 ATR (stop 3.119 %) — p(stop avant cible) 0.6337 [0.58 ; 0.68], R/R 3.774, perte reelle 5.057 % (gap inclus), EV -1.0273 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.634, borne haute 0.683 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 2.2 % x 19.09 % + P(rien) 34.4 % x 5.11 % ne couvrent pas P(stop) 63.4 % x 5.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 4.044 %) — p(stop avant cible) 0.5412 [0.49 ; 0.59], R/R 2.846, perte reelle 6.706 % (gap inclus), EV -1.1554 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.541, borne haute 0.593 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 2.5 % x 19.09 % + P(rien) 43.3 % x 4.59 % ne couvrent pas P(stop) 54.1 % x 6.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.15 ATR (stop 10.205 %) — p(stop avant cible) 0.1266 [0.09 ; 0.16], R/R 1.87, perte reelle 10.205 % (gap inclus), EV 0.6564 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 8.03 ATR (stop 23.358 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.817, perte reelle 23.358 % (gap inclus), EV 0.7618 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.36 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.674 %) — p(stop avant cible) 0.9105 [0.88 ; 0.94], R/R 11.504, perte reelle 1.659 % (gap inclus), EV -0.7826 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 11.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.910, borne haute 0.937 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 0.7 % x 19.09 % + P(rien) 8.2 % x 7.16 % ne couvrent pas P(stop) 91.0 % x 1.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.52 ATR (stop 2.221 %) — p(stop avant cible) 0.7329 [0.68 ; 0.78], R/R 4.612, perte reelle 4.138 % (gap inclus), EV -1.2943 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.733, borne haute 0.777 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.29 %) : P(cible) 1.5 % x 19.09 % + P(rien) 25.2 % x 5.74 % ne couvrent pas P(stop) 73.3 % x 4.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.696 %) — p(stop avant cible) 0.6828 [0.63 ; 0.73], R/R 4.183, perte reelle 4.563 % (gap inclus), EV -1.179 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.683, borne haute 0.730 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 2.2 % x 19.09 % + P(rien) 29.5 % x 5.14 % ne couvrent pas P(stop) 68.3 % x 4.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 4.718 %) — p(stop avant cible) 0.4726 [0.42 ; 0.53], R/R 2.48, perte reelle 7.697 % (gap inclus), EV -1.0422 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 2.5 % x 19.09 % + P(rien) 50.2 % x 4.20 % ne couvrent pas P(stop) 47.3 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 5.392 %) — p(stop avant cible) 0.4271 [0.38 ; 0.48], R/R 2.349, perte reelle 8.124 % (gap inclus), EV -0.811 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 2.5 % x 19.09 % + P(rien) 54.7 % x 3.97 % ne couvrent pas P(stop) 42.7 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.066 %) — p(stop avant cible) 0.3854 [0.34 ; 0.44], R/R 2.349, perte reelle 8.124 % (gap inclus), EV -0.4849 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 2.5 % x 19.09 % + P(rien) 58.9 % x 3.67 % ne couvrent pas P(stop) 38.5 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 6.74 %) — p(stop avant cible) 0.3177 [0.27 ; 0.37], R/R 2.349, perte reelle 8.124 % (gap inclus), EV 0.0073 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 7.414 %) — p(stop avant cible) 0.2626 [0.22 ; 0.31], R/R 2.227, perte reelle 8.571 % (gap inclus), EV 0.2614 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.15 ATR (stop 9.307 %) — p(stop avant cible) 0.1574 [0.12 ; 0.20], R/R 1.989, perte reelle 9.596 % (gap inclus), EV 0.6324 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 10.784 %) — p(stop avant cible) 0.1009 [0.07 ; 0.14], R/R 1.77, perte reelle 10.784 % (gap inclus), EV 0.6905 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 12.132 %) — p(stop avant cible) 0.0806 [0.06 ; 0.11], R/R 1.573, perte reelle 12.132 % (gap inclus), EV 0.651 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.13 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 13.481 %) — p(stop avant cible) 0.045 [0.03 ; 0.07], R/R 1.416, perte reelle 13.481 % (gap inclus), EV 0.6629 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.48 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 14.829 %) — p(stop avant cible) 0.0264 [0.01 ; 0.05], R/R 1.287, perte reelle 14.829 % (gap inclus), EV 0.6941 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.83 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 16.177 %) — p(stop avant cible) 0.0141 [0.01 ; 0.03], R/R 1.18, perte reelle 16.177 % (gap inclus), EV 0.7132 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.18 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 17.525 %) — p(stop avant cible) 0.0096 [0.00 ; 0.02], R/R 1.089, perte reelle 17.525 % (gap inclus), EV 0.7252 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 18.873 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 1.011, perte reelle 18.873 % (gap inclus), EV 0.7512 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.87 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 20.221 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.944, perte reelle 20.221 % (gap inclus), EV 0.7572 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.22 % > budget 12.00 %
   - 🟢 grid_snapped a 8.03 ATR (stop 22.461 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.85, perte reelle 22.461 % (gap inclus), EV 0.7632 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.46 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 137.5, ATR14 3.7071 (2.696 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.349 ATR = 0.941 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.135 % | 137.3146 | 87.84 % | 91.46 % | 93.22 % | 95.28 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.27 % | 137.1293 | 82.06 % | 87.73 % | 90.28 % | 93.11 % | 95.45 % | 96.9 % |
| 0.15 ATR | 0.404 % | 136.9439 | 75.39 % | 83.51 % | 86.84 % | 90.16 % | 93.97 % | 95.6 % |
| 0.2 ATR | 0.539 % | 136.7586 | 68.73 % | 78.41 % | 83.2 % | 88.19 % | 92.48 % | 94.91 % |
| 0.25 ATR | 0.674 % | 136.5732 | 62.16 % | 73.6 % | 79.08 % | 84.94 % | 90.41 % | 93.71 % |
| 0.35 ATR | 0.944 % | 136.2025 | 49.9 % | 64.38 % | 71.81 % | 78.84 % | 86.45 % | 91.51 % |
| 0.5 ATR | 1.348 % | 135.6464 | 34.71 % | 52.6 % | 61.39 % | 70.57 % | 80.22 % | 87.51 % |
| 0.75 ATR | 2.022 % | 134.7196 | 20.29 % | 36.6 % | 47.45 % | 58.76 % | 70.33 % | 81.02 % |
| 1.0 ATR | 2.696 % | 133.7929 | 10.69 % | 24.44 % | 34.87 % | 48.52 % | 61.42 % | 74.53 % |
| 1.25 ATR | 3.37 % | 132.8661 | 4.9 % | 16.19 % | 24.95 % | 39.47 % | 54.4 % | 68.03 % |
| 1.5 ATR | 4.044 % | 131.9393 | 2.45 % | 10.89 % | 18.27 % | 30.51 % | 46.79 % | 60.54 % |
| 2.0 ATR | 5.392 % | 130.0857 | 0.78 % | 5.2 % | 9.92 % | 19.29 % | 35.41 % | 51.05 % |
| 2.5 ATR | 6.74 % | 128.2321 | 0.49 % | 2.65 % | 5.6 % | 11.42 % | 24.93 % | 39.26 % |
| 3.0 ATR | 8.088 % | 126.3786 | 0.2 % | 1.67 % | 3.24 % | 7.19 % | 17.71 % | 30.67 % |
| 4.0 ATR | 10.784 % | 122.6714 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.62 % | 18.08 % |
| 6.0 ATR | 16.177 % | 115.2571 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.14 ATR | 1.58 ATR | 2.04 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.80 ATR | 1.05 ATR | 1.25 ATR | 1.44 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.10 ATR | 1.43 ATR | 1.75 ATR | 1.97 ATR | 2.67 ATR | 3.41 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.12 ATR | 2.50 ATR | 2.84 ATR | 3.76 ATR | 4.84 ATR |
| **20 s.** | 0.98 ATR | 2.04 ATR | 2.26 ATR | 2.86 ATR | 3.45 ATR | 3.85 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (79.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.619–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.022 %, prix 134.7198), p(touche) 36.6 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.799–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.696 %, prix 133.793), p(touche) 34.87 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.097–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.37 %, prix 132.8663), p(touche) 39.47 % (en stress 94.12 %)  ✅ optimum identifie (63.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.579–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.392 %, prix 130.086), p(touche) 35.41 % (en stress 98.04 %)  ✅ optimum identifie (73.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.257–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (6.74 %, prix 128.2325), p(touche) 39.26 % (en stress 98.02 %)  ✅ optimum identifie (69.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.026 | EV/share : €0.098 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 27 % | T3 10 %
- Kelly (position) : f* 0.034 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.3 | bear 16.6 | side 73.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 275.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.054% → cible +1.109% / stop −8.0%, p_fill 38%, n_eff≈16.9) : P(cible|rempli) **36%** · **EV/risk -0.005** (×p_fill ; si rempli -0.10% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=14, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=10))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→62% · +1.0%→50% · +2.0%→24% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 2.95% (p90 4.72%) · excursion haute méd. +1.0% / basse méd. −1.4%
- Profil de vol intra : ouverture 1.741% vs midi 0.52% vs clôture 0.708% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 17%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr -0.022)_ ; drift intra méd. -0.461% ; recovery-V 14%
- **σ réalisé intraday** 1.966% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 66% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 140.3438 (VA 140.1687–140.7812 ; dernier close 139.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 17% · rebond 50% · **stop −1.94%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.35% · baisse 33% (gap-down >1% 5% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.51% (p90 −1.83%) · haut méd +0.22% · range méd 1.01%
- Excursion ouverture 15min (n=160) : bas méd −0.68% (p90 −1.96%) · haut méd +0.38% · range méd 1.29%
- Excursion ouverture 30min (n=160) : bas méd −0.77% (p90 −2.25%) · haut méd +0.46% · range méd 1.41%
- Excursion ouverture 60min (n=160) : bas méd −0.86% (p90 −2.49%) · haut méd +0.58% · range méd 1.6%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 139.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 60% (91/159) · gap 11% · délai 3.8min · rebond 43% (43/91) (MFE +0.7%)
   - −1.0% : fill 30min 29% · séance 53% (75/159) · gap 5% · délai 23.0min · rebond 42% (35/75) (MFE +0.72%)
   - −1.5% : fill 30min 15% · séance 41% (56/159) · gap 1% · délai 40.6min · rebond 40% (25/56) (MFE +0.8%)
   - −2.0% : fill 30min 11% · séance 29% (41/159) · gap 1% · délai 62.1min · rebond 47% (20/41) (MFE +0.8%)
   - −3.0% : fill 30min 4% · séance 17% (24/159) · gap 0% · délai 207.9min · rebond 50% (13/24) (MFE +1.05%)
   - −4.0% : fill 30min 0% · séance 5% (9/159) · gap 0% · délai 350.2min · rebond 11% (3/9) (MFE +0.48%)
   - −5.0% : fill 30min 0% · séance 2% (3/159) · gap 0% · délai 410.2min · rebond 42% (1/3) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.98%) → stop au-delà de −0.81% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.9%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −0.6%) → stop au-delà de −0.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=323 jambes) : jambe baissière méd −1.09% (p90 −2.39%) · ~6.0 jambes/séance
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
      · −1.0% : fill 42% (29/94) · rebond 41% (13/29)
      · −2.0% : fill 21% (14/94) · rebond 64% (9/14)
      · −3.0% : fill 10% (6/94) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/94) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/94) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 70% si les 15 1res min sont vertes (85 cas) · 17% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **30min** → P(séance verte=clôture>ouverture) 76% si début vert vs 20% si rouge (base 44% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 221min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **76%** · continue >prix actuel 53% ; creux résiduel méd -0.95% (q20 -1.91%) → **SL/trailing à −1.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.15% / q75 +1.81% → **scale +1.15% / runner +1.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **20%** (continue à baisser 58%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.07%** (au-delà de la MAE q10 -3.07%), cible rebond +1.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.94% .. +2.2%] · haut q95 +2.53% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.81% .. +2.51%] · haut q95 +2.73% · bas q05 -3.24%
   - 2h (n=160) : retour [-3.4% .. +2.48%] · haut q95 +2.93% · bas q05 -3.73%
   - 4h (n=160) : retour [-2.92% .. +3.23%] · haut q95 +3.32% · bas q05 -3.81%
   - 6h (n=160) : retour [-3.68% .. +3.68%] · haut q95 +3.97% · bas q05 -4.15%
   - session (n=160) : retour [-3.44% .. +2.84%] · haut q95 +3.95% · bas q05 -4.66%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 36.9  _(momentum baissier)_
- **ADX** : 12.8  _(pas de tendance nette)_
- **MACD** : hist -0.036  _(bearish_recent)_
- **BB** : %B 0.19 · largeur 5.9%
- **ATR** : 3.71 (28.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.291  _(distribution)_
- **Vol ratio** : 0.99  _(volume normal)_
- **Choppiness** : 62.8  _(marche en range (choppy))_
- **MA** : MA20 140.04 · MA50 137.4 · MA200 133.81  _(prix < MA20)_
- **Dist MA** : MA20 -1.8% · MA50 +0.1% · MA200 +2.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (789492 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
