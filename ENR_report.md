# ENR

**Generated** : 2026-10-06T21:44:40.441083+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €147.44  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 42/125 fenêtres (p_fill pondéré 31 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €147.44 (+2.9% vs entrée) · entrée €143.29 · stop €131.82 · T1 €145.64 · R/R 0.2  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.190 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €142.85–€143.73 (mid €143.29)
- Spot actuel : €147.44 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : €131.82 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 €145.64 · R/R 0.2 | T2 €147.98 · R/R 0.41 | T3 €150.33 · R/R 0.61
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €131.82


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.59 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.38 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **6.79 pt plus bas** dans le cas TYPIQUE (médiane), 22.46 au p90, **26.377 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 9.38 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0294 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.33 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0073** [0.001 ; 0.0294] _(largeur 2.8 pt, n_eff 173.1)_
   - swing : **0.516** [0.4634 ; 0.5684] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4946** [0.4421 ; 0.5472] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 37.1 observations effectives », dont la borne haute a 95 % vaut environ 8.1 %.
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 18.5 observations effectives », dont la borne haute a 95 % vaut environ 16.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.0 pt), swing (40.4 pt), deep (42.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.63 %** | CVaR **-6.59 %** | vol 3.19 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.97 % contre 3.00 % aujourd'hui, rapport 1.99)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.355** (β de hausse 1.087, asymétrie 1.2466) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.343× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 134.5229 sur atr_grid (2.75 ATR, 8.761 %) — p(stop avant cible) 0.3203 [0.27 ; 0.37], R/R 3.041, perte reelle 9.016 % (gap inclus), CVaR 10.395 %, EV -0.1986 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9573 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.779 %) — p(stop avant cible) 0.6102 [0.56 ; 0.66], R/R 5.569, perte reelle 4.924 % (gap inclus), EV -0.2752 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.610, borne haute 0.660 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 0.6 % x 27.42 % + P(rien) 38.4 % x 6.70 % ne couvrent pas P(stop) 61.0 % x 4.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.96 ATR (stop 8.25 %) — p(stop avant cible) 0.3715 [0.32 ; 0.42], R/R 3.221, perte reelle 8.512 % (gap inclus), EV -0.3343 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.6 % x 27.42 % + P(rien) 62.2 % x 4.26 % ne couvrent pas P(stop) 37.1 % x 8.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 3.64 ATR (stop 13.583 %) — p(stop avant cible) 0.0877 [0.06 ; 0.12], R/R 1.877, perte reelle 14.607 % (gap inclus), EV 0.6743 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.38 % > budget 12.00 %
   - 🟢 support a 7.23 ATR (stop 25.04 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 0.983, perte reelle 27.886 % (gap inclus), EV 1.1794 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.51 % > budget 12.00 %
   - 🟢 support a 11.38 ATR (stop 38.243 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.717, perte reelle 38.243 % (gap inclus), EV 1.2072 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.03 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.796 %) — p(stop avant cible) 0.9329 [0.90 ; 0.96], R/R 32.303, perte reelle 0.849 % (gap inclus), EV -0.1221 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 32.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.933, borne haute 0.956 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.1 % x 27.42 % + P(rien) 6.6 % x 9.61 % ne couvrent pas P(stop) 93.3 % x 0.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.593 %) — p(stop avant cible) 0.8668 [0.83 ; 0.90], R/R 16.496, perte reelle 1.662 % (gap inclus), EV -0.1719 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 16.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.867, borne haute 0.899 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.3 % x 27.42 % + P(rien) 13.1 % x 9.17 % ne couvrent pas P(stop) 86.7 % x 1.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.389 %) — p(stop avant cible) 0.8014 [0.76 ; 0.84], R/R 10.999, perte reelle 2.493 % (gap inclus), EV -0.265 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 11.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.801, borne haute 0.841 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 0.4 % x 27.42 % + P(rien) 19.4 % x 8.29 % ne couvrent pas P(stop) 80.1 % x 2.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.186 %) — p(stop avant cible) 0.7292 [0.68 ; 0.77], R/R 8.283, perte reelle 3.311 % (gap inclus), EV -0.1553 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 8.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.729, borne haute 0.774 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.5 % x 27.42 % + P(rien) 26.6 % x 8.01 % ne couvrent pas P(stop) 72.9 % x 3.31 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 3.982 %) — p(stop avant cible) 0.6574 [0.61 ; 0.71], R/R 6.675, perte reelle 4.108 % (gap inclus), EV -0.1953 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.657, borne haute 0.706 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.5 % x 27.42 % + P(rien) 33.8 % x 7.02 % ne couvrent pas P(stop) 65.7 % x 4.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.96 ATR (stop 7.209 %) — p(stop avant cible) 0.4467 [0.39 ; 0.50], R/R 3.694, perte reelle 7.424 % (gap inclus), EV -0.4292 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 0.6 % x 27.42 % + P(rien) 54.7 % x 4.96 % ne couvrent pas P(stop) 44.7 % x 7.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 8.761 %) — p(stop avant cible) 0.3203 [0.27 ; 0.37], R/R 3.041, perte reelle 9.016 % (gap inclus), EV -0.1986 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.6 % x 27.42 % + P(rien) 67.3 % x 3.73 % ne couvrent pas P(stop) 32.0 % x 9.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 9.557 %) — p(stop avant cible) 0.2821 [0.24 ; 0.33], R/R 2.794, perte reelle 9.816 % (gap inclus), EV -0.1165 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.6 % x 27.42 % + P(rien) 71.2 % x 3.48 % ne couvrent pas P(stop) 28.2 % x 9.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 3.64 ATR (stop 12.541 %) — p(stop avant cible) 0.124 [0.09 ; 0.16], R/R 2.07, perte reelle 13.244 % (gap inclus), EV 0.4636 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.28 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 14.336 %) — p(stop avant cible) 0.0719 [0.05 ; 0.10], R/R 1.767, perte reelle 15.521 % (gap inclus), EV 0.7513 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.04 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 15.929 %) — p(stop avant cible) 0.0393 [0.02 ; 0.06], R/R 1.576, perte reelle 17.404 % (gap inclus), EV 0.9518 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.36 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.522 %) — p(stop avant cible) 0.0289 [0.01 ; 0.05], R/R 1.469, perte reelle 18.668 % (gap inclus), EV 1.0071 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.96 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 19.115 %) — p(stop avant cible) 0.0222 [0.01 ; 0.04], R/R 1.359, perte reelle 20.175 % (gap inclus), EV 1.0342 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.67 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 20.708 %) — p(stop avant cible) 0.0077 [0.00 ; 0.02], R/R 1.17, perte reelle 23.445 % (gap inclus), EV 1.1164 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.98 % > budget 12.00 %
   - 🟢 grid_snapped a 7.23 ATR (stop 23.998 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 1.012, perte reelle 27.091 % (gap inclus), EV 1.1603 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.66 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 25.486 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 0.977, perte reelle 28.055 % (gap inclus), EV 1.1788 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.52 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 147.44, ATR14 4.6971 (3.186 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.169 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.159 % | 147.2051 | 91.52 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.319 % | 146.9703 | 83.73 % | 88.15 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.478 % | 146.7354 | 76.33 % | 82.13 % | 85.87 % | 88.51 % | 91.04 % | 93.27 % |
| 0.2 ATR | 0.637 % | 146.5006 | 70.41 % | 78.87 % | 83.0 % | 86.34 % | 89.25 % | 91.86 % |
| 0.25 ATR | 0.796 % | 146.2657 | 63.91 % | 74.53 % | 79.35 % | 83.17 % | 87.16 % | 90.45 % |
| 0.35 ATR | 1.115 % | 145.796 | 51.78 % | 64.66 % | 70.26 % | 75.64 % | 81.79 % | 86.33 % |
| 0.5 ATR | 1.593 % | 145.0914 | 36.39 % | 51.63 % | 59.39 % | 66.14 % | 74.13 % | 80.2 % |
| 0.75 ATR | 2.389 % | 143.9171 | 19.43 % | 35.54 % | 44.86 % | 54.06 % | 64.88 % | 73.27 % |
| 1.0 ATR | 3.186 % | 142.7429 | 10.95 % | 25.17 % | 33.99 % | 43.66 % | 56.32 % | 65.03 % |
| 1.25 ATR | 3.982 % | 141.5686 | 6.02 % | 17.08 % | 24.6 % | 35.25 % | 47.76 % | 57.39 % |
| 1.5 ATR | 4.779 % | 140.3943 | 2.76 % | 10.86 % | 17.59 % | 27.43 % | 40.5 % | 51.06 % |
| 2.0 ATR | 6.372 % | 138.0457 | 0.79 % | 3.95 % | 8.5 % | 15.94 % | 27.76 % | 39.8 % |
| 2.5 ATR | 7.964 % | 135.6971 | 0.3 % | 1.97 % | 3.95 % | 9.21 % | 19.1 % | 30.15 % |
| 3.0 ATR | 9.557 % | 133.3486 | 0.1 % | 0.79 % | 1.88 % | 4.85 % | 12.14 % | 22.41 % |
| 4.0 ATR | 12.743 % | 128.6514 | 0.1 % | 0.39 % | 1.09 % | 2.28 % | 6.27 % | 12.46 % |
| 6.0 ATR | 19.115 % | 119.2572 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 1.05 ATR | 1.33 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.81 ATR | 1.00 ATR | 1.16 ATR | 1.56 ATR | 1.92 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.03 ATR | 1.24 ATR | 1.41 ATR | 1.92 ATR | 2.38 ATR |
| **5 s.** | 0.36 ATR | 0.85 ATR | 0.97 ATR | 1.32 ATR | 1.61 ATR | 1.82 ATR | 2.44 ATR | 2.98 ATR |
| **10 s.** | 0.48 ATR | 1.19 ATR | 1.34 ATR | 1.79 ATR | 2.16 ATR | 2.45 ATR | 3.37 ATR | 4.62 ATR |
| **20 s.** | 0.69 ATR | 1.55 ATR | 1.77 ATR | 2.35 ATR | 2.83 ATR | 3.24 ATR | 4.69 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.389 %, prix 143.9177), p(touche) 35.54 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.748–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.389 %, prix 143.9177), p(touche) 44.86 % (en stress 96.08 %)  ✅ optimum identifie (85.9 % des re-echantillons)
- **5 seance(s)** : plage utile 0.968–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.186 %, prix 142.7426), p(touche) 43.66 % (en stress 99.01 %)  ✅ optimum identifie (90.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.345–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.779 %, prix 140.3938), p(touche) 40.5 % (en stress 100.0 %)  ✅ optimum identifie (92.9 % des re-echantillons)
- **20 seance(s)** : plage utile 1.769–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.372 %, prix 138.0451), p(touche) 39.8 % (en stress 99.0 %)  ✅ optimum identifie (88.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 84.0 | bear 11.0 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 295.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.815% → cible +1.639% / stop −8.0%, p_fill 31%, n_eff≈37.1) : P(cible|rempli) **31%** · **EV/risk +0.002** (×p_fill ; si rempli +0.04% du capital)
  - **swing** (entrée dip −6.194% → cible +3.797% / stop −3.396%, p_fill 15%, n_eff≈18.5) : P(cible|rempli) **67%** · **EV/risk +0.053** (×p_fill ; si rempli +1.19% du capital)
  - **deep** (entrée dip −9.582% → cible +5.571% / stop −5.285%, p_fill 13%, n_eff≈15.4) : P(cible|rempli) **71%** · **EV/risk +0.059** (×p_fill ; si rempli +2.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→77% · +1.0%→62% · +2.0%→38% · +3.0%→18% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.7% (p90 6.11%) · excursion haute méd. +1.52% / basse méd. −1.74%
- Profil de vol intra : ouverture 1.958% vs midi 0.866% vs clôture 1.062% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. -0.357% ; recovery-V 20%
- **σ réalisé intraday** 2.187% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 72% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 146.1558 (VA 145.4312–146.3972 ; dernier close 145.44)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 49% · rebond 59% · **stop −3.83%** sous le fill (sous le bruit) · cible +1.48% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 33% (gap-down >1% 15% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.53% (p90 −1.67%) · haut méd +0.44% · range méd 1.12%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.17%) · haut méd +0.59% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.23%) · haut méd +0.62% · range méd 1.68%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.44%) · haut méd +0.73% · range méd 1.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 145.42 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 69% (116/159) · gap 24% · délai 0.5min · rebond 58% (62/116) (MFE +1.2%)
   - −1.0% : fill 30min 38% · séance 64% (108/159) · gap 15% · délai 10.3min · rebond 61% (62/108) (MFE +1.36%)
   - −1.5% : fill 30min 25% · séance 49% (88/159) · gap 11% · délai 22.9min · rebond 59% (50/88) (MFE +1.48%)
   - −2.0% : fill 30min 17% · séance 40% (73/159) · gap 8% · délai 62.1min · rebond 54% (44/73) (MFE +1.08%)
   - −3.0% : fill 30min 9% · séance 22% (46/159) · gap 2% · délai 189.8min · rebond 44% (26/46) (MFE +0.86%)
   - −4.0% : fill 30min 6% · séance 14% (33/159) · gap 1% · délai 76.7min · rebond 58% (22/33) (MFE +1.12%)
   - −5.0% : fill 30min 2% · séance 11% (24/159) · gap 0% · délai 388.5min · rebond 43% (12/24) (MFE +0.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.72%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.33% (p90 −1.32%) → stop au-delà de −0.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −0.95%) → stop au-delà de −0.7% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=521 jambes) : jambe baissière méd −1.02% (p90 −2.33%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 98% (52/53) · rebond 55% (28/52)
      · −2.0% : fill 75% (39/53) · rebond 44% (20/39)
      · −3.0% : fill 45% (27/53) · rebond 33% (14/27)
      · −4.0% : fill 37% (22/53) · rebond 60% (16/22)
      · −5.0% : fill 31% (18/53) · rebond 49% (11/18)
   - **flat** (17 séances) :
      · −1.0% : fill 78% (14/17) · rebond 65% (10/14)
      · −2.0% : fill 44% (9/17) · rebond 67% (6/9)
      · −3.0% : fill 27% (6/17) · rebond 46% (3/6)
      · −4.0% : fill 9% (4/17) · rebond 52% (2/4)
      · −5.0% : fill 7% (3/17) · rebond 0% (0/3)
   - **gap-up** (89 séances) :
      · −1.0% : fill 43% (42/89) · rebond 66% (24/42)
      · −2.0% : fill 21% (25/89) · rebond 65% (18/25)
      · −3.0% : fill 8% (13/89) · rebond 72% (9/13)
      · −4.0% : fill 4% (7/89) · rebond 47% (4/7)
      · −5.0% : fill 2% (3/89) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 66% si les 15 1res min sont vertes (75 cas) · 24% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:29** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 219min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **73%** · continue >prix actuel 54% ; creux résiduel méd -1.07% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.24% / q75 +2.25% → **scale +1.24% / runner +2.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.65%** (au-delà de la MAE q10 -3.65%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.93% .. +1.69%] · haut q95 +2.36% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.46% .. +1.94%] · haut q95 +2.55% · bas q05 -2.86%
   - 2h (n=160) : retour [-2.78% .. +2.36%] · haut q95 +2.76% · bas q05 -3.56%
   - 4h (n=160) : retour [-3.15% .. +2.63%] · haut q95 +3.22% · bas q05 -3.93%
   - 6h (n=160) : retour [-3.69% .. +3.35%] · haut q95 +4.15% · bas q05 -4.56%
   - session (n=160) : retour [-4.9% .. +3.08%] · haut q95 +4.77% · bas q05 -6.18%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.56 · part idiosyncratique 0.44
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 66.6  _(momentum haussier)_
- **ADX** : 8.6  _(pas de tendance nette)_
- **MACD** : hist 0.938  _(pas de croisement recent)_
- **BB** : %B 0.83 · largeur 11.3%
- **ATR** : 4.7 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.194  _(distribution)_
- **Vol ratio** : 1.08  _(volume normal)_
- **Choppiness** : 59.9  _(transition)_
- **MA** : MA20 142.17 · MA50 147.39 · MA200 153.56  _(prix > MA20)_
- **Dist MA** : MA20 +3.7% · MA50 +0.0% · MA200 -4.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (559399 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
