# RGTI

**Generated** : 2026-09-16T00:40:12.448165+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.11  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot $15.11 (+3.6% vs entrée) · entrée $14.59 · stop $14.09 · T1 $15.59 · R/R 2.0  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.096 _(réel 5 s)_ (GBM 0.195) · ¼-Kelly 0.048 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.45% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +8.1 % ≠ (strike 16.5 − spot 15.11)/spot = +9.2 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.240 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $14.52–$14.66 (mid $14.59)
- Spot actuel : $15.11 (+3.6% au-dessus de la zone — repli à attendre)
- Stop : $14.09 (stop swing_plan-based (-12.78%))
- Targets : T1 $15.59 · R/R 2.0 | T2 $15.64 · R/R 2.1 | T3 $15.68 · R/R 2.18
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.09


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.78 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **1.85 pt plus bas** dans le cas TYPIQUE (médiane), 11.785 au p90, **18.433 au pire**
   - perte réelle **17.61 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 12.78 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0231 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.113 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3941** [0.3236 ; 0.4682] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.5291** [0.4764 ; 0.5813] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5037** [0.4511 ; 0.5562] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.8 pt), swing (50.0 pt), deep (42.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.77 %** | CVaR **-10.77 %** | vol 6.77 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 12.20 % contre 6.47 % aujourd'hui, rapport 1.89)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8258** (β de hausse 1.9882, asymétrie 0.9183) vs IWM — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.623× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 13.1505 sur atr_grid (2.5 ATR, 12.968 %) — p(stop avant cible) 0.4869 [0.43 ; 0.54], R/R 1.379, perte reelle 17.61 % (gap inclus), CVaR 12.99 %, EV -3.0789 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0825 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.99 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.86 ATR (stop 7.429 %) — p(stop avant cible) 0.7087 [0.66 ; 0.75], R/R 2.037, perte reelle 11.924 % (gap inclus), EV -3.6279 % — **REFUSE**
      - refuse : p_stop_first 0.709, borne haute 0.755 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.63 %) : P(cible) 16.8 % x 24.29 % + P(rien) 12.3 % x 6.01 % ne couvrent pas P(stop) 70.9 % x 11.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.76 ATR (stop 17.312 %) — p(stop avant cible) 0.302 [0.26 ; 0.35], R/R 0.989, perte reelle 24.565 % (gap inclus), EV -2.5395 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.54 %) : P(cible) 22.2 % x 24.29 % + P(rien) 47.5 % x -1.10 % ne couvrent pas P(stop) 30.2 % x 24.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.29 ATR (stop 20.058 %) — p(stop avant cible) 0.2197 [0.18 ; 0.27], R/R 0.778, perte reelle 31.213 % (gap inclus), EV -2.5613 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.56 %) : P(cible) 22.9 % x 24.29 % + P(rien) 55.2 % x -2.28 % ne couvrent pas P(stop) 22.0 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.297 %) — p(stop avant cible) 0.9403 [0.91 ; 0.96], R/R 7.11, perte reelle 3.416 % (gap inclus), EV -1.9713 % — **REFUSE**
      - refuse : cible atteinte seulement 4.7 % du temps (< 15 %) meme a 10 seances : le R/R de 7.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.940, borne haute 0.962 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.97 %) : P(cible) 4.7 % x 24.29 % + P(rien) 1.3 % x 8.06 % ne couvrent pas P(stop) 94.0 % x 3.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.594 %) — p(stop avant cible) 0.8753 [0.84 ; 0.91], R/R 4.786, perte reelle 5.075 % (gap inclus), EV -1.9365 % — **REFUSE**
      - refuse : cible atteinte seulement 9.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.875, borne haute 0.907 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 9.1 % x 24.29 % + P(rien) 3.4 % x 8.72 % ne couvrent pas P(stop) 87.5 % x 5.07 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.86 ATR (stop 6.002 %) — p(stop avant cible) 0.76 [0.71 ; 0.80], R/R 2.397, perte reelle 10.131 % (gap inclus), EV -3.4572 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.760, borne haute 0.803 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.46 %) : P(cible) 14.8 % x 24.29 % + P(rien) 9.2 % x 7.10 % ne couvrent pas P(stop) 76.0 % x 10.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 9.078 %) — p(stop avant cible) 0.6669 [0.62 ; 0.71], R/R 1.77, perte reelle 13.724 % (gap inclus), EV -3.9691 % — **REFUSE**
      - refuse : p_stop_first 0.667, borne haute 0.715 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.97 %) : P(cible) 18.0 % x 24.29 % + P(rien) 15.3 % x 5.29 % ne couvrent pas P(stop) 66.7 % x 13.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 10.374 %) — p(stop avant cible) 0.6405 [0.59 ; 0.69], R/R 1.619, perte reelle 15.002 % (gap inclus), EV -4.3939 % — **REFUSE**
      - refuse : p_stop_first 0.640, borne haute 0.690 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.39 %) : P(cible) 18.5 % x 24.29 % + P(rien) 17.5 % x 4.16 % ne couvrent pas P(stop) 64.0 % x 15.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 11.671 %) — p(stop avant cible) 0.5602 [0.51 ; 0.61], R/R 1.444, perte reelle 16.825 % (gap inclus), EV -3.9815 % — **REFUSE**
      - refuse : p_stop_first 0.560, borne haute 0.612 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.98 %) : P(cible) 19.6 % x 24.29 % + P(rien) 24.4 % x 2.81 % ne couvrent pas P(stop) 56.0 % x 16.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 12.968 %) — p(stop avant cible) 0.4869 [0.43 ; 0.54], R/R 1.379, perte reelle 17.61 % (gap inclus), EV -3.0789 % — **REFUSE**
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.08 %) : P(cible) 20.2 % x 24.29 % + P(rien) 31.1 % x 1.87 % ne couvrent pas P(stop) 48.7 % x 17.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.76 ATR (stop 15.885 %) — p(stop avant cible) 0.3522 [0.30 ; 0.40], R/R 0.989, perte reelle 24.565 % (gap inclus), EV -3.6024 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.60 %) : P(cible) 21.3 % x 24.29 % + P(rien) 43.5 % x -0.28 % ne couvrent pas P(stop) 35.2 % x 24.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.29 ATR (stop 18.631 %) — p(stop avant cible) 0.259 [0.21 ; 0.31], R/R 0.778, perte reelle 31.213 % (gap inclus), EV -3.4752 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.48 %) : P(cible) 22.4 % x 24.29 % + P(rien) 51.7 % x -1.59 % ne couvrent pas P(stop) 25.9 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 20.749 %) — p(stop avant cible) 0.201 [0.16 ; 0.25], R/R 0.778, perte reelle 31.213 % (gap inclus), EV -2.166 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.17 %) : P(cible) 22.9 % x 24.29 % + P(rien) 57.0 % x -2.54 % ne couvrent pas P(stop) 20.1 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 23.342 %) — p(stop avant cible) 0.1286 [0.10 ; 0.17], R/R 0.778, perte reelle 31.213 % (gap inclus), EV -0.9452 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 22.9 % x 24.29 % + P(rien) 64.2 % x -3.90 % ne couvrent pas P(stop) 12.9 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 25.936 %) — p(stop avant cible) 0.0893 [0.06 ; 0.12], R/R 0.778, perte reelle 31.213 % (gap inclus), EV -0.2574 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 23.4 % x 24.29 % + P(rien) 67.7 % x -4.64 % ne couvrent pas P(stop) 8.9 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 28.53 %) — p(stop avant cible) 0.0703 [0.05 ; 0.10], R/R 0.778, perte reelle 31.213 % (gap inclus), EV 0.0197 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.53 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 31.123 %) — p(stop avant cible) 0.046 [0.03 ; 0.07], R/R 0.778, perte reelle 31.213 % (gap inclus), EV 0.2112 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.12 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 33.717 %) — p(stop avant cible) 0.0291 [0.02 ; 0.05], R/R 0.72, perte reelle 33.717 % (gap inclus), EV 0.3036 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.72 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 36.31 %) — p(stop avant cible) 0.0247 [0.01 ; 0.05], R/R 0.669, perte reelle 36.31 % (gap inclus), EV 0.2661 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.31 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 38.904 %) — p(stop avant cible) 0.0135 [0.01 ; 0.03], R/R 0.624, perte reelle 38.904 % (gap inclus), EV 0.3157 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.90 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 41.498 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.585, perte reelle 41.498 % (gap inclus), EV 0.3721 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.50 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.11, ATR14 0.7838 (5.187 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.408 ATR = 2.116 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.259 % | 15.0708 | 91.94 % | 94.46 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.519 % | 15.0316 | 86.2 % | 91.03 % | 92.33 % | 94.84 % | 95.83 % | 97.43 % |
| 0.15 ATR | 0.778 % | 14.9924 | 80.77 % | 87.3 % | 89.0 % | 91.91 % | 93.9 % | 96.1 % |
| 0.2 ATR | 1.037 % | 14.9532 | 74.32 % | 82.76 % | 85.57 % | 88.78 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.297 % | 14.9141 | 68.18 % | 78.43 % | 81.53 % | 85.64 % | 88.82 % | 92.51 % |
| 0.35 ATR | 1.816 % | 14.8357 | 55.69 % | 68.45 % | 73.76 % | 79.47 % | 84.45 % | 89.63 % |
| 0.5 ATR | 2.594 % | 14.7181 | 40.99 % | 56.85 % | 64.58 % | 71.49 % | 79.27 % | 85.52 % |
| 0.75 ATR | 3.89 % | 14.5222 | 21.85 % | 39.01 % | 49.55 % | 58.85 % | 71.04 % | 79.26 % |
| 1.0 ATR | 5.187 % | 14.3262 | 9.57 % | 23.69 % | 33.5 % | 46.41 % | 62.09 % | 73.0 % |
| 1.25 ATR | 6.484 % | 14.1303 | 4.03 % | 14.52 % | 23.71 % | 37.11 % | 53.35 % | 65.5 % |
| 1.5 ATR | 7.781 % | 13.9343 | 1.71 % | 7.16 % | 13.82 % | 25.78 % | 43.6 % | 57.39 % |
| 2.0 ATR | 10.374 % | 13.5424 | 0.4 % | 1.71 % | 3.94 % | 10.72 % | 25.71 % | 41.38 % |
| 2.5 ATR | 12.968 % | 13.1505 | 0.1 % | 0.4 % | 1.21 % | 4.45 % | 14.53 % | 29.06 % |
| 3.0 ATR | 15.562 % | 12.7586 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.45 % |
| 4.0 ATR | 20.749 % | 11.9749 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.93 % |
| 6.0 ATR | 31.123 % | 10.4073 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.33 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.22 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.04 ATR | 1.34 ATR | 1.53 ATR | 1.69 ATR | 2.06 ATR | 2.46 ATR |
| **10 s.** | 0.63 ATR | 1.34 ATR | 1.46 ATR | 1.80 ATR | 2.03 ATR | 2.25 ATR | 2.81 ATR | 3.41 ATR |
| **20 s.** | 0.92 ATR | 1.73 ATR | 1.89 ATR | 2.34 ATR | 2.67 ATR | 2.89 ATR | 3.60 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.459–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.594 %, prix 14.718), p(touche) 40.99 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (70.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.666–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.89 %, prix 14.5222), p(touche) 39.01 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.821–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.187 %, prix 14.3262), p(touche) 33.5 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.038–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.484 %, prix 14.1303), p(touche) 37.11 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.464–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.781 %, prix 13.9343), p(touche) 43.6 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.887–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.374 %, prix 13.5425), p(touche) 41.38 % (en stress 97.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.195 | EV/share : $0.098 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.191 | ¼-Kelly 0.048 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 71.2 | side 23.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.454% → cible +6.891% / stop −3.445%, p_fill 30%, n_eff≈14.4) : P(cible|rempli) **3%** · **EV/risk -0.096** (×p_fill ; si rempli -1.10% du capital)
  - **swing** (entrée dip −7.593% → cible +5.589% / stop −5.614%, p_fill 15%, n_eff≈10.7) : P(cible|rempli) **70%** · **EV/risk +0.057** (×p_fill ; si rempli +2.13% du capital)
  - **deep** (entrée dip −11.739% → cible +7.905% / stop −8.816%, p_fill 19%, n_eff≈11.4) : P(cible|rempli) **81%** · **EV/risk +0.092** (×p_fill ; si rempli +4.37% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.0  _(momentum baissier)_
- **ADX** : 11.4  _(pas de tendance nette)_
- **MACD** : hist -0.051  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 22.8%
- **ATR** : 0.78 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.239  _(distribution)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 55.6  _(transition)_
- **MA** : MA20 15.89 · MA50 16.03 · MA200 19.0  _(prix < MA20)_
- **Dist MA** : MA20 -4.9% · MA50 -5.8% · MA200 -20.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (764695 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
