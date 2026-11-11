# RGTI

**Generated** : 2026-11-11T01:25:28.093577+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 7.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $12.12  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)  
> ↳ spot $12.12 (+2.1% vs entrée) · entrée $11.87 · stop $11.39 · T1 $12.81 · R/R 1.96  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -7.5 % ≠ (strike 12.0 − spot 12.12)/spot = -1.0 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-10 : 12.12 · ATR Wilder 1.01 (8.33 %)_
- **Swing** : plage **10.89 → 10.37** (-10.17 % a -14.46 % sous la cloture, 0.51 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 10.71-11.12 (B). stop INDICATIF 9.55 (-7.94 % sous le bas ; sous le support 10.05-10.31 (- 0,5 ATR)).
- **Deep** : plage **10.37 → 9.04** (-14.46 % a -25.45 % sous la cloture, 1.32 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 10.05-10.31 (A) ; 9.5-9.74 (C) ; 8.92-9.19 (A). stop INDICATIF 7.85 (-13.18 % sous le bas ; sous le support 8.35-8.45 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.09 ATR sous le plus haut 20 s., RSI(2) 51.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 10.71-11.12 (B, -8.24 %) ; 10.05-10.31 (A, -14.93 %) ; 9.5-9.74 (C, -19.64 %) ; 8.92-9.19 (A, -24.17 %) ; 8.35-8.45 (B, -30.28 %) ; 6.86-7.03 (B, -42.04 %)
- Resistances reelles au-dessus : 12.59-12.75 (B, 3.88 %) ; 13.13-13.61 (A, 8.33 %) ; 13.82-14.24 (A, 14.03 %) ; 14.37-14.83 (A, 18.56 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.94 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.86 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **1.77 pt plus bas** dans le cas TYPIQUE (médiane), 11.705 au p90, **18.353 au pire**
   - perte réelle **17.61 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 12.86 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0227 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.144 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3442** [0.2765 ; 0.4171] _(largeur 14.1 pt, n_eff 173.1)_
   - swing : **0.4734** [0.4212 ; 0.5261] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4432** [0.3915 ; 0.4959] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (25.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.71 %** | CVaR **-10.67 %** | vol 6.79 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 16.42 % contre 6.46 % aujourd'hui, rapport 2.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.29 % si l'on extrapolait par √5 _(rapport 0.976 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8519** (β de hausse 2.0394, asymétrie 0.908) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.374× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 10.8242 sur support (1.01 ATR, 10.691 %) — p(stop avant cible) 0.5884 [0.54 ; 0.64], R/R 2.234, perte reelle 10.85 % (gap inclus), CVaR 12.498 %, EV -2.0066 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4595 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.50 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.01 ATR (stop 10.691 %) — p(stop avant cible) 0.5884 [0.54 ; 0.64], R/R 2.234, perte reelle 10.85 % (gap inclus), EV -2.0066 % — **REFUSE**
      - refuse : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.01 %) : P(cible) 15.3 % x 24.23 % + P(rien) 25.9 % x 2.60 % ne couvrent pas P(stop) 58.8 % x 10.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 3.12 ATR (stop 28.18 %) — p(stop avant cible) 0.0629 [0.04 ; 0.09], R/R 0.85, perte reelle 28.512 % (gap inclus), EV -1.1798 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 18.6 % x 24.23 % + P(rien) 75.1 % x -5.18 % ne couvrent pas P(stop) 6.3 % x 28.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 2.068 %) — p(stop avant cible) 0.9042 [0.87 ; 0.93], R/R 11.214, perte reelle 2.161 % (gap inclus), EV -0.1093 % — **REFUSE**
      - refuse : cible atteinte seulement 6.4 % du temps (< 15 %) meme a 10 seances : le R/R de 11.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.904, borne haute 0.932 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 6.4 % x 24.23 % + P(rien) 3.2 % x 9.19 % ne couvrent pas P(stop) 90.4 % x 2.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 4.137 %) — p(stop avant cible) 0.8293 [0.79 ; 0.87], R/R 5.749, perte reelle 4.215 % (gap inclus), EV -0.6678 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.829, borne haute 0.866 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 9.2 % x 24.23 % + P(rien) 7.9 % x 7.64 % ne couvrent pas P(stop) 82.9 % x 4.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 6.205 %) — p(stop avant cible) 0.7475 [0.70 ; 0.79], R/R 3.811, perte reelle 6.359 % (gap inclus), EV -1.0421 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.748, borne haute 0.791 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 11.8 % x 24.23 % + P(rien) 13.4 % x 6.28 % ne couvrent pas P(stop) 74.8 % x 6.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.5 ATR (stop 12.41 %) — p(stop avant cible) 0.5189 [0.47 ; 0.57], R/R 1.921, perte reelle 12.612 % (gap inclus), EV -2.1008 % — **REFUSE**
      - refuse : p_stop_first 0.519, borne haute 0.571 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.10 %) : P(cible) 15.8 % x 24.23 % + P(rien) 32.3 % x 1.87 % ne couvrent pas P(stop) 51.9 % x 12.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 14.479 %) — p(stop avant cible) 0.421 [0.37 ; 0.47], R/R 1.649, perte reelle 14.694 % (gap inclus), EV -1.9306 % — **REFUSE**
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 16.5 % x 24.23 % + P(rien) 41.4 % x 0.63 % ne couvrent pas P(stop) 42.1 % x 14.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 16.547 %) — p(stop avant cible) 0.3424 [0.29 ; 0.39], R/R 1.442, perte reelle 16.806 % (gap inclus), EV -1.8777 % — **REFUSE**
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.88 %) : P(cible) 17.3 % x 24.23 % + P(rien) 48.5 % x -0.65 % ne couvrent pas P(stop) 34.2 % x 16.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 18.616 %) — p(stop avant cible) 0.2755 [0.23 ; 0.32], R/R 1.286, perte reelle 18.837 % (gap inclus), EV -1.7511 % — **REFUSE**
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.75 %) : P(cible) 17.8 % x 24.23 % + P(rien) 54.7 % x -1.58 % ne couvrent pas P(stop) 27.6 % x 18.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 20.684 %) — p(stop avant cible) 0.2023 [0.16 ; 0.25], R/R 1.148, perte reelle 21.101 % (gap inclus), EV -1.5715 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 18.2 % x 24.23 % + P(rien) 61.6 % x -2.77 % ne couvrent pas P(stop) 20.2 % x 21.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 22.752 %) — p(stop avant cible) 0.1407 [0.11 ; 0.18], R/R 1.051, perte reelle 23.059 % (gap inclus), EV -1.3047 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 18.2 % x 24.23 % + P(rien) 67.7 % x -3.66 % ne couvrent pas P(stop) 14.1 % x 23.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 33.094 %) — p(stop avant cible) 0.0286 [0.01 ; 0.05], R/R 0.728, perte reelle 33.27 % (gap inclus), EV -1.1025 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 18.6 % x 24.23 % + P(rien) 78.5 % x -5.94 % ne couvrent pas P(stop) 2.9 % x 33.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 37.231 %) — p(stop avant cible) 0.0148 [0.01 ; 0.03], R/R 0.644, perte reelle 37.605 % (gap inclus), EV -1.0643 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 18.7 % x 24.23 % + P(rien) 79.8 % x -6.30 % ne couvrent pas P(stop) 1.5 % x 37.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 41.368 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 0.585, perte reelle 41.429 % (gap inclus), EV -0.9991 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 18.8 % x 24.23 % + P(rien) 80.6 % x -6.56 % ne couvrent pas P(stop) 0.6 % x 41.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 45.505 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 0.527, perte reelle 45.946 % (gap inclus), EV -1.0046 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 18.8 % x 24.23 % + P(rien) 80.9 % x -6.64 % ne couvrent pas P(stop) 0.4 % x 45.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 49.641 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.488, perte reelle 49.641 % (gap inclus), EV -1.0031 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 18.8 % x 24.23 % + P(rien) 81.0 % x -6.71 % ne couvrent pas P(stop) 0.2 % x 49.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 53.778 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.442, perte reelle 54.819 % (gap inclus), EV -0.9901 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.99 %) : P(cible) 18.8 % x 24.23 % + P(rien) 81.1 % x -6.71 % ne couvrent pas P(stop) 0.2 % x 54.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 57.915 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.399, perte reelle 60.715 % (gap inclus), EV -1.0009 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 18.8 % x 24.23 % + P(rien) 81.1 % x -6.71 % ne couvrent pas P(stop) 0.2 % x 60.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 62.052 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.389, perte reelle 62.286 % (gap inclus), EV -1.0036 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 18.8 % x 24.23 % + P(rien) 81.1 % x -6.71 % ne couvrent pas P(stop) 0.2 % x 62.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 66.189 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.366, perte reelle 66.189 % (gap inclus), EV -0.9991 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 18.8 % x 24.23 % + P(rien) 81.1 % x -6.73 % ne couvrent pas P(stop) 0.1 % x 66.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 12.12, ATR14 1.0028 (8.274 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.407 ATR = 3.367 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.414 % | 12.0699 | 92.04 % | 94.35 % | 95.66 % | 97.07 % | 97.56 % | 98.56 % |
| 0.1 ATR | 0.827 % | 12.0197 | 86.2 % | 90.83 % | 92.43 % | 95.05 % | 96.04 % | 97.43 % |
| 0.15 ATR | 1.241 % | 11.9696 | 80.87 % | 87.2 % | 89.1 % | 92.21 % | 94.21 % | 96.1 % |
| 0.2 ATR | 1.655 % | 11.9194 | 73.82 % | 82.46 % | 85.47 % | 88.88 % | 91.57 % | 94.46 % |
| 0.25 ATR | 2.068 % | 11.8693 | 67.88 % | 78.33 % | 81.63 % | 85.84 % | 89.02 % | 92.51 % |
| 0.35 ATR | 2.896 % | 11.769 | 55.49 % | 68.65 % | 74.17 % | 79.78 % | 84.65 % | 89.63 % |
| 0.5 ATR | 4.137 % | 11.6186 | 41.09 % | 57.16 % | 65.19 % | 72.09 % | 79.47 % | 85.32 % |
| 0.75 ATR | 6.205 % | 11.3679 | 21.65 % | 39.31 % | 50.55 % | 59.56 % | 71.34 % | 79.06 % |
| 1.0 ATR | 8.274 % | 11.1172 | 9.47 % | 24.19 % | 34.01 % | 47.32 % | 62.5 % | 72.59 % |
| 1.25 ATR | 10.342 % | 10.8666 | 4.13 % | 14.72 % | 24.02 % | 37.51 % | 53.25 % | 65.3 % |
| 1.5 ATR | 12.41 % | 10.6159 | 1.81 % | 7.36 % | 13.93 % | 25.78 % | 43.5 % | 57.29 % |
| 2.0 ATR | 16.547 % | 10.1145 | 0.3 % | 1.71 % | 4.34 % | 11.12 % | 25.61 % | 41.27 % |
| 2.5 ATR | 20.684 % | 9.6131 | 0.0 % | 0.3 % | 1.11 % | 4.45 % | 14.74 % | 28.95 % |
| 3.0 ATR | 24.821 % | 9.1117 | 0.0 % | 0.1 % | 0.3 % | 1.42 % | 7.32 % | 17.45 % |
| 4.0 ATR | 33.094 % | 8.109 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.63 % | 4.93 % |
| 6.0 ATR | 49.641 % | 6.1035 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.72 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.78 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.41 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.76 ATR | 0.83 ATR | 1.02 ATR | 1.23 ATR | 1.35 ATR | 1.71 ATR | 1.97 ATR |
| **5 s.** | 0.44 ATR | 0.94 ATR | 1.06 ATR | 1.35 ATR | 1.53 ATR | 1.70 ATR | 2.08 ATR | 2.46 ATR |
| **10 s.** | 0.64 ATR | 1.33 ATR | 1.46 ATR | 1.79 ATR | 2.03 ATR | 2.26 ATR | 2.82 ATR | 3.41 ATR |
| **20 s.** | 0.91 ATR | 1.73 ATR | 1.88 ATR | 2.34 ATR | 2.67 ATR | 2.89 ATR | 3.60 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.459–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.137 %, prix 11.6186), p(touche) 41.09 % (en stress 85.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.67–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.205 %, prix 11.368), p(touche) 39.31 % (en stress 92.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.834–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.274 %, prix 11.1172), p(touche) 34.01 % (en stress 88.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.059–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.342 %, prix 10.8665), p(touche) 37.51 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.462–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (12.41 %, prix 10.6159), p(touche) 43.5 % (en stress 95.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (73.9 % des re-echantillons)
- **20 seance(s)** : plage utile 1.884–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (16.547 %, prix 10.1145), p(touche) 41.27 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 63.0 | bear 25.9 | side 11.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.082% → cible +7.981% / stop −3.991%, p_fill 50%, n_eff≈55.4) : P(cible|rempli) **6%** · **EV/risk -0.134** (×p_fill ; si rempli -1.08% du capital)
  - **swing** (entrée dip −4.586% → cible +10.811% / stop −8.671%, p_fill 54%, n_eff≈62.2) : P(cible|rempli) **25%** · **EV/risk -0.100** (×p_fill ; si rempli -1.62% du capital)
  - **deep** (entrée dip −7.079% → cible +13.792% / stop −13.356%, p_fill 51%, n_eff≈57.8) : P(cible|rempli) **27%** · **EV/risk -0.122** (×p_fill ; si rempli -3.17% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→74% · +2.0%→62% · +3.0%→45% · +5.0%→30% · +8.0%→10%
- Range intraday médian 6.39% (p90 11.03%) · excursion haute méd. +2.64% / basse méd. −2.45%
- Profil de vol intra : ouverture 4.544% vs midi 1.307% vs clôture 1.583% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 21% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. -0.493% ; recovery-V 29%
- **σ réalisé intraday** 3.543% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 69% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 11.4051 (VA 11.2514–11.4461 ; dernier close 11.515)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 64% · **stop −4.84%** sous le fill (sous le bruit) · cible +1.64% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.47% · baisse 58% (gap-down >1% 42% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.72%) · haut méd +1.04% · range méd 2.29%
- Excursion ouverture 15min (n=160) : bas méd −1.23% (p90 −3.5%) · haut méd +1.39% · range méd 3.07%
- Excursion ouverture 30min (n=160) : bas méd −1.46% (p90 −4.21%) · haut méd +1.57% · range méd 3.46%
- Excursion ouverture 60min (n=160) : bas méd −1.69% (p90 −4.91%) · haut méd +1.85% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 11.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 73% · séance 83% (132/159) · gap 49% · délai 0.0min · rebond 56% (80/132) (MFE +1.37%)
   - −1.0% : fill 30min 65% · séance 76% (121/159) · gap 42% · délai 0.0min · rebond 62% (76/121) (MFE +1.41%)
   - −1.5% : fill 30min 60% · séance 68% (112/159) · gap 31% · délai 0.0min · rebond 64% (71/112) (MFE +1.58%)
   - −2.0% : fill 30min 54% · séance 62% (102/159) · gap 28% · délai 0.0min · rebond 64% (65/102) (MFE +1.78%)
   - −3.0% : fill 30min 37% · séance 49% (88/159) · gap 11% · délai 2.6min · rebond 64% (61/88) (MFE +1.71%)
   - −4.0% : fill 30min 26% · séance 39% (67/159) · gap 6% · délai 11.9min · rebond 66% (48/67) (MFE +1.75%)
   - −5.0% : fill 30min 10% · séance 28% (53/159) · gap 1% · délai 37.8min · rebond 64% (35/53) (MFE +1.64%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.3% (p90 −1.69%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.55% (p90 −2.09%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −2.13%) → stop au-delà de −1.42% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1023 jambes) : jambe baissière méd −1.27% (p90 −2.97%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (82 séances) :
      · −1.0% : fill 94% (78/82) · rebond 57% (45/78)
      · −2.0% : fill 87% (72/82) · rebond 62% (44/72)
      · −3.0% : fill 73% (65/82) · rebond 62% (43/65)
      · −4.0% : fill 63% (52/82) · rebond 61% (36/52)
      · −5.0% : fill 45% (42/82) · rebond 60% (26/42)
   - **flat** (16 séances) :
      · −1.0% : fill 86% (14/16) · rebond 83% (12/14)
      · −2.0% : fill 55% (10/16) · rebond 92% (9/10)
      · −3.0% : fill 21% (5/16) · rebond 92% (4/5)
      · −4.0% : fill 14% (4/16) · rebond 87% (3/4)
      · −5.0% : fill 8% (3/16) · rebond 100% (3/3)
   - **gap-up** (61 séances) :
      · −1.0% : fill 47% (29/61) · rebond 65% (19/29)
      · −2.0% : fill 29% (20/61) · rebond 60% (12/20)
      · −3.0% : fill 24% (18/61) · rebond 65% (14/18)
      · −4.0% : fill 13% (11/61) · rebond 91% (9/11)
      · −5.0% : fill 9% (8/61) · rebond 78% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 66% si les 15 1res min sont vertes (83 cas) · 22% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 86% si début vert vs 7% si rouge (base 44% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **86%** · continue >prix actuel 47% ; creux résiduel méd -1.47% (q20 -2.26%) → **SL/trailing à −2.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.76% / q75 +3.11% → **scale +1.76% / runner +3.11%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **7%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.13%** (au-delà de la MAE q10 -4.13%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.99% .. +4.08%] · haut q95 +5.52% · bas q05 -5.26%
   - 60min (n=160) : retour [-5.24% .. +5.35%] · haut q95 +6.4% · bas q05 -6.73%
   - 2h (n=160) : retour [-6.01% .. +6.03%] · haut q95 +6.9% · bas q05 -7.02%
   - 4h (n=160) : retour [-6.03% .. +6.35%] · haut q95 +7.93% · bas q05 -7.32%
   - 6h (n=160) : retour [-6.11% .. +7.73%] · haut q95 +9.19% · bas q05 -7.59%
   - session (n=160) : retour [-6.43% .. +7.31%] · haut q95 +9.61% · bas q05 -7.79%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 6.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 10% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.16% (p75 1.63% / p90 2.44%) · ~5.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 15.0 min, n=48)
   - −1.0% → **87%** (reprise méd 35.0 min, n=29)
   - −1.5% → **86%** (reprise méd 48.4 min, n=17)
   - −2.0% → **90%** (reprise méd 15.0 min, n=9)
   - −3.0% → **66%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.44%** (p90, défaut prudent ; serré/agressif −1.63%) ; extension open→close méd +9.37% (q75 +10.69% / q95 +12.08%), MFE méd +10.33% / q90 +12.7%
   - Échelle scale-out : +10.33% (33%) / +12.07% (33%) / +12.7% (34%)
- **DÉSARMER** : repli > **−2.44%** depuis le plus-haut = décay → P(retournement) **13%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.7% : P(retournement après) 0% (mèche méd None%)
- **CONTEXTE** : la dernière heure tient les gains 76% du temps (retour médian dernière heure +0.7%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.4  _(neutre)_
- **ADX** : 30.6  _(tendance etablie)_
- **MACD** : hist 0.219  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 24.1%
- **ATR** : 1.0 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.05  _(neutre)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 47.3  _(transition)_
- **MA** : MA20 11.69 · MA50 13.84 · MA200 16.73  _(prix > MA20)_
- **Dist MA** : MA20 +3.7% · MA50 -12.4% · MA200 -27.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (706876 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
