# SOFI

**Generated** : 2026-08-31T00:35:12.944337+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $18.06  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $18.06 (+6.4% vs entrée) · entrée $16.98 · stop $15.85 · T1 $19.25 · R/R 2.01  
> ↳ P(T1 av. stop) 15 % · EV/risk -0.031 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.83–$17.14 (mid $16.98)
- Spot actuel : $18.06 (+6.4% au-dessus de la zone — repli à attendre)
- Stop : $15.85 (stop swing_plan-based (-12.22%))
- Targets : T1 $19.25 · R/R 2.01 | T2 $19.28 · R/R 2.04 | T3 $19.32 · R/R 2.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.85


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.98 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.22 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1254).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.22 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.267 % | p01 -6.517 % | pire -11.105 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3213** [0.2551 ; 0.3934] _(largeur 13.8 pt, n_eff 173.1)_
   - swing : **0.3577** [0.3085 ; 0.4092] _(largeur 10.1 pt, n_eff 345.7)_
   - deep : **0.396** [0.3455 ; 0.4482] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.4 observations effectives », dont la borne haute a 95 % vaut environ 20.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (41.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-5.98 %** | CVaR **-8.48 %** | vol 3.87 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 6.22 % contre 3.51 % aujourd'hui, rapport 1.77)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.022 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8269** (β de hausse 1.7089, asymétrie 1.0691) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.297× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 16.3386 sur atr_grid (2.0 ATR, 9.532 %) — p(stop avant cible) 0.3794 [0.33 ; 0.43], R/R 3.85, perte reelle 10.246 % (gap inclus), CVaR 9.534 %, EV -0.518 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.69 ATR (stop 5.823 %) — p(stop avant cible) 0.5806 [0.53 ; 0.63], R/R 5.169, perte reelle 7.631 % (gap inclus), EV -0.9955 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.581, borne haute 0.632 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 0.1 % x 39.45 % + P(rien) 41.8 % x 8.12 % ne couvrent pas P(stop) 58.1 % x 7.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 7.149 %) — p(stop avant cible) 0.4809 [0.43 ; 0.53], R/R 4.39, perte reelle 8.985 % (gap inclus), EV -0.8431 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.84 %) : P(cible) 0.1 % x 39.45 % + P(rien) 51.8 % x 6.64 % ne couvrent pas P(stop) 48.1 % x 8.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.37 ATR (stop 13.862 %) — p(stop avant cible) 0.1687 [0.13 ; 0.21], R/R 2.846, perte reelle 13.862 % (gap inclus), EV 0.3671 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.86 % > budget 12.00 %
   - 🟢 support a 3.69 ATR (stop 20.153 %) — p(stop avant cible) 0.0507 [0.03 ; 0.08], R/R 1.957, perte reelle 20.153 % (gap inclus), EV 0.5123 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.15 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.191 %) — p(stop avant cible) 0.9197 [0.89 ; 0.94], R/R 14.702, perte reelle 2.683 % (gap inclus), EV -1.3888 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 14.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.920, borne haute 0.945 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.39 %) : P(cible) 0.0 % x 39.45 % + P(rien) 8.0 % x 13.37 % ne couvrent pas P(stop) 92.0 % x 2.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.69 ATR (stop 4.708 %) — p(stop avant cible) 0.6515 [0.60 ; 0.70], R/R 5.584, perte reelle 7.064 % (gap inclus), EV -1.4861 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.651, borne haute 0.700 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.49 %) : P(cible) 0.1 % x 39.45 % + P(rien) 34.8 % x 8.86 % ne couvrent pas P(stop) 65.1 % x 7.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.34 %) — p(stop avant cible) 0.4125 [0.36 ; 0.46], R/R 4.064, perte reelle 9.707 % (gap inclus), EV -0.5539 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 0.1 % x 39.45 % + P(rien) 58.7 % x 5.82 % ne couvrent pas P(stop) 41.2 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.532 %) — p(stop avant cible) 0.3794 [0.33 ; 0.43], R/R 3.85, perte reelle 10.246 % (gap inclus), EV -0.518 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 0.1 % x 39.45 % + P(rien) 62.0 % x 5.37 % ne couvrent pas P(stop) 37.9 % x 10.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.37 ATR (stop 12.746 %) — p(stop avant cible) 0.2326 [0.19 ; 0.28], R/R 3.095, perte reelle 12.746 % (gap inclus), EV 0.0982 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.75 % > budget 12.00 %
   - 🟢 grid_snapped a 3.69 ATR (stop 19.038 %) — p(stop avant cible) 0.0631 [0.04 ; 0.09], R/R 2.072, perte reelle 19.038 % (gap inclus), EV 0.5197 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.04 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 21.446 %) — p(stop avant cible) 0.0372 [0.02 ; 0.06], R/R 1.839, perte reelle 21.446 % (gap inclus), EV 0.493 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.45 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 23.829 %) — p(stop avant cible) 0.0258 [0.01 ; 0.05], R/R 1.655, perte reelle 23.829 % (gap inclus), EV 0.4893 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.83 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 26.212 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 1.505, perte reelle 26.212 % (gap inclus), EV 0.6211 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.21 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 28.595 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 1.379, perte reelle 28.595 % (gap inclus), EV 0.6313 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.60 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 30.978 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.273, perte reelle 30.978 % (gap inclus), EV 0.6271 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.98 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 33.361 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 1.182, perte reelle 33.361 % (gap inclus), EV 0.6405 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.36 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 35.744 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 1.104, perte reelle 35.744 % (gap inclus), EV 0.6399 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.74 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 38.127 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.035, perte reelle 38.127 % (gap inclus), EV 0.6489 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.13 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 18.06, ATR14 0.8607 (4.766 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.375 ATR = 1.787 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.238 % | 18.017 | 92.86 % | 95.77 % | 96.98 % | 97.37 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.477 % | 17.9739 | 85.11 % | 89.53 % | 91.94 % | 93.23 % | 95.53 % | 97.23 % |
| 0.15 ATR | 0.715 % | 17.9309 | 79.07 % | 84.99 % | 88.21 % | 90.4 % | 92.79 % | 94.87 % |
| 0.2 ATR | 0.953 % | 17.8879 | 71.53 % | 79.76 % | 83.57 % | 86.87 % | 90.46 % | 93.33 % |
| 0.25 ATR | 1.191 % | 17.8448 | 66.3 % | 75.23 % | 80.14 % | 84.14 % | 88.83 % | 91.9 % |
| 0.35 ATR | 1.668 % | 17.7587 | 52.52 % | 65.46 % | 72.18 % | 78.28 % | 85.28 % | 88.62 % |
| 0.5 ATR | 2.383 % | 17.6296 | 37.63 % | 53.37 % | 61.59 % | 68.99 % | 79.29 % | 84.41 % |
| 0.75 ATR | 3.574 % | 17.4145 | 20.12 % | 36.66 % | 46.77 % | 56.77 % | 69.75 % | 77.54 % |
| 1.0 ATR | 4.766 % | 17.1993 | 8.75 % | 24.27 % | 33.67 % | 44.95 % | 59.39 % | 68.82 % |
| 1.25 ATR | 5.957 % | 16.9841 | 4.02 % | 14.9 % | 23.59 % | 35.45 % | 50.15 % | 62.15 % |
| 1.5 ATR | 7.149 % | 16.7689 | 2.01 % | 9.47 % | 16.63 % | 27.47 % | 42.13 % | 55.59 % |
| 2.0 ATR | 9.532 % | 16.3386 | 0.7 % | 4.33 % | 8.27 % | 15.25 % | 29.34 % | 45.33 % |
| 2.5 ATR | 11.915 % | 15.9082 | 0.3 % | 1.91 % | 3.73 % | 9.39 % | 20.0 % | 36.0 % |
| 3.0 ATR | 14.298 % | 15.4779 | 0.1 % | 0.91 % | 2.82 % | 6.06 % | 14.31 % | 28.62 % |
| 4.0 ATR | 19.063 % | 14.6171 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.51 % | 14.87 % |
| 6.0 ATR | 28.595 % | 12.8957 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.75 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.11 ATR | 1.48 ATR | 1.94 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.78 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.90 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.89 ATR | 1.00 ATR | 1.33 ATR | 1.60 ATR | 1.81 ATR | 2.45 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.25 ATR | 1.41 ATR | 1.86 ATR | 2.23 ATR | 2.50 ATR | 3.63 ATR | 4.76 ATR |
| **20 s.** | 0.82 ATR | 1.77 ATR | 2.02 ATR | 2.70 ATR | 3.26 ATR | 3.63 ATR | 4.83 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.426–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.383 %, prix 17.6296), p(touche) 37.63 % (en stress 83.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.625–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.574 %, prix 17.4145), p(touche) 36.66 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.784–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.766 %, prix 17.1993), p(touche) 33.67 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.999–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.766 %, prix 17.1993), p(touche) 44.95 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.411–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.149 %, prix 16.7689), p(touche) 42.13 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.018–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (11.915 %, prix 15.9082), p(touche) 36.0 % (en stress 98.98 %)  ✅ optimum identifie (70.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.094 | EV/share : $-0.106 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 9 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 68.2 | bear 13.8 | side 18.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 271.0 (= 15 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.712% → cible +5.732% / stop −2.866%, p_fill 35%, n_eff≈14.4) : P(cible|rempli) **0%** · **EV/risk -0.057** (×p_fill ; si rempli -0.47% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→70% · +2.0%→50% · +3.0%→38% · +5.0%→12% · +8.0%→1%
- Range intraday médian 4.41% (p90 7.54%) · excursion haute méd. +2.04% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.049% vs midi 0.872% vs clôture 0.992% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑2%/↓0% ; spike-down 63% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.151 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.174% ; recovery-V 23%
- **σ réalisé intraday** 2.707% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 60% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 18.1206 (VA 18.0481–18.7369 ; dernier close 18.05)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 67% · **stop −2.97%** sous le fill (sous le bruit) · cible +1.82% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 42% (gap-down >1% 21% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −1.79%) · haut méd +0.71% · range méd 1.66%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.85%) · haut méd +0.99% · range méd 2.31%
- Excursion ouverture 30min (n=160) : bas méd −1.15% (p90 −3.2%) · haut méd +1.16% · range méd 2.68%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.73%) · haut méd +1.43% · range méd 3.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.06 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (120/159) · gap 28% · délai 0.1min · rebond 54% (65/120) (MFE +1.26%)
   - −1.0% : fill 30min 52% · séance 65% (109/159) · gap 21% · délai 1.5min · rebond 58% (65/109) (MFE +1.19%)
   - −1.5% : fill 30min 40% · séance 60% (100/159) · gap 17% · délai 11.2min · rebond 68% (68/100) (MFE +1.47%)
   - −2.0% : fill 30min 32% · séance 46% (79/159) · gap 10% · délai 9.8min · rebond 67% (55/79) (MFE +1.82%)
   - −3.0% : fill 30min 13% · séance 34% (57/159) · gap 3% · délai 48.4min · rebond 58% (38/57) (MFE +1.13%)
   - −4.0% : fill 30min 8% · séance 17% (35/159) · gap 2% · délai 39.2min · rebond 57% (23/35) (MFE +1.36%)
   - −5.0% : fill 30min 3% · séance 9% (19/159) · gap 2% · délai 99.6min · rebond 32% (9/19) (MFE +0.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.98%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −2.07%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.45%) → stop au-delà de −1.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=668 jambes) : jambe baissière méd −1.08% (p90 −2.78%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (64/65) · rebond 60% (40/64)
      · −2.0% : fill 84% (54/65) · rebond 74% (39/54)
      · −3.0% : fill 68% (42/65) · rebond 62% (29/42)
      · −4.0% : fill 36% (27/65) · rebond 70% (20/27)
      · −5.0% : fill 19% (15/65) · rebond 40% (8/15)
   - **flat** (22 séances) :
      · −1.0% : fill 67% (13/22) · rebond 42% (6/13)
      · −2.0% : fill 45% (8/22) · rebond 56% (5/8)
      · −3.0% : fill 35% (6/22) · rebond 38% (3/6)
      · −4.0% : fill 22% (3/22) · rebond 30% (1/3)
      · −5.0% : fill 13% (1/22) · rebond 0% (0/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 42% (32/72) · rebond 62% (19/32)
      · −2.0% : fill 21% (17/72) · rebond 58% (11/17)
      · −3.0% : fill 11% (9/72) · rebond 60% (6/9)
      · −4.0% : fill 3% (5/72) · rebond 22% (2/5)
      · −5.0% : fill 1% (3/72) · rebond 44% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 61% si les 15 1res min sont vertes (75 cas) · 23% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 74% si début vert vs 10% si rouge (base 41% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **74%** · continue >prix actuel 49% ; creux résiduel méd -1.54% (q20 -2.58%) → **SL/trailing à −2.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.78% / q75 +2.87% → **scale +1.78% / runner +2.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **10%** (continue à baisser 65%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.61%** (au-delà de la MAE q10 -3.61%), cible rebond +1.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.92% .. +3.76%] · haut q95 +4.04% · bas q05 -3.4%
   - 60min (n=160) : retour [-3.14% .. +3.78%] · haut q95 +4.56% · bas q05 -4.01%
   - 2h (n=160) : retour [-3.58% .. +3.98%] · haut q95 +5.33% · bas q05 -4.65%
   - 4h (n=160) : retour [-4.63% .. +4.61%] · haut q95 +5.68% · bas q05 -5.15%
   - 6h (n=160) : retour [-4.82% .. +4.08%] · haut q95 +5.71% · bas q05 -5.85%
   - session (n=160) : retour [-4.77% .. +5.11%] · haut q95 +5.71% · bas q05 -6.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 49.6  _(neutre)_
- **ADX** : 16.1  _(pas de tendance nette)_
- **MACD** : hist 0.025  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 8.8%
- **ATR** : 0.86 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.065  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 70.9  _(marche en range (choppy))_
- **MA** : MA20 18.34 · MA50 17.83 · MA200 20.25  _(prix < MA20)_
- **Dist MA** : MA20 -1.5% · MA50 +1.3% · MA200 -10.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (889225 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
