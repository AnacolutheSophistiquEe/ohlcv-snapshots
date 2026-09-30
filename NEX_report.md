# NEX

**Generated** : 2026-09-30T21:48:00.288620+00:00  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €131.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €131.90 (+0.7% vs entrée) · entrée €130.96 · stop €129.00 · T1 €133.16 · R/R 1.12  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -104 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €130.60–€131.33 (mid €130.96)
- Spot actuel : €131.90 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €129.00 (plancher anti-bruit 5 s — stop EV-optimal −1.5% (first-passage 5 s réel) ; -1.50 % depuis l'entree)
- Targets : T1 €133.16 · R/R 1.12 | T2 €135.37 · R/R 2.25 | T3 €137.57 · R/R 3.37
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.58 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **2.588 pt plus bas** dans le cas TYPIQUE (médiane), 3.394 au p90, **4.016 au pire**
   - perte réelle **8.124 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 5.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0119 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3785** [0.3087 ; 0.4523] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.3816** [0.3316 ; 0.4336] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.4119** [0.3609 ; 0.4643] _(largeur 10.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.52 %** | CVaR **-5.28 %** | vol 2.31 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.88 % si l'on extrapolait par √5 _(rapport 0.953 ; < 1 = le √5 surestime)_
- **β de baisse : 1.006** (β de hausse 1.0892, asymétrie 0.9236) vs FCHI — 620 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 121.9839 sur atr_grid (2.25 ATR, 7.518 %) — p(stop avant cible) 0.2308 [0.19 ; 0.28], R/R 3.109, perte reelle 7.713 % (gap inclus), CVaR 8.419 %, EV 0.369 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9573 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.43 ATR (stop 3.541 %) — p(stop avant cible) 0.5998 [0.55 ; 0.65], R/R 6.502, perte reelle 3.688 % (gap inclus), EV -0.1453 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 6.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.600, borne haute 0.650 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.6 % x 23.98 % + P(rien) 39.4 % x 4.86 % ne couvrent pas P(stop) 60.0 % x 3.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 0.95 ATR (stop 5.298 %) — p(stop avant cible) 0.4085 [0.36 ; 0.46], R/R 4.325, perte reelle 5.545 % (gap inclus), EV 0.0701 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - 🔴 support a 5.48 ATR (stop 20.44 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 1.142, perte reelle 20.992 % (gap inclus), EV 0.6004 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.57 % > budget 12.00 %
      - ⚠ support DETECTE a 0.85 ATR du spot — compartiment <1, mesure a 45.4 % de casse (IC clusterise [0.423 ; 0.484] sur 1130 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ grid_snapped a 0.43 ATR (stop 2.429 %) — p(stop avant cible) 0.7079 [0.66 ; 0.75], R/R 9.546, perte reelle 2.512 % (gap inclus), EV -0.1195 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 9.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.708, borne haute 0.754 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.6 % x 23.98 % + P(rien) 28.6 % x 5.27 % ne couvrent pas P(stop) 70.8 % x 2.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.95 ATR (stop 4.185 %) — p(stop avant cible) 0.5435 [0.49 ; 0.60], R/R 5.509, perte reelle 4.353 % (gap inclus), EV -0.1588 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.543, borne haute 0.596 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.6 % x 23.98 % + P(rien) 45.0 % x 4.56 % ne couvrent pas P(stop) 54.4 % x 4.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 5.847 %) — p(stop avant cible) 0.3771 [0.33 ; 0.43], R/R 3.946, perte reelle 6.078 % (gap inclus), EV 0.0308 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 6.683 %) — p(stop avant cible) 0.2936 [0.25 ; 0.34], R/R 3.497, perte reelle 6.859 % (gap inclus), EV 0.2133 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 7.518 %) — p(stop avant cible) 0.2308 [0.19 ; 0.28], R/R 3.109, perte reelle 7.713 % (gap inclus), EV 0.369 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.5 ATR (stop 8.353 %) — p(stop avant cible) 0.1845 [0.15 ; 0.23], R/R 2.818, perte reelle 8.511 % (gap inclus), EV 0.4501 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 9.189 %) — p(stop avant cible) 0.1442 [0.11 ; 0.18], R/R 2.564, perte reelle 9.355 % (gap inclus), EV 0.4898 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 10.024 %) — p(stop avant cible) 0.1127 [0.08 ; 0.15], R/R 2.357, perte reelle 10.177 % (gap inclus), EV 0.5149 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 11.694 %) — p(stop avant cible) 0.0738 [0.05 ; 0.10], R/R 1.985, perte reelle 12.082 % (gap inclus), EV 0.5026 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.27 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 13.365 %) — p(stop avant cible) 0.0399 [0.02 ; 0.06], R/R 1.723, perte reelle 13.921 % (gap inclus), EV 0.4995 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.50 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 15.036 %) — p(stop avant cible) 0.0193 [0.01 ; 0.04], R/R 1.522, perte reelle 15.755 % (gap inclus), EV 0.545 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.09 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.706 %) — p(stop avant cible) 0.0125 [0.00 ; 0.03], R/R 1.39, perte reelle 17.257 % (gap inclus), EV 0.5484 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.08 % > budget 12.00 %
   - 🔴 grid_snapped a 5.48 ATR (stop 19.328 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 1.174, perte reelle 20.423 % (gap inclus), EV 0.6001 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.54 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 21.718 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 1.044, perte reelle 22.964 % (gap inclus), EV 0.6013 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.52 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 23.389 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.994, perte reelle 24.135 % (gap inclus), EV 0.605 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.47 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 25.06 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.957, perte reelle 25.06 % (gap inclus), EV 0.6072 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.40 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 26.73 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.897, perte reelle 26.73 % (gap inclus), EV 0.6126 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.31 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 131.9, ATR14 4.4071 (3.341 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 1.163 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.167 % | 131.6796 | 87.84 % | 91.46 % | 93.22 % | 95.18 % | 97.03 % | 97.9 % |
| 0.1 ATR | 0.334 % | 131.4593 | 81.96 % | 87.73 % | 90.37 % | 93.21 % | 95.65 % | 97.0 % |
| 0.15 ATR | 0.501 % | 131.2389 | 75.29 % | 83.51 % | 86.94 % | 90.26 % | 94.16 % | 95.7 % |
| 0.2 ATR | 0.668 % | 131.0186 | 68.73 % | 78.31 % | 83.2 % | 88.29 % | 92.78 % | 95.0 % |
| 0.25 ATR | 0.835 % | 130.7982 | 62.16 % | 73.6 % | 79.17 % | 85.14 % | 90.7 % | 93.81 % |
| 0.35 ATR | 1.169 % | 130.3575 | 49.71 % | 64.28 % | 71.71 % | 78.84 % | 86.65 % | 91.61 % |
| 0.5 ATR | 1.671 % | 129.6964 | 34.51 % | 52.4 % | 61.2 % | 70.57 % | 80.22 % | 87.41 % |
| 0.75 ATR | 2.506 % | 128.5946 | 20.29 % | 36.31 % | 47.25 % | 58.56 % | 70.13 % | 80.82 % |
| 1.0 ATR | 3.341 % | 127.4929 | 10.59 % | 24.14 % | 34.68 % | 48.33 % | 61.52 % | 74.13 % |
| 1.25 ATR | 4.177 % | 126.3911 | 4.8 % | 16.0 % | 24.85 % | 39.37 % | 54.4 % | 67.63 % |
| 1.5 ATR | 5.012 % | 125.2893 | 2.45 % | 11.19 % | 18.66 % | 30.71 % | 46.88 % | 60.24 % |
| 2.0 ATR | 6.683 % | 123.0857 | 0.88 % | 5.3 % | 10.02 % | 19.49 % | 35.11 % | 50.65 % |
| 2.5 ATR | 8.353 % | 120.8821 | 0.49 % | 2.65 % | 5.6 % | 11.52 % | 24.43 % | 38.86 % |
| 3.0 ATR | 10.024 % | 118.6786 | 0.2 % | 1.67 % | 3.24 % | 7.09 % | 17.51 % | 30.37 % |
| 4.0 ATR | 13.365 % | 114.2714 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.52 % | 17.88 % |
| 6.0 ATR | 20.048 % | 105.4571 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.02 ATR | 1.24 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.60 ATR | 2.06 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.80 ATR | 1.04 ATR | 1.25 ATR | 1.45 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.09 ATR | 1.43 ATR | 1.75 ATR | 1.98 ATR | 2.67 ATR | 3.40 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.10 ATR | 2.47 ATR | 2.82 ATR | 3.75 ATR | 4.82 ATR |
| **20 s.** | 0.97 ATR | 2.03 ATR | 2.24 ATR | 2.85 ATR | 3.43 ATR | 3.83 ATR | 5.17 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (76.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.615–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.506 %, prix 128.5946), p(touche) 36.31 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.795–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.341 %, prix 127.4932), p(touche) 34.68 % (en stress 84.31 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.093–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.177 %, prix 126.3905), p(touche) 39.37 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.58–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.683 %, prix 123.0851), p(touche) 35.11 % (en stress 98.04 %)  ✅ optimum identifie (70.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.24–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.353 %, prix 120.8824), p(touche) 38.86 % (en stress 98.02 %)  ✅ optimum identifie (69.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 34.2 | bear 10.4 | side 55.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.711% → cible +1.683% / stop −1.5%, p_fill 71%, n_eff≈72.5) : P(cible|rempli) **24%** · **EV/risk -0.183** (×p_fill ; si rempli -0.39% du capital)
  - **swing** (entrée dip −1.571% → cible +8.146% / stop −4.073%, p_fill 53%, n_eff≈62.1) : P(cible|rempli) **8%** · **EV/risk -0.106** (×p_fill ; si rempli -0.82% du capital)
  - **deep** (entrée dip −2.418% → cible +9.093% / stop −5.136%, p_fill 60%, n_eff≈66.1) : P(cible|rempli) **20%** · **EV/risk -0.022** (×p_fill ; si rempli -0.19% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→58% · +2.0%→29% · +3.0%→12% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.77% (p90 4.75%) · excursion haute méd. +1.14% / basse méd. −1.05%
- Profil de vol intra : ouverture 1.671% vs midi 0.524% vs clôture 0.714% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 44% · recovery-V 14%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.05)_ ; drift intra méd. -0.46% ; recovery-V 11%
- **σ réalisé intraday** 1.965% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 72% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 134.1675 (VA 133.4875–134.4225 ; dernier close 133.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 26% · rebond 31% · **stop −2.1%** sous le fill (sous le bruit) · cible +0.53% · R/R 0.25 (high win-rate)
- Gaps overnight (n=159) : méd. 0.37% · baisse 26% (gap-down >1% 3% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.43% (p90 −1.74%) · haut méd +0.25% · range méd 0.93%
- Excursion ouverture 15min (n=160) : bas méd −0.51% (p90 −1.98%) · haut méd +0.43% · range méd 1.23%
- Excursion ouverture 30min (n=160) : bas méd −0.6% (p90 −2.09%) · haut méd +0.58% · range méd 1.39%
- Excursion ouverture 60min (n=160) : bas méd −0.76% (p90 −2.29%) · haut méd +0.62% · range méd 1.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 133.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 40% · séance 59% (90/159) · gap 10% · délai 3.2min · rebond 42% (39/90) (MFE +0.65%)
   - −1.0% : fill 30min 21% · séance 48% (71/159) · gap 3% · délai 52.9min · rebond 35% (28/71) (MFE +0.58%)
   - −1.5% : fill 30min 13% · séance 38% (55/159) · gap 0% · délai 62.3min · rebond 31% (20/55) (MFE +0.58%)
   - −2.0% : fill 30min 8% · séance 26% (39/159) · gap 0% · délai 111.9min · rebond 31% (15/39) (MFE +0.53%)
   - −3.0% : fill 30min 4% · séance 14% (23/159) · gap 0% · délai 268.3min · rebond 37% (10/23) (MFE +0.59%)
   - −4.0% : fill 30min 2% · séance 5% (10/159) · gap 0% · délai 161.7min · rebond 8% (3/10) (MFE +0.38%)
   - −5.0% : fill 30min 0% · séance 3% (4/159) · gap 0% · délai 260.4min · rebond 24% (2/4) (MFE +0.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.0%) → stop au-delà de −0.82% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.82%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −0.91%) → stop au-delà de −0.74% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=329 jambes) : jambe baissière méd −1.05% (p90 −2.37%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 77% (17/22) · rebond 27% (6/17)
      · −2.0% : fill 61% (12/22) · rebond 12% (2/12)
      · −3.0% : fill 43% (9/22) · rebond 15% (3/9)
      · −4.0% : fill 26% (6/22) · rebond 4% (1/6)
      · −5.0% : fill 20% (3/22) · rebond 20% (1/3)
   - **flat** (37 séances) :
      · −1.0% : fill 58% (22/37) · rebond 28% (8/22)
      · −2.0% : fill 26% (12/37) · rebond 33% (5/12)
      · −3.0% : fill 17% (8/37) · rebond 32% (3/8)
      · −4.0% : fill 6% (3/37) · rebond 8% (1/3)
      · −5.0% : fill 0% (1/37) · rebond 100% (1/1)
   - **gap-up** (100 séances) :
      · −1.0% : fill 37% (32/100) · rebond 44% (14/32)
      · −2.0% : fill 19% (15/100) · rebond 45% (8/15)
      · −3.0% : fill 6% (6/100) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/100) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/100) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 64% si les 15 1res min sont vertes (84 cas) · 22% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **20min** → P(séance verte=clôture>ouverture) 67% si début vert vs 24% si rouge (base 44% · écart 43 pts) ; prédictivité sature ensuite (plafond brut 247min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **67%** · continue >prix actuel 55% ; creux résiduel méd -0.98% (q20 -1.95%) → **SL/trailing à −1.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.09% / q75 +1.67% → **scale +1.09% / runner +1.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **24%** (continue à baisser 61%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.1%** (au-delà de la MAE q10 -3.1%), cible rebond +0.96% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.98% .. +1.65%] · haut q95 +2.02% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.68% .. +2.17%] · haut q95 +2.46% · bas q05 -3.24%
   - 2h (n=160) : retour [-3.4% .. +2.16%] · haut q95 +2.68% · bas q05 -3.73%
   - 4h (n=160) : retour [-2.92% .. +2.57%] · haut q95 +3.15% · bas q05 -3.81%
   - 6h (n=160) : retour [-3.68% .. +3.42%] · haut q95 +3.56% · bas q05 -4.15%
   - session (n=160) : retour [-3.44% .. +2.76%] · haut q95 +3.97% · bas q05 -4.66%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.43 · part idiosyncratique 0.56
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.0  _(momentum baissier)_
- **ADX** : 11.1  _(pas de tendance nette)_
- **MACD** : hist -0.707  _(bearish_recent)_
- **BB** : %B 0.11 · largeur 10.2%
- **ATR** : 4.41 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.234  _(distribution)_
- **Vol ratio** : 1.27  _(volume normal)_
- **Choppiness** : 54.4  _(transition)_
- **MA** : MA20 137.34 · MA50 137.2 · MA200 135.34  _(prix < MA20)_
- **Dist MA** : MA20 -4.0% · MA50 -3.9% · MA200 -2.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (837754 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
