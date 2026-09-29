# IONQ

**Generated** : 2026-09-29T00:37:59.954890+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $44.56  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $44.56 (+5.5% vs entrée) · entrée $42.24 · stop $39.53 · T1 $44.08 · R/R 0.68  
> ↳ P(T1 av. stop) 53 % _(réel 5 s)_ · EV/risk -0.029 _(réel 5 s)_ (GBM -0.032) · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -7.7 % ≠ (strike 42.0 − spot 44.56)/spot = -5.7 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.170 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $41.87–$42.61 (mid $42.24)
- Spot actuel : $44.56 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : $39.53 (plancher anti-bruit (R/R<2) ; -6.42 % depuis l'entree)
- Targets : T1 $44.08 · R/R 0.68 | T2 $45.93 · R/R 1.36 | T3 $47.77 · R/R 2.04
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $39.53


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.28 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **0.666 pt plus bas** dans le cas TYPIQUE (médiane), 8.597 au p90, **10.579 au pire**
   - perte réelle **15.082 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 11.28 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0091 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.069 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5019** [0.4279 ; 0.5758] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4197** [0.3685 ; 0.4722] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4144** [0.3634 ; 0.4669] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (38.3 pt), swing (45.1 pt), deep (45.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.53 %** | CVaR **-10.49 %** | vol 6.1 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 11.61 % contre 5.96 % aujourd'hui, rapport 1.95)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.88 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.899 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2142** (β de hausse 1.9813, asymétrie 1.1175) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 39.2627 sur grid_snapped (1.66 ATR, 11.888 %) — p(stop avant cible) 0.471 [0.42 ; 0.52], R/R 1.167, perte reelle 16.903 % (gap inclus), CVaR 11.896 %, EV -2.694 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.118 %) — p(stop avant cible) 0.615 [0.56 ; 0.67], R/R 1.515, perte reelle 13.019 % (gap inclus), EV -2.7441 % — **REFUSE**
      - refuse : p_stop_first 0.615, borne haute 0.665 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.74 %) : P(cible) 23.8 % x 19.73 % + P(rien) 14.7 % x 3.83 % ne couvrent pas P(stop) 61.5 % x 13.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 1.66 ATR (stop 12.861 %) — p(stop avant cible) 0.4293 [0.38 ; 0.48], R/R 0.902, perte reelle 21.859 % (gap inclus), EV -4.1076 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.11 %) : P(cible) 26.8 % x 19.73 % + P(rien) 30.2 % x -0.06 % ne couvrent pas P(stop) 42.9 % x 21.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.83 ATR (stop 26.091 %) — p(stop avant cible) 0.0848 [0.06 ; 0.12], R/R 0.756, perte reelle 26.091 % (gap inclus), EV 0.1183 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.09 % > budget 12.00 %
   - 🟢 support a 5.38 ATR (stop 35.494 %) — p(stop avant cible) 0.0122 [0.00 ; 0.03], R/R 0.556, perte reelle 35.494 % (gap inclus), EV 0.1439 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.49 % > budget 12.00 %
   - 🟢 support a 6.89 ATR (stop 44.695 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.441, perte reelle 44.695 % (gap inclus), EV 0.141 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.70 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.52 %) — p(stop avant cible) 0.9178 [0.89 ; 0.94], R/R 6.031, perte reelle 3.271 % (gap inclus), EV -1.5006 % — **REFUSE**
      - refuse : cible atteinte seulement 7.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.918, borne haute 0.943 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.50 %) : P(cible) 7.2 % x 19.73 % + P(rien) 1.0 % x 7.85 % ne couvrent pas P(stop) 91.8 % x 3.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.039 %) — p(stop avant cible) 0.8608 [0.82 ; 0.89], R/R 3.966, perte reelle 4.974 % (gap inclus), EV -1.8224 % — **REFUSE**
      - refuse : cible atteinte seulement 11.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.861, borne haute 0.894 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.82 %) : P(cible) 11.7 % x 19.73 % + P(rien) 2.2 % x 6.93 % ne couvrent pas P(stop) 86.1 % x 4.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.559 %) — p(stop avant cible) 0.7983 [0.75 ; 0.84], R/R 3.049, perte reelle 6.469 % (gap inclus), EV -1.9037 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.798, borne haute 0.838 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.90 %) : P(cible) 14.7 % x 19.73 % + P(rien) 5.5 % x 6.60 % ne couvrent pas P(stop) 79.8 % x 6.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 6.079 %) — p(stop avant cible) 0.7501 [0.70 ; 0.79], R/R 2.267, perte reelle 8.701 % (gap inclus), EV -2.6139 % — **REFUSE**
      - refuse : p_stop_first 0.750, borne haute 0.793 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.61 %) : P(cible) 17.6 % x 19.73 % + P(rien) 7.4 % x 5.96 % ne couvrent pas P(stop) 75.0 % x 8.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 7.599 %) — p(stop avant cible) 0.665 [0.61 ; 0.71], R/R 1.854, perte reelle 10.638 % (gap inclus), EV -2.2307 % — **REFUSE**
      - refuse : p_stop_first 0.665, borne haute 0.713 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.23 %) : P(cible) 22.1 % x 19.73 % + P(rien) 11.4 % x 4.26 % ne couvrent pas P(stop) 66.5 % x 10.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.66 ATR (stop 11.888 %) — p(stop avant cible) 0.471 [0.42 ; 0.52], R/R 1.167, perte reelle 16.903 % (gap inclus), EV -2.694 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.69 %) : P(cible) 26.1 % x 19.73 % + P(rien) 26.8 % x 0.47 % ne couvrent pas P(stop) 47.1 % x 16.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 13.677 %) — p(stop avant cible) 0.3791 [0.33 ; 0.43], R/R 0.902, perte reelle 21.859 % (gap inclus), EV -3.3654 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.37 %) : P(cible) 27.0 % x 19.73 % + P(rien) 35.1 % x -1.17 % ne couvrent pas P(stop) 37.9 % x 21.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 15.197 %) — p(stop avant cible) 0.3172 [0.27 ; 0.37], R/R 0.902, perte reelle 21.859 % (gap inclus), EV -2.4353 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.44 %) : P(cible) 27.3 % x 19.73 % + P(rien) 41.0 % x -2.14 % ne couvrent pas P(stop) 31.7 % x 21.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 16.717 %) — p(stop avant cible) 0.2613 [0.22 ; 0.31], R/R 0.902, perte reelle 21.859 % (gap inclus), EV -1.4943 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.49 %) : P(cible) 28.1 % x 19.73 % + P(rien) 45.8 % x -2.88 % ne couvrent pas P(stop) 26.1 % x 21.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 18.236 %) — p(stop avant cible) 0.2296 [0.19 ; 0.28], R/R 0.902, perte reelle 21.859 % (gap inclus), EV -1.0184 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 28.2 % x 19.73 % + P(rien) 48.8 % x -3.21 % ne couvrent pas P(stop) 23.0 % x 21.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 21.276 %) — p(stop avant cible) 0.1641 [0.13 ; 0.21], R/R 0.902, perte reelle 21.859 % (gap inclus), EV -0.0154 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 28.5 % x 19.73 % + P(rien) 55.1 % x -3.73 % ne couvrent pas P(stop) 16.4 % x 21.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 3.83 ATR (stop 25.118 %) — p(stop avant cible) 0.0907 [0.06 ; 0.12], R/R 0.785, perte reelle 25.118 % (gap inclus), EV 0.1631 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.12 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 27.355 %) — p(stop avant cible) 0.068 [0.04 ; 0.10], R/R 0.721, perte reelle 27.355 % (gap inclus), EV 0.1044 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.35 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 30.394 %) — p(stop avant cible) 0.0444 [0.03 ; 0.07], R/R 0.649, perte reelle 30.394 % (gap inclus), EV 0.0541 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.39 % > budget 12.00 %
   - 🟢 grid_snapped a 5.38 ATR (stop 34.521 %) — p(stop avant cible) 0.0219 [0.01 ; 0.04], R/R 0.571, perte reelle 34.521 % (gap inclus), EV 0.0711 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.52 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 36.473 %) — p(stop avant cible) 0.011 [0.00 ; 0.03], R/R 0.541, perte reelle 36.473 % (gap inclus), EV 0.1402 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.47 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 39.512 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.499, perte reelle 39.512 % (gap inclus), EV 0.146 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.51 % > budget 12.00 %
   - 🟢 grid_snapped a 6.89 ATR (stop 43.722 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.451, perte reelle 43.722 % (gap inclus), EV 0.1404 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.72 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 45.591 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.433, perte reelle 45.591 % (gap inclus), EV 0.1442 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.59 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 48.63 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.406, perte reelle 48.63 % (gap inclus), EV 0.1613 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.63 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 44.56, ATR14 2.7087 (6.079 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.377 ATR = 2.292 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.304 % | 44.4246 | 93.55 % | 95.36 % | 96.06 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.608 % | 44.2891 | 85.8 % | 91.03 % | 92.13 % | 94.44 % | 95.93 % | 96.92 % |
| 0.15 ATR | 0.912 % | 44.1537 | 78.75 % | 85.99 % | 88.29 % | 91.51 % | 93.7 % | 95.69 % |
| 0.2 ATR | 1.216 % | 44.0183 | 71.2 % | 80.24 % | 84.26 % | 88.37 % | 90.96 % | 93.63 % |
| 0.25 ATR | 1.52 % | 43.8828 | 65.16 % | 76.21 % | 80.52 % | 85.64 % | 88.82 % | 92.09 % |
| 0.35 ATR | 2.128 % | 43.612 | 52.67 % | 67.24 % | 73.86 % | 79.07 % | 84.15 % | 88.5 % |
| 0.5 ATR | 3.039 % | 43.2056 | 37.87 % | 54.23 % | 61.96 % | 70.78 % | 78.66 % | 84.5 % |
| 0.75 ATR | 4.559 % | 42.5285 | 22.46 % | 39.01 % | 48.13 % | 58.54 % | 69.11 % | 76.8 % |
| 1.0 ATR | 6.079 % | 41.8513 | 10.17 % | 24.4 % | 34.51 % | 45.5 % | 57.83 % | 68.17 % |
| 1.25 ATR | 7.599 % | 41.1741 | 3.83 % | 14.31 % | 23.92 % | 34.38 % | 49.9 % | 61.91 % |
| 1.5 ATR | 9.118 % | 40.4969 | 1.11 % | 7.06 % | 15.54 % | 25.18 % | 40.96 % | 56.26 % |
| 2.0 ATR | 12.158 % | 39.1426 | 0.1 % | 1.92 % | 4.94 % | 14.05 % | 28.05 % | 45.17 % |
| 2.5 ATR | 15.197 % | 37.7882 | 0.0 % | 0.2 % | 1.21 % | 5.66 % | 17.99 % | 34.19 % |
| 3.0 ATR | 18.236 % | 36.4339 | 0.0 % | 0.1 % | 0.4 % | 2.53 % | 11.28 % | 25.87 % |
| 4.0 ATR | 24.315 % | 33.7251 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 36.473 % | 28.3077 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.01 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.23 ATR | 1.37 ATR | 1.76 ATR | 2.00 ATR |
| **5 s.** | 0.42 ATR | 0.91 ATR | 1.01 ATR | 1.29 ATR | 1.51 ATR | 1.73 ATR | 2.24 ATR | 2.60 ATR |
| **10 s.** | 0.60 ATR | 1.25 ATR | 1.39 ATR | 1.81 ATR | 2.15 ATR | 2.40 ATR | 3.15 ATR | 3.75 ATR |
| **20 s.** | 0.80 ATR | 1.78 ATR | 2.01 ATR | 2.57 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.428–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.652–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.559 %, prix 42.5285), p(touche) 39.01 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.807–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.079 %, prix 41.8512), p(touche) 34.51 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.011–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.599 %, prix 41.1739), p(touche) 34.38 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.387–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.118 %, prix 40.497), p(touche) 40.96 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.008–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.197 %, prix 37.7882), p(touche) 34.19 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (66.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.032 | EV/share : $-0.087 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 40 % | T3 26 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 72.5 | bear 10.0 | side 17.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 490.0 (= 11 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.361% → cible +4.831% / stop −2.416%, p_fill 47%, n_eff≈23.6) : P(cible|rempli) **8%** · **EV/risk -0.042** (×p_fill ; si rempli -0.21% du capital)
  - **swing** (entrée dip −5.201% → cible +4.36% / stop −6.412%, p_fill 40%, n_eff≈16.4) : P(cible|rempli) **53%** · **EV/risk -0.029** (×p_fill ; si rempli -0.47% du capital)
  - **deep** (entrée dip −8.042% → cible +6.166% / stop −9.915%, p_fill 28%, n_eff≈15.8) : P(cible|rempli) **52%** · **EV/risk -0.046** (×p_fill ; si rempli -1.65% du capital)
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

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 62.0  _(momentum haussier)_
- **ADX** : 17.4  _(pas de tendance nette)_
- **MACD** : hist 0.907  _(pas de croisement recent)_
- **BB** : %B 0.94 · largeur 27.7%
- **ATR** : 2.71 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.169  _(distribution)_
- **Vol ratio** : 1.33  _(volume normal)_
- **Choppiness** : 40.8  _(transition)_
- **MA** : MA20 39.76 · MA50 39.86 · MA200 43.58  _(prix > MA20)_
- **Dist MA** : MA20 +12.1% · MA50 +11.8% · MA200 +2.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (867930 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
