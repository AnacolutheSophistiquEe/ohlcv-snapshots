# SMR

**Generated** : 2026-10-07T00:30:25.468960+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $8.02  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (2 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $8.02 (+2.0% vs entrée) · entrée $7.86 · stop $7.70 · T1 $8.12 · R/R 1.62  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.97% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +4.2 % ≠ (strike 8.0 − spot 8.02)/spot = -0.2 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $7.81–$7.91 (mid $7.86)
- Spot actuel : $8.02 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : $7.70 (plancher anti-bruit (R/R<2) ; -2.04 % depuis l'entree)
- Targets : T1 $8.12 · R/R 1.62 | T2 $8.38 · R/R 3.25 | T3 $8.63 · R/R 4.81
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.70


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.41 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.46 %)** : le gap seul le franchit 0.433 % des séances (5 fois sur 1154).
   - exécution **3.325 pt plus bas** dans le cas TYPIQUE (médiane), 13.627 au p90, **18.863 au pire**
   - perte réelle **17.667 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 11.46 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0269 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.476 % | p01 -6.958 % | pire -30.323 % _(sur 1154 séances)_
- **P(stop avant cible)** _(source : daily, 1155 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5832** [0.5089 ; 0.6548] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.5539** [0.5012 ; 0.6057] _(largeur 10.4 pt, n_eff 345.3)_
   - deep : **0.5567** [0.504 ; 0.6084] _(largeur 10.4 pt, n_eff 345.3)_
- ⚠ **5 s — échantillon insuffisant sur : deep (25.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.13 %** | vol 6.95 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.76 % contre 6.00 % aujourd'hui, rapport 1.79)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.11 % vs -18.73 % si l'on extrapolait par √5 _(rapport 1.02 ; < 1 = le √5 surestime)_
- **β de baisse : 1.611** (β de hausse 1.3812, asymétrie 1.1664) vs IWM — 550 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.932× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 7.3745 sur atr_grid (1.25 ATR, 8.049 %) — p(stop avant cible) 0.6846 [0.63 ; 0.73], R/R 2.925, perte reelle 8.222 % (gap inclus), CVaR 9.986 %, EV -1.0161 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3556 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.685, borne haute 0.732 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.15 ATR (stop 3.945 %) — p(stop avant cible) 0.8471 [0.81 ; 0.88], R/R 5.852, perte reelle 4.111 % (gap inclus), EV -0.7445 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.847, borne haute 0.882 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 10.1 % x 24.05 % + P(rien) 5.2 % x 5.94 % ne couvrent pas P(stop) 84.7 % x 4.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 9.658 %) — p(stop avant cible) 0.6063 [0.55 ; 0.66], R/R 2.468, perte reelle 9.748 % (gap inclus), EV -1.2843 % — **REFUSE**
      - refuse : p_stop_first 0.606, borne haute 0.657 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 16.6 % x 24.05 % + P(rien) 22.8 % x 2.78 % ne couvrent pas P(stop) 60.6 % x 9.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 1.57 ATR (stop 13.069 %) — p(stop avant cible) 0.467 [0.41 ; 0.52], R/R 1.821, perte reelle 13.212 % (gap inclus), EV -1.1931 % — **REFUSE**
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 18.8 % x 24.05 % + P(rien) 34.5 % x 1.35 % ne couvrent pas P(stop) 46.7 % x 13.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.15 ATR (stop 2.908 %) — p(stop avant cible) 0.8796 [0.84 ; 0.91], R/R 7.98, perte reelle 3.014 % (gap inclus), EV -0.435 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 7.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.880, borne haute 0.911 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 8.2 % x 24.05 % + P(rien) 3.8 % x 6.12 % ne couvrent pas P(stop) 88.0 % x 3.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.829 %) — p(stop avant cible) 0.818 [0.77 ; 0.86], R/R 4.847, perte reelle 4.962 % (gap inclus), EV -0.9534 % — **REFUSE**
      - refuse : cible atteinte seulement 11.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.818, borne haute 0.856 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 11.2 % x 24.05 % + P(rien) 6.9 % x 5.76 % ne couvrent pas P(stop) 81.8 % x 4.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 6.439 %) — p(stop avant cible) 0.7608 [0.71 ; 0.80], R/R 3.644, perte reelle 6.601 % (gap inclus), EV -1.0294 % — **REFUSE**
      - refuse : cible atteinte seulement 14.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.761, borne haute 0.803 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 14.4 % x 24.05 % + P(rien) 9.6 % x 5.62 % ne couvrent pas P(stop) 76.1 % x 6.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 8.049 %) — p(stop avant cible) 0.6846 [0.63 ; 0.73], R/R 2.925, perte reelle 8.222 % (gap inclus), EV -1.0161 % — **REFUSE**
      - refuse : p_stop_first 0.685, borne haute 0.732 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 16.1 % x 24.05 % + P(rien) 15.4 % x 4.81 % ne couvrent pas P(stop) 68.5 % x 8.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 1.57 ATR (stop 12.032 %) — p(stop avant cible) 0.5033 [0.45 ; 0.56], R/R 1.972, perte reelle 12.196 % (gap inclus), EV -1.3138 % — **REFUSE**
      - refuse : p_stop_first 0.503, borne haute 0.556 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 18.2 % x 24.05 % + P(rien) 31.5 % x 1.42 % ne couvrent pas P(stop) 50.3 % x 12.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 14.488 %) — p(stop avant cible) 0.4277 [0.38 ; 0.48], R/R 1.645, perte reelle 14.619 % (gap inclus), EV -1.2187 % — **REFUSE**
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 19.1 % x 24.05 % + P(rien) 38.2 % x 1.17 % ne couvrent pas P(stop) 42.8 % x 14.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 16.098 %) — p(stop avant cible) 0.3623 [0.31 ; 0.41], R/R 1.48, perte reelle 16.256 % (gap inclus), EV -1.3025 % — **REFUSE**
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 19.3 % x 24.05 % + P(rien) 44.5 % x -0.14 % ne couvrent pas P(stop) 36.2 % x 16.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 17.708 %) — p(stop avant cible) 0.2972 [0.25 ; 0.35], R/R 1.346, perte reelle 17.871 % (gap inclus), EV -1.1702 % — **REFUSE**
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 19.4 % x 24.05 % + P(rien) 50.9 % x -1.01 % ne couvrent pas P(stop) 29.7 % x 17.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 19.318 %) — p(stop avant cible) 0.2434 [0.20 ; 0.29], R/R 1.227, perte reelle 19.6 % (gap inclus), EV -1.1255 % — **REFUSE**
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 19.4 % x 24.05 % + P(rien) 56.3 % x -1.81 % ne couvrent pas P(stop) 24.3 % x 19.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 22.537 %) — p(stop avant cible) 0.1678 [0.13 ; 0.21], R/R 1.055, perte reelle 22.797 % (gap inclus), EV -1.1466 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 19.4 % x 24.05 % + P(rien) 63.8 % x -3.12 % ne couvrent pas P(stop) 16.8 % x 22.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 25.757 %) — p(stop avant cible) 0.0975 [0.07 ; 0.13], R/R 0.922, perte reelle 26.076 % (gap inclus), EV -0.8766 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 19.4 % x 24.05 % + P(rien) 70.8 % x -4.25 % ne couvrent pas P(stop) 9.8 % x 26.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 28.977 %) — p(stop avant cible) 0.0631 [0.04 ; 0.09], R/R 0.818, perte reelle 29.401 % (gap inclus), EV -0.8992 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 19.4 % x 24.05 % + P(rien) 74.2 % x -5.01 % ne couvrent pas P(stop) 6.3 % x 29.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 32.196 %) — p(stop avant cible) 0.0378 [0.02 ; 0.06], R/R 0.744, perte reelle 32.334 % (gap inclus), EV -0.8457 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 19.5 % x 24.05 % + P(rien) 76.8 % x -5.61 % ne couvrent pas P(stop) 3.8 % x 32.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 35.416 %) — p(stop avant cible) 0.0261 [0.01 ; 0.05], R/R 0.678, perte reelle 35.47 % (gap inclus), EV -0.8222 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 19.5 % x 24.05 % + P(rien) 77.9 % x -5.87 % ne couvrent pas P(stop) 2.6 % x 35.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 38.636 %) — p(stop avant cible) 0.0196 [0.01 ; 0.04], R/R 0.622, perte reelle 38.645 % (gap inclus), EV -0.8757 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 19.5 % x 24.05 % + P(rien) 78.6 % x -6.11 % ne couvrent pas P(stop) 2.0 % x 38.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 41.855 %) — p(stop avant cible) 0.0131 [0.00 ; 0.03], R/R 0.573, perte reelle 41.95 % (gap inclus), EV -0.87 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 19.5 % x 24.05 % + P(rien) 79.2 % x -6.31 % ne couvrent pas P(stop) 1.3 % x 41.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 45.075 %) — p(stop avant cible) 0.0107 [0.00 ; 0.03], R/R 0.534, perte reelle 45.075 % (gap inclus), EV -0.8676 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 19.5 % x 24.05 % + P(rien) 79.5 % x -6.37 % ne couvrent pas P(stop) 1.1 % x 45.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 48.294 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.486, perte reelle 49.539 % (gap inclus), EV -0.8663 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 19.5 % x 24.05 % + P(rien) 80.3 % x -6.78 % ne couvrent pas P(stop) 0.2 % x 49.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 51.514 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.467, perte reelle 51.514 % (gap inclus), EV -0.8654 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 19.5 % x 24.05 % + P(rien) 80.5 % x -6.87 % ne couvrent pas P(stop) 0.0 % x 51.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 8.02, ATR14 0.5164 (6.439 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.425 ATR = 2.737 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.322 % | 7.9942 | 92.51 % | 95.07 % | 96.3 % | 97.08 % | 97.97 % | 98.4 % |
| 0.1 ATR | 0.644 % | 7.9684 | 86.8 % | 91.27 % | 93.27 % | 94.72 % | 96.27 % | 97.49 % |
| 0.15 ATR | 0.966 % | 7.9425 | 80.87 % | 87.01 % | 89.69 % | 91.8 % | 94.01 % | 96.11 % |
| 0.2 ATR | 1.288 % | 7.9167 | 75.06 % | 82.64 % | 86.43 % | 89.33 % | 92.43 % | 95.09 % |
| 0.25 ATR | 1.61 % | 7.8909 | 69.8 % | 79.62 % | 83.86 % | 87.19 % | 90.73 % | 93.94 % |
| 0.35 ATR | 2.254 % | 7.8393 | 58.05 % | 72.12 % | 77.47 % | 82.81 % | 87.68 % | 91.54 % |
| 0.5 ATR | 3.22 % | 7.7618 | 41.95 % | 58.9 % | 67.04 % | 74.16 % | 83.28 % | 88.57 % |
| 0.75 ATR | 4.829 % | 7.6327 | 20.58 % | 37.18 % | 47.42 % | 59.78 % | 72.43 % | 81.14 % |
| 1.0 ATR | 6.439 % | 7.5036 | 11.3 % | 25.64 % | 35.65 % | 49.33 % | 64.63 % | 75.31 % |
| 1.25 ATR | 8.049 % | 7.3745 | 4.7 % | 15.9 % | 24.89 % | 38.31 % | 54.8 % | 68.91 % |
| 1.5 ATR | 9.659 % | 7.2454 | 2.24 % | 9.74 % | 16.14 % | 28.2 % | 45.42 % | 62.17 % |
| 2.0 ATR | 12.879 % | 6.9871 | 0.34 % | 3.25 % | 6.5 % | 14.61 % | 31.19 % | 49.03 % |
| 2.5 ATR | 16.098 % | 6.7289 | 0.11 % | 1.34 % | 2.91 % | 6.85 % | 20.56 % | 38.17 % |
| 3.0 ATR | 19.318 % | 6.4707 | 0.11 % | 0.56 % | 1.91 % | 3.82 % | 11.75 % | 28.34 % |
| 4.0 ATR | 25.757 % | 5.9543 | 0.0 % | 0.22 % | 0.34 % | 1.12 % | 4.52 % | 13.49 % |
| 6.0 ATR | 38.636 % | 4.9214 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.34 % | 1.6 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.42 ATR | 0.47 ATR | 0.60 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.84 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.86 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.80 ATR | 1.06 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.21 ATR |
| **5 s.** | 0.48 ATR | 0.98 ATR | 1.10 ATR | 1.38 ATR | 1.62 ATR | 1.80 ATR | 2.30 ATR | 2.81 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.51 ATR | 1.94 ATR | 2.29 ATR | 2.53 ATR | 3.24 ATR | 3.93 ATR |
| **20 s.** | 1.01 ATR | 1.96 ATR | 2.19 ATR | 2.76 ATR | 3.23 ATR | 3.56 ATR | 4.59 ATR | 5.43 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.472–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.22 %, prix 7.7618), p(touche) 41.95 % (en stress 82.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.66–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.829 %, prix 7.6327), p(touche) 37.18 % (en stress 88.89 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (71.9 % des re-echantillons)
- **3 seance(s)** : plage utile 0.801–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.439 %, prix 7.5036), p(touche) 35.65 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.098–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.049 %, prix 7.3745), p(touche) 38.31 % (en stress 95.51 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.515–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.879 %, prix 6.9871), p(touche) 31.19 % (en stress 96.63 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.186–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.098 %, prix 6.7289), p(touche) 38.17 % (en stress 98.86 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.022 | EV/share : $-0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.4 | bear 10.6 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.007% → cible +3.285% / stop −1.972%, p_fill 65%, n_eff≈70.9) : P(cible|rempli) **28%** · **EV/risk -0.035** (×p_fill ; si rempli -0.11% du capital)
  - **swing** (entrée dip −4.42% → cible +14.73% / stop −7.366%, p_fill 56%, n_eff≈66.4) : P(cible|rempli) **24%** · **EV/risk +0.020** (×p_fill ; si rempli +0.27% du capital)
  - **deep** (entrée dip −6.83% → cible +17.701% / stop −10.368%, p_fill 48%, n_eff≈55.0) : P(cible|rempli) **34%** · **EV/risk +0.041** (×p_fill ; si rempli +0.88% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→62% · +3.0%→54% · +5.0%→34% · +8.0%→14%
- Range intraday médian 7.02% (p90 12.09%) · excursion haute méd. +3.23% / basse méd. −3.1%
- Profil de vol intra : ouverture 4.766% vs midi 1.404% vs clôture 1.695% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.568% ; recovery-V 32%
- **σ réalisé intraday** 4.046% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 62% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 7.8201 (VA 7.7996–7.8714 ; dernier close 7.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 45% · rebond 75% · **stop −4.75%** sous le fill (sous le bruit) · cible +2.64% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.3% · baisse 53% (gap-down >1% 35% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.94%) · haut méd +1.32% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −4.33%) · haut méd +1.53% · range méd 3.57%
- Excursion ouverture 30min (n=160) : bas méd −1.69% (p90 −4.84%) · haut méd +1.7% · range méd 4.04%
- Excursion ouverture 60min (n=160) : bas méd −2.12% (p90 −5.34%) · haut méd +2.25% · range méd 4.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 7.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (127/159) · gap 48% · délai 0.0min · rebond 60% (77/127) (MFE +1.63%)
   - −1.0% : fill 30min 63% · séance 75% (121/159) · gap 36% · délai 0.0min · rebond 62% (75/121) (MFE +1.79%)
   - −1.5% : fill 30min 60% · séance 72% (115/159) · gap 26% · délai 0.1min · rebond 67% (80/115) (MFE +1.81%)
   - −2.0% : fill 30min 52% · séance 64% (105/159) · gap 22% · délai 1.0min · rebond 61% (69/105) (MFE +1.75%)
   - −3.0% : fill 30min 40% · séance 52% (90/159) · gap 10% · délai 4.8min · rebond 74% (69/90) (MFE +1.92%)
   - −4.0% : fill 30min 31% · séance 45% (79/159) · gap 4% · délai 7.8min · rebond 75% (60/79) (MFE +2.64%)
   - −5.0% : fill 30min 19% · séance 34% (60/159) · gap 2% · délai 23.4min · rebond 76% (44/60) (MFE +2.19%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −2.48%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.29%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.99% (p90 −2.71%) → stop au-delà de −2.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1089 jambes) : jambe baissière méd −1.28% (p90 −3.12%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (86 séances) :
      · −1.0% : fill 96% (83/86) · rebond 59% (51/83)
      · −2.0% : fill 89% (78/86) · rebond 68% (56/78)
      · −3.0% : fill 83% (73/86) · rebond 79% (59/73)
      · −4.0% : fill 70% (63/86) · rebond 82% (51/63)
      · −5.0% : fill 53% (47/86) · rebond 80% (37/47)
   - **flat** (11 séances) :
      · −1.0% : fill 94% (9/11) · rebond 66% (5/9)
      · −2.0% : fill 52% (6/11) · rebond 39% (2/6)
      · −3.0% : fill 52% (6/11) · rebond 50% (3/6)
      · −4.0% : fill 52% (6/11) · rebond 62% (4/6)
      · −5.0% : fill 39% (4/11) · rebond 78% (3/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 49% (29/62) · rebond 70% (19/29)
      · −2.0% : fill 36% (21/62) · rebond 46% (11/21)
      · −3.0% : fill 15% (11/62) · rebond 49% (7/11)
      · −4.0% : fill 14% (10/62) · rebond 41% (5/10)
      · −5.0% : fill 11% (9/62) · rebond 49% (4/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 72% si les 15 1res min sont vertes (73 cas) · 29% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **51min** → P(séance verte=clôture>ouverture) 84% si début vert vs 19% si rouge (base 47% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 222min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **84%** · continue >prix actuel 59% ; creux résiduel méd -1.71% (q20 -3.75%) → **SL/trailing à −3.75%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.66% / q75 +4.53% → **scale +2.66% / runner +4.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **19%** (continue à baisser 53%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.21%** (au-delà de la MAE q10 -5.21%), cible rebond +2.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.68% .. +4.36%] · haut q95 +6.14% · bas q05 -5.36%
   - 60min (n=160) : retour [-5.02% .. +4.72%] · haut q95 +6.47% · bas q05 -5.85%
   - 2h (n=160) : retour [-7.52% .. +5.37%] · haut q95 +7.8% · bas q05 -7.94%
   - 4h (n=160) : retour [-7.67% .. +6.92%] · haut q95 +8.32% · bas q05 -9.19%
   - 6h (n=160) : retour [-6.72% .. +8.0%] · haut q95 +9.66% · bas q05 -9.21%
   - session (n=160) : retour [-7.99% .. +8.0%] · haut q95 +10.29% · bas q05 -9.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.62%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.33 · part idiosyncratique 0.67
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.5  _(neutre)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist -0.064  _(pas de croisement recent)_
- **BB** : %B 0.35 · largeur 37.6%
- **ATR** : 0.52 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.387  _(distribution)_
- **Vol ratio** : 1.11  _(volume normal)_
- **Choppiness** : 56.0  _(transition)_
- **MA** : MA20 8.51 · MA50 8.99 · MA200 11.86  _(prix < MA20)_
- **Dist MA** : MA20 -5.8% · MA50 -10.8% · MA200 -32.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (528258 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
