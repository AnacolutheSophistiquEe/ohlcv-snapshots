# AL2SI

**Generated** : 2026-08-31T00:12:01.214270+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.48  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €27.48 (+2.0% vs entrée) · entrée €26.94 · stop €26.54 · T1 €27.42 · R/R 1.2  
> ↳ P(T1 av. stop) 21 % _(réel 5 s)_ · EV/risk -0.202 _(réel 5 s)_ (GBM 0.06) · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 260 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


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
- Entry (zone de repli) : €26.84–€27.04 (mid €26.94)
- Spot actuel : €27.48 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : €26.54 (stop swing_plan-based (-9.03%))
- Targets : T1 €27.42 · R/R 1.2 | T2 €27.90 · R/R 2.4 | T3 €28.39 · R/R 3.62
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €26.54


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.03 %)** : le gap seul le franchit 0.703 % des séances (9 fois sur 1280).
   - exécution **6.256 pt plus bas** dans le cas TYPIQUE (médiane), 20.326 au p90, **29.087 au pire**
   - perte réelle **18.187 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 9.03 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0644 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5394** [0.465 ; 0.6125] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4314** [0.38 ; 0.484] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4117** [0.3607 ; 0.4641] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.3 pt), swing (38.1 pt), deep (35.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.27 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.09 % contre 7.22 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1996** (β de hausse 0.9478, asymétrie 1.2658) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.877× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 24.2461 sur atr_grid (2.5 ATR, 11.768 %) — p(stop avant cible) 0.2956 [0.25 ; 0.35], R/R 0.382, perte reelle 24.668 % (gap inclus), CVaR 11.818 %, EV -2.3923 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.061 %) — p(stop avant cible) 0.5174 [0.46 ; 0.57], R/R 0.627, perte reelle 15.045 % (gap inclus), EV -3.572 % — **REFUSE**
      - refuse : p_stop_first 0.517, borne haute 0.570 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.57 %) : P(cible) 44.1 % x 9.43 % + P(rien) 4.2 % x 1.27 % ne couvrent pas P(stop) 51.7 % x 15.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.67 ATR (stop 10.374 %) — p(stop avant cible) 0.3454 [0.30 ; 0.40], R/R 0.419, perte reelle 22.515 % (gap inclus), EV -2.809 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.81 %) : P(cible) 54.5 % x 9.43 % + P(rien) 11.0 % x -1.54 % ne couvrent pas P(stop) 34.5 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.77 ATR (stop 20.272 %) — p(stop avant cible) 0.1585 [0.12 ; 0.20], R/R 0.314, perte reelle 30.031 % (gap inclus), EV -0.5792 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 57.5 % x 9.43 % + P(rien) 26.7 % x -4.64 % ne couvrent pas P(stop) 15.8 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.71 ATR (stop 29.37 %) — p(stop avant cible) 0.0888 [0.06 ; 0.12], R/R 0.247, perte reelle 38.117 % (gap inclus), EV -0.2778 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 57.5 % x 9.43 % + P(rien) 33.7 % x -6.88 % ne couvrent pas P(stop) 8.9 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.177 %) — p(stop avant cible) 0.8508 [0.81 ; 0.89], R/R 2.907, perte reelle 3.245 % (gap inclus), EV -1.3602 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.851, borne haute 0.885 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 14.8 % x 9.43 % + P(rien) 0.1 % x 2.87 % ne couvrent pas P(stop) 85.1 % x 3.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.354 %) — p(stop avant cible) 0.7569 [0.71 ; 0.80], R/R 1.593, perte reelle 5.921 % (gap inclus), EV -2.2333 % — **REFUSE**
      - refuse : p_stop_first 0.757, borne haute 0.800 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.23 %) : P(cible) 23.7 % x 9.43 % + P(rien) 0.6 % x 2.46 % ne couvrent pas P(stop) 75.7 % x 5.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.53 %) — p(stop avant cible) 0.6804 [0.63 ; 0.73], R/R 1.127, perte reelle 8.366 % (gap inclus), EV -2.7385 % — **REFUSE**
      - refuse : p_stop_first 0.680, borne haute 0.728 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.74 %) : P(cible) 31.1 % x 9.43 % + P(rien) 0.9 % x 2.76 % ne couvrent pas P(stop) 68.0 % x 8.37 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 4.707 %) — p(stop avant cible) 0.612 [0.56 ; 0.66], R/R 0.802, perte reelle 11.766 % (gap inclus), EV -3.6672 % — **REFUSE**
      - refuse : p_stop_first 0.612, borne haute 0.662 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 36.9 % x 9.43 % + P(rien) 1.9 % x 2.66 % ne couvrent pas P(stop) 61.2 % x 11.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 5.884 %) — p(stop avant cible) 0.5654 [0.51 ; 0.62], R/R 0.703, perte reelle 13.415 % (gap inclus), EV -3.718 % — **REFUSE**
      - refuse : p_stop_first 0.565, borne haute 0.617 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.72 %) : P(cible) 40.3 % x 9.43 % + P(rien) 3.2 % x 2.08 % ne couvrent pas P(stop) 56.5 % x 13.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.67 ATR (stop 9.272 %) — p(stop avant cible) 0.399 [0.35 ; 0.45], R/R 0.488, perte reelle 19.309 % (gap inclus), EV -2.9532 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.95 %) : P(cible) 51.2 % x 9.43 % + P(rien) 8.9 % x -0.87 % ne couvrent pas P(stop) 39.9 % x 19.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 11.768 %) — p(stop avant cible) 0.2956 [0.25 ; 0.35], R/R 0.382, perte reelle 24.668 % (gap inclus), EV -2.3923 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.39 %) : P(cible) 55.3 % x 9.43 % + P(rien) 15.1 % x -2.12 % ne couvrent pas P(stop) 29.6 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 12.945 %) — p(stop avant cible) 0.2677 [0.22 ; 0.32], R/R 0.382, perte reelle 24.668 % (gap inclus), EV -1.6266 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.63 %) : P(cible) 56.7 % x 9.43 % + P(rien) 16.6 % x -2.23 % ne couvrent pas P(stop) 26.8 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 14.122 %) — p(stop avant cible) 0.2561 [0.21 ; 0.30], R/R 0.382, perte reelle 24.668 % (gap inclus), EV -1.363 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.16 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 56.9 % x 9.43 % + P(rien) 17.5 % x -2.34 % ne couvrent pas P(stop) 25.6 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 16.476 %) — p(stop avant cible) 0.2177 [0.18 ; 0.26], R/R 0.349, perte reelle 27.014 % (gap inclus), EV -1.1627 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 57.0 % x 9.43 % + P(rien) 21.2 % x -3.09 % ne couvrent pas P(stop) 21.8 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.77 ATR (stop 19.171 %) — p(stop avant cible) 0.1843 [0.15 ; 0.23], R/R 0.314, perte reelle 30.031 % (gap inclus), EV -1.0854 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 57.5 % x 9.43 % + P(rien) 24.1 % x -4.02 % ne couvrent pas P(stop) 18.4 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 21.183 %) — p(stop avant cible) 0.1506 [0.12 ; 0.19], R/R 0.314, perte reelle 30.031 % (gap inclus), EV -0.4545 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 57.5 % x 9.43 % + P(rien) 27.5 % x -4.92 % ne couvrent pas P(stop) 15.1 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 23.537 %) — p(stop avant cible) 0.116 [0.09 ; 0.15], R/R 0.314, perte reelle 30.031 % (gap inclus), EV 0.1368 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.55 % > budget 12.00 %
   - 🟢 grid_snapped a 5.71 ATR (stop 28.268 %) — p(stop avant cible) 0.0894 [0.06 ; 0.12], R/R 0.247, perte reelle 38.117 % (gap inclus), EV -0.2879 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 57.5 % x 9.43 % + P(rien) 33.6 % x -6.85 % ne couvrent pas P(stop) 8.9 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 30.598 %) — p(stop avant cible) 0.0879 [0.06 ; 0.12], R/R 0.247, perte reelle 38.117 % (gap inclus), EV -0.2614 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 57.5 % x 9.43 % + P(rien) 33.8 % x -6.91 % ne couvrent pas P(stop) 8.8 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 32.951 %) — p(stop avant cible) 0.0806 [0.06 ; 0.11], R/R 0.247, perte reelle 38.117 % (gap inclus), EV -0.1337 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 57.5 % x 9.43 % + P(rien) 34.5 % x -7.20 % ne couvrent pas P(stop) 8.1 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 35.305 %) — p(stop avant cible) 0.0576 [0.04 ; 0.09], R/R 0.247, perte reelle 38.117 % (gap inclus), EV 0.3862 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.31 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 37.659 %) — p(stop avant cible) 0.0549 [0.03 ; 0.08], R/R 0.247, perte reelle 38.117 % (gap inclus), EV 0.4441 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.66 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 27.48, ATR14 1.2936 (4.707 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.401 ATR = 1.888 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.235 % | 27.4153 | 86.86 % | 90.48 % | 92.83 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.471 % | 27.3506 | 82.45 % | 86.95 % | 90.08 % | 91.93 % | 93.77 % | 96.0 % |
| 0.15 ATR | 0.706 % | 27.286 | 78.53 % | 83.32 % | 87.03 % | 88.88 % | 91.79 % | 94.81 % |
| 0.2 ATR | 0.941 % | 27.2213 | 72.65 % | 79.2 % | 83.2 % | 85.83 % | 89.52 % | 92.61 % |
| 0.25 ATR | 1.177 % | 27.1566 | 66.57 % | 74.58 % | 79.08 % | 82.48 % | 87.24 % | 91.01 % |
| 0.35 ATR | 1.648 % | 27.0272 | 54.61 % | 65.85 % | 70.92 % | 75.79 % | 82.39 % | 87.71 % |
| 0.5 ATR | 2.354 % | 26.8332 | 40.98 % | 54.37 % | 61.89 % | 69.0 % | 77.84 % | 85.31 % |
| 0.75 ATR | 3.53 % | 26.5098 | 22.84 % | 37.98 % | 47.84 % | 56.0 % | 67.16 % | 76.72 % |
| 1.0 ATR | 4.707 % | 26.1864 | 13.04 % | 25.61 % | 34.48 % | 45.08 % | 57.67 % | 68.53 % |
| 1.25 ATR | 5.884 % | 25.863 | 7.75 % | 17.86 % | 25.25 % | 36.61 % | 50.64 % | 62.54 % |
| 1.5 ATR | 7.061 % | 25.5396 | 3.82 % | 11.48 % | 17.88 % | 28.94 % | 43.72 % | 56.44 % |
| 2.0 ATR | 9.415 % | 24.8929 | 0.88 % | 5.4 % | 9.92 % | 17.42 % | 32.25 % | 44.86 % |
| 2.5 ATR | 11.768 % | 24.2461 | 0.1 % | 2.36 % | 5.01 % | 10.63 % | 22.35 % | 35.06 % |
| 3.0 ATR | 14.122 % | 23.5993 | 0.1 % | 0.98 % | 2.55 % | 7.09 % | 16.22 % | 27.77 % |
| 4.0 ATR | 18.829 % | 22.3057 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.5 % | 19.08 % |
| 6.0 ATR | 28.244 % | 19.7186 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.47 % | 9.39 % |

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
- **1 seance(s)** : plage utile 0.456–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.354 %, prix 26.8331), p(touche) 40.98 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (93.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.643–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.53 %, prix 26.51), p(touche) 37.98 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.707 %, prix 26.1865), p(touche) 34.48 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.002–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.884 %, prix 25.8631), p(touche) 36.61 % (en stress 92.16 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.454–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.061 %, prix 25.5396), p(touche) 43.72 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.994–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.415 %, prix 24.8928), p(touche) 44.86 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.06 | EV/share : €0.024 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 32 % | T3 26 %
- Kelly (position) : f* 0.035 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.5 | bear 6.3 | side 8.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 385.0 (= 14 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.97% → cible +1.79% / stop −1.5%, p_fill 60%, n_eff≈28.0) : P(cible|rempli) **21%** · **EV/risk -0.202** (×p_fill ; si rempli -0.51% du capital)
  - **swing** (entrée dip −4.323% → cible +4.003% / stop −4.92%, p_fill 45%, n_eff≈24.0) : P(cible|rempli) **51%** · **EV/risk -0.008** (×p_fill ; si rempli -0.09% du capital)
  - **deep** (entrée dip −6.679% → cible +5.661% / stop −7.567%, p_fill 62%, n_eff≈25.2) : P(cible|rempli) **64%** · **EV/risk +0.067** (×p_fill ; si rempli +0.82% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→68% · +3.0%→54% · +5.0%→42% · +8.0%→20%
- Range intraday médian 7.5% (p90 22.19%) · excursion haute méd. +4.2% / basse méd. −3.9%
- Profil de vol intra : ouverture 5.335% vs midi 1.714% vs clôture 1.821% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓1% ; spike-down 72% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.135% ; recovery-V 24%
- **σ réalisé intraday** 5.275% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 70% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 27.272 (VA 27.2–27.584 ; dernier close 27.48)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 89% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.58% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 41% (gap-down >1% 14% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.95% (p90 −4.35%) · haut méd +0.9% · range méd 2.66%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −5.44%) · haut méd +1.4% · range méd 3.18%
- Excursion ouverture 30min (n=160) : bas méd −1.44% (p90 −5.58%) · haut méd +1.96% · range méd 4.07%
- Excursion ouverture 60min (n=160) : bas méd −1.68% (p90 −6.12%) · haut méd +2.2% · range méd 5.06%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.48 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 78% (122/159) · gap 21% · délai 0.3min · rebond 66% (85/122) (MFE +2.33%)
   - −1.0% : fill 30min 50% · séance 74% (116/159) · gap 14% · délai 1.2min · rebond 65% (79/116) (MFE +1.99%)
   - −1.5% : fill 30min 41% · séance 67% (103/159) · gap 10% · délai 6.7min · rebond 61% (64/103) (MFE +1.52%)
   - −2.0% : fill 30min 35% · séance 61% (95/159) · gap 5% · délai 7.3min · rebond 60% (59/95) (MFE +1.82%)
   - −3.0% : fill 30min 24% · séance 50% (81/159) · gap 4% · délai 37.1min · rebond 66% (60/81) (MFE +1.65%)
   - −4.0% : fill 30min 20% · séance 44% (71/159) · gap 3% · délai 86.3min · rebond 76% (58/71) (MFE +1.91%)
   - −5.0% : fill 30min 14% · séance 32% (58/159) · gap 2% · délai 81.6min · rebond 89% (53/58) (MFE +2.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −4.28%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.07% (p90 −4.55%) → stop au-delà de −2.87% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −5.09%) → stop au-delà de −3.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1530 jambes) : jambe baissière méd −1.27% (p90 −3.19%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 94% (47/50) · rebond 57% (28/47)
      · −2.0% : fill 84% (43/50) · rebond 50% (24/43)
      · −3.0% : fill 78% (41/50) · rebond 71% (32/41)
      · −4.0% : fill 73% (38/50) · rebond 68% (30/38)
      · −5.0% : fill 55% (32/50) · rebond 79% (28/32)
   - **flat** (30 séances) :
      · −1.0% : fill 72% (23/30) · rebond 65% (16/23)
      · −2.0% : fill 49% (18/30) · rebond 57% (12/18)
      · −3.0% : fill 41% (13/30) · rebond 53% (8/13)
      · −4.0% : fill 36% (12/30) · rebond 85% (10/12)
      · −5.0% : fill 22% (9/30) · rebond 100% (9/9)
   - **gap-up** (79 séances) :
      · −1.0% : fill 63% (46/79) · rebond 71% (35/46)
      · −2.0% : fill 52% (34/79) · rebond 71% (23/34)
      · −3.0% : fill 38% (27/79) · rebond 66% (20/27)
      · −4.0% : fill 30% (21/79) · rebond 84% (18/21)
      · −5.0% : fill 24% (17/79) · rebond 99% (16/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 55% si les 15 1res min sont vertes (74 cas) · 34% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:02** → P(séance verte=clôture>ouverture) 73% si début vert vs 13% si rouge (base 44% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 43% ; creux résiduel méd -2.73% (q20 -4.95%) → **SL/trailing à −4.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.37% → **scale +1.72% / runner +3.37%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **13%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.69%** (au-delà de la MAE q10 -6.69%), cible rebond +1.75% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.06% .. +6.27%] · haut q95 +7.81% · bas q05 -7.25%
   - 60min (n=160) : retour [-5.78% .. +6.2%] · haut q95 +8.53% · bas q05 -7.63%
   - 2h (n=160) : retour [-5.88% .. +9.11%] · haut q95 +9.95% · bas q05 -7.88%
   - 4h (n=160) : retour [-6.44% .. +9.0%] · haut q95 +11.5% · bas q05 -9.63%
   - 6h (n=160) : retour [-6.7% .. +9.3%] · haut q95 +13.05% · bas q05 -10.4%
   - session (n=160) : retour [-7.66% .. +11.84%] · haut q95 +13.25% · bas q05 -11.08%


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

- **RSI** : 42.4  _(momentum baissier)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist 0.274  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 15.4%
- **ATR** : 1.29 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.158  _(distribution)_
- **Vol ratio** : 0.44  _(volume atone)_
- **Choppiness** : 57.8  _(transition)_
- **MA** : MA20 26.98 · MA50 28.24 · MA200 26.14  _(prix > MA20)_
- **Dist MA** : MA20 +1.8% · MA50 -2.7% · MA200 +5.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (907358 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
