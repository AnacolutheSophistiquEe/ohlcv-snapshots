# SAF

**Generated** : 2026-09-24T00:10:19.966399+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €336.40  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €336.40 (+3.1% vs entrée) · entrée €326.24 · stop €319.72 · T1 €329.29 · R/R 0.47  
> ↳ P(T1 av. stop) 52 % · EV/risk -0.0 · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.180 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €325.63–€326.85 (mid €326.24)
- Spot actuel : €336.40 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : €319.72 (stop swing_plan-based (-8.88%))
- Targets : T1 €329.29 · R/R 0.47 | T2 €332.34 · R/R 0.94 | T3 €335.39 · R/R 1.4
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €319.72


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.88 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **1.106 pt plus bas** dans le cas TYPIQUE (médiane), 1.106 au p90, **1.106 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 8.88 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0009 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.396 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1936** [0.1401 ; 0.2573] _(largeur 11.7 pt, n_eff 173.1)_
   - swing : **0.4118** [0.3608 ; 0.4642] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3582** [0.309 ; 0.4097] _(largeur 10.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.21 %** | CVaR **-4.01 %** | vol 2.09 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.39 % contre 2.41 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3913** (β de hausse 1.3447, asymétrie 1.0346) vs FCHI — 618 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 302.4571 sur atr_grid (4.5 ATR, 10.09 %) — p(stop avant cible) 0.0732 [0.05 ; 0.10], R/R 0.736, perte reelle 10.09 % (gap inclus), CVaR 10.09 %, EV 0.6301 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.363 %) — p(stop avant cible) 0.468 [0.42 ; 0.52], R/R 1.399, perte reelle 5.309 % (gap inclus), EV -0.3014 % — **REFUSE**
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 20.9 % x 7.43 % + P(rien) 32.3 % x 1.96 % ne couvrent pas P(stop) 46.8 % x 5.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.52 ATR (stop 7.018 %) — p(stop avant cible) 0.1591 [0.12 ; 0.20], R/R 0.744, perte reelle 9.986 % (gap inclus), EV 0.2893 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 5.49 ATR (stop 13.667 %) — p(stop avant cible) 0.0279 [0.01 ; 0.05], R/R 0.543, perte reelle 13.667 % (gap inclus), EV 0.5892 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.67 % > budget 12.00 %
   - 🟢 support a 10.17 ATR (stop 24.173 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.307, perte reelle 24.173 % (gap inclus), EV 0.6127 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.17 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.561 %) — p(stop avant cible) 0.8944 [0.86 ; 0.92], R/R 5.736, perte reelle 1.295 % (gap inclus), EV -0.5297 % — **REFUSE**
      - refuse : cible atteinte seulement 6.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.894, borne haute 0.923 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 6.2 % x 7.43 % + P(rien) 4.3 % x 3.82 % ne couvrent pas P(stop) 89.4 % x 1.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.121 %) — p(stop avant cible) 0.7885 [0.74 ; 0.83], R/R 3.807, perte reelle 1.951 % (gap inclus), EV -0.3968 % — **REFUSE**
      - refuse : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.788, borne haute 0.829 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 10.4 % x 7.43 % + P(rien) 10.7 % x 3.41 % ne couvrent pas P(stop) 78.8 % x 1.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 1.682 %) — p(stop avant cible) 0.7022 [0.65 ; 0.75], R/R 2.757, perte reelle 2.694 % (gap inclus), EV -0.3227 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.702, borne haute 0.749 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 14.8 % x 7.43 % + P(rien) 15.0 % x 3.15 % ne couvrent pas P(stop) 70.2 % x 2.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.242 %) — p(stop avant cible) 0.6282 [0.58 ; 0.68], R/R 2.026, perte reelle 3.667 % (gap inclus), EV -0.4938 % — **REFUSE**
      - refuse : p_stop_first 0.628, borne haute 0.678 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 17.0 % x 7.43 % + P(rien) 20.1 % x 2.71 % ne couvrent pas P(stop) 62.8 % x 3.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 2.803 %) — p(stop avant cible) 0.5446 [0.49 ; 0.60], R/R 1.679, perte reelle 4.424 % (gap inclus), EV -0.3722 % — **REFUSE**
      - refuse : p_stop_first 0.545, borne haute 0.597 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 19.4 % x 7.43 % + P(rien) 26.1 % x 2.27 % ne couvrent pas P(stop) 54.5 % x 4.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 3.924 %) — p(stop avant cible) 0.393 [0.34 ; 0.45], R/R 1.205, perte reelle 6.163 % (gap inclus), EV -0.1412 % — **REFUSE**
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 22.8 % x 7.43 % + P(rien) 37.9 % x 1.55 % ne couvrent pas P(stop) 39.3 % x 6.16 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 4.484 %) — p(stop avant cible) 0.335 [0.29 ; 0.39], R/R 1.093, perte reelle 6.799 % (gap inclus), EV -0.039 % — **REFUSE**
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 23.2 % x 7.43 % + P(rien) 43.4 % x 1.20 % ne couvrent pas P(stop) 33.5 % x 6.80 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 5.045 %) — p(stop avant cible) 0.2893 [0.24 ; 0.34], R/R 0.967, perte reelle 7.683 % (gap inclus), EV 0.0584 % — **REFUSE**
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.52 ATR (stop 6.323 %) — p(stop avant cible) 0.2162 [0.18 ; 0.26], R/R 0.744, perte reelle 9.986 % (gap inclus), EV 0.0047 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 6.727 %) — p(stop avant cible) 0.1878 [0.15 ; 0.23], R/R 0.744, perte reelle 9.986 % (gap inclus), EV 0.147 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.848 %) — p(stop avant cible) 0.1358 [0.10 ; 0.17], R/R 0.744, perte reelle 9.986 % (gap inclus), EV 0.4375 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 8.969 %) — p(stop avant cible) 0.099 [0.07 ; 0.13], R/R 0.744, perte reelle 9.986 % (gap inclus), EV 0.582 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 10.09 %) — p(stop avant cible) 0.0732 [0.05 ; 0.10], R/R 0.736, perte reelle 10.09 % (gap inclus), EV 0.6301 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 11.211 %) — p(stop avant cible) 0.0539 [0.03 ; 0.08], R/R 0.663, perte reelle 11.211 % (gap inclus), EV 0.6234 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 5.49 ATR (stop 12.972 %) — p(stop avant cible) 0.04 [0.02 ; 0.06], R/R 0.573, perte reelle 12.972 % (gap inclus), EV 0.5983 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.97 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 14.574 %) — p(stop avant cible) 0.0182 [0.01 ; 0.04], R/R 0.51, perte reelle 14.574 % (gap inclus), EV 0.5897 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.57 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 15.696 %) — p(stop avant cible) 0.009 [0.00 ; 0.02], R/R 0.473, perte reelle 15.696 % (gap inclus), EV 0.596 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.70 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 16.817 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 0.442, perte reelle 16.817 % (gap inclus), EV 0.6015 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.82 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 17.938 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 0.414, perte reelle 17.938 % (gap inclus), EV 0.6012 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.94 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 336.4, ATR14 7.5429 (2.242 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 0.771 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.112 % | 336.0229 | 89.22 % | 92.54 % | 93.71 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.224 % | 335.6457 | 81.37 % | 87.14 % | 89.19 % | 91.44 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.336 % | 335.2686 | 75.0 % | 83.22 % | 86.25 % | 88.68 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.448 % | 334.8914 | 68.04 % | 77.92 % | 82.51 % | 85.24 % | 88.92 % | 90.91 % |
| 0.25 ATR | 0.561 % | 334.5143 | 60.98 % | 73.31 % | 78.88 % | 83.17 % | 87.64 % | 90.01 % |
| 0.35 ATR | 0.785 % | 333.76 | 49.31 % | 63.2 % | 69.74 % | 76.87 % | 82.69 % | 87.01 % |
| 0.5 ATR | 1.121 % | 332.6286 | 35.2 % | 51.62 % | 59.04 % | 68.41 % | 75.87 % | 81.32 % |
| 0.75 ATR | 1.682 % | 330.7429 | 20.49 % | 35.43 % | 42.73 % | 52.95 % | 63.2 % | 70.73 % |
| 1.0 ATR | 2.242 % | 328.8571 | 9.8 % | 23.65 % | 32.32 % | 41.73 % | 53.51 % | 61.24 % |
| 1.25 ATR | 2.803 % | 326.9714 | 4.41 % | 15.31 % | 23.77 % | 32.87 % | 46.19 % | 54.45 % |
| 1.5 ATR | 3.363 % | 325.0857 | 2.25 % | 9.91 % | 16.4 % | 24.7 % | 37.88 % | 46.45 % |
| 2.0 ATR | 4.484 % | 321.3143 | 0.98 % | 4.42 % | 7.47 % | 15.16 % | 26.71 % | 36.76 % |
| 2.5 ATR | 5.606 % | 317.5428 | 0.2 % | 1.47 % | 3.63 % | 8.56 % | 18.2 % | 28.17 % |
| 3.0 ATR | 6.727 % | 313.7714 | 0.0 % | 0.88 % | 2.06 % | 5.71 % | 12.07 % | 21.98 % |
| 4.0 ATR | 8.969 % | 306.2286 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 4.55 % | 10.79 % |
| 6.0 ATR | 13.453 % | 291.1428 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.67 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.50 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.71 ATR | 0.98 ATR | 1.21 ATR | 1.38 ATR | 1.86 ATR | 2.32 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.25 ATR | 1.49 ATR | 1.75 ATR | 2.39 ATR | 3.15 ATR |
| **10 s.** | 0.52 ATR | 1.12 ATR | 1.29 ATR | 1.72 ATR | 2.10 ATR | 2.39 ATR | 3.27 ATR | 3.94 ATR |
| **20 s.** | 0.65 ATR | 1.39 ATR | 1.57 ATR | 2.22 ATR | 2.76 ATR | 3.18 ATR | 4.20 ATR | 5.49 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.602–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.682 %, prix 330.7417), p(touche) 35.43 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.715–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.682 %, prix 330.7417), p(touche) 42.73 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.927–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.242 %, prix 328.8579), p(touche) 41.73 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.286–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.363 %, prix 325.0869), p(touche) 37.88 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.575–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.484 %, prix 321.3158), p(touche) 36.76 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.0 | EV/share : €-0.000 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 31 % | T3 12 %
- Kelly (position) : f* 0.094 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 41.0 | bear 53.6 | side 5.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 336.0 (= 1 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→52% · +2.0%→28% · +3.0%→9% · +5.0%→0% · +8.0%→0%
- Range intraday médian 2.45% (p90 3.72%) · excursion haute méd. +1.09% / basse méd. −0.77%
- Profil de vol intra : ouverture 1.461% vs midi 0.5% vs clôture 0.665% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.3% ; recovery-V 12%
- **σ réalisé intraday** 1.544% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 61% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 331.8075 (VA 331.3325–332.7575 ; dernier close 333.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 23% · rebond 36% · **stop −1.2%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 31% (gap-down >1% 1% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.56%) · haut méd +0.18% · range méd 0.85%
- Excursion ouverture 15min (n=160) : bas méd −0.48% (p90 −1.76%) · haut méd +0.31% · range méd 1.02%
- Excursion ouverture 30min (n=160) : bas méd −0.49% (p90 −1.78%) · haut méd +0.44% · range méd 1.22%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.84%) · haut méd +0.53% · range méd 1.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 333.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 60% (86/159) · gap 10% · délai 0.4min · rebond 38% (34/86) (MFE +0.84%)
   - −1.0% : fill 30min 25% · séance 48% (71/159) · gap 1% · délai 25.1min · rebond 42% (33/71) (MFE +0.79%)
   - −1.5% : fill 30min 11% · séance 29% (45/159) · gap 1% · délai 67.5min · rebond 31% (19/45) (MFE +0.52%)
   - −2.0% : fill 30min 4% · séance 23% (37/159) · gap 0% · délai 240.5min · rebond 36% (16/37) (MFE +0.74%)
   - −3.0% : fill 30min 1% · séance 7% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −0.77%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.77%) → stop au-delà de −0.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=205 jambes) : jambe baissière méd −1.05% (p90 −2.26%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 76% (18/22) · rebond 29% (7/18)
      · −2.0% : fill 48% (12/22) · rebond 42% (6/12)
      · −3.0% : fill 16% (5/22) · rebond 31% (2/5)
      · −4.0% : fill 7% (2/22) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/22) · rebond 0% (0/0)
   - **flat** (38 séances) :
      · −1.0% : fill 49% (20/38) · rebond 40% (10/20)
      · −2.0% : fill 26% (9/38) · rebond 12% (1/9)
      · −3.0% : fill 5% (3/38) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/38) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/38) · rebond 0% (0/0)
   - **gap-up** (99 séances) :
      · −1.0% : fill 39% (33/99) · rebond 53% (16/33)
      · −2.0% : fill 13% (16/99) · rebond 59% (9/16)
      · −3.0% : fill 5% (6/99) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/99) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/99) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 70% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 77% si début vert vs 22% si rouge (base 48% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **77%** · continue >prix actuel 50% ; creux résiduel méd -0.71% (q20 -1.34%) → **SL/trailing à −1.34%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.96% / q75 +1.45% → **scale +0.96% / runner +1.45%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **22%** (continue à baisser 60%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.29%** (au-delà de la MAE q10 -2.29%), cible rebond +0.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.49% .. +1.54%] · haut q95 +1.94% · bas q05 -2.06%
   - 60min (n=160) : retour [-1.63% .. +1.81%] · haut q95 +1.99% · bas q05 -2.34%
   - 2h (n=160) : retour [-2.32% .. +2.06%] · haut q95 +2.49% · bas q05 -2.92%
   - 4h (n=160) : retour [-1.87% .. +2.1%] · haut q95 +2.7% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.06% .. +2.31%] · haut q95 +2.78% · bas q05 -2.98%
   - session (n=160) : retour [-2.7% .. +2.39%] · haut q95 +3.33% · bas q05 -3.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 53.9  _(neutre)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist 1.075  _(bullish_recent)_
- **BB** : %B 0.72 · largeur 7.9%
- **ATR** : 7.54 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.185  _(distribution)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 63.1  _(marche en range (choppy))_
- **MA** : MA20 330.77 · MA50 339.3 · MA200 313.84  _(prix > MA20)_
- **Dist MA** : MA20 +1.7% · MA50 -0.9% · MA200 +7.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (841432 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
