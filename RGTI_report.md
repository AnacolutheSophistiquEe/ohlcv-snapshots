# RGTI

**Generated** : 2026-09-14T00:40:44.020224+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.27  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $15.27 (+3.8% vs entrée) · entrée $14.71 · stop $14.39 · T1 $15.35 · R/R 2.0  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.137 _(réel 5 s)_ (GBM 0.264) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.18% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

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

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $14.63–$14.78 (mid $14.71)
- Spot actuel : $15.27 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : $14.39 (stop swing_plan-based (-13.64%))
- Targets : T1 $15.35 · R/R 2.0 | T2 $15.58 · R/R 2.72 | T3 $15.82 · R/R 3.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.39


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.37 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.64 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1254).
   - exécution **1.015 pt plus bas** dans le cas TYPIQUE (médiane), 12.254 au p90, **17.573 au pire**
   - perte réelle **18.441 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 13.64 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0191 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.103 % | p01 -8.97 % | pire -31.213 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5269** [0.4526 ; 0.6003] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4833** [0.4309 ; 0.5359] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4947** [0.4422 ; 0.5473] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (47.7 pt), swing (49.9 pt), deep (42.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.77 %** | CVaR **-10.77 %** | vol 6.8 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 13.52 % contre 6.50 % aujourd'hui, rapport 2.08)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.75 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.823** (β de hausse 1.99, asymétrie 0.9161) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.658× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 13.3639 sur atr_grid (2.25 ATR, 12.482 %) — p(stop avant cible) 0.5343 [0.48 ; 0.59], R/R 1.298, perte reelle 17.61 % (gap inclus), CVaR 12.507 %, EV -3.9719 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1084 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.534, borne haute 0.586 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.51 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.0 ATR (stop 8.62 %) — p(stop avant cible) 0.6782 [0.63 ; 0.73], R/R 1.709, perte reelle 13.376 % (gap inclus), EV -3.9451 % — **REFUSE**
      - refuse : p_stop_first 0.678, borne haute 0.726 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.95 %) : P(cible) 19.7 % x 22.86 % + P(rien) 12.5 % x 4.94 % ne couvrent pas P(stop) 67.8 % x 13.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.75 ATR (stop 18.358 %) — p(stop avant cible) 0.2695 [0.22 ; 0.32], R/R 0.732, perte reelle 31.213 % (gap inclus), EV -3.8123 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.81 %) : P(cible) 24.4 % x 22.86 % + P(rien) 48.6 % x -2.02 % ne couvrent pas P(stop) 27.0 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.23 ATR (stop 21.034 %) — p(stop avant cible) 0.1938 [0.15 ; 0.24], R/R 0.732, perte reelle 31.213 % (gap inclus), EV -2.0807 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 25.0 % x 22.86 % + P(rien) 55.6 % x -3.14 % ne couvrent pas P(stop) 19.4 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.387 %) — p(stop avant cible) 0.9361 [0.91 ; 0.96], R/R 6.509, perte reelle 3.512 % (gap inclus), EV -1.9791 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.936, borne haute 0.958 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.98 %) : P(cible) 5.4 % x 22.86 % + P(rien) 1.0 % x 7.47 % ne couvrent pas P(stop) 93.6 % x 3.51 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.774 %) — p(stop avant cible) 0.8666 [0.83 ; 0.90], R/R 4.32, perte reelle 5.292 % (gap inclus), EV -1.9733 % — **REFUSE**
      - refuse : cible atteinte seulement 10.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.867, borne haute 0.899 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.97 %) : P(cible) 10.3 % x 22.86 % + P(rien) 3.1 % x 8.70 % ne couvrent pas P(stop) 86.7 % x 5.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.0 ATR (stop 7.194 %) — p(stop avant cible) 0.7186 [0.67 ; 0.76], R/R 1.917, perte reelle 11.924 % (gap inclus), EV -3.8762 % — **REFUSE**
      - refuse : p_stop_first 0.719, borne haute 0.764 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.88 %) : P(cible) 18.2 % x 22.86 % + P(rien) 10.0 % x 5.41 % ne couvrent pas P(stop) 71.9 % x 11.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 9.709 %) — p(stop avant cible) 0.6529 [0.60 ; 0.70], R/R 1.572, perte reelle 14.538 % (gap inclus), EV -4.2264 % — **REFUSE**
      - refuse : p_stop_first 0.653, borne haute 0.702 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.23 %) : P(cible) 20.5 % x 22.86 % + P(rien) 14.2 % x 4.10 % ne couvrent pas P(stop) 65.3 % x 14.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 11.096 %) — p(stop avant cible) 0.6013 [0.55 ; 0.65], R/R 1.417, perte reelle 16.129 % (gap inclus), EV -4.2988 % — **REFUSE**
      - refuse : p_stop_first 0.601, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.30 %) : P(cible) 21.4 % x 22.86 % + P(rien) 18.5 % x 2.79 % ne couvrent pas P(stop) 60.1 % x 16.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 12.482 %) — p(stop avant cible) 0.5343 [0.48 ; 0.59], R/R 1.298, perte reelle 17.61 % (gap inclus), EV -3.9719 % — **REFUSE**
      - refuse : p_stop_first 0.534, borne haute 0.586 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.97 %) : P(cible) 22.0 % x 22.86 % + P(rien) 24.5 % x 1.63 % ne couvrent pas P(stop) 53.4 % x 17.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 13.869 %) — p(stop avant cible) 0.4468 [0.40 ; 0.50], R/R 1.167, perte reelle 19.597 % (gap inclus), EV -3.2884 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.29 %) : P(cible) 22.7 % x 22.86 % + P(rien) 32.6 % x 0.83 % ne couvrent pas P(stop) 44.7 % x 19.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.75 ATR (stop 16.932 %) — p(stop avant cible) 0.3264 [0.28 ; 0.38], R/R 0.931, perte reelle 24.565 % (gap inclus), EV -3.0495 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.05 %) : P(cible) 24.0 % x 22.86 % + P(rien) 43.4 % x -1.17 % ne couvrent pas P(stop) 32.6 % x 24.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.23 ATR (stop 19.608 %) — p(stop avant cible) 0.2392 [0.20 ; 0.29], R/R 0.732, perte reelle 31.213 % (gap inclus), EV -3.0395 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.04 %) : P(cible) 24.9 % x 22.86 % + P(rien) 51.2 % x -2.48 % ne couvrent pas P(stop) 23.9 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 22.191 %) — p(stop avant cible) 0.1597 [0.12 ; 0.20], R/R 0.732, perte reelle 31.213 % (gap inclus), EV -1.4994 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.50 %) : P(cible) 25.1 % x 22.86 % + P(rien) 59.0 % x -3.81 % ne couvrent pas P(stop) 16.0 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 24.965 %) — p(stop avant cible) 0.1148 [0.08 ; 0.15], R/R 0.732, perte reelle 31.213 % (gap inclus), EV -0.6145 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 25.5 % x 22.86 % + P(rien) 63.0 % x -4.55 % ne couvrent pas P(stop) 11.5 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 27.739 %) — p(stop avant cible) 0.076 [0.05 ; 0.11], R/R 0.732, perte reelle 31.213 % (gap inclus), EV -0.1355 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 25.6 % x 22.86 % + P(rien) 66.8 % x -5.40 % ne couvrent pas P(stop) 7.6 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 30.513 %) — p(stop avant cible) 0.0527 [0.03 ; 0.08], R/R 0.732, perte reelle 31.213 % (gap inclus), EV 0.1022 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.51 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.287 %) — p(stop avant cible) 0.0359 [0.02 ; 0.06], R/R 0.687, perte reelle 33.287 % (gap inclus), EV 0.1907 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.29 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 36.06 %) — p(stop avant cible) 0.0256 [0.01 ; 0.05], R/R 0.634, perte reelle 36.06 % (gap inclus), EV 0.1917 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.06 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 38.834 %) — p(stop avant cible) 0.0137 [0.01 ; 0.03], R/R 0.589, perte reelle 38.834 % (gap inclus), EV 0.2379 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.83 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.608 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.549, perte reelle 41.608 % (gap inclus), EV 0.2943 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.61 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.382 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 0.515, perte reelle 44.382 % (gap inclus), EV 0.2933 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.38 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.27, ATR14 0.8471 (5.548 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.409 ATR = 2.269 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.277 % | 15.2276 | 92.05 % | 94.46 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.555 % | 15.1853 | 86.32 % | 91.14 % | 92.34 % | 94.85 % | 95.84 % | 97.44 % |
| 0.15 ATR | 0.832 % | 15.1429 | 80.89 % | 87.41 % | 89.01 % | 91.92 % | 93.91 % | 96.1 % |
| 0.2 ATR | 1.11 % | 15.1006 | 74.45 % | 82.88 % | 85.58 % | 88.79 % | 91.47 % | 94.46 % |
| 0.25 ATR | 1.387 % | 15.0582 | 68.21 % | 78.45 % | 81.55 % | 85.66 % | 88.83 % | 92.51 % |
| 0.35 ATR | 1.942 % | 14.9735 | 55.84 % | 68.48 % | 73.79 % | 79.49 % | 84.47 % | 89.64 % |
| 0.5 ATR | 2.774 % | 14.8464 | 41.05 % | 56.9 % | 64.72 % | 71.62 % | 79.29 % | 85.54 % |
| 0.75 ATR | 4.161 % | 14.6346 | 21.83 % | 38.87 % | 49.4 % | 58.89 % | 70.96 % | 79.28 % |
| 1.0 ATR | 5.548 % | 14.4229 | 9.56 % | 23.67 % | 33.47 % | 46.26 % | 61.93 % | 73.03 % |
| 1.25 ATR | 6.935 % | 14.2111 | 4.02 % | 14.5 % | 23.69 % | 36.97 % | 53.2 % | 65.23 % |
| 1.5 ATR | 8.322 % | 13.9993 | 1.71 % | 7.15 % | 13.81 % | 25.66 % | 43.45 % | 57.13 % |
| 2.0 ATR | 11.096 % | 13.5757 | 0.4 % | 1.71 % | 3.93 % | 10.71 % | 25.69 % | 41.13 % |
| 2.5 ATR | 13.869 % | 13.1521 | 0.1 % | 0.4 % | 1.21 % | 4.44 % | 14.52 % | 28.82 % |
| 3.0 ATR | 16.643 % | 12.7286 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.23 % |
| 4.0 ATR | 22.191 % | 11.8814 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.92 % |
| 6.0 ATR | 33.287 % | 10.1871 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.33 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.22 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.03 ATR | 1.34 ATR | 1.52 ATR | 1.69 ATR | 2.06 ATR | 2.46 ATR |
| **10 s.** | 0.63 ATR | 1.33 ATR | 1.46 ATR | 1.79 ATR | 2.03 ATR | 2.25 ATR | 2.81 ATR | 3.41 ATR |
| **20 s.** | 0.92 ATR | 1.72 ATR | 1.88 ATR | 2.33 ATR | 2.67 ATR | 2.88 ATR | 3.59 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.46–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.774 %, prix 14.8464), p(touche) 41.05 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.665–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.161 %, prix 14.6346), p(touche) 38.87 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.819–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.548 %, prix 14.4228), p(touche) 33.47 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.034–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.935 %, prix 14.211), p(touche) 36.97 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.46–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.322 %, prix 13.9992), p(touche) 43.45 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.879–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.096 %, prix 13.5756), p(touche) 41.13 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.264 | EV/share : $0.085 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 30 % | T3 30 %
- Kelly (position) : f* 0.121 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 38.2 | side 56.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.676% → cible +4.368% / stop −2.184%, p_fill 30%, n_eff≈14.4) : P(cible|rempli) **1%** · **EV/risk -0.137** (×p_fill ; si rempli -0.99% du capital)
  - **swing** (entrée dip −8.093% → cible +5.613% / stop −6.036%, p_fill 14%, n_eff≈10.2) : P(cible|rempli) **73%** · **EV/risk +0.067** (×p_fill ; si rempli +2.79% du capital)
  - **deep** (entrée dip −12.509% → cible +7.938% / stop −9.511%, p_fill 19%, n_eff≈11.4) : P(cible|rempli) **81%** · **EV/risk +0.088** (×p_fill ; si rempli +4.48% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→80% · +2.0%→70% · +3.0%→52% · +5.0%→38% · +8.0%→11%
- Range intraday médian 7.28% (p90 11.35%) · excursion haute méd. +3.41% / basse méd. −2.46%
- Profil de vol intra : ouverture 5.227% vs midi 1.5% vs clôture 1.718% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 23% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. 0.053% ; recovery-V 33%
- **σ réalisé intraday** 3.929% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 47% / whipsaw 3%
- POC intraday (dernière séance, temps-au-prix) : 15.2248 (VA 15.1512–15.2668 ; dernier close 15.21)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 43% · rebond 74% · **stop −5.86%** sous le fill (sous le bruit) · cible +2.06% · R/R 0.35 (high win-rate)
- Gaps overnight (n=159) : méd. -0.56% · baisse 61% (gap-down >1% 42% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.16% (p90 −2.84%) · haut méd +1.32% · range méd 2.52%
- Excursion ouverture 15min (n=160) : bas méd −1.38% (p90 −3.63%) · haut méd +1.77% · range méd 3.48%
- Excursion ouverture 30min (n=160) : bas méd −1.68% (p90 −4.49%) · haut méd +2.04% · range méd 4.21%
- Excursion ouverture 60min (n=160) : bas méd −2.04% (p90 −5.47%) · haut méd +2.21% · range méd 5.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (133/159) · gap 50% · délai 0.0min · rebond 61% (83/133) (MFE +1.61%)
   - −1.0% : fill 30min 64% · séance 72% (124/159) · gap 42% · délai 0.0min · rebond 64% (78/124) (MFE +1.58%)
   - −1.5% : fill 30min 59% · séance 66% (117/159) · gap 32% · délai 0.0min · rebond 64% (76/117) (MFE +1.92%)
   - −2.0% : fill 30min 53% · séance 60% (108/159) · gap 26% · délai 0.0min · rebond 64% (72/108) (MFE +1.86%)
   - −3.0% : fill 30min 43% · séance 53% (96/159) · gap 11% · délai 1.2min · rebond 64% (68/96) (MFE +1.9%)
   - −4.0% : fill 30min 34% · séance 43% (75/159) · gap 6% · délai 6.3min · rebond 74% (54/75) (MFE +2.06%)
   - −5.0% : fill 30min 18% · séance 36% (65/159) · gap 2% · délai 25.1min · rebond 57% (45/65) (MFE +1.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −2.2%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.85% (p90 −2.77%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.87% (p90 −2.87%) → stop au-delà de −1.98% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1136 jambes) : jambe baissière méd −1.27% (p90 −3.04%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (88 séances) :
      · −1.0% : fill 90% (84/88) · rebond 57% (48/84)
      · −2.0% : fill 82% (79/88) · rebond 61% (50/79)
      · −3.0% : fill 76% (74/88) · rebond 57% (49/74)
      · −4.0% : fill 64% (60/88) · rebond 72% (42/60)
      · −5.0% : fill 55% (53/88) · rebond 54% (35/53)
   - **flat** (14 séances) :
      · −1.0% : fill 96% (13/14) · rebond 97% (12/13)
      · −2.0% : fill 60% (10/14) · rebond 86% (9/10)
      · −3.0% : fill 40% (5/14) · rebond 92% (4/5)
      · −4.0% : fill 26% (4/14) · rebond 88% (3/4)
      · −5.0% : fill 16% (3/14) · rebond 100% (3/3)
   - **gap-up** (57 séances) :
      · −1.0% : fill 37% (27/57) · rebond 67% (18/27)
      · −2.0% : fill 25% (19/57) · rebond 64% (13/19)
      · −3.0% : fill 21% (17/57) · rebond 90% (15/17)
      · −4.0% : fill 13% (11/57) · rebond 83% (9/11)
      · −5.0% : fill 11% (9/57) · rebond 67% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 75% si les 15 1res min sont vertes (82 cas) · 26% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 95% si début vert vs 9% si rouge (base 52% · écart 86 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **95%** · continue >prix actuel 52% ; creux résiduel méd -1.81% (q20 -2.74%) → **SL/trailing à −2.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.54% / q75 +4.04% → **scale +1.54% / runner +4.04%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **9%** (continue à baisser 65%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.26%** (au-delà de la MAE q10 -5.26%), cible rebond +1.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.98% .. +4.73%] · haut q95 +6.18% · bas q05 -6.02%
   - 60min (n=160) : retour [-5.26% .. +6.01%] · haut q95 +6.6% · bas q05 -6.57%
   - 2h (n=160) : retour [-6.04% .. +6.46%] · haut q95 +8.52% · bas q05 -7.25%
   - 4h (n=160) : retour [-6.16% .. +7.69%] · haut q95 +9.18% · bas q05 -7.73%
   - 6h (n=160) : retour [-6.9% .. +8.52%] · haut q95 +9.73% · bas q05 -8.47%
   - session (n=160) : retour [-7.06% .. +8.89%] · haut q95 +10.31% · bas q05 -8.54%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **27%**. Lecture précoce 30 min : signature présente → 13% vs absente 5% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.66% / p90 2.45%) · ~4.39 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 15.0 min, n=47)
   - −1.0% → **83%** (reprise méd 35.0 min, n=29)
   - −1.5% → **84%** (reprise méd 94.96 min, n=17)
   - −2.0% → **86%** (reprise méd 54.27 min, n=9)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.45%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.3% (q75 +9.62% / q95 +9.99%), MFE méd +9.65% / q90 +11.14%
   - Échelle scale-out : +9.65% (33%) / +10.43% (33%) / +11.14% (34%)
- **DÉSARMER** : repli > **−2.45%** depuis le plus-haut = décay → P(retournement) **23%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.14% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.16%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.2  _(momentum baissier)_
- **ADX** : 12.8  _(pas de tendance nette)_
- **MACD** : hist -0.088  _(pas de croisement recent)_
- **BB** : %B 0.3 · largeur 30.1%
- **ATR** : 0.85 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.228  _(distribution)_
- **Vol ratio** : 0.86  _(volume normal)_
- **Choppiness** : 53.3  _(transition)_
- **MA** : MA20 16.24 · MA50 16.14 · MA200 19.11  _(prix < MA20)_
- **Dist MA** : MA20 -6.0% · MA50 -5.4% · MA200 -20.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (764449 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
