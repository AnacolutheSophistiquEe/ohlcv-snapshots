# EVT

**Generated** : 2026-10-09T00:07:51.772903+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €2.80  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (4 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €2.80 (+1.1% vs entrée) · entrée €2.77 · stop €2.55 · T1 €2.84 · R/R 0.32  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-08 : 2.8 · ATR Wilder 0.1326 (4.74 %)_
- **Swing** : plage **2.62 → 2.49** (-6.27 % a -10.77 % sous la cloture, 0.95 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 2.36 (-5.31 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **2.49 → 1.94** (-10.77 % a -30.65 % sous la cloture, 4.19 ATR) — touchee 48 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 1.81 (-6.84 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (2.59 ATR sous le plus haut 20 s., RSI(2) 5.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Resistances reelles au-dessus : 3.1-3.14 (A, 10.8 %) ; 3.18-3.24 (B, 13.59 %) ; 3.37-3.41 (A, 20.67 %) ; 3.45-3.51 (B, 23.29 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.52 %)** : le gap seul le franchit 0.549 % des séances (7 fois sur 1274).
   - exécution **5.338 pt plus bas** dans le cas TYPIQUE (médiane), 19.412 au p90, **25.893 au pire**
   - perte réelle **14.861 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 6.52 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0458 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0152** [0.0039 ; 0.0423] _(largeur 3.8 pt, n_eff 173.1)_
   - swing : **0.4268** [0.3755 ; 0.4794] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4131** [0.3621 ; 0.4655] _(largeur 10.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.94 %** | CVaR **-9.56 %** | vol 3.59 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.99 % contre 3.47 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1175** (β de hausse 0.9388, asymétrie 1.1903) vs GDAXI — 599 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.6695 sur grid_snapped (0.64 ATR, 4.524 %) — p(stop avant cible) 0.6603 [0.61 ; 0.71], R/R 7.962, perte reelle 5.054 % (gap inclus), CVaR 10.953 %, EV -0.8089 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2792 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.660, borne haute 0.709 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 0.64 ATR (stop 5.347 %) — p(stop avant cible) 0.5817 [0.53 ; 0.63], R/R 6.57, perte reelle 6.125 % (gap inclus), EV -0.8606 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.582, borne haute 0.633 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 13.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 0.1 % x 40.24 % + P(rien) 41.7 % x 6.35 % ne couvrent pas P(stop) 58.2 % x 6.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 7.242 %) — p(stop avant cible) 0.4592 [0.41 ; 0.51], R/R 4.674, perte reelle 8.609 % (gap inclus), EV -1.417 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.42 %) : P(cible) 0.2 % x 40.24 % + P(rien) 53.9 % x 4.57 % ne couvrent pas P(stop) 45.9 % x 8.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.207 %) — p(stop avant cible) 0.9007 [0.87 ; 0.93], R/R 28.721, perte reelle 1.401 % (gap inclus), EV -0.222 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 28.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.901, borne haute 0.929 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 0.1 % x 40.24 % + P(rien) 9.9 % x 10.26 % ne couvrent pas P(stop) 90.1 % x 1.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 grid_snapped a 0.64 ATR (stop 4.524 %) — p(stop avant cible) 0.6603 [0.61 ; 0.71], R/R 7.962, perte reelle 5.054 % (gap inclus), EV -0.8089 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.660, borne haute 0.709 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 0.1 % x 40.24 % + P(rien) 33.8 % x 7.31 % ne couvrent pas P(stop) 66.0 % x 5.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 6.035 %) — p(stop avant cible) 0.5454 [0.49 ; 0.60], R/R 5.77, perte reelle 6.975 % (gap inclus), EV -1.0812 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.545, borne haute 0.597 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 15.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 0.2 % x 40.24 % + P(rien) 45.3 % x 5.85 % ne couvrent pas P(stop) 54.5 % x 6.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 8.45 %) — p(stop avant cible) 0.3914 [0.34 ; 0.44], R/R 4.004, perte reelle 10.05 % (gap inclus), EV -1.6025 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 0.2 % x 40.24 % + P(rien) 60.7 % x 3.72 % ne couvrent pas P(stop) 39.1 % x 10.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 9.657 %) — p(stop avant cible) 0.3347 [0.29 ; 0.39], R/R 3.542, perte reelle 11.361 % (gap inclus), EV -1.6777 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.68 %) : P(cible) 0.2 % x 40.24 % + P(rien) 66.3 % x 3.09 % ne couvrent pas P(stop) 33.5 % x 11.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 10.864 %) — p(stop avant cible) 0.3036 [0.26 ; 0.35], R/R 3.21, perte reelle 12.538 % (gap inclus), EV -1.8597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.86 %) : P(cible) 0.2 % x 40.24 % + P(rien) 69.5 % x 2.70 % ne couvrent pas P(stop) 30.4 % x 12.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 12.071 %) — p(stop avant cible) 0.2471 [0.20 ; 0.29], R/R 2.899, perte reelle 13.882 % (gap inclus), EV -1.9221 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.92 %) : P(cible) 0.2 % x 40.24 % + P(rien) 75.1 % x 1.91 % ne couvrent pas P(stop) 24.7 % x 13.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 13.278 %) — p(stop avant cible) 0.2027 [0.16 ; 0.25], R/R 2.641, perte reelle 15.237 % (gap inclus), EV -1.9458 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.95 %) : P(cible) 0.2 % x 40.24 % + P(rien) 79.5 % x 1.35 % ne couvrent pas P(stop) 20.3 % x 15.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 14.485 %) — p(stop avant cible) 0.1607 [0.12 ; 0.20], R/R 2.399, perte reelle 16.775 % (gap inclus), EV -1.9503 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.95 %) : P(cible) 0.2 % x 40.24 % + P(rien) 83.8 % x 0.80 % ne couvrent pas P(stop) 16.1 % x 16.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 16.899 %) — p(stop avant cible) 0.1156 [0.09 ; 0.15], R/R 2.083, perte reelle 19.32 % (gap inclus), EV -1.9174 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.92 %) : P(cible) 0.2 % x 40.24 % + P(rien) 88.3 % x 0.28 % ne couvrent pas P(stop) 11.6 % x 19.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 19.313 %) — p(stop avant cible) 0.0947 [0.07 ; 0.13], R/R 1.894, perte reelle 21.249 % (gap inclus), EV -1.9124 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 0.2 % x 40.24 % + P(rien) 90.3 % x 0.03 % ne couvrent pas P(stop) 9.5 % x 21.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 21.727 %) — p(stop avant cible) 0.0875 [0.06 ; 0.12], R/R 1.764, perte reelle 22.817 % (gap inclus), EV -1.9958 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.00 %) : P(cible) 0.2 % x 40.24 % + P(rien) 91.1 % x -0.08 % ne couvrent pas P(stop) 8.8 % x 22.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 24.142 %) — p(stop avant cible) 0.0749 [0.05 ; 0.11], R/R 1.63, perte reelle 24.691 % (gap inclus), EV -2.08 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 0.2 % x 40.24 % + P(rien) 92.3 % x -0.33 % ne couvrent pas P(stop) 7.5 % x 24.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 26.556 %) — p(stop avant cible) 0.0654 [0.04 ; 0.10], R/R 1.5, perte reelle 26.829 % (gap inclus), EV -2.2014 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 0.2 % x 40.24 % + P(rien) 93.3 % x -0.56 % ne couvrent pas P(stop) 6.5 % x 26.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 28.97 %) — p(stop avant cible) 0.0479 [0.03 ; 0.07], R/R 1.379, perte reelle 29.182 % (gap inclus), EV -2.2771 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.28 %) : P(cible) 0.2 % x 40.24 % + P(rien) 95.0 % x -1.00 % ne couvrent pas P(stop) 4.8 % x 29.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 31.384 %) — p(stop avant cible) 0.0412 [0.02 ; 0.07], R/R 1.277, perte reelle 31.519 % (gap inclus), EV -2.3474 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.35 %) : P(cible) 0.2 % x 40.24 % + P(rien) 95.7 % x -1.17 % ne couvrent pas P(stop) 4.1 % x 31.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 33.798 %) — p(stop avant cible) 0.0412 [0.02 ; 0.07], R/R 1.189, perte reelle 33.842 % (gap inclus), EV -2.4432 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.44 %) : P(cible) 0.2 % x 40.24 % + P(rien) 95.7 % x -1.17 % ne couvrent pas P(stop) 4.1 % x 33.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 36.212 %) — p(stop avant cible) 0.0274 [0.01 ; 0.05], R/R 1.111, perte reelle 36.212 % (gap inclus), EV -2.4443 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.44 %) : P(cible) 0.2 % x 40.24 % + P(rien) 97.1 % x -1.57 % ne couvrent pas P(stop) 2.7 % x 36.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 38.627 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 1.042, perte reelle 38.627 % (gap inclus), EV -2.3314 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.33 %) : P(cible) 0.2 % x 40.24 % + P(rien) 99.2 % x -2.20 % ne couvrent pas P(stop) 0.6 % x 38.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.796, ATR14 0.135 (4.828 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.368 ATR = 1.777 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.241 % | 2.7893 | 88.95 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.483 % | 2.7825 | 81.26 % | 86.67 % | 89.62 % | 92.67 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.724 % | 2.7758 | 75.05 % | 82.82 % | 86.56 % | 89.9 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.966 % | 2.769 | 68.74 % | 78.87 % | 83.3 % | 87.13 % | 91.94 % | 94.77 % |
| 0.25 ATR | 1.207 % | 2.7623 | 63.12 % | 75.62 % | 80.24 % | 84.75 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.69 % | 2.7488 | 51.97 % | 67.42 % | 73.72 % | 79.8 % | 86.07 % | 91.56 % |
| 0.5 ATR | 2.414 % | 2.7285 | 35.5 % | 54.79 % | 62.65 % | 70.69 % | 80.0 % | 88.24 % |
| 0.75 ATR | 3.621 % | 2.6947 | 19.03 % | 37.51 % | 47.23 % | 59.21 % | 71.64 % | 81.91 % |
| 1.0 ATR | 4.828 % | 2.661 | 10.06 % | 24.88 % | 35.67 % | 47.23 % | 62.19 % | 75.38 % |
| 1.25 ATR | 6.035 % | 2.6272 | 4.73 % | 17.18 % | 27.17 % | 39.31 % | 55.62 % | 70.25 % |
| 1.5 ATR | 7.242 % | 2.5935 | 2.96 % | 11.25 % | 19.47 % | 31.29 % | 48.46 % | 65.13 % |
| 2.0 ATR | 9.657 % | 2.526 | 1.28 % | 4.94 % | 9.39 % | 19.21 % | 35.02 % | 53.37 % |
| 2.5 ATR | 12.071 % | 2.4585 | 0.49 % | 2.67 % | 5.63 % | 12.08 % | 27.66 % | 45.73 % |
| 3.0 ATR | 14.485 % | 2.391 | 0.39 % | 1.68 % | 3.66 % | 8.51 % | 20.8 % | 38.89 % |
| 4.0 ATR | 19.313 % | 2.256 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 11.74 % | 25.23 % |
| 6.0 ATR | 28.97 % | 1.986 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.73 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.60 ATR | 2.00 ATR |
| **3 s.** | 0.33 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.32 ATR | 1.48 ATR | 1.97 ATR | 2.66 ATR |
| **5 s.** | 0.43 ATR | 0.94 ATR | 1.07 ATR | 1.45 ATR | 1.76 ATR | 1.97 ATR | 2.79 ATR | 3.81 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.63 ATR | 2.14 ATR | 2.69 ATR | 3.09 ATR | 4.53 ATR | hors grille |
| **20 s.** | 1.02 ATR | 2.22 ATR | 2.55 ATR | 3.43 ATR | 4.04 ATR | 4.91 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.413–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (60.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.642–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.621 %, prix 2.6948), p(touche) 37.51 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.9 % des re-echantillons)
- **3 seance(s)** : plage utile 0.798–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.828 %, prix 2.661), p(touche) 35.67 % (en stress 96.08 %)  ✅ optimum identifie (68.6 % des re-echantillons)
- **5 seance(s)** : plage utile 1.07–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.035 %, prix 2.6273), p(touche) 39.31 % (en stress 95.05 %)  ✅ optimum identifie (79.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.629–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.657 %, prix 2.526), p(touche) 35.02 % (en stress 97.03 %)  ✅ optimum identifie (78.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.553–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (14.485 %, prix 2.391), p(touche) 38.89 % (en stress 98.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (84.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 26.1 | bear 5.0 | side 69.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.77% → cible +2.433% / stop −8.001%, p_fill 79%, n_eff≈84.6) : P(cible|rempli) **25%** · **EV/risk -0.050** (×p_fill ; si rempli -0.51% du capital)
  - **swing** (entrée dip −1.692% → cible +5.49% / stop −4.911%, p_fill 65%, n_eff≈74.9) : P(cible|rempli) **32%** · **EV/risk -0.114** (×p_fill ; si rempli -0.86% du capital)
  - **deep** (entrée dip −2.618% → cible +7.841% / stop −7.437%, p_fill 67%, n_eff≈73.8) : P(cible|rempli) **28%** · **EV/risk -0.172** (×p_fill ; si rempli -1.92% du capital)
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
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.05 · part idiosyncratique 0.95
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.6  _(momentum baissier)_
- **ADX** : 22.4  _(pas de tendance nette)_
- **MACD** : hist 0.023  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 12.6%
- **ATR** : 0.14 (13.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.24  _(distribution)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 56.1  _(transition)_
- **MA** : MA20 2.88 · MA50 3.18 · MA200 4.64  _(prix < MA20)_
- **Dist MA** : MA20 -3.1% · MA50 -12.0% · MA200 -39.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (865627 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
