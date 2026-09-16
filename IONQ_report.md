# IONQ

**Generated** : 2026-09-16T00:38:09.982782+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $37.06  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot $37.06 (+2.0% vs entrée) · entrée $36.34 · stop $35.42 · T1 $38.18 · R/R 2.0  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.064 _(réel 5 s)_ (GBM 0.009) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.54% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +6.7 % ≠ (strike 40.0 − spot 37.06)/spot = +7.9 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.270 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $36.16–$36.52 (mid $36.34)
- Spot actuel : $37.06 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : $35.42 (stop swing_plan-based (-10.66%))
- Targets : T1 $38.18 · R/R 2.0 | T2 $38.61 · R/R 2.47 | T3 $39.03 · R/R 2.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $35.42


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.66 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **1.286 pt plus bas** dans le cas TYPIQUE (médiane), 9.217 au p90, **11.199 au pire**
   - perte réelle **15.082 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 10.66 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0106 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.069 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4992** [0.4252 ; 0.5732] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4718** [0.4196 ; 0.5245] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4651** [0.413 ; 0.5178] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.6 pt), swing (40.7 pt), deep (40.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.61 %** | CVaR **-10.74 %** | vol 6.4 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 10.66 % contre 6.03 % aujourd'hui, rapport 1.77)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.23 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2271** (β de hausse 1.9854, asymétrie 1.1217) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 32.8194 sur support (1.22 ATR, 11.443 %) — p(stop avant cible) 0.5121 [0.46 ; 0.56], R/R 1.111, perte reelle 16.903 % (gap inclus), CVaR 11.452 %, EV -3.586 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0264 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.512, borne haute 0.565 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.32 ATR (stop 5.691 %) — p(stop avant cible) 0.7539 [0.71 ; 0.80], R/R 2.289, perte reelle 8.204 % (gap inclus), EV -2.5185 % — **REFUSE**
      - refuse : p_stop_first 0.754, borne haute 0.797 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.52 %) : P(cible) 17.4 % x 18.78 % + P(rien) 7.2 % x 5.51 % ne couvrent pas P(stop) 75.4 % x 8.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 9.577 %) — p(stop avant cible) 0.6088 [0.56 ; 0.66], R/R 1.345, perte reelle 13.966 % (gap inclus), EV -3.3913 % — **REFUSE**
      - refuse : p_stop_first 0.609, borne haute 0.659 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.39 %) : P(cible) 24.5 % x 18.78 % + P(rien) 14.6 % x 3.47 % ne couvrent pas P(stop) 60.9 % x 13.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.22 ATR (stop 11.443 %) — p(stop avant cible) 0.5121 [0.46 ; 0.56], R/R 1.111, perte reelle 16.903 % (gap inclus), EV -3.586 % — **REFUSE**
      - refuse : p_stop_first 0.512, borne haute 0.565 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.59 %) : P(cible) 26.3 % x 18.78 % + P(rien) 22.5 % x 0.56 % ne couvrent pas P(stop) 51.2 % x 16.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.99 ATR (stop 22.749 %) — p(stop avant cible) 0.1394 [0.11 ; 0.18], R/R 0.826, perte reelle 22.749 % (gap inclus), EV -0.4085 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 29.3 % x 18.78 % + P(rien) 56.7 % x -4.85 % ne couvrent pas P(stop) 13.9 % x 22.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.72 ATR (stop 33.812 %) — p(stop avant cible) 0.0232 [0.01 ; 0.04], R/R 0.555, perte reelle 33.812 % (gap inclus), EV -0.4795 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 29.4 % x 18.78 % + P(rien) 68.2 % x -7.66 % ne couvrent pas P(stop) 2.3 % x 33.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.32 ATR (stop 3.935 %) — p(stop avant cible) 0.818 [0.77 ; 0.86], R/R 3.23, perte reelle 5.815 % (gap inclus), EV -1.8356 % — **REFUSE**
      - refuse : cible atteinte seulement 14.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.818, borne haute 0.856 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 14.1 % x 18.78 % + P(rien) 4.1 % x 6.66 % ne couvrent pas P(stop) 81.8 % x 5.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.789 %) — p(stop avant cible) 0.7904 [0.75 ; 0.83], R/R 2.802, perte reelle 6.703 % (gap inclus), EV -2.0571 % — **REFUSE**
      - refuse : p_stop_first 0.790, borne haute 0.831 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 15.3 % x 18.78 % + P(rien) 5.6 % x 6.41 % ne couvrent pas P(stop) 79.0 % x 6.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 12.77 %) — p(stop avant cible) 0.4537 [0.40 ; 0.51], R/R 0.859, perte reelle 21.859 % (gap inclus), EV -4.9082 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.91 %) : P(cible) 27.1 % x 18.78 % + P(rien) 27.5 % x -0.32 % ne couvrent pas P(stop) 45.4 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 14.366 %) — p(stop avant cible) 0.3731 [0.32 ; 0.42], R/R 0.859, perte reelle 21.859 % (gap inclus), EV -3.7171 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.72 %) : P(cible) 27.4 % x 18.78 % + P(rien) 35.3 % x -2.02 % ne couvrent pas P(stop) 37.3 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 15.963 %) — p(stop avant cible) 0.3062 [0.26 ; 0.36], R/R 0.859, perte reelle 21.859 % (gap inclus), EV -2.6758 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 27.7 % x 18.78 % + P(rien) 41.7 % x -2.82 % ne couvrent pas P(stop) 30.6 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.99 ATR (stop 20.993 %) — p(stop avant cible) 0.1772 [0.14 ; 0.22], R/R 0.859, perte reelle 21.859 % (gap inclus), EV -0.6287 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 29.3 % x 18.78 % + P(rien) 52.9 % x -4.28 % ne couvrent pas P(stop) 17.7 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 25.54 %) — p(stop avant cible) 0.0907 [0.06 ; 0.12], R/R 0.735, perte reelle 25.54 % (gap inclus), EV -0.4114 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 29.4 % x 18.78 % + P(rien) 61.5 % x -5.88 % ne couvrent pas P(stop) 9.1 % x 25.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.72 ATR (stop 32.056 %) — p(stop avant cible) 0.0379 [0.02 ; 0.06], R/R 0.586, perte reelle 32.056 % (gap inclus), EV -0.5212 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 29.4 % x 18.78 % + P(rien) 66.8 % x -7.25 % ne couvrent pas P(stop) 3.8 % x 32.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 35.118 %) — p(stop avant cible) 0.0154 [0.01 ; 0.03], R/R 0.535, perte reelle 35.118 % (gap inclus), EV -0.4445 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 29.4 % x 18.78 % + P(rien) 69.0 % x -7.88 % ne couvrent pas P(stop) 1.5 % x 35.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 38.31 %) — p(stop avant cible) 0.0073 [0.00 ; 0.02], R/R 0.49, perte reelle 38.31 % (gap inclus), EV -0.4119 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 29.4 % x 18.78 % + P(rien) 69.8 % x -8.11 % ne couvrent pas P(stop) 0.7 % x 38.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 41.503 %) — p(stop avant cible) 0.0042 [0.00 ; 0.02], R/R 0.453, perte reelle 41.503 % (gap inclus), EV -0.422 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 29.4 % x 18.78 % + P(rien) 70.1 % x -8.24 % ne couvrent pas P(stop) 0.4 % x 41.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 44.695 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.42, perte reelle 44.695 % (gap inclus), EV -0.4193 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 29.4 % x 18.78 % + P(rien) 70.4 % x -8.38 % ne couvrent pas P(stop) 0.1 % x 44.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 47.888 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.392, perte reelle 47.888 % (gap inclus), EV -0.4026 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 29.4 % x 18.78 % + P(rien) 70.5 % x -8.38 % ne couvrent pas P(stop) 0.1 % x 47.89 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 51.08 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.368, perte reelle 51.08 % (gap inclus), EV -0.3848 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 29.4 % x 18.78 % + P(rien) 70.5 % x -8.39 % ne couvrent pas P(stop) 0.0 % x 51.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 37.06, ATR14 2.3663 (6.385 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.379 ATR = 2.42 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.319 % | 36.9417 | 93.66 % | 95.36 % | 96.06 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.639 % | 36.8234 | 85.8 % | 91.13 % | 92.23 % | 94.64 % | 96.04 % | 96.92 % |
| 0.15 ATR | 0.958 % | 36.7051 | 78.85 % | 86.19 % | 88.4 % | 91.71 % | 93.8 % | 95.69 % |
| 0.2 ATR | 1.277 % | 36.5867 | 71.3 % | 80.44 % | 84.36 % | 88.57 % | 91.06 % | 93.63 % |
| 0.25 ATR | 1.596 % | 36.4684 | 65.36 % | 76.51 % | 80.73 % | 85.95 % | 88.92 % | 92.09 % |
| 0.35 ATR | 2.235 % | 36.2318 | 52.87 % | 67.54 % | 74.17 % | 79.37 % | 84.25 % | 88.5 % |
| 0.5 ATR | 3.193 % | 35.8769 | 38.07 % | 54.54 % | 62.26 % | 71.08 % | 78.76 % | 84.5 % |
| 0.75 ATR | 4.789 % | 35.2853 | 22.36 % | 39.11 % | 48.23 % | 58.65 % | 69.11 % | 76.69 % |
| 1.0 ATR | 6.385 % | 34.6937 | 9.97 % | 24.5 % | 34.61 % | 45.8 % | 58.13 % | 68.07 % |
| 1.25 ATR | 7.981 % | 34.1021 | 3.63 % | 14.21 % | 24.02 % | 34.58 % | 50.3 % | 61.7 % |
| 1.5 ATR | 9.578 % | 33.5106 | 1.01 % | 7.06 % | 15.74 % | 25.48 % | 41.26 % | 55.95 % |
| 2.0 ATR | 12.77 % | 32.3274 | 0.1 % | 1.92 % | 5.05 % | 14.36 % | 28.35 % | 44.66 % |
| 2.5 ATR | 15.963 % | 31.1443 | 0.0 % | 0.2 % | 1.21 % | 5.86 % | 18.09 % | 33.88 % |
| 3.0 ATR | 19.155 % | 29.9611 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.38 % | 25.87 % |
| 4.0 ATR | 25.54 % | 27.5949 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 38.31 % | 22.8623 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.66 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.23 ATR | 1.37 ATR | 1.77 ATR | 2.01 ATR |
| **5 s.** | 0.43 ATR | 0.92 ATR | 1.02 ATR | 1.29 ATR | 1.52 ATR | 1.75 ATR | 2.26 ATR | 2.63 ATR |
| **10 s.** | 0.60 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.16 ATR | 2.41 ATR | 3.16 ATR | 3.76 ATR |
| **20 s.** | 0.80 ATR | 1.76 ATR | 1.99 ATR | 2.56 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.43–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.655–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.789 %, prix 35.2852), p(touche) 39.11 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.809–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.385 %, prix 34.6937), p(touche) 34.61 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.018–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.981 %, prix 34.1022), p(touche) 34.58 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.397–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.578 %, prix 33.5104), p(touche) 41.26 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.985–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.77 %, prix 32.3274), p(touche) 44.66 % (en stress 98.98 %)  ✅ optimum identifie (68.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.009 | EV/share : $0.008 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 25 % | T3 25 %
- Kelly (position) : f* 0.034 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 63.6 | bear 29.4 | side 7.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.943% → cible +5.072% / stop −2.536%, p_fill 51%, n_eff≈26.0) : P(cible|rempli) **3%** · **EV/risk -0.064** (×p_fill ; si rempli -0.32% du capital)
  - **swing** (entrée dip −4.275% → cible +5.521% / stop −6.67%, p_fill 51%, n_eff≈20.6) : P(cible|rempli) **48%** · **EV/risk -0.067** (×p_fill ; si rempli -0.87% du capital)
  - **deep** (entrée dip −6.602% → cible +7.807% / stop −10.255%, p_fill 50%, n_eff≈20.7) : P(cible|rempli) **52%** · **EV/risk -0.021** (×p_fill ; si rempli -0.43% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.5  _(momentum baissier)_
- **ADX** : 12.5  _(pas de tendance nette)_
- **MACD** : hist -0.299  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 24.9%
- **ATR** : 2.37 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.275  _(distribution)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 47.6  _(transition)_
- **MA** : MA20 39.94 · MA50 39.63 · MA200 43.98  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -6.5% · MA200 -15.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (758621 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
