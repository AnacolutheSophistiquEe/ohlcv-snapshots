# EVT

**Generated** : 2026-10-02T00:07:08.623787+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.04  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €3.04 (+6.3% vs entrée) · entrée €2.86 · stop €2.73 · T1 €3.01 · R/R 1.15  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 152 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.250 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €2.84–€2.88 (mid €2.86)
- Spot actuel : €3.04 (+6.3% au-dessus de la zone — repli à attendre)
- Stop : €2.73 (plancher anti-bruit (R/R<2) ; -4.55 % depuis l'entree)
- Targets : T1 €3.01 · R/R 1.15 | T2 €3.15 · R/R 2.23 | T3 €3.30 · R/R 3.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €2.73


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (10.31 %)** : le gap seul le franchit 0.314 % des séances (4 fois sur 1274).
   - exécution **7.407 pt plus bas** dans le cas TYPIQUE (médiane), 18.862 au p90, **22.103 au pire**
   - perte réelle **19.926 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 10.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0302 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1068** [0.0673 ; 0.1593] _(largeur 9.2 pt, n_eff 173.1)_
   - swing : **0.4567** [0.4047 ; 0.5094] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4426** [0.3909 ; 0.4952] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.0 pt), swing (40.3 pt), deep (45.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.94 %** | CVaR **-9.56 %** | vol 3.57 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.06 % contre 3.47 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1187** (β de hausse 0.9368, asymétrie 1.1942) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.9111 sur atr_grid (1.0 ATR, 4.302 %) — p(stop avant cible) 0.6814 [0.63 ; 0.73], R/R 5.995, perte reelle 4.828 % (gap inclus), CVaR 10.909 %, EV -0.8562 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2124 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.681, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.453 %) — p(stop avant cible) 0.5279 [0.48 ; 0.58], R/R 3.888, perte reelle 7.445 % (gap inclus), EV -1.2448 % — **REFUSE**
      - refuse : cible atteinte seulement 2.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.528, borne haute 0.580 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 16.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 2.0 % x 28.94 % + P(rien) 45.2 % x 4.64 % ne couvrent pas P(stop) 52.8 % x 7.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.54 ATR (stop 12.936 %) — p(stop avant cible) 0.2265 [0.18 ; 0.27], R/R 1.954, perte reelle 14.812 % (gap inclus), EV -2.1212 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 2.1 % x 28.94 % + P(rien) 75.2 % x 0.83 % ne couvrent pas P(stop) 22.7 % x 14.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.075 %) — p(stop avant cible) 0.9076 [0.87 ; 0.93], R/R 22.884, perte reelle 1.265 % (gap inclus), EV -0.161 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 22.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.908, borne haute 0.935 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.9 % x 28.94 % + P(rien) 8.3 % x 8.73 % ne couvrent pas P(stop) 90.8 % x 1.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.151 %) — p(stop avant cible) 0.8407 [0.80 ; 0.88], R/R 11.322, perte reelle 2.556 % (gap inclus), EV -0.6693 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 11.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.841, borne haute 0.876 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 1.1 % x 28.94 % + P(rien) 14.9 % x 7.87 % ne couvrent pas P(stop) 84.1 % x 2.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 3.226 %) — p(stop avant cible) 0.7442 [0.70 ; 0.79], R/R 7.93, perte reelle 3.65 % (gap inclus), EV -0.6319 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 7.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.744, borne haute 0.788 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 1.6 % x 28.94 % + P(rien) 24.0 % x 6.79 % ne couvrent pas P(stop) 74.4 % x 3.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 4.302 %) — p(stop avant cible) 0.6814 [0.63 ; 0.73], R/R 5.995, perte reelle 4.828 % (gap inclus), EV -0.8562 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.681, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 1.7 % x 28.94 % + P(rien) 30.2 % x 6.44 % ne couvrent pas P(stop) 68.1 % x 4.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 5.377 %) — p(stop avant cible) 0.587 [0.53 ; 0.64], R/R 4.698, perte reelle 6.161 % (gap inclus), EV -0.9116 % — **REFUSE**
      - refuse : cible atteinte seulement 1.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.587, borne haute 0.638 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 14.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 1.9 % x 28.94 % + P(rien) 39.4 % x 5.47 % ne couvrent pas P(stop) 58.7 % x 6.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 7.528 %) — p(stop avant cible) 0.4379 [0.39 ; 0.49], R/R 3.172, perte reelle 9.126 % (gap inclus), EV -1.5555 % — **REFUSE**
      - refuse : cible atteinte seulement 2.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.56 %) : P(cible) 2.0 % x 28.94 % + P(rien) 54.2 % x 3.42 % ne couvrent pas P(stop) 43.8 % x 9.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 8.603 %) — p(stop avant cible) 0.3912 [0.34 ; 0.44], R/R 2.832, perte reelle 10.219 % (gap inclus), EV -1.7331 % — **REFUSE**
      - refuse : cible atteinte seulement 2.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 2.0 % x 28.94 % + P(rien) 58.8 % x 2.85 % ne couvrent pas P(stop) 39.1 % x 10.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 9.679 %) — p(stop avant cible) 0.3445 [0.30 ; 0.40], R/R 2.544, perte reelle 11.379 % (gap inclus), EV -1.831 % — **REFUSE**
      - refuse : cible atteinte seulement 2.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 2.0 % x 28.94 % + P(rien) 63.5 % x 2.36 % ne couvrent pas P(stop) 34.4 % x 11.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 2.54 ATR (stop 12.204 %) — p(stop avant cible) 0.2424 [0.20 ; 0.29], R/R 2.056, perte reelle 14.078 % (gap inclus), EV -2.0642 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 2.1 % x 28.94 % + P(rien) 73.7 % x 1.00 % ne couvrent pas P(stop) 24.2 % x 14.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 15.056 %) — p(stop avant cible) 0.1527 [0.12 ; 0.19], R/R 1.662, perte reelle 17.409 % (gap inclus), EV -2.1155 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 2.1 % x 28.94 % + P(rien) 82.6 % x -0.08 % ne couvrent pas P(stop) 15.3 % x 17.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 17.207 %) — p(stop avant cible) 0.1141 [0.08 ; 0.15], R/R 1.474, perte reelle 19.633 % (gap inclus), EV -2.0384 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.04 %) : P(cible) 2.1 % x 28.94 % + P(rien) 86.5 % x -0.47 % ne couvrent pas P(stop) 11.4 % x 19.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 19.358 %) — p(stop avant cible) 0.0973 [0.07 ; 0.13], R/R 1.36, perte reelle 21.276 % (gap inclus), EV -2.0644 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 2.1 % x 28.94 % + P(rien) 88.1 % x -0.69 % ne couvrent pas P(stop) 9.7 % x 21.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 21.508 %) — p(stop avant cible) 0.091 [0.06 ; 0.12], R/R 1.28, perte reelle 22.606 % (gap inclus), EV -2.1356 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 2.1 % x 28.94 % + P(rien) 88.8 % x -0.78 % ne couvrent pas P(stop) 9.1 % x 22.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 23.659 %) — p(stop avant cible) 0.0831 [0.06 ; 0.12], R/R 1.19, perte reelle 24.33 % (gap inclus), EV -2.2452 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 2.1 % x 28.94 % + P(rien) 89.6 % x -0.93 % ne couvrent pas P(stop) 8.3 % x 24.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 25.81 %) — p(stop avant cible) 0.0691 [0.05 ; 0.10], R/R 1.108, perte reelle 26.128 % (gap inclus), EV -2.3175 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.32 %) : P(cible) 2.1 % x 28.94 % + P(rien) 91.0 % x -1.23 % ne couvrent pas P(stop) 6.9 % x 26.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 27.961 %) — p(stop avant cible) 0.0551 [0.03 ; 0.08], R/R 1.027, perte reelle 28.188 % (gap inclus), EV -2.4155 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.42 %) : P(cible) 2.1 % x 28.94 % + P(rien) 92.4 % x -1.59 % ne couvrent pas P(stop) 5.5 % x 28.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 30.112 %) — p(stop avant cible) 0.0424 [0.02 ; 0.07], R/R 0.955, perte reelle 30.304 % (gap inclus), EV -2.4602 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.46 %) : P(cible) 2.1 % x 28.94 % + P(rien) 93.7 % x -1.91 % ne couvrent pas P(stop) 4.2 % x 30.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 32.263 %) — p(stop avant cible) 0.0424 [0.02 ; 0.07], R/R 0.894, perte reelle 32.361 % (gap inclus), EV -2.5474 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.55 %) : P(cible) 2.1 % x 28.94 % + P(rien) 93.7 % x -1.91 % ne couvrent pas P(stop) 4.2 % x 32.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 34.413 %) — p(stop avant cible) 0.0421 [0.02 ; 0.07], R/R 0.841, perte reelle 34.435 % (gap inclus), EV -2.6314 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.63 %) : P(cible) 2.1 % x 28.94 % + P(rien) 93.7 % x -1.91 % ne couvrent pas P(stop) 4.2 % x 34.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.042, ATR14 0.1309 (4.302 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.366 ATR = 1.574 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.215 % | 3.0355 | 88.95 % | 91.81 % | 93.58 % | 95.64 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.43 % | 3.0289 | 81.36 % | 86.87 % | 89.62 % | 92.77 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.645 % | 3.0224 | 75.15 % | 83.02 % | 86.56 % | 90.0 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.86 % | 3.0158 | 68.84 % | 79.07 % | 83.3 % | 87.23 % | 91.94 % | 94.77 % |
| 0.25 ATR | 1.075 % | 3.0093 | 63.12 % | 75.81 % | 80.24 % | 84.85 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.506 % | 2.9962 | 51.78 % | 67.62 % | 73.81 % | 80.0 % | 86.17 % | 91.56 % |
| 0.5 ATR | 2.151 % | 2.9766 | 35.5 % | 54.99 % | 62.85 % | 70.89 % | 80.1 % | 88.24 % |
| 0.75 ATR | 3.226 % | 2.9439 | 19.03 % | 37.71 % | 47.53 % | 59.6 % | 71.94 % | 81.91 % |
| 1.0 ATR | 4.302 % | 2.9111 | 9.96 % | 24.78 % | 35.87 % | 47.52 % | 62.39 % | 75.28 % |
| 1.25 ATR | 5.377 % | 2.8784 | 4.73 % | 17.18 % | 27.37 % | 39.5 % | 55.72 % | 70.05 % |
| 1.5 ATR | 6.453 % | 2.8457 | 2.96 % | 11.25 % | 19.66 % | 31.49 % | 48.56 % | 64.92 % |
| 2.0 ATR | 8.603 % | 2.7803 | 1.28 % | 4.94 % | 9.49 % | 19.41 % | 35.12 % | 53.07 % |
| 2.5 ATR | 10.754 % | 2.7149 | 0.49 % | 2.67 % | 5.63 % | 12.18 % | 27.76 % | 45.33 % |
| 3.0 ATR | 12.905 % | 2.6494 | 0.39 % | 1.68 % | 3.66 % | 8.51 % | 20.8 % | 38.39 % |
| 4.0 ATR | 17.207 % | 2.5186 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 11.74 % | 24.72 % |
| 6.0 ATR | 25.81 % | 2.2569 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.73 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.60 ATR | 2.00 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.08 ATR | 1.33 ATR | 1.49 ATR | 1.98 ATR | 2.66 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.80 ATR | 3.81 ATR |
| **10 s.** | 0.66 ATR | 1.45 ATR | 1.63 ATR | 2.14 ATR | 2.70 ATR | 3.09 ATR | 4.53 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.20 ATR | 2.52 ATR | 3.39 ATR | 3.98 ATR | 4.85 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.412–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.226 %, prix 2.9439), p(touche) 37.71 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (62.2 % des re-echantillons)
- **3 seance(s)** : plage utile 0.804–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.302 %, prix 2.9111), p(touche) 35.87 % (en stress 96.08 %)  ✅ optimum identifie (65.5 % des re-echantillons)
- **5 seance(s)** : plage utile 1.079–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.377 %, prix 2.8784), p(touche) 39.5 % (en stress 95.05 %)  ✅ optimum identifie (75.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.632–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.603 %, prix 2.7803), p(touche) 35.12 % (en stress 97.03 %)  ✅ optimum identifie (76.8 % des re-echantillons)
- **20 seance(s)** : plage utile 2.524–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (12.905 %, prix 2.6494), p(touche) 38.39 % (en stress 98.0 %)  ✅ optimum identifie (85.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.079 | EV/share : €-0.010 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 12 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 33.1 | bear 5.0 | side 61.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 286.0 (= 94 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.728% → cible +2.21% / stop −4.001%, p_fill 31%, n_eff≈32.7) : P(cible|rempli) **27%** · **EV/risk -0.021** (×p_fill ; si rempli -0.28% du capital)
  - **swing** (entrée dip −5.997% → cible +5.116% / stop −4.578%, p_fill 19%, n_eff≈21.1) : P(cible|rempli) **36%** · **EV/risk -0.025** (×p_fill ; si rempli -0.62% du capital)
  - **deep** (entrée dip −9.277% → cible +7.497% / stop −7.113%, p_fill 14%, n_eff≈15.4) : P(cible|rempli) **42%** · **EV/risk -0.007** (×p_fill ; si rempli -0.36% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→42% · +3.0%→24% · +5.0%→10% · +8.0%→2%
- Range intraday médian 3.96% (p90 6.64%) · excursion haute méd. +1.61% / basse méd. −1.88%
- Profil de vol intra : ouverture 2.602% vs midi 1.195% vs clôture 1.202% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 97% · range 3% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.103 ; mean-reverting — autocorr -0.144)_ ; drift intra méd. -0.207% ; recovery-V 21%
- **σ réalisé intraday** 3.007% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 70% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 3.0922 (VA 3.0695–3.1059 ; dernier close 3.091)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 22% · rebond 65% · **stop −2.12%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.66 (high win-rate)
- Gaps overnight (n=159) : méd. 0.3% · baisse 38% (gap-down >1% 8% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −2.15%) · haut méd +0.42% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.75% (p90 −2.36%) · haut méd +0.64% · range méd 1.75%
- Excursion ouverture 30min (n=160) : bas méd −0.84% (p90 −2.68%) · haut méd +0.72% · range méd 1.97%
- Excursion ouverture 60min (n=160) : bas méd −1.01% (p90 −3.02%) · haut méd +0.88% · range méd 2.35%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 80% (129/159) · gap 21% · délai 0.4min · rebond 65% (87/129) (MFE +1.48%)
   - −1.0% : fill 30min 35% · séance 66% (110/159) · gap 8% · délai 9.4min · rebond 63% (74/110) (MFE +1.42%)
   - −1.5% : fill 30min 23% · séance 53% (90/159) · gap 3% · délai 36.3min · rebond 61% (57/90) (MFE +1.25%)
   - −2.0% : fill 30min 15% · séance 44% (75/159) · gap 3% · délai 77.9min · rebond 55% (42/75) (MFE +1.17%)
   - −3.0% : fill 30min 7% · séance 22% (43/159) · gap 2% · délai 99.6min · rebond 65% (30/43) (MFE +1.39%)
   - −4.0% : fill 30min 3% · séance 9% (23/159) · gap 1% · délai 45.8min · rebond 47% (13/23) (MFE +0.77%)
   - −5.0% : fill 30min 2% · séance 4% (13/159) · gap 1% · délai 33.7min · rebond 33% (7/13) (MFE +0.67%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −2.16%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.23% (p90 −1.65%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.06% (p90 −1.83%) → stop au-delà de −1.24% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=799 jambes) : jambe baissière méd −1.06% (p90 −2.31%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 74% (46/55) · rebond 63% (31/46)
      · −2.0% : fill 52% (35/55) · rebond 49% (19/35)
      · −3.0% : fill 26% (22/55) · rebond 62% (15/22)
      · −4.0% : fill 15% (15/55) · rebond 34% (8/15)
      · −5.0% : fill 10% (10/55) · rebond 33% (5/10)
   - **flat** (32 séances) :
      · −1.0% : fill 73% (24/32) · rebond 58% (15/24)
      · −2.0% : fill 49% (17/32) · rebond 49% (8/17)
      · −3.0% : fill 29% (10/32) · rebond 83% (8/10)
      · −4.0% : fill 10% (4/32) · rebond 14% (1/4)
      · −5.0% : fill 6% (2/32) · rebond 23% (1/2)
   - **gap-up** (72 séances) :
      · −1.0% : fill 58% (40/72) · rebond 66% (28/40)
      · −2.0% : fill 36% (23/72) · rebond 62% (15/23)
      · −3.0% : fill 16% (11/72) · rebond 53% (7/11)
      · −4.0% : fill 5% (4/72) · rebond 100% (4/4)
      · −5.0% : fill 0% (1/72) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 60% si les 15 1res min sont vertes (76 cas) · 29% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **12min** → P(séance verte=clôture>ouverture) 58% si début vert vs 30% si rouge (base 44% · écart 28 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **58%** · continue >prix actuel 38% ; creux résiduel méd -1.71% (q20 -2.8%) → **SL/trailing à −2.8%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +2.35% → **scale +1.67% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **30%** (continue à baisser 56%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.34%** (au-delà de la MAE q10 -4.34%), cible rebond +1.49% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.56% .. +3.3%] · haut q95 +3.74% · bas q05 -3.75%
   - 60min (n=160) : retour [-2.94% .. +4.15%] · haut q95 +4.84% · bas q05 -3.75%
   - 2h (n=160) : retour [-2.98% .. +3.52%] · haut q95 +5.27% · bas q05 -3.91%
   - 4h (n=160) : retour [-3.27% .. +4.39%] · haut q95 +5.31% · bas q05 -3.91%
   - 6h (n=160) : retour [-2.87% .. +5.63%] · haut q95 +5.98% · bas q05 -3.93%
   - session (n=160) : retour [-4.32% .. +4.09%] · haut q95 +6.39% · bas q05 -5.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.18 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.3  _(neutre)_
- **ADX** : 29.6  _(tendance etablie)_
- **MACD** : hist 0.047  _(pas de croisement recent)_
- **BB** : %B 0.66 · largeur 20.8%
- **ATR** : 0.13 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.249  _(distribution)_
- **Vol ratio** : 0.32  _(volume atone)_
- **Choppiness** : 54.9  _(transition)_
- **MA** : MA20 2.95 · MA50 3.23 · MA200 4.69  _(prix > MA20)_
- **Dist MA** : MA20 +3.3% · MA50 -5.9% · MA200 -35.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (859938 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
