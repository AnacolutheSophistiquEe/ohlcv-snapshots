# AL2SI

**Generated** : 2026-08-27T21:46:56.855806+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €26.92  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €26.92 (+3.4% vs entrée) · entrée €26.04 · stop €24.64 · T1 €27.10 · R/R 0.76  
> ↳ P(T1 av. stop) 34 % _(réel 5 s)_ · EV/risk -0.267 _(réel 5 s)_ (GBM 0.097) · ¼-Kelly 0.018 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 213 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.230 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €25.83–€26.25 (mid €26.04)
- Spot actuel : €26.92 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : €24.64 (stop swing_plan-based (-8.47%))
- Targets : T1 €27.10 · R/R 0.76 | T2 €28.16 · R/R 1.51 | T3 €29.23 · R/R 2.28
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €24.64


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.47 %)** : le gap seul le franchit 0.781 % des séances (10 fois sur 1280).
   - exécution **5.047 pt plus bas** dans le cas TYPIQUE (médiane), 19.79 au p90, **29.647 au pire**
   - perte réelle **17.22 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 8.47 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0684 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4805** [0.4069 ; 0.5547] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4084** [0.3575 ; 0.4608] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3857** [0.3355 ; 0.4378] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 29.4 observations effectives », dont la borne haute a 95 % vaut environ 10.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.9 pt), swing (35.0 pt), deep (33.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.27 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.08 % contre 7.23 % aujourd'hui, rapport 0.56)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1996** (β de hausse 0.9395, asymétrie 1.2769) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.883× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 23.7716 sur atr_grid (2.25 ATR, 11.695 %) — p(stop avant cible) 0.3245 [0.28 ; 0.38], R/R 0.515, perte reelle 22.515 % (gap inclus), CVaR 11.746 %, EV -1.8644 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 27 des 27 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 52.8 % de la queue et il ne reste que -406.12 EUR a partager. Prix du risque -0.191 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.14 ATR (stop 8.735 %) — p(stop avant cible) 0.4581 [0.41 ; 0.51], R/R 0.637, perte reelle 18.187 % (gap inclus), EV -3.1731 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.17 %) : P(cible) 43.7 % x 11.59 % + P(rien) 10.5 % x 0.93 % ne couvrent pas P(stop) 45.8 % x 18.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.09 ATR (stop 18.839 %) — p(stop avant cible) 0.2012 [0.16 ; 0.25], R/R 0.386, perte reelle 30.031 % (gap inclus), EV -1.0764 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 50.1 % x 11.59 % + P(rien) 29.7 % x -2.84 % ne couvrent pas P(stop) 20.1 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.87 ATR (stop 28.126 %) — p(stop avant cible) 0.0967 [0.07 ; 0.13], R/R 0.304, perte reelle 38.117 % (gap inclus), EV -0.034 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 50.6 % x 11.59 % + P(rien) 39.7 % x -5.58 % ne couvrent pas P(stop) 9.7 % x 38.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.299 %) — p(stop avant cible) 0.8603 [0.82 ; 0.89], R/R 3.33, perte reelle 3.481 % (gap inclus), EV -1.3856 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.860, borne haute 0.894 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.39 %) : P(cible) 13.8 % x 11.59 % + P(rien) 0.1 % x 4.03 % ne couvrent pas P(stop) 86.0 % x 3.48 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.599 %) — p(stop avant cible) 0.76 [0.71 ; 0.80], R/R 1.807, perte reelle 6.416 % (gap inclus), EV -2.2003 % — **REFUSE**
      - refuse : p_stop_first 0.760, borne haute 0.803 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 22.5 % x 11.59 % + P(rien) 1.5 % x 4.66 % ne couvrent pas P(stop) 76.0 % x 6.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.898 %) — p(stop avant cible) 0.6908 [0.64 ; 0.74], R/R 1.296, perte reelle 8.945 % (gap inclus), EV -2.7624 % — **REFUSE**
      - refuse : p_stop_first 0.691, borne haute 0.738 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.76 %) : P(cible) 28.8 % x 11.59 % + P(rien) 2.1 % x 3.80 % ne couvrent pas P(stop) 69.1 % x 8.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.14 ATR (stop 7.503 %) — p(stop avant cible) 0.5247 [0.47 ; 0.58], R/R 0.739, perte reelle 15.687 % (gap inclus), EV -3.5254 % — **REFUSE**
      - refuse : p_stop_first 0.525, borne haute 0.577 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.53 %) : P(cible) 39.7 % x 11.59 % + P(rien) 7.8 % x 1.29 % ne couvrent pas P(stop) 52.5 % x 15.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 10.396 %) — p(stop avant cible) 0.3727 [0.32 ; 0.42], R/R 0.515, perte reelle 22.515 % (gap inclus), EV -2.8844 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.88 %) : P(cible) 47.6 % x 11.59 % + P(rien) 15.1 % x -0.09 % ne couvrent pas P(stop) 37.3 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 11.695 %) — p(stop avant cible) 0.3245 [0.28 ; 0.38], R/R 0.515, perte reelle 22.515 % (gap inclus), EV -1.8644 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.86 %) : P(cible) 48.2 % x 11.59 % + P(rien) 19.3 % x -0.78 % ne couvrent pas P(stop) 32.5 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 12.995 %) — p(stop avant cible) 0.2883 [0.24 ; 0.34], R/R 0.47, perte reelle 24.668 % (gap inclus), EV -1.5732 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 49.3 % x 11.59 % + P(rien) 21.9 % x -0.81 % ne couvrent pas P(stop) 28.8 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 14.294 %) — p(stop avant cible) 0.2721 [0.23 ; 0.32], R/R 0.47, perte reelle 24.668 % (gap inclus), EV -1.1597 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 50.0 % x 11.59 % + P(rien) 22.8 % x -1.07 % ne couvrent pas P(stop) 27.2 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.09 ATR (stop 17.607 %) — p(stop avant cible) 0.219 [0.18 ; 0.26], R/R 0.429, perte reelle 27.014 % (gap inclus), EV -0.7408 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 50.1 % x 11.59 % + P(rien) 28.0 % x -2.28 % ne couvrent pas P(stop) 21.9 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 20.792 %) — p(stop avant cible) 0.159 [0.12 ; 0.20], R/R 0.386, perte reelle 30.031 % (gap inclus), EV -0.1564 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 50.6 % x 11.59 % + P(rien) 33.5 % x -3.73 % ne couvrent pas P(stop) 15.9 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 23.391 %) — p(stop avant cible) 0.1235 [0.09 ; 0.16], R/R 0.386, perte reelle 30.031 % (gap inclus), EV 0.4472 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.41 % > budget 12.00 %
   - 🟢 grid_snapped a 4.87 ATR (stop 26.894 %) — p(stop avant cible) 0.1065 [0.08 ; 0.14], R/R 0.355, perte reelle 32.641 % (gap inclus), EV 0.3508 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.90 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 31.188 %) — p(stop avant cible) 0.0934 [0.07 ; 0.13], R/R 0.304, perte reelle 38.117 % (gap inclus), EV 0.0362 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.19 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 33.787 %) — p(stop avant cible) 0.0738 [0.05 ; 0.10], R/R 0.304, perte reelle 38.117 % (gap inclus), EV 0.3314 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.79 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 36.386 %) — p(stop avant cible) 0.0602 [0.04 ; 0.09], R/R 0.304, perte reelle 38.117 % (gap inclus), EV 0.7568 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.39 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 38.985 %) — p(stop avant cible) 0.0451 [0.03 ; 0.07], R/R 0.297, perte reelle 38.985 % (gap inclus), EV 0.8673 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.99 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 41.584 %) — p(stop avant cible) 0.0406 [0.02 ; 0.07], R/R 0.279, perte reelle 41.584 % (gap inclus), EV 0.9905 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.58 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 26.92, ATR14 1.3993 (5.198 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.401 ATR = 2.084 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.26 % | 26.85 | 86.86 % | 90.48 % | 92.83 % | 94.19 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.52 % | 26.7801 | 82.45 % | 86.95 % | 90.08 % | 92.03 % | 93.77 % | 96.0 % |
| 0.15 ATR | 0.78 % | 26.7101 | 78.53 % | 83.32 % | 87.03 % | 88.98 % | 91.79 % | 94.81 % |
| 0.2 ATR | 1.04 % | 26.6401 | 72.65 % | 79.2 % | 83.3 % | 85.93 % | 89.52 % | 92.61 % |
| 0.25 ATR | 1.299 % | 26.5702 | 66.57 % | 74.58 % | 79.17 % | 82.58 % | 87.24 % | 91.01 % |
| 0.35 ATR | 1.819 % | 26.4303 | 54.61 % | 65.75 % | 71.02 % | 75.89 % | 82.39 % | 87.71 % |
| 0.5 ATR | 2.599 % | 26.2204 | 40.98 % | 54.27 % | 61.98 % | 69.09 % | 77.84 % | 85.31 % |
| 0.75 ATR | 3.898 % | 25.8705 | 22.84 % | 37.88 % | 47.84 % | 56.1 % | 67.16 % | 76.72 % |
| 1.0 ATR | 5.198 % | 25.5207 | 13.04 % | 25.52 % | 34.48 % | 45.18 % | 57.67 % | 68.63 % |
| 1.25 ATR | 6.497 % | 25.1709 | 7.75 % | 17.86 % | 25.25 % | 36.71 % | 50.74 % | 62.64 % |
| 1.5 ATR | 7.797 % | 24.8211 | 3.82 % | 11.48 % | 17.88 % | 29.04 % | 43.82 % | 56.54 % |
| 2.0 ATR | 10.396 % | 24.1214 | 0.88 % | 5.4 % | 9.92 % | 17.52 % | 32.34 % | 44.96 % |
| 2.5 ATR | 12.995 % | 23.4218 | 0.1 % | 2.36 % | 5.01 % | 10.63 % | 22.45 % | 35.16 % |
| 3.0 ATR | 15.594 % | 22.7221 | 0.1 % | 0.98 % | 2.55 % | 7.09 % | 16.22 % | 27.87 % |
| 4.0 ATR | 20.792 % | 21.3229 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.5 % | 19.18 % |
| 6.0 ATR | 31.188 % | 18.5243 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.47 % | 9.39 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.46 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.14 ATR | 1.43 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.85 ATR | 1.02 ATR | 1.18 ATR | 1.62 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.26 ATR | 1.43 ATR | 2.00 ATR | 2.50 ATR |
| **5 s.** | 0.37 ATR | 0.89 ATR | 1.00 ATR | 1.37 ATR | 1.68 ATR | 1.89 ATR | 2.59 ATR | 3.52 ATR |
| **10 s.** | 0.57 ATR | 1.28 ATR | 1.46 ATR | 1.97 ATR | 2.37 ATR | 2.70 ATR | 3.93 ATR | 5.28 ATR |
| **20 s.** | 0.80 ATR | 1.78 ATR | 2.00 ATR | 2.65 ATR | 3.33 ATR | 3.91 ATR | 5.88 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.456–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.599 %, prix 26.2203), p(touche) 40.98 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (92.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.641–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.898 %, prix 25.8707), p(touche) 37.88 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.198 %, prix 25.5207), p(touche) 34.48 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.005–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.497 %, prix 25.171), p(touche) 36.71 % (en stress 92.16 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.457–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.797 %, prix 24.821), p(touche) 43.82 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.998–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.396 %, prix 24.1214), p(touche) 44.96 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.097 | EV/share : €0.136 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 59 % | T2 42 % | T3 30 %
- Kelly (position) : f* 0.071 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.5 | bear 5.5 | side 9.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 377.0 (= 14 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.49% → cible +1.823% / stop −2.0%, p_fill 69%, n_eff≈32.4) : P(cible|rempli) **33%** · **EV/risk -0.214** (×p_fill ; si rempli -0.62% du capital)
  - **swing** (entrée dip −3.272% → cible +4.077% / stop −5.374%, p_fill 69%, n_eff≈28.7) : P(cible|rempli) **34%** · **EV/risk -0.267** (×p_fill ; si rempli -2.08% du capital)
  - **deep** (entrée dip −5.053% → cible +5.766% / stop −8.212%, p_fill 61%, n_eff≈29.4) : P(cible|rempli) **63%** · **EV/risk -0.035** (×p_fill ; si rempli -0.46% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→69% · +3.0%→57% · +5.0%→44% · +8.0%→20%
- Range intraday médian 7.66% (p90 22.19%) · excursion haute méd. +4.29% / basse méd. −3.9%
- Profil de vol intra : ouverture 5.503% vs midi 1.744% vs clôture 1.892% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓1% ; spike-down 73% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.062)_ ; drift intra méd. -0.16% ; recovery-V 29%
- **σ réalisé intraday** 5.795% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 66% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 27.013 (VA 26.519–27.165 ; dernier close 26.76)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 89% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.58% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.23% · baisse 42% (gap-down >1% 15% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −1.1% (p90 −4.38%) · haut méd +0.93% · range méd 2.77%
- Excursion ouverture 15min (n=160) : bas méd −1.45% (p90 −5.56%) · haut méd +1.52% · range méd 3.44%
- Excursion ouverture 30min (n=160) : bas méd −1.54% (p90 −5.61%) · haut méd +2.06% · range méd 4.54%
- Excursion ouverture 60min (n=160) : bas méd −1.77% (p90 −6.33%) · haut méd +2.42% · range méd 5.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.64 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 80% (121/159) · gap 21% · délai 0.3min · rebond 66% (84/121) (MFE +2.21%)
   - −1.0% : fill 30min 55% · séance 77% (116/159) · gap 15% · délai 1.1min · rebond 65% (79/116) (MFE +2.22%)
   - −1.5% : fill 30min 45% · séance 70% (103/159) · gap 11% · délai 2.6min · rebond 62% (64/103) (MFE +1.52%)
   - −2.0% : fill 30min 38% · séance 65% (96/159) · gap 6% · délai 7.1min · rebond 62% (61/96) (MFE +1.84%)
   - −3.0% : fill 30min 27% · séance 53% (81/159) · gap 4% · délai 30.9min · rebond 68% (61/81) (MFE +1.7%)
   - −4.0% : fill 30min 21% · séance 46% (70/159) · gap 3% · délai 67.3min · rebond 80% (58/70) (MFE +2.03%)
   - −5.0% : fill 30min 15% · séance 35% (58/159) · gap 2% · délai 81.6min · rebond 89% (53/58) (MFE +2.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −4.63%) → stop au-delà de −2.1% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.11% (p90 −4.91%) → stop au-delà de −3.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.09% (p90 −5.17%) → stop au-delà de −3.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1547 jambes) : jambe baissière méd −1.28% (p90 −3.26%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 94% (46/49) · rebond 61% (28/46)
      · −2.0% : fill 83% (42/49) · rebond 55% (24/42)
      · −3.0% : fill 76% (40/49) · rebond 77% (32/40)
      · −4.0% : fill 71% (37/49) · rebond 74% (30/37)
      · −5.0% : fill 58% (32/49) · rebond 79% (28/32)
   - **flat** (31 séances) :
      · −1.0% : fill 76% (24/31) · rebond 61% (16/24)
      · −2.0% : fill 57% (20/31) · rebond 58% (14/20)
      · −3.0% : fill 48% (14/31) · rebond 54% (9/14)
      · −4.0% : fill 41% (12/31) · rebond 85% (10/12)
      · −5.0% : fill 26% (9/31) · rebond 100% (9/9)
   - **gap-up** (79 séances) :
      · −1.0% : fill 68% (46/79) · rebond 71% (35/46)
      · −2.0% : fill 56% (34/79) · rebond 71% (23/34)
      · −3.0% : fill 41% (27/79) · rebond 66% (20/27)
      · −4.0% : fill 33% (21/79) · rebond 84% (18/21)
      · −5.0% : fill 26% (17/79) · rebond 99% (16/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 55% si les 15 1res min sont vertes (77 cas) · 34% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 71% si début vert vs 17% si rouge (base 45% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **71%** · continue >prix actuel 48% ; creux résiduel méd -2.35% (q20 -5.44%) → **SL/trailing à −5.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.7% / q75 +5.25% → **scale +2.7% / runner +5.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **17%** (continue à baisser 53%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.49%** (au-delà de la MAE q10 -7.49%), cible rebond +2.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.2% .. +6.46%] · haut q95 +7.87% · bas q05 -7.39%
   - 60min (n=160) : retour [-5.84% .. +6.58%] · haut q95 +9.09% · bas q05 -7.67%
   - 2h (n=160) : retour [-5.98% .. +9.58%] · haut q95 +10.0% · bas q05 -7.98%
   - 4h (n=160) : retour [-7.05% .. +9.36%] · haut q95 +11.79% · bas q05 -10.07%
   - 6h (n=160) : retour [-6.71% .. +9.73%] · haut q95 +13.66% · bas q05 -10.74%
   - session (n=160) : retour [-7.89% .. +12.54%] · haut q95 +13.66% · bas q05 -11.2%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.36%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 46.0  _(neutre)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist 0.244  _(pas de croisement recent)_
- **BB** : %B 0.51 · largeur 15.9%
- **ATR** : 1.4 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.235  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 54.3  _(transition)_
- **MA** : MA20 26.9 · MA50 28.2 · MA200 26.07  _(prix > MA20)_
- **Dist MA** : MA20 +0.1% · MA50 -4.5% · MA200 +3.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (861961 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
