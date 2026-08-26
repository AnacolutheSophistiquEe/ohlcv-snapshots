# SRT3

**Generated** : 2026-08-26T00:02:40.429700+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €245.70  

> 🟡 **WAIT-FOR-DIP** — spot +5.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €245.70 (+5.0% vs entrée) · entrée €233.91 · stop €226.59 · T1 €239.72 · R/R 0.79  
> ↳ P(T1 av. stop) 63 % · EV/risk 0.118 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €232.75–€235.08 (mid €233.91)
- Spot actuel : €245.70 (+5.0% au-dessus de la zone — repli à attendre)
- Stop : €226.59 (stop swing_plan-based (-7.78%))
- Targets : T1 €239.72 · R/R 0.79 | T2 €245.53 · R/R 1.59 | T3 €251.34 · R/R 2.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €226.59


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.78 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **1.877 pt plus bas** dans le cas TYPIQUE (médiane), 4.732 au p90, **6.425 au pire**
   - perte réelle **10.096 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 7.78 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0091 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.157** [0.1087 ; 0.2167] _(largeur 10.8 pt, n_eff 173.1)_
   - swing : **0.428** [0.3766 ; 0.4806] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4288** [0.3774 ; 0.4814] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (41.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.12 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0647** (β de hausse 1.1723, asymétrie 0.9083) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.341× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 222.2393 sur grid_snapped (2.9 ATR, 9.549 %) — p(stop avant cible) 0.1441 [0.11 ; 0.18], R/R 0.203, perte reelle 11.278 % (gap inclus), CVaR 9.553 %, EV -0.2701 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.20 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.47 %) — p(stop avant cible) 0.3531 [0.30 ; 0.40], R/R 0.299, perte reelle 7.669 % (gap inclus), EV -1.2475 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 64.0 % x 2.29 % + P(rien) 0.7 % x -0.98 % ne couvrent pas P(stop) 35.3 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.9 ATR (stop 10.505 %) — p(stop avant cible) 0.1282 [0.10 ; 0.17], R/R 0.161, perte reelle 14.205 % (gap inclus), EV -0.5438 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 75.7 % x 2.29 % + P(rien) 11.5 % x -4.01 % ne couvrent pas P(stop) 12.8 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 8.06 ATR (stop 25.881 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.089, perte reelle 25.881 % (gap inclus), EV 0.1124 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.88 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.745 %) — p(stop avant cible) 0.689 [0.64 ; 0.74], R/R 1.365, perte reelle 1.681 % (gap inclus), EV -0.4448 % — **REFUSE**
      - refuse : p_stop_first 0.689, borne haute 0.736 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 31.1 % x 2.29 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 68.9 % x 1.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.49 %) — p(stop avant cible) 0.5996 [0.55 ; 0.65], R/R 0.808, perte reelle 2.839 % (gap inclus), EV -0.7837 % — **REFUSE**
      - refuse : p_stop_first 0.600, borne haute 0.650 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.81 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 40.0 % x 2.29 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 60.0 % x 2.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.235 %) — p(stop avant cible) 0.4998 [0.45 ; 0.55], R/R 0.484, perte reelle 4.737 % (gap inclus), EV -1.2201 % — **REFUSE**
      - refuse : p_stop_first 0.500, borne haute 0.552 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.48 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 50.0 % x 2.29 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 50.0 % x 4.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.98 %) — p(stop avant cible) 0.4325 [0.38 ; 0.49], R/R 0.339, perte reelle 6.774 % (gap inclus), EV -1.6335 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.63 %) : P(cible) 56.6 % x 2.29 % + P(rien) 0.1 % x -1.68 % ne couvrent pas P(stop) 43.2 % x 6.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.725 %) — p(stop avant cible) 0.3846 [0.33 ; 0.44], R/R 0.299, perte reelle 7.669 % (gap inclus), EV -1.5579 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.56 %) : P(cible) 60.9 % x 2.29 % + P(rien) 0.6 % x -1.00 % ne couvrent pas P(stop) 38.5 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.215 %) — p(stop avant cible) 0.3169 [0.27 ; 0.37], R/R 0.278, perte reelle 8.26 % (gap inclus), EV -1.0902 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 67.0 % x 2.29 % + P(rien) 1.3 % x -0.85 % ne couvrent pas P(stop) 31.7 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 5.96 %) — p(stop avant cible) 0.2705 [0.23 ; 0.32], R/R 0.259, perte reelle 8.862 % (gap inclus), EV -0.8036 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.80 %) : P(cible) 70.5 % x 2.29 % + P(rien) 2.4 % x -1.04 % ne couvrent pas P(stop) 27.1 % x 8.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.705 %) — p(stop avant cible) 0.2422 [0.20 ; 0.29], R/R 0.247, perte reelle 9.276 % (gap inclus), EV -0.6306 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 72.6 % x 2.29 % + P(rien) 3.2 % x -1.53 % ne couvrent pas P(stop) 24.2 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.45 %) — p(stop avant cible) 0.2142 [0.17 ; 0.26], R/R 0.227, perte reelle 10.096 % (gap inclus), EV -0.5916 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 73.9 % x 2.29 % + P(rien) 4.7 % x -2.64 % ne couvrent pas P(stop) 21.4 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.9 ATR (stop 9.549 %) — p(stop avant cible) 0.1441 [0.11 ; 0.18], R/R 0.203, perte reelle 11.278 % (gap inclus), EV -0.2701 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 75.5 % x 2.29 % + P(rien) 10.1 % x -3.71 % ne couvrent pas P(stop) 14.4 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 11.919 %) — p(stop avant cible) 0.0977 [0.07 ; 0.13], R/R 0.161, perte reelle 14.205 % (gap inclus), EV -0.2737 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 76.0 % x 2.29 % + P(rien) 14.2 % x -4.43 % ne couvrent pas P(stop) 9.8 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.409 %) — p(stop avant cible) 0.0674 [0.04 ; 0.10], R/R 0.161, perte reelle 14.205 % (gap inclus), EV -0.096 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 76.0 % x 2.29 % + P(rien) 17.2 % x -5.11 % ne couvrent pas P(stop) 6.7 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 14.899 %) — p(stop avant cible) 0.0386 [0.02 ; 0.06], R/R 0.154, perte reelle 14.899 % (gap inclus), EV 0.001 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.90 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.389 %) — p(stop avant cible) 0.0165 [0.01 ; 0.03], R/R 0.14, perte reelle 16.389 % (gap inclus), EV 0.074 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.39 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 17.879 %) — p(stop avant cible) 0.01 [0.00 ; 0.03], R/R 0.128, perte reelle 17.879 % (gap inclus), EV 0.0975 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.88 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.369 %) — p(stop avant cible) 0.0083 [0.00 ; 0.02], R/R 0.118, perte reelle 19.369 % (gap inclus), EV 0.0936 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.37 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 20.859 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 0.11, perte reelle 20.859 % (gap inclus), EV 0.0897 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.86 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 22.349 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.103, perte reelle 22.349 % (gap inclus), EV 0.1032 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.35 % > budget 12.00 %
   - 🟢 grid_snapped a 8.06 ATR (stop 24.925 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.092, perte reelle 24.925 % (gap inclus), EV 0.1126 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.93 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 245.7, ATR14 7.3214 (2.98 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.383 ATR = 1.141 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.149 % | 245.3339 | 89.05 % | 92.99 % | 94.37 % | 96.04 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.298 % | 244.9679 | 82.54 % | 88.45 % | 90.71 % | 93.37 % | 95.72 % | 97.09 % |
| 0.15 ATR | 0.447 % | 244.6018 | 74.85 % | 83.91 % | 86.96 % | 90.5 % | 93.63 % | 95.08 % |
| 0.2 ATR | 0.596 % | 244.2357 | 68.34 % | 78.97 % | 83.0 % | 87.33 % | 92.24 % | 94.47 % |
| 0.25 ATR | 0.745 % | 243.8696 | 63.21 % | 75.62 % | 79.74 % | 85.05 % | 90.55 % | 93.17 % |
| 0.35 ATR | 1.043 % | 243.1375 | 53.25 % | 69.3 % | 74.21 % | 80.99 % | 87.06 % | 91.36 % |
| 0.5 ATR | 1.49 % | 242.0393 | 38.26 % | 56.66 % | 64.53 % | 74.36 % | 82.69 % | 88.94 % |
| 0.75 ATR | 2.235 % | 240.2089 | 19.72 % | 37.02 % | 48.12 % | 59.5 % | 72.34 % | 82.71 % |
| 1.0 ATR | 2.98 % | 238.3786 | 10.26 % | 24.78 % | 34.68 % | 47.72 % | 62.89 % | 75.68 % |
| 1.25 ATR | 3.725 % | 236.5482 | 4.83 % | 15.0 % | 24.7 % | 38.32 % | 53.53 % | 68.74 % |
| 1.5 ATR | 4.47 % | 234.7179 | 2.37 % | 10.07 % | 18.08 % | 31.09 % | 46.47 % | 63.12 % |
| 2.0 ATR | 5.96 % | 231.0571 | 0.79 % | 4.74 % | 8.5 % | 17.62 % | 35.32 % | 53.27 % |
| 2.5 ATR | 7.45 % | 227.3964 | 0.3 % | 2.17 % | 5.04 % | 11.09 % | 25.17 % | 43.22 % |
| 3.0 ATR | 8.939 % | 223.7357 | 0.2 % | 1.68 % | 3.16 % | 6.83 % | 18.21 % | 35.68 % |
| 4.0 ATR | 11.919 % | 216.4143 | 0.0 % | 0.69 % | 1.88 % | 3.96 % | 9.55 % | 21.61 % |
| 6.0 ATR | 17.879 % | 201.7714 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.19 % | 7.34 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.75 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 1.00 ATR | 1.12 ATR | 1.51 ATR | 1.98 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.24 ATR | 1.43 ATR | 1.92 ATR | 2.51 ATR |
| **5 s.** | 0.49 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.73 ATR | 1.91 ATR | 2.63 ATR | 3.64 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.57 ATR | 2.11 ATR | 2.51 ATR | 2.87 ATR | 3.95 ATR | 5.24 ATR |
| **20 s.** | 1.02 ATR | 2.16 ATR | 2.41 ATR | 3.19 ATR | 3.76 ATR | 4.23 ATR | 5.63 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.433–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.49 %, prix 242.0391), p(touche) 38.26 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.648–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.235 %, prix 240.2086), p(touche) 37.02 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.808–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.98 %, prix 238.3781), p(touche) 34.68 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.072–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.725 %, prix 236.5477), p(touche) 38.32 % (en stress 92.08 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.566–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.96 %, prix 231.0563), p(touche) 35.32 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.411–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.45 %, prix 227.3953), p(touche) 43.22 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : €-0.124 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 32 % | T3 18 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 18.7 | bear 8.2 | side 73.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 491.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.175% → cible +3.069% / stop −3.0%, p_fill 30%, n_eff≈15.0) : P(cible|rempli) **24%** · **EV/risk +0.091** (×p_fill ; si rempli +0.92% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→48% · +3.0%→25% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.33% (p90 6.3%) · excursion haute méd. +1.89% / basse méd. −1.47%
- Profil de vol intra : ouverture 2.035% vs midi 0.845% vs clôture 0.994% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.098 ; neutre — autocorr -0.021)_ ; drift intra méd. 0.147% ; recovery-V 26%
- **σ réalisé intraday** 2.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 70% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 244.5125 (VA 243.7725–245.6225 ; dernier close 246.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 15% · rebond 68% · **stop −2.69%** sous le fill (sous le bruit) · cible +1.89% · R/R 0.7 (high win-rate)
- Gaps overnight (n=159) : méd. 0.05% · baisse 48% (gap-down >1% 7% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.44% (p90 −1.81%) · haut méd +0.53% · range méd 1.21%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −1.91%) · haut méd +0.64% · range méd 1.49%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −2.04%) · haut méd +0.8% · range méd 1.71%
- Excursion ouverture 60min (n=160) : bas méd −0.75% (p90 −2.45%) · haut méd +0.82% · range méd 1.83%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 246.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 77% (120/159) · gap 25% · délai 0.4min · rebond 53% (67/120) (MFE +1.15%)
   - −1.0% : fill 30min 41% · séance 64% (104/159) · gap 7% · délai 3.0min · rebond 62% (61/104) (MFE +1.34%)
   - −1.5% : fill 30min 26% · séance 49% (86/159) · gap 5% · délai 19.6min · rebond 57% (49/86) (MFE +1.51%)
   - −2.0% : fill 30min 10% · séance 36% (66/159) · gap 1% · délai 106.0min · rebond 65% (38/66) (MFE +1.39%)
   - −3.0% : fill 30min 5% · séance 15% (35/159) · gap 1% · délai 113.2min · rebond 68% (22/35) (MFE +1.89%)
   - −4.0% : fill 30min 3% · séance 9% (18/159) · gap 0% · délai 55.3min · rebond 68% (13/18) (MFE +2.14%)
   - −5.0% : fill 30min 0% · séance 6% (10/159) · gap 0% · délai 122.6min · rebond 86% (9/10) (MFE +2.89%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.97%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.17% (p90 −2.24%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.59%) → stop au-delà de −1.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=446 jambes) : jambe baissière méd −1.04% (p90 −2.34%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 78% (47/56) · rebond 73% (31/47)
      · −2.0% : fill 38% (29/56) · rebond 70% (18/29)
      · −3.0% : fill 20% (19/56) · rebond 63% (12/19)
      · −4.0% : fill 14% (12/56) · rebond 68% (10/12)
      · −5.0% : fill 7% (6/56) · rebond 100% (6/6)
   - **flat** (38 séances) :
      · −1.0% : fill 73% (26/38) · rebond 48% (12/26)
      · −2.0% : fill 48% (18/38) · rebond 54% (9/18)
      · −3.0% : fill 12% (7/38) · rebond 40% (3/7)
      · −4.0% : fill 4% (2/38) · rebond 0% (0/2)
      · −5.0% : fill 3% (1/38) · rebond 0% (0/1)
   - **gap-up** (65 séances) :
      · −1.0% : fill 46% (31/65) · rebond 58% (18/31)
      · −2.0% : fill 26% (19/65) · rebond 72% (11/19)
      · −3.0% : fill 13% (9/65) · rebond 90% (7/9)
      · −4.0% : fill 8% (4/65) · rebond 90% (3/4)
      · −5.0% : fill 7% (3/65) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 57% si les 15 1res min sont vertes (87 cas) · 37% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **8min** → P(séance verte=clôture>ouverture) 57% si début vert vs 38% si rouge (base 48% · écart 19 pts) ; prédictivité sature ensuite (plafond brut 268min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **57%** · continue >prix actuel 46% ; creux résiduel méd -1.43% (q20 -2.45%) → **SL/trailing à −2.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.36% → **scale +1.34% / runner +2.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **38%** (continue à baisser 52%) → **RÉDUIRE ~62%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.51%** (au-delà de la MAE q10 -4.51%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.86% .. +2.12%] · haut q95 +2.63% · bas q05 -3.25%
   - 60min (n=160) : retour [-2.58% .. +2.34%] · haut q95 +2.83% · bas q05 -3.66%
   - 2h (n=160) : retour [-2.18% .. +2.49%] · haut q95 +2.94% · bas q05 -3.82%
   - 4h (n=160) : retour [-2.52% .. +2.28%] · haut q95 +3.26% · bas q05 -3.83%
   - 6h (n=160) : retour [-2.57% .. +2.94%] · haut q95 +3.61% · bas q05 -3.92%
   - session (n=160) : retour [-3.59% .. +4.13%] · haut q95 +5.59% · bas q05 -4.59%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 66.0  _(momentum haussier)_
- **ADX** : 14.6  _(pas de tendance nette)_
- **MACD** : hist 1.504  _(pas de croisement recent)_
- **BB** : %B 0.86 · largeur 14.3%
- **ATR** : 7.32 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.117  _(distribution)_
- **Vol ratio** : 0.19  _(volume atone)_
- **Choppiness** : 51.5  _(transition)_
- **MA** : MA20 233.83 · MA50 230.51 · MA200 232.15  _(prix > MA20)_
- **Dist MA** : MA20 +5.1% · MA50 +6.6% · MA200 +5.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (814809 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
