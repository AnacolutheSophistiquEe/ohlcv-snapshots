# NEX

**Generated** : 2026-09-18T21:48:23.146886+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €136.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €136.80 (+4.2% vs entrée) · entrée €131.34 · stop €126.82 · T1 €135.36 · R/R 0.89  
> ↳ P(T1 av. stop) 56 % · EV/risk -0.047 · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

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

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €130.54–€132.15 (mid €131.34)
- Spot actuel : €136.80 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : €126.82 (stop swing_plan-based (-7.29%))
- Targets : T1 €135.36 · R/R 0.89 | T2 €139.37 · R/R 1.78 | T3 €143.39 · R/R 2.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.82


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.29 %)** : le gap seul le franchit 0.391 % des séances (5 fois sur 1279).
   - exécution **0.977 pt plus bas** dans le cas TYPIQUE (médiane), 1.809 au p90, **2.306 au pire**
   - perte réelle **8.333 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 7.29 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0041 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.644 % | pire -9.596 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0039** [0.0003 ; 0.0231] _(largeur 2.3 pt, n_eff 173.1)_
   - swing : **0.3965** [0.346 ; 0.4487] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3571** [0.308 ; 0.4086] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 18.2 observations effectives », dont la borne haute a 95 % vaut environ 16.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.9 pt), swing (58.1 pt), deep (46.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.28 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.957 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0054** (β de hausse 1.0916, asymétrie 0.9211) vs FCHI — 618 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 120.975 sur atr_grid (3.5 ATR, 11.568 %) — p(stop avant cible) 0.0778 [0.05 ; 0.11], R/R 1.687, perte reelle 11.568 % (gap inclus), CVaR 11.568 %, EV 0.5577 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.4 ATR (stop 3.474 %) — p(stop avant cible) 0.594 [0.54 ; 0.64], R/R 3.489, perte reelle 5.593 % (gap inclus), EV -1.1783 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.594, borne haute 0.645 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 2.4 % x 19.52 % + P(rien) 38.2 % x 4.39 % ne couvrent pas P(stop) 59.4 % x 5.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 4.958 %) — p(stop avant cible) 0.4402 [0.39 ; 0.49], R/R 2.536, perte reelle 7.697 % (gap inclus), EV -0.9795 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 2.4 % x 19.52 % + P(rien) 53.6 % x 3.63 % ne couvrent pas P(stop) 44.0 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.29 ATR (stop 9.736 %) — p(stop avant cible) 0.1263 [0.09 ; 0.16], R/R 2.005, perte reelle 9.736 % (gap inclus), EV 0.5479 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 6.43 ATR (stop 23.406 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.834, perte reelle 23.406 % (gap inclus), EV 0.6259 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.41 % > budget 12.00 %
   - ⚪ grid_snapped a 0.4 ATR (stop 2.31 %) — p(stop avant cible) 0.7161 [0.67 ; 0.76], R/R 4.716, perte reelle 4.138 % (gap inclus), EV -1.2682 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.716, borne haute 0.762 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 1.7 % x 19.52 % + P(rien) 26.7 % x 5.09 % ne couvrent pas P(stop) 71.6 % x 4.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.131 %) — p(stop avant cible) 0.5323 [0.48 ; 0.58], R/R 2.91, perte reelle 6.706 % (gap inclus), EV -1.2739 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.532, borne haute 0.584 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 2.4 % x 19.52 % + P(rien) 44.4 % x 4.13 % ne couvrent pas P(stop) 53.2 % x 6.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.784 %) — p(stop avant cible) 0.3744 [0.32 ; 0.43], R/R 2.402, perte reelle 8.124 % (gap inclus), EV -0.6368 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 2.4 % x 19.52 % + P(rien) 60.2 % x 3.22 % ne couvrent pas P(stop) 37.4 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.61 %) — p(stop avant cible) 0.3033 [0.26 ; 0.35], R/R 2.402, perte reelle 8.124 % (gap inclus), EV -0.149 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 2.4 % x 19.52 % + P(rien) 67.3 % x 2.75 % ne couvrent pas P(stop) 30.3 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.29 ATR (stop 8.572 %) — p(stop avant cible) 0.1866 [0.15 ; 0.23], R/R 2.034, perte reelle 9.596 % (gap inclus), EV 0.2844 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 9.089 %) — p(stop avant cible) 0.1588 [0.12 ; 0.20], R/R 2.034, perte reelle 9.596 % (gap inclus), EV 0.4223 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 11.568 %) — p(stop avant cible) 0.0778 [0.05 ; 0.11], R/R 1.687, perte reelle 11.568 % (gap inclus), EV 0.5577 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 13.221 %) — p(stop avant cible) 0.0472 [0.03 ; 0.07], R/R 1.476, perte reelle 13.221 % (gap inclus), EV 0.5265 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.22 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 14.873 %) — p(stop avant cible) 0.0246 [0.01 ; 0.05], R/R 1.312, perte reelle 14.873 % (gap inclus), EV 0.5621 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.526 %) — p(stop avant cible) 0.0131 [0.00 ; 0.03], R/R 1.181, perte reelle 16.526 % (gap inclus), EV 0.5768 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.53 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 18.178 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 1.074, perte reelle 18.178 % (gap inclus), EV 0.607 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.18 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 19.831 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.984, perte reelle 19.831 % (gap inclus), EV 0.6231 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.83 % > budget 12.00 %
   - 🟢 grid_snapped a 6.43 ATR (stop 22.242 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.877, perte reelle 22.242 % (gap inclus), EV 0.6234 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.24 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.789 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.787, perte reelle 24.789 % (gap inclus), EV 0.6292 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.79 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 26.441 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.738, perte reelle 26.441 % (gap inclus), EV 0.6338 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.44 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 136.8, ATR14 4.5214 (3.305 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 1.144 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.165 % | 136.5739 | 87.63 % | 91.36 % | 93.12 % | 95.17 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.331 % | 136.3479 | 81.94 % | 87.82 % | 90.36 % | 93.2 % | 95.54 % | 96.9 % |
| 0.15 ATR | 0.496 % | 136.1218 | 75.17 % | 83.6 % | 86.92 % | 90.25 % | 94.06 % | 95.6 % |
| 0.2 ATR | 0.661 % | 135.8957 | 68.5 % | 78.39 % | 83.19 % | 88.28 % | 92.67 % | 94.9 % |
| 0.25 ATR | 0.826 % | 135.6696 | 61.92 % | 73.67 % | 79.15 % | 85.12 % | 90.59 % | 93.7 % |
| 0.35 ATR | 1.157 % | 135.2175 | 49.56 % | 64.34 % | 71.88 % | 79.01 % | 86.63 % | 91.5 % |
| 0.5 ATR | 1.653 % | 134.5393 | 34.54 % | 52.55 % | 61.46 % | 70.74 % | 80.3 % | 87.3 % |
| 0.75 ATR | 2.479 % | 133.4089 | 20.41 % | 36.54 % | 47.49 % | 58.92 % | 70.2 % | 80.7 % |
| 1.0 ATR | 3.305 % | 132.2786 | 10.7 % | 24.26 % | 34.81 % | 48.57 % | 61.49 % | 73.9 % |
| 1.25 ATR | 4.131 % | 131.1482 | 4.91 % | 16.21 % | 25.07 % | 39.51 % | 54.36 % | 67.5 % |
| 1.5 ATR | 4.958 % | 130.0179 | 2.45 % | 11.1 % | 18.58 % | 30.54 % | 46.63 % | 59.8 % |
| 2.0 ATR | 6.61 % | 127.7571 | 0.88 % | 5.3 % | 10.03 % | 19.21 % | 34.85 % | 50.2 % |
| 2.5 ATR | 8.263 % | 125.4964 | 0.49 % | 2.65 % | 5.6 % | 11.43 % | 24.36 % | 38.5 % |
| 3.0 ATR | 9.915 % | 123.2357 | 0.2 % | 1.67 % | 3.24 % | 7.09 % | 17.52 % | 30.2 % |
| 4.0 ATR | 13.221 % | 118.7143 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.52 % | 17.9 % |
| 6.0 ATR | 19.831 % | 109.6714 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.29 % | 4.3 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.59 ATR | 2.06 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.80 ATR | 1.05 ATR | 1.25 ATR | 1.45 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.10 ATR | 1.43 ATR | 1.74 ATR | 1.97 ATR | 2.67 ATR | 3.40 ATR |
| **10 s.** | 0.63 ATR | 1.39 ATR | 1.57 ATR | 2.09 ATR | 2.47 ATR | 2.82 ATR | 3.75 ATR | 4.81 ATR |
| **20 s.** | 0.96 ATR | 2.01 ATR | 2.22 ATR | 2.83 ATR | 3.42 ATR | 3.83 ATR | 5.16 ATR | 5.90 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (75.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.618–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.479 %, prix 133.4087), p(touche) 36.54 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.799–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.305 %, prix 132.2788), p(touche) 34.81 % (en stress 84.31 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.099–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.131 %, prix 131.1488), p(touche) 39.51 % (en stress 93.14 %)  ✅ optimum identifie (62.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.569–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.61 %, prix 127.7575), p(touche) 34.85 % (en stress 98.02 %)  ✅ optimum identifie (71.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.222–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.263 %, prix 125.4962), p(touche) 38.5 % (en stress 98.0 %)  ✅ optimum identifie (69.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.007 | EV/share : €0.031 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 18 % | T3 8 %
- Kelly (position) : f* 0.031 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 24.2 | bear 26.0 | side 49.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 274.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.815% → cible +1.367% / stop −8.0%, p_fill 43%, n_eff≈18.2) : P(cible|rempli) **23%** · **EV/risk -0.021** (×p_fill ; si rempli -0.39% du capital)
  - **swing** (entrée dip −3.985% → cible +3.057% / stop −3.442%, p_fill 18%, n_eff≈8.8) : P(cible|rempli) **49%** · **EV/risk +0.020** (×p_fill ; si rempli +0.39% du capital)
  - **deep** (entrée dip −6.162% → cible +4.323% / stop −5.283%, p_fill 14%, n_eff≈12.1) : P(cible|rempli) **72%** · **EV/risk +0.054** (×p_fill ; si rempli +2.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→65% · +1.0%→51% · +2.0%→22% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 2.95% (p90 4.72%) · excursion haute méd. +1.01% / basse méd. −1.35%
- Profil de vol intra : ouverture 1.739% vs midi 0.517% vs clôture 0.7% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. -0.566% ; recovery-V 11%
- **σ réalisé intraday** 1.96% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 68% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 138.1975 (VA 137.3925–138.7725 ; dernier close 136.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 50% · **stop −1.94%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 31% (gap-down >1% 5% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.55% (p90 −1.78%) · haut méd +0.15% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.76% (p90 −1.95%) · haut méd +0.37% · range méd 1.29%
- Excursion ouverture 30min (n=160) : bas méd −0.8% (p90 −2.21%) · haut méd +0.48% · range méd 1.41%
- Excursion ouverture 60min (n=160) : bas méd −0.86% (p90 −2.44%) · haut méd +0.58% · range méd 1.59%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 136.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 61% (94/159) · gap 10% · délai 3.0min · rebond 45% (45/94) (MFE +0.74%)
   - −1.0% : fill 30min 27% · séance 53% (77/159) · gap 5% · délai 26.0min · rebond 43% (36/77) (MFE +0.73%)
   - −1.5% : fill 30min 14% · séance 42% (58/159) · gap 1% · délai 47.0min · rebond 36% (25/58) (MFE +0.67%)
   - −2.0% : fill 30min 10% · séance 29% (42/159) · gap 1% · délai 66.4min · rebond 45% (20/42) (MFE +0.78%)
   - −3.0% : fill 30min 4% · séance 16% (24/159) · gap 0% · délai 207.9min · rebond 50% (13/24) (MFE +1.05%)
   - −4.0% : fill 30min 0% · séance 5% (9/159) · gap 0% · délai 350.2min · rebond 11% (3/9) (MFE +0.48%)
   - −5.0% : fill 30min 0% · séance 2% (3/159) · gap 0% · délai 410.2min · rebond 42% (1/3) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.27%) → stop au-delà de −0.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.88%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −0.6%) → stop au-delà de −0.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=327 jambes) : jambe baissière méd −1.06% (p90 −2.3%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 80% (25/30) · rebond 55% (13/25)
      · −2.0% : fill 50% (16/30) · rebond 44% (7/16)
      · −3.0% : fill 32% (11/30) · rebond 44% (6/11)
      · −4.0% : fill 21% (6/30) · rebond 12% (2/6)
      · −5.0% : fill 12% (3/30) · rebond 42% (1/3)
   - **flat** (36 séances) :
      · −1.0% : fill 55% (21/36) · rebond 37% (9/21)
      · −2.0% : fill 30% (11/36) · rebond 32% (4/11)
      · −3.0% : fill 20% (7/36) · rebond 33% (3/7)
      · −4.0% : fill 6% (2/36) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (93 séances) :
      · −1.0% : fill 45% (31/93) · rebond 42% (14/31)
      · −2.0% : fill 23% (15/93) · rebond 55% (9/15)
      · −3.0% : fill 9% (6/93) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/93) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/93) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 71% si les 15 1res min sont vertes (86 cas) · 15% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **30min** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 43% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 221min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **78%** · continue >prix actuel 51% ; creux résiduel méd -1.0% (q20 -1.89%) → **SL/trailing à −1.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +1.76% → **scale +1.06% / runner +1.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **18%** (continue à baisser 59%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.2%** (au-delà de la MAE q10 -3.2%), cible rebond +0.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.85% .. +2.03%] · haut q95 +2.5% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.77% .. +2.4%] · haut q95 +2.64% · bas q05 -3.21%
   - 2h (n=160) : retour [-3.18% .. +2.43%] · haut q95 +2.93% · bas q05 -3.68%
   - 4h (n=160) : retour [-2.91% .. +3.17%] · haut q95 +3.22% · bas q05 -3.77%
   - 6h (n=160) : retour [-3.48% .. +3.64%] · haut q95 +3.9% · bas q05 -4.14%
   - session (n=160) : retour [-3.39% .. +2.81%] · haut q95 +3.91% · bas q05 -4.65%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 41.9  _(momentum baissier)_
- **ADX** : 10.9  _(pas de tendance nette)_
- **MACD** : hist -0.473  _(bearish_recent)_
- **BB** : %B 0.34 · largeur 8.6%
- **ATR** : 4.52 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.289  _(distribution)_
- **Vol ratio** : 1.25  _(volume normal)_
- **Choppiness** : 55.3  _(transition)_
- **MA** : MA20 138.71 · MA50 136.75 · MA200 134.77  _(prix < MA20)_
- **Dist MA** : MA20 -1.4% · MA50 +0.0% · MA200 +1.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (811655 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
