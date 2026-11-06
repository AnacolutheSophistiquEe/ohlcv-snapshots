# ENR

**Generated** : 2026-11-06T21:44:12.754302+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €118.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €118.10 (+0.4% vs entrée) · entrée €117.61 · stop €114.62 · T1 €123.57 · R/R 1.99  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-06 : 118.1 · ATR Wilder 6.93 (5.87 %)_
- **Swing** : plage **109.69 → 104.05** (-7.12 % a -11.89 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 103.21-104.4 (B). stop INDICATIF 95.09 (-8.61 % sous le bas ; sous le support 98.56-100.32 (- 0,5 ATR)).
- **Deep** : plage **104.05 → 93.68** (-11.89 % a -20.68 % sous la cloture, 1.5 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 103.21-104.4 (B) ; 98.56-100.32 (A) ; 94.0-95.27 (A). stop INDICATIF 85.83 (-8.38 % sous le bas ; sous le support 89.3-92.68 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.37 ATR sous le plus haut 20 s., RSI(2) 44.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 109.88-110.08 (C, -6.79 %) ; 103.21-104.4 (B, -11.6 %) ; 98.56-100.32 (A, -15.05 %) ; 94.0-95.27 (A, -19.33 %) ; 89.3-92.68 (A, -21.52 %) ; 85.71-89.14 (A, -24.52 %)
- Resistances reelles au-dessus : 122.83-124.46 (A, 4.0 %) ; 130.89-133.85 (A, 10.83 %) ; 135.7-139.16 (A, 14.9 %) ; 140.18-143.38 (B, 18.7 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.75 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.26 %)** : le gap seul le franchit 0.314 % des séances (4 fois sur 1274).
   - exécution **7.643 pt plus bas** dans le cas TYPIQUE (médiane), 22.621 au p90, **28.497 au pire**
   - perte réelle **18.578 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 7.26 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0355 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.382 % | p01 -5.39 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3353** [0.2682 ; 0.4079] _(largeur 14.0 pt, n_eff 173.1)_
   - swing : **0.3417** [0.2932 ; 0.3928] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.3275** [0.2796 ; 0.3782] _(largeur 9.9 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.83 %** | CVaR **-6.82 %** | vol 3.21 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 6.21 % contre 3.17 % aujourd'hui, rapport 1.96)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.9 % vs -10.11 % si l'on extrapolait par √5 _(rapport 0.881 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3069** (β de hausse 1.038, asymétrie 1.259) vs GDAXI — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 111.1063 sur support (0.48 ATR, 5.922 %) — p(stop avant cible) 0.549 [0.50 ; 0.60], R/R 5.574, perte reelle 6.257 % (gap inclus), CVaR 9.294 %, EV -0.9377 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0832 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.549, borne haute 0.601 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 0.48 ATR (stop 5.922 %) — p(stop avant cible) 0.549 [0.50 ; 0.60], R/R 5.574, perte reelle 6.257 % (gap inclus), EV -0.9377 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.549, borne haute 0.601 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 0.1 % x 34.88 % + P(rien) 45.0 % x 5.45 % ne couvrent pas P(stop) 54.9 % x 6.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 9.506 %) — p(stop avant cible) 0.3334 [0.29 ; 0.38], R/R 3.421, perte reelle 10.194 % (gap inclus), EV -1.0192 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 0.1 % x 34.88 % + P(rien) 66.5 % x 3.50 % ne couvrent pas P(stop) 33.3 % x 10.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.44 ATR (stop 18.316 %) — p(stop avant cible) 0.0386 [0.02 ; 0.06], R/R 1.836, perte reelle 18.998 % (gap inclus), EV 0.2009 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.75 % > budget 12.00 %
   - 🟢 grid_snapped a 0.48 ATR (stop 4.94 %) — p(stop avant cible) 0.6287 [0.58 ; 0.68], R/R 6.805, perte reelle 5.125 % (gap inclus), EV -0.7741 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.629, borne haute 0.678 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.77 %) : P(cible) 0.1 % x 34.88 % + P(rien) 37.0 % x 6.49 % ne couvrent pas P(stop) 62.9 % x 5.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 7.922 %) — p(stop avant cible) 0.4231 [0.37 ; 0.48], R/R 4.02, perte reelle 8.675 % (gap inclus), EV -1.1075 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 0.1 % x 34.88 % + P(rien) 57.6 % x 4.37 % ne couvrent pas P(stop) 42.3 % x 8.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 11.09 %) — p(stop avant cible) 0.2279 [0.19 ; 0.27], R/R 2.943, perte reelle 11.85 % (gap inclus), EV -0.6951 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 0.1 % x 34.88 % + P(rien) 77.1 % x 2.54 % ne couvrent pas P(stop) 22.8 % x 11.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 12.674 %) — p(stop avant cible) 0.1591 [0.12 ; 0.20], R/R 2.624, perte reelle 13.29 % (gap inclus), EV -0.3697 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 0.1 % x 34.88 % + P(rien) 84.0 % x 2.02 % ne couvrent pas P(stop) 15.9 % x 13.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 2.44 ATR (stop 17.334 %) — p(stop avant cible) 0.042 [0.02 ; 0.07], R/R 1.928, perte reelle 18.085 % (gap inclus), EV 0.203 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.43 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 22.18 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 1.395, perte reelle 25.003 % (gap inclus), EV 0.3362 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.11 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 25.349 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 1.245, perte reelle 28.003 % (gap inclus), EV 0.3955 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.63 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 28.518 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 1.176, perte reelle 29.662 % (gap inclus), EV 0.4037 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.54 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 31.686 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.057, perte reelle 33.007 % (gap inclus), EV 0.4234 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.14 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 34.855 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.991, perte reelle 35.199 % (gap inclus), EV 0.421 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.19 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 38.023 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.917, perte reelle 38.023 % (gap inclus), EV 0.4211 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.21 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 41.192 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.847, perte reelle 41.192 % (gap inclus), EV 0.4246 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.14 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 44.361 %) — p(stop avant cible) 0.0003 [0.00 ; 0.01], R/R 0.786, perte reelle 44.361 % (gap inclus), EV 0.427 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.07 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 47.529 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.734, perte reelle 47.529 % (gap inclus), EV 0.4311 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.00 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 50.698 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.688, perte reelle 50.698 % (gap inclus), EV 0.4311 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.00 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 118.1, ATR14 7.4843 (6.337 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.37 ATR = 2.345 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.317 % | 117.7258 | 91.42 % | 94.18 % | 95.65 % | 96.24 % | 97.31 % | 97.99 % |
| 0.1 ATR | 0.634 % | 117.3516 | 83.63 % | 88.25 % | 90.61 % | 92.67 % | 94.73 % | 95.78 % |
| 0.15 ATR | 0.951 % | 116.9774 | 76.33 % | 82.43 % | 85.97 % | 88.71 % | 91.44 % | 93.57 % |
| 0.2 ATR | 1.267 % | 116.6031 | 70.41 % | 79.07 % | 83.0 % | 86.63 % | 89.65 % | 92.16 % |
| 0.25 ATR | 1.584 % | 116.2289 | 63.71 % | 74.63 % | 79.25 % | 83.37 % | 87.66 % | 90.85 % |
| 0.35 ATR | 2.218 % | 115.4805 | 52.07 % | 65.15 % | 70.55 % | 76.14 % | 82.59 % | 87.04 % |
| 0.5 ATR | 3.169 % | 114.3579 | 36.79 % | 52.22 % | 59.88 % | 66.93 % | 75.12 % | 81.11 % |
| 0.75 ATR | 4.753 % | 112.4868 | 19.92 % | 36.23 % | 45.65 % | 54.95 % | 66.17 % | 74.47 % |
| 1.0 ATR | 6.337 % | 110.6157 | 11.24 % | 26.06 % | 35.08 % | 45.05 % | 58.01 % | 66.73 % |
| 1.25 ATR | 7.922 % | 108.7446 | 6.21 % | 17.47 % | 25.4 % | 36.24 % | 49.35 % | 59.2 % |
| 1.5 ATR | 9.506 % | 106.8736 | 2.96 % | 11.35 % | 18.38 % | 28.51 % | 42.29 % | 52.96 % |
| 2.0 ATR | 12.674 % | 103.1314 | 0.79 % | 4.34 % | 9.09 % | 17.03 % | 29.25 % | 41.71 % |
| 2.5 ATR | 15.843 % | 99.3893 | 0.3 % | 2.07 % | 4.25 % | 10.1 % | 20.4 % | 31.96 % |
| 3.0 ATR | 19.012 % | 95.6471 | 0.1 % | 0.89 % | 2.08 % | 5.35 % | 13.23 % | 24.12 % |
| 4.0 ATR | 25.349 % | 88.1628 | 0.1 % | 0.39 % | 1.19 % | 2.48 % | 7.06 % | 13.67 % |
| 6.0 ATR | 38.023 % | 73.1943 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.68 ATR | 0.75 ATR | 1.06 ATR | 1.34 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.83 ATR | 1.03 ATR | 1.18 ATR | 1.60 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.77 ATR | 1.05 ATR | 1.26 ATR | 1.44 ATR | 1.95 ATR | 2.42 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 1.00 ATR | 1.35 ATR | 1.65 ATR | 1.87 ATR | 2.51 ATR | 3.12 ATR |
| **10 s.** | 0.50 ATR | 1.23 ATR | 1.40 ATR | 1.86 ATR | 2.24 ATR | 2.53 ATR | 3.52 ATR | 4.85 ATR |
| **20 s.** | 0.73 ATR | 1.63 ATR | 1.85 ATR | 2.45 ATR | 2.94 ATR | 3.39 ATR | 4.91 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.419 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.613–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.753 %, prix 112.4867), p(touche) 36.23 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.765–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.337 %, prix 110.616), p(touche) 35.08 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (86.4 % des re-echantillons)
- **5 seance(s)** : plage utile 1.001–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.922 %, prix 108.7441), p(touche) 36.24 % (en stress 96.04 %)  ✅ optimum identifie (91.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.404–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.506 %, prix 106.8734), p(touche) 42.29 % (en stress 100.0 %)  ✅ optimum identifie (92.2 % des re-echantillons)
- **20 seance(s)** : plage utile 1.854–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.674 %, prix 103.132), p(touche) 41.71 % (en stress 99.0 %)  ✅ optimum identifie (90.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 25.1 | bear 69.8 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.414% → cible +5.073% / stop −2.536%, p_fill 87%, n_eff≈92.9) : P(cible|rempli) **4%** · **EV/risk -0.188** (×p_fill ; si rempli -0.55% du capital)
  - **swing** (entrée dip −0.922% → cible +7.152% / stop −6.397%, p_fill 80%, n_eff≈92.2) : P(cible|rempli) **11%** · **EV/risk -0.246** (×p_fill ; si rempli -1.98% du capital)
  - **deep** (entrée dip −1.364% → cible +16.547% / stop −9.637%, p_fill 83%, n_eff≈93.4) : P(cible|rempli) **2%** · **EV/risk -0.318** (×p_fill ; si rempli -3.70% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→34% · +3.0%→15% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.62% (p90 6.06%) · excursion haute méd. +1.37% / basse méd. −1.89%
- Profil de vol intra : ouverture 1.961% vs midi 0.824% vs clôture 1.048% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 61% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. -0.864% ; recovery-V 25%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 83% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 121.5065 (VA 120.2185–123.5995 ; dernier close 118.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 18% · rebond 57% · **stop −4.86%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.22 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 38% (gap-down >1% 20% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.49% (p90 −1.69%) · haut méd +0.49% · range méd 1.14%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.05%) · haut méd +0.58% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.19%) · haut méd +0.62% · range méd 1.69%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.35%) · haut méd +0.68% · range méd 1.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 118.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 70% (115/159) · gap 30% · délai 0.2min · rebond 48% (59/115) (MFE +0.88%)
   - −1.0% : fill 30min 40% · séance 66% (107/159) · gap 20% · délai 8.6min · rebond 51% (59/107) (MFE +1.04%)
   - −1.5% : fill 30min 29% · séance 53% (88/159) · gap 13% · délai 12.6min · rebond 55% (48/88) (MFE +1.28%)
   - −2.0% : fill 30min 23% · séance 44% (73/159) · gap 9% · délai 20.7min · rebond 50% (41/73) (MFE +1.0%)
   - −3.0% : fill 30min 10% · séance 29% (48/159) · gap 3% · délai 251.6min · rebond 40% (24/48) (MFE +0.66%)
   - −4.0% : fill 30min 6% · séance 18% (32/159) · gap 2% · délai 200.1min · rebond 57% (20/32) (MFE +1.05%)
   - −5.0% : fill 30min 4% · séance 13% (24/159) · gap 0% · délai 397.7min · rebond 38% (11/24) (MFE +0.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.17%) → stop au-delà de −1.55% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.63%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.66%) → stop au-delà de −0.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=526 jambes) : jambe baissière méd −1.04% (p90 −2.31%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (53/54) · rebond 41% (26/53)
      · −2.0% : fill 84% (41/54) · rebond 49% (20/41)
      · −3.0% : fill 59% (30/54) · rebond 40% (14/30)
      · −4.0% : fill 39% (22/54) · rebond 75% (16/22)
      · −5.0% : fill 30% (18/54) · rebond 47% (10/18)
   - **flat** (18 séances) :
      · −1.0% : fill 59% (13/18) · rebond 64% (9/13)
      · −2.0% : fill 33% (8/18) · rebond 68% (6/8)
      · −3.0% : fill 20% (5/18) · rebond 48% (3/5)
      · −4.0% : fill 6% (3/18) · rebond 59% (2/3)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 46% (41/87) · rebond 61% (24/41)
      · −2.0% : fill 23% (24/87) · rebond 46% (15/24)
      · −3.0% : fill 13% (13/87) · rebond 36% (7/13)
      · −4.0% : fill 9% (7/87) · rebond 11% (2/7)
      · −5.0% : fill 5% (4/87) · rebond 12% (1/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 61% si les 15 1res min sont vertes (71 cas) · 30% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 43% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **72%** · continue >prix actuel 56% ; creux résiduel méd -1.18% (q20 -2.25%) → **SL/trailing à −2.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.1% → **scale +1.08% / runner +2.1%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **21%** (continue à baisser 57%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.96%** (au-delà de la MAE q10 -4.96%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.97% .. +1.62%] · haut q95 +2.08% · bas q05 -2.65%
   - 60min (n=160) : retour [-2.5% .. +1.42%] · haut q95 +2.41% · bas q05 -3.07%
   - 2h (n=160) : retour [-2.53% .. +2.22%] · haut q95 +2.56% · bas q05 -3.58%
   - 4h (n=160) : retour [-2.61% .. +2.42%] · haut q95 +3.02% · bas q05 -4.04%
   - 6h (n=160) : retour [-3.22% .. +3.06%] · haut q95 +3.68% · bas q05 -4.31%
   - session (n=160) : retour [-5.78% .. +2.83%] · haut q95 +4.66% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.37%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.51 · part idiosyncratique 0.49
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.5  _(momentum baissier)_
- **ADX** : 23.1  _(pas de tendance nette)_
- **MACD** : hist -1.004  _(bearish_recent)_
- **BB** : %B 0.16 · largeur 25.9%
- **ATR** : 7.48 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.012  _(neutre)_
- **Vol ratio** : 1.28  _(volume normal)_
- **Choppiness** : 51.6  _(transition)_
- **MA** : MA20 129.49 · MA50 137.59 · MA200 153.88  _(prix < MA20)_
- **Dist MA** : MA20 -8.8% · MA50 -14.2% · MA200 -23.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (714015 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
