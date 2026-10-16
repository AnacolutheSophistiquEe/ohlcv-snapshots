# EVT

**Generated** : 2026-10-16T00:07:36.642254+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €2.53  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 4/125 fenêtres (p_fill pondéré 3 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €2.53 (+6.8% vs entrée) · entrée €2.37 · stop €2.18 · T1 €2.45 · R/R 0.42  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-15 : 2.53 · ATR Wilder 0.1568 (6.19 %)_
- **Swing** : plage **2.32 → 2.17** (-8.27 % a -14.11 % sous la cloture, 0.94 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 2.02 (-7.21 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **2.17 → 1.52** (-14.11 % a -40.02 % sous la cloture, 4.18 ATR) — touchee 48 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 1.36 (-10.32 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (3.88 ATR sous le plus haut 20 s., RSI(2) 39.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Resistances reelles au-dessus : 2.71-2.77 (B, 7.03 %) ; 3.1-3.18 (A, 22.35 %) ; 3.37-3.41 (A, 33.25 %) ; 3.88-3.88 (C, 53.24 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (19.59 %)** : le gap seul le franchit 0.157 % des séances (2 fois sur 1274).
   - exécution **7.422 pt plus bas** dans le cas TYPIQUE (médiane), 11.743 au p90, **12.823 au pire**
   - perte réelle **27.012 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 19.59 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0117 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0265** [0.0097 ; 0.0588] _(largeur 4.9 pt, n_eff 173.1)_
   - swing : **0.2574** [0.2135 ; 0.3054] _(largeur 9.2 pt, n_eff 345.8)_
   - deep : **0.2466** [0.2034 ; 0.294] _(largeur 9.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-5.0 %** | CVaR **-10.03 %** | vol 3.66 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.89 % contre 3.63 % aujourd'hui, rapport 0.52)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.04 % vs -11.16 % si l'on extrapolait par √5 _(rapport 1.169 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1145** (β de hausse 0.9237, asymétrie 1.2066) vs GDAXI — 599 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.3667 sur atr_grid (1.0 ATR, 6.528 %) — p(stop avant cible) 0.5146 [0.46 ; 0.57], R/R 4.282, perte reelle 7.521 % (gap inclus), CVaR 16.115 %, EV -1.2879 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2965 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.515, borne haute 0.567 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 16.11 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.791 %) — p(stop avant cible) 0.3409 [0.29 ; 0.39], R/R 2.828, perte reelle 11.388 % (gap inclus), EV -1.7991 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.80 %) : P(cible) 1.2 % x 32.20 % + P(rien) 64.8 % x 2.64 % ne couvrent pas P(stop) 34.1 % x 11.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.632 %) — p(stop avant cible) 0.8657 [0.83 ; 0.90], R/R 16.024, perte reelle 2.01 % (gap inclus), EV -0.5304 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 16.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.866, borne haute 0.898 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.5 % x 32.20 % + P(rien) 12.9 % x 8.09 % ne couvrent pas P(stop) 86.6 % x 2.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.264 %) — p(stop avant cible) 0.7285 [0.68 ; 0.77], R/R 8.702, perte reelle 3.701 % (gap inclus), EV -0.6223 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 8.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.729, borne haute 0.773 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 0.8 % x 32.20 % + P(rien) 26.4 % x 6.91 % ne couvrent pas P(stop) 72.9 % x 3.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.896 %) — p(stop avant cible) 0.6343 [0.58 ; 0.68], R/R 5.718, perte reelle 5.632 % (gap inclus), EV -1.0219 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.634, borne haute 0.684 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 13.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 1.0 % x 32.20 % + P(rien) 35.6 % x 6.27 % ne couvrent pas P(stop) 63.4 % x 5.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 6.528 %) — p(stop avant cible) 0.5146 [0.46 ; 0.57], R/R 4.282, perte reelle 7.521 % (gap inclus), EV -1.2879 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.515, borne haute 0.567 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 16.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.29 %) : P(cible) 1.2 % x 32.20 % + P(rien) 47.4 % x 4.66 % ne couvrent pas P(stop) 51.5 % x 7.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 8.16 %) — p(stop avant cible) 0.414 [0.36 ; 0.47], R/R 3.335, perte reelle 9.658 % (gap inclus), EV -1.6495 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.65 %) : P(cible) 1.2 % x 32.20 % + P(rien) 57.4 % x 3.44 % ne couvrent pas P(stop) 41.4 % x 9.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 11.424 %) — p(stop avant cible) 0.2918 [0.25 ; 0.34], R/R 2.475, perte reelle 13.014 % (gap inclus), EV -2.0202 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.02 %) : P(cible) 1.2 % x 32.20 % + P(rien) 69.7 % x 2.01 % ne couvrent pas P(stop) 29.2 % x 13.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 13.056 %) — p(stop avant cible) 0.2281 [0.19 ; 0.27], R/R 2.178, perte reelle 14.785 % (gap inclus), EV -2.1381 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 1.2 % x 32.20 % + P(rien) 76.0 % x 1.13 % ne couvrent pas P(stop) 22.8 % x 14.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 14.688 %) — p(stop avant cible) 0.1648 [0.13 ; 0.21], R/R 1.912, perte reelle 16.84 % (gap inclus), EV -2.1442 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 1.2 % x 32.20 % + P(rien) 82.4 % x 0.31 % ne couvrent pas P(stop) 16.5 % x 16.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 16.32 %) — p(stop avant cible) 0.1334 [0.10 ; 0.17], R/R 1.742, perte reelle 18.488 % (gap inclus), EV -2.1276 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.13 %) : P(cible) 1.2 % x 32.20 % + P(rien) 85.5 % x -0.04 % ne couvrent pas P(stop) 13.3 % x 18.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 17.952 %) — p(stop avant cible) 0.1102 [0.08 ; 0.15], R/R 1.602, perte reelle 20.106 % (gap inclus), EV -2.1069 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.11 %) : P(cible) 1.2 % x 32.20 % + P(rien) 87.8 % x -0.30 % ne couvrent pas P(stop) 11.0 % x 20.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 19.584 %) — p(stop avant cible) 0.1023 [0.07 ; 0.14], R/R 1.515, perte reelle 21.259 % (gap inclus), EV -2.1652 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.17 %) : P(cible) 1.2 % x 32.20 % + P(rien) 88.6 % x -0.41 % ne couvrent pas P(stop) 10.2 % x 21.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 22.848 %) — p(stop avant cible) 0.0823 [0.06 ; 0.11], R/R 1.366, perte reelle 23.58 % (gap inclus), EV -2.248 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 1.2 % x 32.20 % + P(rien) 90.6 % x -0.75 % ne couvrent pas P(stop) 8.2 % x 23.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 26.111 %) — p(stop avant cible) 0.0641 [0.04 ; 0.09], R/R 1.219, perte reelle 26.413 % (gap inclus), EV -2.3757 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.38 %) : P(cible) 1.2 % x 32.20 % + P(rien) 92.4 % x -1.14 % ne couvrent pas P(stop) 6.4 % x 26.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 29.375 %) — p(stop avant cible) 0.0425 [0.02 ; 0.07], R/R 1.088, perte reelle 29.589 % (gap inclus), EV -2.4727 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.47 %) : P(cible) 1.2 % x 32.20 % + P(rien) 94.6 % x -1.68 % ne couvrent pas P(stop) 4.2 % x 29.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 32.639 %) — p(stop avant cible) 0.04 [0.02 ; 0.06], R/R 0.984, perte reelle 32.724 % (gap inclus), EV -2.5908 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.59 %) : P(cible) 1.2 % x 32.20 % + P(rien) 94.8 % x -1.75 % ne couvrent pas P(stop) 4.0 % x 32.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 35.903 %) — p(stop avant cible) 0.0268 [0.01 ; 0.05], R/R 0.897, perte reelle 35.903 % (gap inclus), EV -2.6315 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.63 %) : P(cible) 1.2 % x 32.20 % + P(rien) 96.2 % x -2.12 % ne couvrent pas P(stop) 2.7 % x 35.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 39.167 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.822, perte reelle 39.167 % (gap inclus), EV -2.5057 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 1.2 % x 32.20 % + P(rien) 98.7 % x -2.86 % ne couvrent pas P(stop) 0.1 % x 39.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 42.431 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.759, perte reelle 42.431 % (gap inclus), EV -2.5015 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.50 %) : P(cible) 1.2 % x 32.20 % + P(rien) 98.8 % x -2.91 % ne couvrent pas P(stop) 0.0 % x 42.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 45.695 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.705, perte reelle 45.695 % (gap inclus), EV -2.5015 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.50 %) : P(cible) 1.2 % x 32.20 % + P(rien) 98.8 % x -2.91 % ne couvrent pas P(stop) 0.0 % x 45.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 48.959 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.658, perte reelle 48.959 % (gap inclus), EV -2.5015 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.50 %) : P(cible) 1.2 % x 32.20 % + P(rien) 98.8 % x -2.91 % ne couvrent pas P(stop) 0.0 % x 48.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 52.223 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.617, perte reelle 52.223 % (gap inclus), EV -2.5015 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.50 %) : P(cible) 1.2 % x 32.20 % + P(rien) 98.8 % x -2.91 % ne couvrent pas P(stop) 0.0 % x 52.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.532, ATR14 0.1653 (6.528 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 2.396 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.326 % | 2.5237 | 88.95 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.653 % | 2.5155 | 81.36 % | 86.67 % | 89.62 % | 92.67 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.979 % | 2.5072 | 75.15 % | 82.82 % | 86.56 % | 89.9 % | 93.83 % | 96.08 % |
| 0.2 ATR | 1.306 % | 2.4989 | 68.93 % | 78.87 % | 83.3 % | 87.13 % | 91.84 % | 94.77 % |
| 0.25 ATR | 1.632 % | 2.4907 | 63.12 % | 75.52 % | 80.24 % | 84.75 % | 89.95 % | 93.57 % |
| 0.35 ATR | 2.285 % | 2.4742 | 51.87 % | 67.42 % | 73.81 % | 79.9 % | 86.07 % | 91.56 % |
| 0.5 ATR | 3.264 % | 2.4494 | 35.6 % | 54.99 % | 62.94 % | 70.99 % | 80.2 % | 88.34 % |
| 0.75 ATR | 4.896 % | 2.408 | 19.13 % | 37.71 % | 47.53 % | 59.5 % | 71.74 % | 82.11 % |
| 1.0 ATR | 6.528 % | 2.3667 | 10.06 % | 25.07 % | 36.07 % | 47.62 % | 62.39 % | 75.68 % |
| 1.25 ATR | 8.16 % | 2.3254 | 4.83 % | 17.37 % | 27.57 % | 39.7 % | 55.92 % | 70.55 % |
| 1.5 ATR | 9.792 % | 2.2841 | 3.06 % | 11.45 % | 19.86 % | 31.68 % | 48.76 % | 65.43 % |
| 2.0 ATR | 13.056 % | 2.2014 | 1.38 % | 5.13 % | 9.68 % | 19.6 % | 35.32 % | 53.77 % |
| 2.5 ATR | 16.32 % | 2.1188 | 0.49 % | 2.86 % | 5.93 % | 12.38 % | 27.96 % | 46.13 % |
| 3.0 ATR | 19.584 % | 2.0361 | 0.39 % | 1.68 % | 3.85 % | 8.81 % | 21.09 % | 39.3 % |
| 4.0 ATR | 26.111 % | 1.8709 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 11.94 % | 25.33 % |
| 6.0 ATR | 39.167 % | 1.5403 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.50 ATR | 1.98 ATR | 2.72 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.46 ATR | 1.78 ATR | 1.98 ATR | 2.83 ATR | 3.82 ATR |
| **10 s.** | 0.65 ATR | 1.46 ATR | 1.64 ATR | 2.16 ATR | 2.71 ATR | 3.12 ATR | 4.57 ATR | hors grille |
| **20 s.** | 1.03 ATR | 2.25 ATR | 2.58 ATR | 3.45 ATR | 4.06 ATR | 4.91 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.413–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (60.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.896 %, prix 2.408), p(touche) 37.71 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.0 % des re-echantillons)
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.528 %, prix 2.3667), p(touche) 36.07 % (en stress 96.08 %)  ✅ optimum identifie (69.8 % des re-echantillons)
- **5 seance(s)** : plage utile 1.083–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.16 %, prix 2.3254), p(touche) 39.7 % (en stress 94.06 %)  ✅ optimum identifie (79.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.64–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.056 %, prix 2.2014), p(touche) 35.32 % (en stress 98.02 %)  ✅ optimum identifie (77.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.583–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (85.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.027 | EV/share : €-0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 29.1 | bear 5.0 | side 65.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→65% · +2.0%→42% · +3.0%→23% · +5.0%→10% · +8.0%→2%
- Range intraday médian 3.96% (p90 6.52%) · excursion haute méd. +1.57% / basse méd. −1.88%
- Profil de vol intra : ouverture 2.571% vs midi 1.19% vs clôture 1.188% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 60% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.152)_ ; drift intra méd. -0.511% ; recovery-V 19%
- **σ réalisé intraday** 3.126% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 72% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 2.9518 (VA 2.9403–2.9711 ; dernier close 2.918)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 25% · rebond 70% · **stop −1.87%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.81 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 37% (gap-down >1% 7% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −2.18%) · haut méd +0.41% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.66%) · haut méd +0.54% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −3.17%) · haut méd +0.67% · range méd 2.04%
- Excursion ouverture 60min (n=160) : bas méd −1.06% (p90 −3.37%) · haut méd +0.84% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 81% (129/159) · gap 20% · délai 0.4min · rebond 64% (86/129) (MFE +1.48%)
   - −1.0% : fill 30min 38% · séance 67% (111/159) · gap 7% · délai 9.3min · rebond 62% (74/111) (MFE +1.42%)
   - −1.5% : fill 30min 26% · séance 55% (92/159) · gap 3% · délai 31.6min · rebond 60% (58/92) (MFE +1.25%)
   - −2.0% : fill 30min 16% · séance 46% (77/159) · gap 3% · délai 67.4min · rebond 54% (43/77) (MFE +1.17%)
   - −3.0% : fill 30min 7% · séance 25% (45/159) · gap 2% · délai 86.4min · rebond 70% (32/45) (MFE +1.52%)
   - −4.0% : fill 30min 3% · séance 10% (24/159) · gap 1% · délai 359.9min · rebond 38% (13/24) (MFE +0.64%)
   - −5.0% : fill 30min 2% · séance 4% (13/159) · gap 1% · délai 33.7min · rebond 33% (7/13) (MFE +0.67%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −2.16%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.23% (p90 −1.65%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.06% (p90 −1.83%) → stop au-delà de −1.24% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=811 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~9.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 74% (46/55) · rebond 63% (31/46)
      · −2.0% : fill 52% (35/55) · rebond 49% (19/35)
      · −3.0% : fill 26% (22/55) · rebond 62% (15/22)
      · −4.0% : fill 15% (15/55) · rebond 34% (8/15)
      · −5.0% : fill 10% (10/55) · rebond 33% (5/10)
   - **flat** (30 séances) :
      · −1.0% : fill 74% (23/30) · rebond 58% (14/23)
      · −2.0% : fill 50% (17/30) · rebond 49% (8/17)
      · −3.0% : fill 29% (10/30) · rebond 83% (8/10)
      · −4.0% : fill 10% (4/30) · rebond 14% (1/4)
      · −5.0% : fill 6% (2/30) · rebond 23% (1/2)
   - **gap-up** (74 séances) :
      · −1.0% : fill 61% (42/74) · rebond 64% (29/42)
      · −2.0% : fill 41% (25/74) · rebond 60% (16/25)
      · −3.0% : fill 22% (13/74) · rebond 68% (9/13)
      · −4.0% : fill 8% (5/74) · rebond 55% (4/5)
      · −5.0% : fill 0% (1/74) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 60% si les 15 1res min sont vertes (75 cas) · 27% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **12min** → P(séance verte=clôture>ouverture) 58% si début vert vs 28% si rouge (base 43% · écart 30 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **58%** · continue >prix actuel 38% ; creux résiduel méd -1.71% (q20 -2.8%) → **SL/trailing à −2.8%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.68% / q75 +2.35% → **scale +1.68% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **28%** (continue à baisser 59%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.09%** (au-delà de la MAE q10 -4.09%), cible rebond +1.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.83% .. +3.3%] · haut q95 +3.68% · bas q05 -3.73%
   - 60min (n=160) : retour [-3.03% .. +4.12%] · haut q95 +4.72% · bas q05 -3.81%
   - 2h (n=160) : retour [-3.2% .. +3.32%] · haut q95 +5.18% · bas q05 -4.3%
   - 4h (n=160) : retour [-3.24% .. +4.34%] · haut q95 +5.21% · bas q05 -4.31%
   - 6h (n=160) : retour [-3.57% .. +5.54%] · haut q95 +5.95% · bas q05 -4.33%
   - session (n=160) : retour [-4.49% .. +4.05%] · haut q95 +6.33% · bas q05 -5.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.04 · part idiosyncratique 0.96
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 39.1  _(momentum baissier)_
- **ADX** : 24.1  _(pas de tendance nette)_
- **MACD** : hist -0.025  _(bearish_recent)_
- **BB** : %B 0.11 · largeur 25.5%
- **ATR** : 0.17 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.387  _(distribution)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 43.5  _(transition)_
- **MA** : MA20 2.81 · MA50 3.09 · MA200 4.57  _(prix < MA20)_
- **Dist MA** : MA20 -9.9% · MA50 -18.0% · MA200 -44.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (847615 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
