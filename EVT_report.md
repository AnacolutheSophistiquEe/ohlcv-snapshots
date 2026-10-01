# EVT

**Generated** : 2026-10-01T00:06:41.518927+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.08  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €3.08 (+4.4% vs entrée) · entrée €2.95 · stop €2.84 · T1 €3.02 · R/R 0.64  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 153 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.290 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €2.95–€2.96 (mid €2.95)
- Spot actuel : €3.08 (+4.4% au-dessus de la zone — repli à attendre)
- Stop : €2.84 (plancher anti-bruit 5 s — stop EV-optimal −4% (first-passage 5 s réel) ; -3.73 % depuis l'entree)
- Targets : T1 €3.02 · R/R 0.64 | T2 €3.08 · R/R 1.18 | T3 €3.15 · R/R 1.82
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €2.84


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.51 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **9.101 pt plus bas** dans le cas TYPIQUE (médiane), 17.743 au p90, **19.903 au pire**
   - perte réelle **22.616 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 12.51 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0238 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1081** [0.0684 ; 0.1608] _(largeur 9.2 pt, n_eff 173.1)_
   - swing : **0.4587** [0.4067 ; 0.5114] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4443** [0.3926 ; 0.497] _(largeur 10.4 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.94 %** | CVaR **-9.56 %** | vol 3.57 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.08 % contre 3.47 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1188** (β de hausse 0.9368, asymétrie 1.1943) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.9534 sur atr_grid (1.0 ATR, 4.172 %) — p(stop avant cible) 0.6947 [0.64 ; 0.74], R/R 5.822, perte reelle 4.688 % (gap inclus), CVaR 10.902 %, EV -0.8708 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.1955 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.695, borne haute 0.742 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.259 %) — p(stop avant cible) 0.5378 [0.49 ; 0.59], R/R 3.759, perte reelle 7.261 % (gap inclus), EV -1.2378 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.538, borne haute 0.590 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 16.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 2.7 % x 27.29 % + P(rien) 43.5 % x 4.44 % ne couvrent pas P(stop) 53.8 % x 7.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 3.09 ATR (stop 14.857 %) — p(stop avant cible) 0.1583 [0.12 ; 0.20], R/R 1.587, perte reelle 17.196 % (gap inclus), EV -2.1728 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.17 %) : P(cible) 2.8 % x 27.29 % + P(rien) 81.4 % x -0.25 % ne couvrent pas P(stop) 15.8 % x 17.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.043 %) — p(stop avant cible) 0.9114 [0.88 ; 0.94], R/R 22.47, perte reelle 1.215 % (gap inclus), EV -0.1563 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 22.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.911, borne haute 0.938 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.9 % x 27.29 % + P(rien) 8.0 % x 8.85 % ne couvrent pas P(stop) 91.1 % x 1.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.086 %) — p(stop avant cible) 0.8399 [0.80 ; 0.88], R/R 10.935, perte reelle 2.496 % (gap inclus), EV -0.6282 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 10.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.840, borne haute 0.876 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 1.1 % x 27.29 % + P(rien) 14.9 % x 7.88 % ne couvrent pas P(stop) 84.0 % x 2.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 3.129 %) — p(stop avant cible) 0.7547 [0.71 ; 0.80], R/R 7.682, perte reelle 3.553 % (gap inclus), EV -0.5937 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 7.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.755, borne haute 0.798 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 2.2 % x 27.29 % + P(rien) 22.4 % x 6.68 % ne couvrent pas P(stop) 75.5 % x 3.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 4.172 %) — p(stop avant cible) 0.6947 [0.64 ; 0.74], R/R 5.822, perte reelle 4.688 % (gap inclus), EV -0.8708 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.695, borne haute 0.742 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 2.3 % x 27.29 % + P(rien) 28.2 % x 6.23 % ne couvrent pas P(stop) 69.5 % x 4.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 5.215 %) — p(stop avant cible) 0.6088 [0.56 ; 0.66], R/R 4.55, perte reelle 5.998 % (gap inclus), EV -1.002 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.609, borne haute 0.659 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 14.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 2.5 % x 27.29 % + P(rien) 36.6 % x 5.39 % ne couvrent pas P(stop) 60.9 % x 6.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 7.3 %) — p(stop avant cible) 0.4572 [0.41 ; 0.51], R/R 3.136, perte reelle 8.704 % (gap inclus), EV -1.5196 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.52 %) : P(cible) 2.7 % x 27.29 % + P(rien) 51.6 % x 3.34 % ne couvrent pas P(stop) 45.7 % x 8.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 8.343 %) — p(stop avant cible) 0.407 [0.36 ; 0.46], R/R 2.743, perte reelle 9.949 % (gap inclus), EV -1.7521 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.75 %) : P(cible) 2.7 % x 27.29 % + P(rien) 56.6 % x 2.76 % ne couvrent pas P(stop) 40.7 % x 9.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 9.386 %) — p(stop avant cible) 0.3532 [0.30 ; 0.40], R/R 2.455, perte reelle 11.118 % (gap inclus), EV -1.8445 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 2.7 % x 27.29 % + P(rien) 62.0 % x 2.17 % ne couvrent pas P(stop) 35.3 % x 11.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 10.429 %) — p(stop avant cible) 0.3216 [0.27 ; 0.37], R/R 2.25, perte reelle 12.132 % (gap inclus), EV -1.9966 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.00 %) : P(cible) 2.7 % x 27.29 % + P(rien) 65.1 % x 1.80 % ne couvrent pas P(stop) 32.2 % x 12.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 11.472 %) — p(stop avant cible) 0.2923 [0.25 ; 0.34], R/R 2.075, perte reelle 13.152 % (gap inclus), EV -2.1043 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.10 %) : P(cible) 2.8 % x 27.29 % + P(rien) 68.0 % x 1.45 % ne couvrent pas P(stop) 29.2 % x 13.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 3.09 ATR (stop 14.155 %) — p(stop avant cible) 0.1669 [0.13 ; 0.21], R/R 1.658, perte reelle 16.463 % (gap inclus), EV -2.1123 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.11 %) : P(cible) 2.8 % x 27.29 % + P(rien) 80.5 % x -0.15 % ne couvrent pas P(stop) 16.7 % x 16.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 16.687 %) — p(stop avant cible) 0.1227 [0.09 ; 0.16], R/R 1.427, perte reelle 19.126 % (gap inclus), EV -2.1258 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.13 %) : P(cible) 2.8 % x 27.29 % + P(rien) 84.9 % x -0.64 % ne couvrent pas P(stop) 12.3 % x 19.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 18.773 %) — p(stop avant cible) 0.0987 [0.07 ; 0.13], R/R 1.304, perte reelle 20.923 % (gap inclus), EV -2.0921 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.09 %) : P(cible) 2.8 % x 27.29 % + P(rien) 87.3 % x -0.91 % ne couvrent pas P(stop) 9.9 % x 20.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 20.858 %) — p(stop avant cible) 0.0916 [0.06 ; 0.13], R/R 1.228, perte reelle 22.23 % (gap inclus), EV -2.1562 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.16 %) : P(cible) 2.8 % x 27.29 % + P(rien) 88.0 % x -1.00 % ne couvrent pas P(stop) 9.2 % x 22.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 22.944 %) — p(stop avant cible) 0.0876 [0.06 ; 0.12], R/R 1.151, perte reelle 23.706 % (gap inclus), EV -2.2648 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.26 %) : P(cible) 2.8 % x 27.29 % + P(rien) 88.4 % x -1.08 % ne couvrent pas P(stop) 8.8 % x 23.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 25.03 %) — p(stop avant cible) 0.0769 [0.05 ; 0.11], R/R 1.077, perte reelle 25.339 % (gap inclus), EV -2.3376 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.34 %) : P(cible) 2.8 % x 27.29 % + P(rien) 89.5 % x -1.29 % ne couvrent pas P(stop) 7.7 % x 25.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 27.116 %) — p(stop avant cible) 0.0644 [0.04 ; 0.09], R/R 0.997, perte reelle 27.361 % (gap inclus), EV -2.4468 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.45 %) : P(cible) 2.8 % x 27.29 % + P(rien) 90.8 % x -1.60 % ne couvrent pas P(stop) 6.4 % x 27.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 29.202 %) — p(stop avant cible) 0.0453 [0.03 ; 0.07], R/R 0.928, perte reelle 29.424 % (gap inclus), EV -2.486 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.49 %) : P(cible) 2.8 % x 27.29 % + P(rien) 92.7 % x -2.07 % ne couvrent pas P(stop) 4.5 % x 29.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 31.288 %) — p(stop avant cible) 0.0426 [0.03 ; 0.07], R/R 0.868, perte reelle 31.427 % (gap inclus), EV -2.563 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.56 %) : P(cible) 2.8 % x 27.29 % + P(rien) 92.9 % x -2.14 % ne couvrent pas P(stop) 4.3 % x 31.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 33.373 %) — p(stop avant cible) 0.0426 [0.03 ; 0.07], R/R 0.816, perte reelle 33.432 % (gap inclus), EV -2.6484 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.65 %) : P(cible) 2.8 % x 27.29 % + P(rien) 92.9 % x -2.14 % ne couvrent pas P(stop) 4.3 % x 33.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.082, ATR14 0.1286 (4.172 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.531 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.209 % | 3.0756 | 89.05 % | 91.81 % | 93.68 % | 95.64 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.417 % | 3.0691 | 81.46 % | 86.87 % | 89.72 % | 92.77 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.626 % | 3.0627 | 75.25 % | 83.02 % | 86.66 % | 90.0 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.834 % | 3.0563 | 68.93 % | 79.07 % | 83.4 % | 87.23 % | 91.94 % | 94.77 % |
| 0.25 ATR | 1.043 % | 3.0499 | 63.21 % | 75.81 % | 80.34 % | 84.85 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.46 % | 3.037 | 51.87 % | 67.72 % | 73.91 % | 80.0 % | 86.17 % | 91.56 % |
| 0.5 ATR | 2.086 % | 3.0177 | 35.6 % | 55.08 % | 62.94 % | 70.89 % | 80.1 % | 88.24 % |
| 0.75 ATR | 3.129 % | 2.9856 | 19.13 % | 37.81 % | 47.63 % | 59.7 % | 71.94 % | 81.91 % |
| 1.0 ATR | 4.172 % | 2.9534 | 10.06 % | 24.88 % | 35.97 % | 47.62 % | 62.49 % | 75.28 % |
| 1.25 ATR | 5.215 % | 2.9213 | 4.83 % | 17.28 % | 27.47 % | 39.6 % | 55.82 % | 70.05 % |
| 1.5 ATR | 6.258 % | 2.8891 | 2.96 % | 11.25 % | 19.76 % | 31.58 % | 48.66 % | 64.92 % |
| 2.0 ATR | 8.343 % | 2.8249 | 1.28 % | 4.94 % | 9.49 % | 19.5 % | 35.22 % | 53.07 % |
| 2.5 ATR | 10.429 % | 2.7606 | 0.49 % | 2.67 % | 5.63 % | 12.28 % | 27.86 % | 45.33 % |
| 3.0 ATR | 12.515 % | 2.6963 | 0.39 % | 1.68 % | 3.66 % | 8.61 % | 20.9 % | 38.39 % |
| 4.0 ATR | 16.687 % | 2.5677 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 11.74 % | 24.62 % |
| 6.0 ATR | 25.03 % | 2.3106 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.60 ATR | 2.00 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.49 ATR | 1.98 ATR | 2.66 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.46 ATR | 1.77 ATR | 1.98 ATR | 2.81 ATR | 3.81 ATR |
| **10 s.** | 0.66 ATR | 1.45 ATR | 1.64 ATR | 2.15 ATR | 2.71 ATR | 3.10 ATR | 4.53 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.20 ATR | 2.52 ATR | 3.39 ATR | 3.97 ATR | 4.84 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.413–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.129 %, prix 2.9856), p(touche) 37.81 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (62.8 % des re-echantillons)
- **3 seance(s)** : plage utile 0.806–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.172 %, prix 2.9534), p(touche) 35.97 % (en stress 96.08 %)  ✅ optimum identifie (64.0 % des re-echantillons)
- **5 seance(s)** : plage utile 1.082–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.215 %, prix 2.9213), p(touche) 39.6 % (en stress 95.05 %)  ✅ optimum identifie (75.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.636–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.343 %, prix 2.8249), p(touche) 35.22 % (en stress 97.03 %)  ✅ optimum identifie (75.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.524–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (12.515 %, prix 2.6963), p(touche) 38.39 % (en stress 98.0 %)  ✅ optimum identifie (85.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.04 | EV/share : €-0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 13 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 65.9 | bear 5.0 | side 29.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 287.0 (= 93 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=12, n_eff=10))
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→42% · +3.0%→24% · +5.0%→9% · +8.0%→2%
- Range intraday médian 3.96% (p90 6.95%) · excursion haute méd. +1.61% / basse méd. −1.92%
- Profil de vol intra : ouverture 2.584% vs midi 1.195% vs clôture 1.212% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 96% · range 4% · trend ↑0%/↓0% ; spike-down 60% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.1 ; mean-reverting — autocorr -0.16)_ ; drift intra méd. -0.43% ; recovery-V 21%
- **σ réalisé intraday** 2.963% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 73% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 2.9294 (VA 2.8975–2.9472 ; dernier close 2.948)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 22% · rebond 65% · **stop −2.11%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.66 (high win-rate)
- Gaps overnight (n=159) : méd. 0.33% · baisse 39% (gap-down >1% 8% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.15%) · haut méd +0.42% · range méd 1.4%
- Excursion ouverture 15min (n=160) : bas méd −0.78% (p90 −2.37%) · haut méd +0.56% · range méd 1.74%
- Excursion ouverture 30min (n=160) : bas méd −0.89% (p90 −2.69%) · haut méd +0.71% · range méd 1.95%
- Excursion ouverture 60min (n=160) : bas méd −1.02% (p90 −3.06%) · haut méd +0.88% · range méd 2.3%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2.95 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 82% (130/159) · gap 21% · délai 0.4min · rebond 65% (87/130) (MFE +1.47%)
   - −1.0% : fill 30min 36% · séance 67% (111/159) · gap 8% · délai 9.6min · rebond 63% (74/111) (MFE +1.42%)
   - −1.5% : fill 30min 23% · séance 54% (91/159) · gap 3% · délai 35.9min · rebond 61% (57/91) (MFE +1.24%)
   - −2.0% : fill 30min 16% · séance 44% (76/159) · gap 3% · délai 77.4min · rebond 54% (42/76) (MFE +1.17%)
   - −3.0% : fill 30min 7% · séance 22% (44/159) · gap 2% · délai 99.9min · rebond 65% (31/44) (MFE +1.4%)
   - −4.0% : fill 30min 3% · séance 9% (23/159) · gap 1% · délai 45.8min · rebond 47% (13/23) (MFE +0.77%)
   - −5.0% : fill 30min 2% · séance 5% (13/159) · gap 1% · délai 33.7min · rebond 33% (7/13) (MFE +0.67%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.29% (p90 −2.19%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.25% (p90 −1.67%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.14% (p90 −1.83%) → stop au-delà de −1.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=797 jambes) : jambe baissière méd −1.05% (p90 −2.31%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 74% (46/55) · rebond 63% (31/46)
      · −2.0% : fill 52% (35/55) · rebond 49% (19/35)
      · −3.0% : fill 26% (22/55) · rebond 62% (15/22)
      · −4.0% : fill 15% (15/55) · rebond 34% (8/15)
      · −5.0% : fill 10% (10/55) · rebond 33% (5/10)
   - **flat** (32 séances) :
      · −1.0% : fill 80% (25/32) · rebond 57% (15/25)
      · −2.0% : fill 54% (18/32) · rebond 49% (8/18)
      · −3.0% : fill 32% (11/32) · rebond 83% (9/11)
      · −4.0% : fill 10% (4/32) · rebond 14% (1/4)
      · −5.0% : fill 7% (2/32) · rebond 23% (1/2)
   - **gap-up** (72 séances) :
      · −1.0% : fill 58% (40/72) · rebond 66% (28/40)
      · −2.0% : fill 36% (23/72) · rebond 62% (15/23)
      · −3.0% : fill 16% (11/72) · rebond 53% (7/11)
      · −4.0% : fill 5% (4/72) · rebond 100% (4/4)
      · −5.0% : fill 0% (1/72) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 58% si les 15 1res min sont vertes (76 cas) · 29% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **12min** → P(séance verte=clôture>ouverture) 56% si début vert vs 30% si rouge (base 43% · écart 26 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **56%** · continue >prix actuel 36% ; creux résiduel méd -1.74% (q20 -2.81%) → **SL/trailing à −2.81%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.61% / q75 +2.42% → **scale +1.61% / runner +2.42%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **30%** (continue à baisser 56%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.34%** (au-delà de la MAE q10 -4.34%), cible rebond +1.49% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.58% .. +2.37%] · haut q95 +3.35% · bas q05 -3.76%
   - 60min (n=160) : retour [-2.94% .. +3.58%] · haut q95 +4.2% · bas q05 -3.76%
   - 2h (n=160) : retour [-2.99% .. +3.29%] · haut q95 +4.75% · bas q05 -3.91%
   - 4h (n=160) : retour [-3.28% .. +3.79%] · haut q95 +5.05% · bas q05 -3.91%
   - 6h (n=160) : retour [-2.88% .. +4.61%] · haut q95 +5.27% · bas q05 -4.02%
   - session (n=160) : retour [-4.42% .. +4.0%] · haut q95 +6.19% · bas q05 -5.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.91%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.17 · part idiosyncratique 0.83
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.2  _(neutre)_
- **ADX** : 31.4  _(tendance etablie)_
- **MACD** : hist 0.039  _(bullish_recent)_
- **BB** : %B 0.69 · largeur 22.8%
- **ATR** : 0.13 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.292  _(distribution)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 54.6  _(transition)_
- **MA** : MA20 2.96 · MA50 3.24 · MA200 4.71  _(prix > MA20)_
- **Dist MA** : MA20 +4.2% · MA50 -4.9% · MA200 -34.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (859035 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
