# AL2SI

**Generated** : 2026-08-28T21:46:59.542942+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.50  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €27.50 (+2.0% vs entrée) · entrée €26.95 · stop €26.55 · T1 €27.44 · R/R 1.23  
> ↳ P(T1 av. stop) 24 % _(réel 5 s)_ · EV/risk -0.172 _(réel 5 s)_ (GBM 0.058) · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 261 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €26.86–€27.05 (mid €26.95)
- Spot actuel : €27.50 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : €26.55 (stop swing_plan-based (-9.06%))
- Targets : T1 €27.44 · R/R 1.23 | T2 €27.92 · R/R 2.43 | T3 €28.40 · R/R 3.63
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €26.55


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.06 %)** : le gap seul le franchit 0.703 % des séances (9 fois sur 1280).
   - exécution **6.226 pt plus bas** dans le cas TYPIQUE (médiane), 20.296 au p90, **29.057 au pire**
   - perte réelle **18.187 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 9.06 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0642 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5394** [0.465 ; 0.6125] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4314** [0.38 ; 0.484] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4117** [0.3607 ; 0.4641] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.8 pt), swing (38.1 pt), deep (36.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.27 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.09 % contre 7.22 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1996** (β de hausse 0.9478, asymétrie 1.2657) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.877× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 24.2661 sur atr_grid (2.5 ATR, 11.76 %) — p(stop avant cible) 0.2957 [0.25 ; 0.35], R/R 0.379, perte reelle 24.668 % (gap inclus), CVaR 11.81 %, EV -2.402 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.056 %) — p(stop avant cible) 0.5174 [0.46 ; 0.57], R/R 0.622, perte reelle 15.045 % (gap inclus), EV -3.5988 % — **REFUSE**
      - refuse : p_stop_first 0.517, borne haute 0.570 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.60 %) : P(cible) 44.3 % x 9.35 % + P(rien) 4.0 % x 1.15 % ne couvrent pas P(stop) 51.7 % x 15.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.69 ATR (stop 10.439 %) — p(stop avant cible) 0.3441 [0.30 ; 0.40], R/R 0.415, perte reelle 22.515 % (gap inclus), EV -2.8053 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.81 %) : P(cible) 54.8 % x 9.35 % + P(rien) 10.8 % x -1.65 % ne couvrent pas P(stop) 34.4 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.79 ATR (stop 20.33 %) — p(stop avant cible) 0.1549 [0.12 ; 0.20], R/R 0.311, perte reelle 30.031 % (gap inclus), EV -0.5245 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 58.0 % x 9.35 % + P(rien) 26.5 % x -4.90 % ne couvrent pas P(stop) 15.5 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.72 ATR (stop 29.421 %) — p(stop avant cible) 0.0888 [0.06 ; 0.12], R/R 0.245, perte reelle 38.117 % (gap inclus), EV -0.2876 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 58.0 % x 9.35 % + P(rien) 33.1 % x -7.04 % ne couvrent pas P(stop) 8.9 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.176 %) — p(stop avant cible) 0.8509 [0.81 ; 0.89], R/R 2.882, perte reelle 3.245 % (gap inclus), EV -1.3723 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.851, borne haute 0.885 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 14.8 % x 9.35 % + P(rien) 0.1 % x 2.87 % ne couvrent pas P(stop) 85.1 % x 3.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.352 %) — p(stop avant cible) 0.7569 [0.71 ; 0.80], R/R 1.579, perte reelle 5.921 % (gap inclus), EV -2.2523 % — **REFUSE**
      - refuse : p_stop_first 0.757, borne haute 0.800 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 23.7 % x 9.35 % + P(rien) 0.6 % x 2.46 % ne couvrent pas P(stop) 75.7 % x 5.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.528 %) — p(stop avant cible) 0.6804 [0.63 ; 0.73], R/R 1.118, perte reelle 8.366 % (gap inclus), EV -2.7633 % — **REFUSE**
      - refuse : p_stop_first 0.680, borne haute 0.728 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.76 %) : P(cible) 31.1 % x 9.35 % + P(rien) 0.9 % x 2.76 % ne couvrent pas P(stop) 68.0 % x 8.37 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 4.704 %) — p(stop avant cible) 0.612 [0.56 ; 0.66], R/R 0.795, perte reelle 11.766 % (gap inclus), EV -3.6882 % — **REFUSE**
      - refuse : p_stop_first 0.612, borne haute 0.662 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.69 %) : P(cible) 37.1 % x 9.35 % + P(rien) 1.7 % x 2.53 % ne couvrent pas P(stop) 61.2 % x 11.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 5.88 %) — p(stop avant cible) 0.5654 [0.51 ; 0.62], R/R 0.697, perte reelle 13.415 % (gap inclus), EV -3.7417 % — **REFUSE**
      - refuse : p_stop_first 0.565, borne haute 0.617 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.74 %) : P(cible) 40.5 % x 9.35 % + P(rien) 3.0 % x 1.98 % ne couvrent pas P(stop) 56.5 % x 13.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.69 ATR (stop 9.338 %) — p(stop avant cible) 0.3956 [0.35 ; 0.45], R/R 0.484, perte reelle 19.309 % (gap inclus), EV -2.8964 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.90 %) : P(cible) 51.6 % x 9.35 % + P(rien) 8.8 % x -0.99 % ne couvrent pas P(stop) 39.6 % x 19.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 11.76 %) — p(stop avant cible) 0.2957 [0.25 ; 0.35], R/R 0.379, perte reelle 24.668 % (gap inclus), EV -2.402 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.40 %) : P(cible) 55.9 % x 9.35 % + P(rien) 14.5 % x -2.30 % ne couvrent pas P(stop) 29.6 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 12.936 %) — p(stop avant cible) 0.2677 [0.22 ; 0.32], R/R 0.379, perte reelle 24.668 % (gap inclus), EV -1.6357 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.64 %) : P(cible) 57.2 % x 9.35 % + P(rien) 16.0 % x -2.40 % ne couvrent pas P(stop) 26.8 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 14.112 %) — p(stop avant cible) 0.2561 [0.21 ; 0.30], R/R 0.379, perte reelle 24.668 % (gap inclus), EV -1.3713 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 57.4 % x 9.35 % + P(rien) 17.0 % x -2.50 % ne couvrent pas P(stop) 25.6 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 16.464 %) — p(stop avant cible) 0.2177 [0.18 ; 0.26], R/R 0.346, perte reelle 27.014 % (gap inclus), EV -1.1721 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 57.5 % x 9.35 % + P(rien) 20.7 % x -3.25 % ne couvrent pas P(stop) 21.8 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.79 ATR (stop 19.229 %) — p(stop avant cible) 0.1843 [0.15 ; 0.23], R/R 0.311, perte reelle 30.031 % (gap inclus), EV -1.0952 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 58.0 % x 9.35 % + P(rien) 23.6 % x -4.18 % ne couvrent pas P(stop) 18.4 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 21.168 %) — p(stop avant cible) 0.1506 [0.12 ; 0.19], R/R 0.311, perte reelle 30.031 % (gap inclus), EV -0.4643 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 58.0 % x 9.35 % + P(rien) 26.9 % x -5.08 % ne couvrent pas P(stop) 15.1 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 23.519 %) — p(stop avant cible) 0.116 [0.09 ; 0.15], R/R 0.311, perte reelle 30.031 % (gap inclus), EV 0.127 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.53 % > budget 12.00 %
   - 🟢 grid_snapped a 5.72 ATR (stop 28.32 %) — p(stop avant cible) 0.0894 [0.06 ; 0.12], R/R 0.245, perte reelle 38.117 % (gap inclus), EV -0.2977 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 58.0 % x 9.35 % + P(rien) 33.0 % x -7.01 % ne couvrent pas P(stop) 8.9 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 30.575 %) — p(stop avant cible) 0.0879 [0.06 ; 0.12], R/R 0.245, perte reelle 38.117 % (gap inclus), EV -0.2706 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 58.0 % x 9.35 % + P(rien) 33.2 % x -7.07 % ne couvrent pas P(stop) 8.8 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 32.927 %) — p(stop avant cible) 0.0806 [0.06 ; 0.11], R/R 0.245, perte reelle 38.117 % (gap inclus), EV -0.1436 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 58.0 % x 9.35 % + P(rien) 33.9 % x -7.36 % ne couvrent pas P(stop) 8.1 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 35.279 %) — p(stop avant cible) 0.0576 [0.04 ; 0.09], R/R 0.245, perte reelle 38.117 % (gap inclus), EV 0.376 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.28 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 37.631 %) — p(stop avant cible) 0.0549 [0.03 ; 0.08], R/R 0.245, perte reelle 38.117 % (gap inclus), EV 0.4346 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.63 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 27.5, ATR14 1.2936 (4.704 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.401 ATR = 1.886 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.235 % | 27.4353 | 86.86 % | 90.48 % | 92.83 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.47 % | 27.3706 | 82.45 % | 86.95 % | 90.08 % | 91.93 % | 93.77 % | 96.0 % |
| 0.15 ATR | 0.706 % | 27.306 | 78.53 % | 83.32 % | 87.03 % | 88.88 % | 91.79 % | 94.81 % |
| 0.2 ATR | 0.941 % | 27.2413 | 72.65 % | 79.2 % | 83.2 % | 85.83 % | 89.52 % | 92.61 % |
| 0.25 ATR | 1.176 % | 27.1766 | 66.57 % | 74.58 % | 79.08 % | 82.48 % | 87.24 % | 91.01 % |
| 0.35 ATR | 1.646 % | 27.0473 | 54.61 % | 65.75 % | 70.92 % | 75.79 % | 82.39 % | 87.71 % |
| 0.5 ATR | 2.352 % | 26.8532 | 40.98 % | 54.37 % | 61.89 % | 69.0 % | 77.84 % | 85.31 % |
| 0.75 ATR | 3.528 % | 26.5298 | 22.84 % | 37.98 % | 47.84 % | 56.0 % | 67.16 % | 76.72 % |
| 1.0 ATR | 4.704 % | 26.2064 | 13.04 % | 25.61 % | 34.48 % | 45.08 % | 57.67 % | 68.53 % |
| 1.25 ATR | 5.88 % | 25.883 | 7.75 % | 17.86 % | 25.25 % | 36.61 % | 50.64 % | 62.54 % |
| 1.5 ATR | 7.056 % | 25.5596 | 3.82 % | 11.48 % | 17.88 % | 28.94 % | 43.72 % | 56.44 % |
| 2.0 ATR | 9.408 % | 24.9129 | 0.88 % | 5.4 % | 9.92 % | 17.42 % | 32.25 % | 44.86 % |
| 2.5 ATR | 11.76 % | 24.2661 | 0.1 % | 2.36 % | 5.01 % | 10.63 % | 22.35 % | 35.06 % |
| 3.0 ATR | 14.112 % | 23.6193 | 0.1 % | 0.98 % | 2.55 % | 7.09 % | 16.22 % | 27.77 % |
| 4.0 ATR | 18.816 % | 22.3257 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.5 % | 19.08 % |
| 6.0 ATR | 28.223 % | 19.7386 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.47 % | 9.39 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.46 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.14 ATR | 1.43 ATR |
| **2 s.** | 0.24 ATR | 0.57 ATR | 0.64 ATR | 0.85 ATR | 1.02 ATR | 1.18 ATR | 1.62 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.26 ATR | 1.43 ATR | 2.00 ATR | 2.50 ATR |
| **5 s.** | 0.37 ATR | 0.89 ATR | 1.00 ATR | 1.37 ATR | 1.67 ATR | 1.89 ATR | 2.59 ATR | 3.52 ATR |
| **10 s.** | 0.57 ATR | 1.27 ATR | 1.45 ATR | 1.97 ATR | 2.37 ATR | 2.69 ATR | 3.93 ATR | 5.28 ATR |
| **20 s.** | 0.80 ATR | 1.78 ATR | 1.99 ATR | 2.64 ATR | 3.32 ATR | 3.89 ATR | 5.87 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.456–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.352 %, prix 26.8532), p(touche) 40.98 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (93.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.643–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.528 %, prix 26.5298), p(touche) 37.98 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.704 %, prix 26.2064), p(touche) 34.48 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.002–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.88 %, prix 25.883), p(touche) 36.61 % (en stress 92.16 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.454–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.056 %, prix 25.5596), p(touche) 43.72 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.994–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.408 %, prix 24.9128), p(touche) 44.86 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.058 | EV/share : €0.023 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 33 % | T3 26 %
- Kelly (position) : f* 0.038 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.5 | bear 6.3 | side 8.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 385.0 (= 14 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.98% → cible +1.791% / stop −1.5%, p_fill 62%, n_eff≈28.0) : P(cible|rempli) **24%** · **EV/risk -0.172** (×p_fill ; si rempli -0.41% du capital)
  - **swing** (entrée dip −4.356% → cible +4.005% / stop −4.918%, p_fill 47%, n_eff≈24.0) : P(cible|rempli) **51%** · **EV/risk -0.008** (×p_fill ; si rempli -0.08% du capital)
  - **deep** (entrée dip −6.734% → cible +5.664% / stop −7.566%, p_fill 60%, n_eff≈25.3) : P(cible|rempli) **61%** · **EV/risk +0.040** (×p_fill ; si rempli +0.50% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→68% · +3.0%→55% · +5.0%→42% · +8.0%→20%
- Range intraday médian 7.5% (p90 22.19%) · excursion haute méd. +4.2% / basse méd. −3.9%
- Profil de vol intra : ouverture 5.375% vs midi 1.712% vs clôture 1.835% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓1% ; spike-down 73% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.068)_ ; drift intra méd. -0.229% ; recovery-V 24%
- **σ réalisé intraday** 5.371% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 68% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 27.356 (VA 26.812–27.42 ; dernier close 27.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 89% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.58% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.23% · baisse 41% (gap-down >1% 14% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.98% (p90 −4.35%) · haut méd +0.93% · range méd 2.73%
- Excursion ouverture 15min (n=160) : bas méd −1.39% (p90 −5.47%) · haut méd +1.42% · range méd 3.23%
- Excursion ouverture 30min (n=160) : bas méd −1.46% (p90 −5.59%) · haut méd +1.97% · range méd 4.1%
- Excursion ouverture 60min (n=160) : bas méd −1.73% (p90 −6.13%) · haut méd +2.27% · range méd 5.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 78% (122/159) · gap 21% · délai 0.3min · rebond 65% (85/122) (MFE +2.22%)
   - −1.0% : fill 30min 51% · séance 76% (117/159) · gap 14% · délai 1.2min · rebond 65% (80/117) (MFE +2.0%)
   - −1.5% : fill 30min 42% · séance 69% (104/159) · gap 10% · délai 6.6min · rebond 61% (65/104) (MFE +1.52%)
   - −2.0% : fill 30min 36% · séance 62% (96/159) · gap 5% · délai 7.3min · rebond 60% (60/96) (MFE +1.82%)
   - −3.0% : fill 30min 25% · séance 51% (82/159) · gap 4% · délai 37.6min · rebond 66% (61/82) (MFE +1.65%)
   - −4.0% : fill 30min 20% · séance 45% (71/159) · gap 3% · délai 86.3min · rebond 76% (58/71) (MFE +1.91%)
   - −5.0% : fill 30min 14% · séance 33% (58/159) · gap 2% · délai 81.6min · rebond 89% (53/58) (MFE +2.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.81% (p90 −4.32%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.1% (p90 −4.62%) → stop au-delà de −2.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −5.09%) → stop au-delà de −3.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1535 jambes) : jambe baissière méd −1.26% (p90 −3.2%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 94% (47/50) · rebond 57% (28/47)
      · −2.0% : fill 84% (43/50) · rebond 50% (24/43)
      · −3.0% : fill 78% (41/50) · rebond 71% (32/41)
      · −4.0% : fill 73% (38/50) · rebond 68% (30/38)
      · −5.0% : fill 55% (32/50) · rebond 79% (28/32)
   - **flat** (30 séances) :
      · −1.0% : fill 78% (24/30) · rebond 65% (17/24)
      · −2.0% : fill 53% (19/30) · rebond 58% (13/19)
      · −3.0% : fill 45% (14/30) · rebond 54% (9/14)
      · −4.0% : fill 38% (12/30) · rebond 85% (10/12)
      · −5.0% : fill 24% (9/30) · rebond 100% (9/9)
   - **gap-up** (79 séances) :
      · −1.0% : fill 63% (46/79) · rebond 71% (35/46)
      · −2.0% : fill 52% (34/79) · rebond 71% (23/34)
      · −3.0% : fill 38% (27/79) · rebond 66% (20/27)
      · −4.0% : fill 30% (21/79) · rebond 84% (18/21)
      · −5.0% : fill 24% (17/79) · rebond 99% (16/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 55% si les 15 1res min sont vertes (75 cas) · 31% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 67% si début vert vs 16% si rouge (base 43% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **67%** · continue >prix actuel 47% ; creux résiduel méd -2.35% (q20 -5.36%) → **SL/trailing à −5.36%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.42% / q75 +3.87% → **scale +2.42% / runner +3.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **16%** (continue à baisser 51%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.48%** (au-delà de la MAE q10 -7.48%), cible rebond +1.95% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.09% .. +6.32%] · haut q95 +7.81% · bas q05 -7.28%
   - 60min (n=160) : retour [-5.8% .. +6.21%] · haut q95 +8.66% · bas q05 -7.64%
   - 2h (n=160) : retour [-5.91% .. +9.3%] · haut q95 +9.95% · bas q05 -7.9%
   - 4h (n=160) : retour [-6.51% .. +9.08%] · haut q95 +11.55% · bas q05 -9.7%
   - 6h (n=160) : retour [-6.7% .. +9.37%] · haut q95 +13.2% · bas q05 -10.49%
   - session (n=160) : retour [-7.71% .. +12.04%] · haut q95 +13.25% · bas q05 -11.08%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 42.5  _(momentum baissier)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist 0.276  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 15.4%
- **ATR** : 1.29 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.155  _(distribution)_
- **Vol ratio** : 0.49  _(volume atone)_
- **Choppiness** : 57.8  _(transition)_
- **MA** : MA20 26.99 · MA50 28.24 · MA200 26.14  _(prix > MA20)_
- **Dist MA** : MA20 +1.9% · MA50 -2.6% · MA200 +5.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (924772 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
