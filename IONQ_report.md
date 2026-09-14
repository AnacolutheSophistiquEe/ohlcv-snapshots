# IONQ

**Generated** : 2026-09-14T00:38:44.415873+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $36.75  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $36.75 (+1.8% vs entrée) · entrée $36.11 · stop $35.07 · T1 $38.18 · R/R 1.99  
> ↳ P(T1 av. stop) 5 % _(réel 5 s)_ · EV/risk -0.065 _(réel 5 s)_ (GBM 0.018) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.87% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.250 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $35.93–$36.29 (mid $36.11)
- Spot actuel : $36.75 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : $35.07 (stop swing_plan-based (-10.31%))
- Targets : T1 $38.18 · R/R 1.99 | T2 $38.50 · R/R 2.3 | T3 $38.82 · R/R 2.61
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $35.07


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.85 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.31 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1254).
   - exécution **1.383 pt plus bas** dans le cas TYPIQUE (médiane), 8.575 au p90, **11.549 au pire**
   - perte réelle **13.966 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 10.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0117 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.033 % | p01 -6.63 % | pire -21.859 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4485** [0.3758 ; 0.5229] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4683** [0.4161 ; 0.521] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4607** [0.4087 ; 0.5134] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.0 pt), swing (38.2 pt), deep (40.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-9.0 %** | CVaR **-12.13 %** | vol 6.96 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 3.73 % contre 6.05 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.22 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2215** (β de hausse 1.9868, asymétrie 1.1181) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 32.0017 sur atr_grid (2.0 ATR, 12.921 %) — p(stop avant cible) 0.4462 [0.39 ; 0.50], R/R 0.917, perte reelle 21.859 % (gap inclus), CVaR 12.928 %, EV -4.4827 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0773 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.93 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.19 ATR (stop 4.795 %) — p(stop avant cible) 0.7921 [0.75 ; 0.83], R/R 2.991, perte reelle 6.703 % (gap inclus), EV -1.9338 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.792, borne haute 0.832 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 14.9 % x 20.05 % + P(rien) 5.9 % x 6.57 % ne couvrent pas P(stop) 79.2 % x 6.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.08 ATR (stop 10.592 %) — p(stop avant cible) 0.5507 [0.50 ; 0.60], R/R 1.435, perte reelle 13.966 % (gap inclus), EV -2.1758 % — **REFUSE**
      - refuse : p_stop_first 0.551, borne haute 0.603 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.18 %) : P(cible) 25.4 % x 20.05 % + P(rien) 19.6 % x 2.19 % ne couvrent pas P(stop) 55.1 % x 13.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.85 ATR (stop 21.993 %) — p(stop avant cible) 0.166 [0.13 ; 0.21], R/R 0.912, perte reelle 21.993 % (gap inclus), EV -0.1514 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 28.3 % x 20.05 % + P(rien) 55.1 % x -3.93 % ne couvrent pas P(stop) 16.6 % x 21.99 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.57 ATR (stop 33.149 %) — p(stop avant cible) 0.0235 [0.01 ; 0.04], R/R 0.605, perte reelle 33.149 % (gap inclus), EV -0.1481 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 28.4 % x 20.05 % + P(rien) 69.3 % x -7.30 % ne couvrent pas P(stop) 2.4 % x 33.15 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.19 ATR (stop 3.135 %) — p(stop avant cible) 0.8565 [0.82 ; 0.89], R/R 3.926, perte reelle 5.107 % (gap inclus), EV -1.8135 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.857, borne haute 0.890 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.81 %) : P(cible) 11.9 % x 20.05 % + P(rien) 2.4 % x 6.93 % ne couvrent pas P(stop) 85.7 % x 5.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.08 ATR (stop 8.931 %) — p(stop avant cible) 0.6395 [0.59 ; 0.69], R/R 1.624, perte reelle 12.345 % (gap inclus), EV -2.6844 % — **REFUSE**
      - refuse : p_stop_first 0.639, borne haute 0.689 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 23.2 % x 20.05 % + P(rien) 12.8 % x 4.34 % ne couvrent pas P(stop) 63.9 % x 12.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 12.921 %) — p(stop avant cible) 0.4462 [0.39 ; 0.50], R/R 0.917, perte reelle 21.859 % (gap inclus), EV -4.4827 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.48 %) : P(cible) 26.5 % x 20.05 % + P(rien) 28.9 % x -0.12 % ne couvrent pas P(stop) 44.6 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 14.536 %) — p(stop avant cible) 0.3755 [0.33 ; 0.43], R/R 0.917, perte reelle 21.859 % (gap inclus), EV -3.4229 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.42 %) : P(cible) 26.8 % x 20.05 % + P(rien) 35.7 % x -1.62 % ne couvrent pas P(stop) 37.5 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 16.151 %) — p(stop avant cible) 0.2998 [0.25 ; 0.35], R/R 0.917, perte reelle 21.859 % (gap inclus), EV -2.2968 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.16 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.30 %) : P(cible) 27.0 % x 20.05 % + P(rien) 43.0 % x -2.69 % ne couvrent pas P(stop) 30.0 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.85 ATR (stop 20.333 %) — p(stop avant cible) 0.1907 [0.15 ; 0.23], R/R 0.917, perte reelle 21.859 % (gap inclus), EV -0.5125 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 28.2 % x 20.05 % + P(rien) 52.7 % x -3.80 % ne couvrent pas P(stop) 19.1 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 25.841 %) — p(stop avant cible) 0.091 [0.06 ; 0.12], R/R 0.776, perte reelle 25.841 % (gap inclus), EV -0.1125 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 28.3 % x 20.05 % + P(rien) 62.6 % x -5.50 % ne couvrent pas P(stop) 9.1 % x 25.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.57 ATR (stop 31.489 %) — p(stop avant cible) 0.0408 [0.02 ; 0.07], R/R 0.637, perte reelle 31.489 % (gap inclus), EV -0.1945 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 28.4 % x 20.05 % + P(rien) 67.5 % x -6.81 % ne couvrent pas P(stop) 4.1 % x 31.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 32.301 %) — p(stop avant cible) 0.0275 [0.01 ; 0.05], R/R 0.621, perte reelle 32.301 % (gap inclus), EV -0.1825 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 28.4 % x 20.05 % + P(rien) 68.9 % x -7.23 % ne couvrent pas P(stop) 2.8 % x 32.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 35.531 %) — p(stop avant cible) 0.0131 [0.00 ; 0.03], R/R 0.564, perte reelle 35.531 % (gap inclus), EV -0.1073 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 28.4 % x 20.05 % + P(rien) 70.3 % x -7.58 % ne couvrent pas P(stop) 1.3 % x 35.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 38.762 %) — p(stop avant cible) 0.0073 [0.00 ; 0.02], R/R 0.517, perte reelle 38.762 % (gap inclus), EV -0.0975 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 28.4 % x 20.05 % + P(rien) 70.9 % x -7.76 % ne couvrent pas P(stop) 0.7 % x 38.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 41.992 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.477, perte reelle 41.992 % (gap inclus), EV -0.1036 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 28.4 % x 20.05 % + P(rien) 71.5 % x -8.00 % ne couvrent pas P(stop) 0.2 % x 41.99 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 45.222 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.443, perte reelle 45.222 % (gap inclus), EV -0.1048 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 28.4 % x 20.05 % + P(rien) 71.5 % x -8.03 % ne couvrent pas P(stop) 0.1 % x 45.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 48.452 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.414, perte reelle 48.452 % (gap inclus), EV -0.0875 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 28.4 % x 20.05 % + P(rien) 71.6 % x -8.03 % ne couvrent pas P(stop) 0.1 % x 48.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 51.682 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.388, perte reelle 51.682 % (gap inclus), EV -0.0694 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 28.4 % x 20.05 % + P(rien) 71.6 % x -8.04 % ne couvrent pas P(stop) 0.0 % x 51.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 36.75, ATR14 2.3741 (6.46 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.38 ATR = 2.455 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.323 % | 36.6313 | 93.66 % | 95.37 % | 96.07 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.646 % | 36.5126 | 85.81 % | 91.04 % | 92.14 % | 94.65 % | 96.04 % | 96.92 % |
| 0.15 ATR | 0.969 % | 36.3939 | 78.87 % | 86.1 % | 88.31 % | 91.72 % | 93.81 % | 95.69 % |
| 0.2 ATR | 1.292 % | 36.2752 | 71.33 % | 80.36 % | 84.27 % | 88.59 % | 91.07 % | 93.64 % |
| 0.25 ATR | 1.615 % | 36.1565 | 65.39 % | 76.44 % | 80.65 % | 85.86 % | 88.83 % | 92.1 % |
| 0.35 ATR | 2.261 % | 35.9191 | 52.92 % | 67.47 % | 74.09 % | 79.29 % | 84.16 % | 88.51 % |
| 0.5 ATR | 3.23 % | 35.5629 | 38.13 % | 54.48 % | 62.1 % | 70.91 % | 78.58 % | 84.51 % |
| 0.75 ATR | 4.845 % | 34.9694 | 22.33 % | 38.97 % | 48.08 % | 58.48 % | 68.93 % | 76.62 % |
| 1.0 ATR | 6.46 % | 34.3759 | 9.96 % | 24.47 % | 34.48 % | 45.56 % | 57.87 % | 67.9 % |
| 1.25 ATR | 8.075 % | 33.7823 | 3.62 % | 14.2 % | 23.99 % | 34.44 % | 50.05 % | 61.54 % |
| 1.5 ATR | 9.69 % | 33.1888 | 1.01 % | 7.05 % | 15.73 % | 25.35 % | 41.12 % | 55.69 % |
| 2.0 ATR | 12.921 % | 32.0017 | 0.1 % | 1.91 % | 5.04 % | 14.24 % | 28.32 % | 44.41 % |
| 2.5 ATR | 16.151 % | 30.8146 | 0.0 % | 0.2 % | 1.21 % | 5.76 % | 18.07 % | 33.64 % |
| 3.0 ATR | 19.381 % | 29.6276 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.37 % | 25.74 % |
| 4.0 ATR | 25.841 % | 27.2534 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.94 % | 10.56 % |
| 6.0 ATR | 38.762 % | 22.5051 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.03 ATR | 1.23 ATR | 1.37 ATR | 1.77 ATR | 2.00 ATR |
| **5 s.** | 0.43 ATR | 0.91 ATR | 1.01 ATR | 1.29 ATR | 1.52 ATR | 1.74 ATR | 2.25 ATR | 2.62 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.16 ATR | 2.41 ATR | 3.16 ATR | 3.76 ATR |
| **20 s.** | 0.80 ATR | 1.75 ATR | 1.97 ATR | 2.54 ATR | 3.05 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.43–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.653–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.845 %, prix 34.9695), p(touche) 38.97 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.807–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.46 %, prix 34.376), p(touche) 34.48 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.013–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.075 %, prix 33.7824), p(touche) 34.44 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.391–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.69 %, prix 33.1889), p(touche) 41.12 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.974–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.921 %, prix 32.0015), p(touche) 44.41 % (en stress 98.98 %)  ✅ optimum identifie (68.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.018 | EV/share : $0.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 26 % | T3 26 %
- Kelly (position) : f* 0.061 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 63.6 | bear 29.5 | side 6.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.746% → cible +5.749% / stop −2.874%, p_fill 52%, n_eff≈26.9) : P(cible|rempli) **5%** · **EV/risk -0.065** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −3.85% → cible +5.599% / stop −6.719%, p_fill 58%, n_eff≈23.8) : P(cible|rempli) **54%** · **EV/risk -0.027** (×p_fill ; si rempli -0.32% du capital)
  - **deep** (entrée dip −5.939% → cible +7.918% / stop −10.303%, p_fill 50%, n_eff≈21.1) : P(cible|rempli) **50%** · **EV/risk -0.044** (×p_fill ; si rempli -0.91% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→82% · +2.0%→66% · +3.0%→55% · +5.0%→28% · +8.0%→12%
- Range intraday médian 7.27% (p90 11.71%) · excursion haute méd. +3.6% / basse méd. −2.65%
- Profil de vol intra : ouverture 4.994% vs midi 1.407% vs clôture 1.611% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 66% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. 0.05% ; recovery-V 28%
- **σ réalisé intraday** 4.012% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 53% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 39.3778 (VA 39.1437–39.4753 ; dernier close 39.52)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 77% · **stop −4.73%** sous le fill (sous le bruit) · cible +2.48% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.44% · baisse 54% (gap-down >1% 39% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.14% (p90 −2.74%) · haut méd +1.35% · range méd 2.72%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.85%) · haut méd +1.69% · range méd 3.56%
- Excursion ouverture 30min (n=160) : bas méd −1.81% (p90 −4.85%) · haut méd +2.05% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −1.95% (p90 −5.3%) · haut méd +2.23% · range méd 4.91%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 78% (130/159) · gap 49% · délai 0.0min · rebond 58% (83/130) (MFE +1.8%)
   - −1.0% : fill 30min 67% · séance 72% (123/159) · gap 39% · délai 0.0min · rebond 67% (88/123) (MFE +2.21%)
   - −1.5% : fill 30min 61% · séance 67% (115/159) · gap 33% · délai 0.0min · rebond 69% (79/115) (MFE +1.96%)
   - −2.0% : fill 30min 54% · séance 60% (105/159) · gap 20% · délai 0.0min · rebond 71% (72/105) (MFE +2.19%)
   - −3.0% : fill 30min 43% · séance 51% (89/159) · gap 10% · délai 4.4min · rebond 68% (63/89) (MFE +2.33%)
   - −4.0% : fill 30min 26% · séance 42% (73/159) · gap 5% · délai 15.6min · rebond 65% (54/73) (MFE +2.14%)
   - −5.0% : fill 30min 17% · séance 32% (60/159) · gap 3% · délai 24.8min · rebond 77% (50/60) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −2.83%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.84% (p90 −2.85%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.78% (p90 −2.66%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1104 jambes) : jambe baissière méd −1.28% (p90 −2.98%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (81 séances) :
      · −1.0% : fill 100% (81/81) · rebond 66% (57/81)
      · −2.0% : fill 88% (74/81) · rebond 74% (55/74)
      · −3.0% : fill 75% (63/81) · rebond 68% (45/63)
      · −4.0% : fill 61% (50/81) · rebond 64% (37/50)
      · −5.0% : fill 46% (41/81) · rebond 69% (32/41)
   - **flat** (15 séances) :
      · −1.0% : fill 62% (11/15) · rebond 67% (7/11)
      · −2.0% : fill 55% (10/15) · rebond 79% (5/10)
      · −3.0% : fill 49% (8/15) · rebond 61% (5/8)
      · −4.0% : fill 42% (7/15) · rebond 54% (4/7)
      · −5.0% : fill 31% (6/15) · rebond 95% (5/6)
   - **gap-up** (63 séances) :
      · −1.0% : fill 36% (31/63) · rebond 73% (24/31)
      · −2.0% : fill 22% (21/63) · rebond 48% (12/21)
      · −3.0% : fill 19% (18/63) · rebond 76% (13/18)
      · −4.0% : fill 16% (16/63) · rebond 78% (13/16)
      · −5.0% : fill 14% (13/63) · rebond 100% (13/13)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 60% si les 15 1res min sont vertes (85 cas) · 28% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:05** → P(séance verte=clôture>ouverture) 72% si début vert vs 17% si rouge (base 47% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 231min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **72%** · continue >prix actuel 41% ; creux résiduel méd -1.93% (q20 -3.68%) → **SL/trailing à −3.68%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.63% / q75 +2.84% → **scale +1.63% / runner +2.84%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **17%** (continue à baisser 53%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.75%** (au-delà de la MAE q10 -4.75%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.52% .. +6.1%] · haut q95 +7.59% · bas q05 -5.47%
   - 60min (n=160) : retour [-4.88% .. +5.95%] · haut q95 +7.86% · bas q05 -6.04%
   - 2h (n=160) : retour [-6.29% .. +6.53%] · haut q95 +8.52% · bas q05 -6.97%
   - 4h (n=160) : retour [-6.89% .. +6.88%] · haut q95 +9.0% · bas q05 -8.03%
   - 6h (n=160) : retour [-7.11% .. +7.68%] · haut q95 +10.23% · bas q05 -8.07%
   - session (n=160) : retour [-6.38% .. +8.29%] · haut q95 +10.34% · bas q05 -8.2%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **23%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.29% (p75 2.28% / p90 3.82%) · ~3.0 replis/séance, durée méd 69.04 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 24.37 min, n=47)
   - −1.0% → **78%** (reprise méd 68.85 min, n=30)
   - −1.5% → **68%** (reprise méd 81.24 min, n=16)
   - −2.0% → **67%** (reprise méd 84.17 min, n=12)
   - −3.0% → **75%** (reprise méd 175.72 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.82%** (p90, défaut prudent ; serré/agressif −2.28%) ; extension open→close méd +8.23% (q75 +10.03% / q95 +16.4%), MFE méd +10.28% / q90 +13.1%
   - Échelle scale-out : +10.28% (33%) / +11.83% (33%) / +13.1% (34%)
- **DÉSARMER** : repli > **−3.82%** depuis le plus-haut = décay → P(retournement) **30%** (préavis méd 235.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.1% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.5  _(momentum baissier)_
- **ADX** : 13.2  _(pas de tendance nette)_
- **MACD** : hist -0.384  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 29.6%
- **ATR** : 2.37 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.247  _(distribution)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 53.5  _(transition)_
- **MA** : MA20 40.86 · MA50 40.1 · MA200 44.08  _(prix < MA20)_
- **Dist MA** : MA20 -10.1% · MA50 -8.4% · MA200 -16.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (758001 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
