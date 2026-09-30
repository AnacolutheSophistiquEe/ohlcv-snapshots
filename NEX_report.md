# NEX

**Generated** : 2026-09-30T00:13:14.918774+00:00  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €133.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €133.40 (+1.1% vs entrée) · entrée €131.99 · stop €121.43 · T1 €133.82 · R/R 0.17  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -57 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €131.62–€132.35 (mid €131.99)
- Spot actuel : €133.40 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : €121.43 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 €133.82 · R/R 0.17 | T2 €135.65 · R/R 0.35 | T3 €137.47 · R/R 0.52
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €121.43


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.76 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **2.408 pt plus bas** dans le cas TYPIQUE (médiane), 3.214 au p90, **3.836 au pire**
   - perte réelle **8.124 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 5.76 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0111 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0035** [0.0002 ; 0.0223] _(largeur 2.2 pt, n_eff 173.1)_
   - swing : **0.3851** [0.3349 ; 0.4372] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3617** [0.3124 ; 0.4133] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 59.2 observations effectives », dont la borne haute a 95 % vaut environ 5.1 %.
- ⚠ **5 s — échantillon insuffisant sur : swing (25.3 pt), deep (28.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.52 %** | CVaR **-5.28 %** | vol 2.31 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.88 % si l'on extrapolait par √5 _(rapport 0.953 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0065** (β de hausse 1.0892, asymétrie 0.9241) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 124.6285 sur sr_based (1.34 ATR, 6.575 %) — p(stop avant cible) 0.3052 [0.26 ; 0.36], R/R 3.338, perte reelle 6.756 % (gap inclus), CVaR 7.681 %, EV 0.179 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9573 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.75 ATR (stop 4.554 %) — p(stop avant cible) 0.5038 [0.45 ; 0.56], R/R 4.761, perte reelle 4.737 % (gap inclus), EV -0.1022 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.504, borne haute 0.556 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.6 % x 22.55 % + P(rien) 49.0 % x 4.37 % ne couvrent pas P(stop) 50.4 % x 4.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 1.34 ATR (stop 6.575 %) — p(stop avant cible) 0.3052 [0.26 ; 0.36], R/R 3.338, perte reelle 6.756 % (gap inclus), EV 0.179 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - 🟢 support a 5.62 ATR (stop 21.238 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.989, perte reelle 22.803 % (gap inclus), EV 0.5972 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.53 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.857 %) — p(stop avant cible) 0.9134 [0.88 ; 0.94], R/R 25.261, perte reelle 0.893 % (gap inclus), EV -0.124 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 25.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.913, borne haute 0.940 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.3 % x 22.55 % + P(rien) 8.3 % x 7.43 % ne couvrent pas P(stop) 91.3 % x 0.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.75 ATR (stop 3.587 %) — p(stop avant cible) 0.6002 [0.55 ; 0.65], R/R 6.044, perte reelle 3.731 % (gap inclus), EV -0.1198 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 6.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.600, borne haute 0.651 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.6 % x 22.55 % + P(rien) 39.3 % x 5.02 % ne couvrent pas P(stop) 60.0 % x 3.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.34 ATR (stop 5.609 %) — p(stop avant cible) 0.3983 [0.35 ; 0.45], R/R 3.868, perte reelle 5.83 % (gap inclus), EV 0.012 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 7.71 %) — p(stop avant cible) 0.2113 [0.17 ; 0.26], R/R 2.849, perte reelle 7.915 % (gap inclus), EV 0.4451 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 8.567 %) — p(stop avant cible) 0.1793 [0.14 ; 0.22], R/R 2.589, perte reelle 8.712 % (gap inclus), EV 0.4288 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 9.424 %) — p(stop avant cible) 0.1401 [0.11 ; 0.18], R/R 2.354, perte reelle 9.581 % (gap inclus), EV 0.4877 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 10.281 %) — p(stop avant cible) 0.1089 [0.08 ; 0.14], R/R 2.157, perte reelle 10.455 % (gap inclus), EV 0.4947 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 11.994 %) — p(stop avant cible) 0.073 [0.05 ; 0.10], R/R 1.828, perte reelle 12.337 % (gap inclus), EV 0.4842 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.50 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 13.707 %) — p(stop avant cible) 0.0358 [0.02 ; 0.06], R/R 1.589, perte reelle 14.188 % (gap inclus), EV 0.4989 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.57 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 15.421 %) — p(stop avant cible) 0.0176 [0.01 ; 0.04], R/R 1.404, perte reelle 16.059 % (gap inclus), EV 0.5465 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.05 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.134 %) — p(stop avant cible) 0.0093 [0.00 ; 0.02], R/R 1.279, perte reelle 17.635 % (gap inclus), EV 0.555 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.99 % > budget 12.00 %
   - 🟢 grid_snapped a 5.62 ATR (stop 20.272 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 1.079, perte reelle 20.908 % (gap inclus), EV 0.594 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.58 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 22.275 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.974, perte reelle 23.151 % (gap inclus), EV 0.5965 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.55 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 23.988 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.907, perte reelle 24.876 % (gap inclus), EV 0.6028 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.41 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 25.701 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.877, perte reelle 25.701 % (gap inclus), EV 0.6022 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.42 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 27.415 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.823, perte reelle 27.415 % (gap inclus), EV 0.608 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.32 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 133.4, ATR14 4.5714 (3.427 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.347 ATR = 1.189 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.171 % | 133.1714 | 87.75 % | 91.36 % | 93.12 % | 95.08 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.343 % | 132.9429 | 81.86 % | 87.63 % | 90.28 % | 93.11 % | 95.55 % | 96.9 % |
| 0.15 ATR | 0.514 % | 132.7143 | 75.2 % | 83.42 % | 86.84 % | 90.16 % | 94.07 % | 95.6 % |
| 0.2 ATR | 0.685 % | 132.4857 | 68.63 % | 78.21 % | 83.1 % | 88.19 % | 92.68 % | 94.91 % |
| 0.25 ATR | 0.857 % | 132.2571 | 62.06 % | 73.5 % | 79.08 % | 85.04 % | 90.6 % | 93.71 % |
| 0.35 ATR | 1.199 % | 131.8 | 49.61 % | 64.18 % | 71.61 % | 78.74 % | 86.55 % | 91.51 % |
| 0.5 ATR | 1.713 % | 131.1143 | 34.41 % | 52.31 % | 61.1 % | 70.47 % | 80.22 % | 87.31 % |
| 0.75 ATR | 2.57 % | 129.9714 | 20.29 % | 36.31 % | 47.15 % | 58.46 % | 70.13 % | 80.72 % |
| 1.0 ATR | 3.427 % | 128.8286 | 10.59 % | 24.14 % | 34.58 % | 48.23 % | 61.52 % | 74.03 % |
| 1.25 ATR | 4.284 % | 127.6857 | 4.8 % | 16.0 % | 24.85 % | 39.27 % | 54.4 % | 67.63 % |
| 1.5 ATR | 5.14 % | 126.5429 | 2.45 % | 11.19 % | 18.66 % | 30.61 % | 46.88 % | 60.14 % |
| 2.0 ATR | 6.854 % | 124.2571 | 0.88 % | 5.3 % | 10.02 % | 19.39 % | 35.11 % | 50.65 % |
| 2.5 ATR | 8.567 % | 121.9714 | 0.49 % | 2.65 % | 5.6 % | 11.42 % | 24.43 % | 38.86 % |
| 3.0 ATR | 10.281 % | 119.6857 | 0.2 % | 1.67 % | 3.24 % | 7.09 % | 17.51 % | 30.37 % |
| 4.0 ATR | 13.707 % | 115.1143 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.52 % | 17.88 % |
| 6.0 ATR | 20.561 % | 105.9714 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.29 % | 4.3 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.02 ATR | 1.24 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.60 ATR | 2.06 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.25 ATR | 1.45 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.09 ATR | 1.43 ATR | 1.75 ATR | 1.97 ATR | 2.66 ATR | 3.40 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.10 ATR | 2.47 ATR | 2.82 ATR | 3.75 ATR | 4.81 ATR |
| **20 s.** | 0.96 ATR | 2.03 ATR | 2.24 ATR | 2.85 ATR | 3.43 ATR | 3.83 ATR | 5.16 ATR | 5.90 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.395–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (76.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.614–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.57 %, prix 129.9716), p(touche) 36.31 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.793–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.427 %, prix 128.8284), p(touche) 34.58 % (en stress 84.31 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.09–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.284 %, prix 127.6851), p(touche) 39.27 % (en stress 93.14 %)  ✅ optimum identifie (60.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.58–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.854 %, prix 124.2568), p(touche) 35.11 % (en stress 98.04 %)  ✅ optimum identifie (70.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.24–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.567 %, prix 121.9716), p(touche) 38.86 % (en stress 98.02 %)  ✅ optimum identifie (68.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.063 | EV/share : €-0.665 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 16 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 52.3 | bear 10.5 | side 37.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.054% → cible +1.386% / stop −8.0%, p_fill 57%, n_eff≈59.2) : P(cible|rempli) **29%** · **EV/risk -0.042** (×p_fill ; si rempli -0.59% du capital)
  - **swing** (entrée dip −2.333% → cible +3.099% / stop −3.509%, p_fill 50%, n_eff≈57.0) : P(cible|rempli) **45%** · **EV/risk -0.038** (×p_fill ; si rempli -0.27% du capital)
  - **deep** (entrée dip −3.6% → cible +4.383% / stop −5.332%, p_fill 40%, n_eff≈43.8) : P(cible|rempli) **47%** · **EV/risk -0.018** (×p_fill ; si rempli -0.24% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→56% · +2.0%→30% · +3.0%→11% · +5.0%→3% · +8.0%→1%
- Range intraday médian 2.85% (p90 4.75%) · excursion haute méd. +1.1% / basse méd. −1.33%
- Profil de vol intra : ouverture 1.712% vs midi 0.55% vs clôture 0.731% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. -0.539% ; recovery-V 11%
- **σ réalisé intraday** 1.962% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 67% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 138.1975 (VA 137.3925–138.7725 ; dernier close 136.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 27% · rebond 42% · **stop −1.95%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. 0.42% · baisse 27% (gap-down >1% 2% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.56% (p90 −1.77%) · haut méd +0.15% · range méd 1.04%
- Excursion ouverture 15min (n=160) : bas méd −0.78% (p90 −1.95%) · haut méd +0.36% · range méd 1.3%
- Excursion ouverture 30min (n=160) : bas méd −0.84% (p90 −2.22%) · haut méd +0.45% · range méd 1.41%
- Excursion ouverture 60min (n=160) : bas méd −0.87% (p90 −2.47%) · haut méd +0.57% · range méd 1.6%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 136.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 42% · séance 58% (83/159) · gap 7% · délai 4.1min · rebond 44% (38/83) (MFE +0.7%)
   - −1.0% : fill 30min 24% · séance 50% (67/159) · gap 2% · délai 31.3min · rebond 41% (30/67) (MFE +0.64%)
   - −1.5% : fill 30min 13% · séance 40% (51/159) · gap 0% · délai 52.6min · rebond 34% (20/51) (MFE +0.63%)
   - −2.0% : fill 30min 8% · séance 27% (36/159) · gap 0% · délai 67.3min · rebond 42% (16/36) (MFE +0.74%)
   - −3.0% : fill 30min 3% · séance 15% (21/159) · gap 0% · délai 237.7min · rebond 48% (10/21) (MFE +0.9%)
   - −4.0% : fill 30min 0% · séance 5% (9/159) · gap 0% · délai 347.8min · rebond 11% (3/9) (MFE +0.48%)
   - −5.0% : fill 30min 0% · séance 2% (3/159) · gap 0% · délai 409.9min · rebond 51% (2/3) (MFE +0.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.28%) → stop au-delà de −0.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.91%) → stop au-delà de −0.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.53%) → stop au-delà de −0.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=332 jambes) : jambe baissière méd −1.07% (p90 −2.32%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (19 séances) :
      · −1.0% : fill 77% (15/19) · rebond 49% (7/15)
      · −2.0% : fill 47% (9/19) · rebond 28% (2/9)
      · −3.0% : fill 34% (7/19) · rebond 34% (3/7)
      · −4.0% : fill 27% (5/19) · rebond 7% (1/5)
      · −5.0% : fill 15% (2/19) · rebond 46% (1/2)
   - **flat** (34 séances) :
      · −1.0% : fill 55% (20/34) · rebond 35% (8/20)
      · −2.0% : fill 32% (12/34) · rebond 33% (5/12)
      · −3.0% : fill 21% (8/34) · rebond 32% (3/8)
      · −4.0% : fill 7% (3/34) · rebond 8% (1/3)
      · −5.0% : fill 1% (1/34) · rebond 100% (1/1)
   - **gap-up** (106 séances) :
      · −1.0% : fill 42% (32/106) · rebond 43% (15/32)
      · −2.0% : fill 21% (15/106) · rebond 55% (9/15)
      · −3.0% : fill 8% (6/106) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/106) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/106) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 70% si les 15 1res min sont vertes (83 cas) · 16% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **30min** → P(séance verte=clôture>ouverture) 77% si début vert vs 18% si rouge (base 43% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 221min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **77%** · continue >prix actuel 50% ; creux résiduel méd -0.99% (q20 -1.9%) → **SL/trailing à −1.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.05% / q75 +1.75% → **scale +1.05% / runner +1.75%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **18%** (continue à baisser 59%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.19%** (au-delà de la MAE q10 -3.19%), cible rebond +0.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.88% .. +1.8%] · haut q95 +2.5% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.78% .. +2.32%] · haut q95 +2.58% · bas q05 -3.21%
   - 2h (n=160) : retour [-3.19% .. +2.37%] · haut q95 +2.93% · bas q05 -3.68%
   - 4h (n=160) : retour [-2.91% .. +2.98%] · haut q95 +3.12% · bas q05 -3.78%
   - 6h (n=160) : retour [-3.49% .. +3.57%] · haut q95 +3.84% · bas q05 -4.14%
   - session (n=160) : retour [-3.39% .. +2.8%] · haut q95 +3.88% · bas q05 -4.65%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.42 · part idiosyncratique 0.58
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.6  _(momentum baissier)_
- **ADX** : 10.8  _(pas de tendance nette)_
- **MACD** : hist -0.542  _(bearish_recent)_
- **BB** : %B 0.17 · largeur 9.4%
- **ATR** : 4.57 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.171  _(distribution)_
- **Vol ratio** : 0.44  _(volume atone)_
- **Choppiness** : 55.7  _(transition)_
- **MA** : MA20 137.64 · MA50 137.25 · MA200 135.29  _(prix < MA20)_
- **Dist MA** : MA20 -3.1% · MA50 -2.8% · MA200 -1.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (835917 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
