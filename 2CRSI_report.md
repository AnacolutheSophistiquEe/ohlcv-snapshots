# AL2SI

**Generated** : 2026-10-16T21:49:32.049018+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €26.24  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (10 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €26.24 (+0.7% vs entrée) · entrée €26.07 · stop €25.12 · T1 €27.98 · R/R 2.01  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-16 : 26.24 · ATR Wilder 1.99 (7.58 %)_
- **Swing** : plage **23.99 → 22.56** (-8.58 % a -14.03 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 22.6-23.55 (A). stop INDICATIF 19.11 (-15.3 % sous le bas ; sous le support 20.1-21.05 (- 0,5 ATR)).
- **Deep** : plage **22.56 → 19.11** (-14.03 % a -27.16 % sous la cloture, 1.73 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 20.1-21.05 (A). stop INDICATIF 17.12 (-10.4 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (2.36 ATR sous le plus haut 20 s., RSI(2) 19.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 25.0-25.32 (C, -3.51 %) ; 22.6-23.55 (A, -10.25 %) ; 20.1-21.05 (A, -19.78 %) ; 16.1-16.65 (A, -36.55 %) ; 14.2-15.0 (A, -42.84 %) ; 13.0-13.24 (B, -49.54 %)
- Resistances reelles au-dessus : 28.18-29.0 (B, 7.39 %) ; 30.0-30.94 (A, 14.33 %) ; 31.38-31.54 (B, 19.59 %) ; 33.02-33.02 (C, 25.84 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.52 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.03 %)** : le gap seul le franchit 0.703 % des séances (9 fois sur 1280).
   - exécution **6.256 pt plus bas** dans le cas TYPIQUE (médiane), 20.326 au p90, **29.087 au pire**
   - perte réelle **18.187 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 9.03 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0644 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.366 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4413** [0.3688 ; 0.5157] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4041** [0.3534 ; 0.4564] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3142** [0.267 ; 0.3645] _(largeur 9.8 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.41 %** | CVaR **-12.97 %** | vol 6.52 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 4.21 % contre 7.23 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -14.08 % si l'on extrapolait par √5 _(rapport 1.048 ; < 1 = le √5 surestime)_
- **β de baisse : 1.208** (β de hausse 0.9482, asymétrie 1.274) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.09× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 24.3585 sur support (0.62 ATR, 7.17 %) — p(stop avant cible) 0.5884 [0.54 ; 0.64], R/R 3.143, perte reelle 7.91 % (gap inclus), CVaR 15.875 %, EV 1.2283 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4854 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 15.87 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.62 ATR (stop 7.17 %) — p(stop avant cible) 0.5884 [0.54 ; 0.64], R/R 3.143, perte reelle 7.91 % (gap inclus), EV 1.2283 % — **REFUSE**
      - refuse : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 15.87 % > budget 12.00 %
      - ⚠ support DETECTE a 0.34 ATR du spot — compartiment <1, mesure a 49.8 % de casse (IC clusterise [0.466 ; 0.530] sur 1220 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 11.425 %) — p(stop avant cible) 0.3389 [0.29 ; 0.39], R/R 1.912, perte reelle 13.007 % (gap inclus), EV 2.5128 % — **REFUSE**
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.15 % > budget 12.00 %
   - 🟢 support a 1.82 ATR (stop 16.317 %) — p(stop avant cible) 0.232 [0.19 ; 0.28], R/R 1.247, perte reelle 19.942 % (gap inclus), EV 1.9649 % — **REFUSE**
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.96 % > budget 12.00 %
   - 🟢 support a 3.07 ATR (stop 25.844 %) — p(stop avant cible) 0.0898 [0.06 ; 0.12], R/R 0.752, perte reelle 33.051 % (gap inclus), EV 2.2678 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.79 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.904 %) — p(stop avant cible) 0.8685 [0.83 ; 0.90], R/R 11.842, perte reelle 2.1 % (gap inclus), EV 0.57 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 11.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.869, borne haute 0.901 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 9.521 %) — p(stop avant cible) 0.4435 [0.39 ; 0.50], R/R 2.29, perte reelle 10.86 % (gap inclus), EV 1.8653 % — **REFUSE**
      - refuse : R/R 2.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.40 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 19.041 %) — p(stop avant cible) 0.1798 [0.14 ; 0.22], R/R 1.007, perte reelle 24.681 % (gap inclus), EV 1.8128 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.74 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 20.945 %) — p(stop avant cible) 0.1406 [0.11 ; 0.18], R/R 0.91, perte reelle 27.311 % (gap inclus), EV 2.0165 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.74 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 30.466 %) — p(stop avant cible) 0.0774 [0.05 ; 0.11], R/R 0.685, perte reelle 36.313 % (gap inclus), EV 2.1905 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.52 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 34.274 %) — p(stop avant cible) 0.0592 [0.04 ; 0.09], R/R 0.624, perte reelle 39.843 % (gap inclus), EV 2.2344 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 38.083 %) — p(stop avant cible) 0.0408 [0.02 ; 0.07], R/R 0.572, perte reelle 43.459 % (gap inclus), EV 2.6101 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.94 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 41.891 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 0.548, perte reelle 45.344 % (gap inclus), EV 2.8387 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.26 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 45.699 %) — p(stop avant cible) 0.0289 [0.01 ; 0.05], R/R 0.532, perte reelle 46.77 % (gap inclus), EV 2.8449 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.13 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 49.507 %) — p(stop avant cible) 0.0289 [0.01 ; 0.05], R/R 0.474, perte reelle 52.508 % (gap inclus), EV 2.6791 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.46 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 53.316 %) — p(stop avant cible) 0.0254 [0.01 ; 0.05], R/R 0.403, perte reelle 61.624 % (gap inclus), EV 2.4465 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.08 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 57.124 %) — p(stop avant cible) 0.0254 [0.01 ; 0.05], R/R 0.393, perte reelle 63.341 % (gap inclus), EV 2.4029 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.95 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 60.932 %) — p(stop avant cible) 0.0254 [0.01 ; 0.05], R/R 0.392, perte reelle 63.445 % (gap inclus), EV 2.4003 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.00 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 26.24, ATR14 1.9986 (7.617 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.401 ATR = 3.054 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.381 % | 26.1401 | 87.16 % | 90.68 % | 93.03 % | 94.49 % | 95.65 % | 97.2 % |
| 0.1 ATR | 0.762 % | 26.0401 | 82.65 % | 87.14 % | 90.37 % | 92.22 % | 94.16 % | 96.3 % |
| 0.15 ATR | 1.142 % | 25.9402 | 78.53 % | 83.51 % | 87.33 % | 89.07 % | 92.28 % | 95.2 % |
| 0.2 ATR | 1.523 % | 25.8403 | 72.84 % | 79.49 % | 83.6 % | 86.02 % | 89.91 % | 93.01 % |
| 0.25 ATR | 1.904 % | 25.7404 | 66.86 % | 74.88 % | 79.47 % | 82.68 % | 87.64 % | 91.41 % |
| 0.35 ATR | 2.666 % | 25.5405 | 54.8 % | 65.85 % | 71.22 % | 75.89 % | 82.79 % | 87.91 % |
| 0.5 ATR | 3.808 % | 25.2407 | 40.78 % | 53.97 % | 62.08 % | 69.0 % | 78.34 % | 85.51 % |
| 0.75 ATR | 5.712 % | 24.7411 | 22.75 % | 37.88 % | 47.64 % | 56.0 % | 67.56 % | 76.92 % |
| 1.0 ATR | 7.617 % | 24.2414 | 12.84 % | 25.12 % | 34.09 % | 44.59 % | 57.67 % | 68.63 % |
| 1.25 ATR | 9.521 % | 23.7418 | 7.45 % | 17.76 % | 24.85 % | 36.71 % | 50.74 % | 62.24 % |
| 1.5 ATR | 11.425 % | 23.2421 | 3.63 % | 11.38 % | 17.49 % | 29.13 % | 43.42 % | 55.84 % |
| 2.0 ATR | 15.233 % | 22.2429 | 0.88 % | 5.2 % | 9.72 % | 17.03 % | 31.75 % | 44.06 % |
| 2.5 ATR | 19.041 % | 21.2436 | 0.1 % | 2.16 % | 4.62 % | 9.84 % | 21.46 % | 33.77 % |
| 3.0 ATR | 22.85 % | 20.2443 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 15.23 % | 26.27 % |
| 4.0 ATR | 30.466 % | 18.2457 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.28 % |
| 6.0 ATR | 45.699 % | 14.2486 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.46 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.64 ATR | 0.85 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.98 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 0.99 ATR | 1.37 ATR | 1.67 ATR | 1.88 ATR | 2.49 ATR | 3.42 ATR |
| **10 s.** | 0.58 ATR | 1.27 ATR | 1.45 ATR | 1.95 ATR | 2.33 ATR | 2.62 ATR | 3.78 ATR | 5.11 ATR |
| **20 s.** | 0.81 ATR | 1.75 ATR | 1.96 ATR | 2.55 ATR | 3.14 ATR | 3.70 ATR | 5.57 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.455–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.808 %, prix 25.2408), p(touche) 40.78 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (91.8 % des re-echantillons)
- **2 seance(s)** : plage utile 0.639–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.712 %, prix 24.7412), p(touche) 37.88 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.799–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.617 %, prix 24.2413), p(touche) 34.09 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.991–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.617 %, prix 24.2413), p(touche) 44.59 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.446–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.425 %, prix 23.2421), p(touche) 43.42 % (en stress 97.06 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.96–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (15.233 %, prix 22.2429), p(touche) 44.06 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 21.0 | side 74.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.644% → cible +7.32% / stop −3.66%, p_fill 85%, n_eff≈90.9) : P(cible|rempli) **10%** · **EV/risk -0.256** (×p_fill ; si rempli -1.10% du capital)
  - **swing** (entrée dip −1.414% → cible +8.158% / stop −7.726%, p_fill 81%, n_eff≈94.4) : P(cible|rempli) **41%** · **EV/risk -0.058** (×p_fill ; si rempli -0.55% du capital)
  - **deep** (entrée dip −2.186% → cible +13.354% / stop −11.68%, p_fill 77%, n_eff≈85.9) : P(cible|rempli) **35%** · **EV/risk -0.017** (×p_fill ; si rempli -0.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→75% · +2.0%→68% · +3.0%→53% · +5.0%→35% · +8.0%→17%
- Range intraday médian 6.98% (p90 14.96%) · excursion haute méd. +3.32% / basse méd. −3.45%
- Profil de vol intra : ouverture 4.807% vs midi 1.539% vs clôture 1.704% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 5% · trend ↑1%/↓0% ; spike-down 74% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. -0.405% ; recovery-V 23%
- **σ réalisé intraday** 4.412% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 70% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 25.8615 (VA 25.2245–26.7435 ; dernier close 26.98)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 88% · **stop −3.68%** sous le fill (sous le bruit) · cible +2.19% · R/R 0.6 (high win-rate)
- Gaps overnight (n=158) : méd. 0.23% · baisse 41% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −3.41%) · haut méd +0.73% · range méd 2.23%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −4.07%) · haut méd +1.39% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −4.39%) · haut méd +1.93% · range méd 3.45%
- Excursion ouverture 60min (n=160) : bas méd −1.52% (p90 −5.59%) · haut méd +2.05% · range méd 3.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.82 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 80% (123/158) · gap 20% · délai 0.3min · rebond 62% (81/123) (MFE +1.87%)
   - −1.0% : fill 30min 50% · séance 75% (118/158) · gap 10% · délai 3.3min · rebond 60% (78/118) (MFE +1.56%)
   - −1.5% : fill 30min 43% · séance 69% (105/158) · gap 7% · délai 9.0min · rebond 58% (65/105) (MFE +1.52%)
   - −2.0% : fill 30min 36% · séance 63% (97/158) · gap 4% · délai 16.0min · rebond 54% (58/97) (MFE +1.11%)
   - −3.0% : fill 30min 19% · séance 46% (79/158) · gap 2% · délai 42.4min · rebond 58% (53/79) (MFE +1.4%)
   - −4.0% : fill 30min 13% · séance 39% (68/158) · gap 1% · délai 88.4min · rebond 73% (54/68) (MFE +1.57%)
   - −5.0% : fill 30min 9% · séance 28% (53/158) · gap 1% · délai 89.9min · rebond 88% (49/53) (MFE +2.19%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −3.05%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.84%) → stop au-delà de −1.98% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −3.92%) → stop au-delà de −2.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1483 jambes) : jambe baissière méd −1.21% (p90 −2.97%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 91% (45/47) · rebond 54% (26/45)
      · −2.0% : fill 84% (41/47) · rebond 49% (22/41)
      · −3.0% : fill 69% (37/47) · rebond 50% (25/37)
      · −4.0% : fill 61% (33/47) · rebond 58% (24/33)
      · −5.0% : fill 44% (27/47) · rebond 86% (24/27)
   - **flat** (34 séances) :
      · −1.0% : fill 78% (26/34) · rebond 66% (18/26)
      · −2.0% : fill 58% (20/34) · rebond 49% (12/20)
      · −3.0% : fill 43% (16/34) · rebond 60% (10/16)
      · −4.0% : fill 40% (15/34) · rebond 77% (12/15)
      · −5.0% : fill 32% (11/34) · rebond 80% (10/11)
   - **gap-up** (77 séances) :
      · −1.0% : fill 64% (47/77) · rebond 60% (34/47)
      · −2.0% : fill 54% (36/77) · rebond 62% (24/36)
      · −3.0% : fill 34% (26/77) · rebond 67% (18/26)
      · −4.0% : fill 26% (20/77) · rebond 88% (18/20)
      · −5.0% : fill 16% (15/77) · rebond 100% (15/15)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 56% si les 15 1res min sont vertes (76 cas) · 26% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:53** → P(séance verte=clôture>ouverture) 74% si début vert vs 14% si rouge (base 41% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **74%** · continue >prix actuel 50% ; creux résiduel méd -2.8% (q20 -5.42%) → **SL/trailing à −5.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.86% / q75 +3.31% → **scale +1.86% / runner +3.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **14%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.93%** (au-delà de la MAE q10 -4.93%), cible rebond +1.4% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.2% .. +5.28%] · haut q95 +6.81% · bas q05 -5.69%
   - 60min (n=160) : retour [-5.33% .. +4.89%] · haut q95 +7.28% · bas q05 -6.85%
   - 2h (n=160) : retour [-5.2% .. +7.14%] · haut q95 +8.79% · bas q05 -7.39%
   - 4h (n=160) : retour [-6.3% .. +7.38%] · haut q95 +9.96% · bas q05 -8.17%
   - 6h (n=160) : retour [-5.99% .. +8.19%] · haut q95 +11.34% · bas q05 -8.55%
   - session (n=160) : retour [-7.17% .. +9.91%] · haut q95 +12.5% · bas q05 -9.62%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.13 · part idiosyncratique 0.87
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 41.3  _(momentum baissier)_
- **ADX** : 14.3  _(pas de tendance nette)_
- **MACD** : hist -0.029  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 26.8%
- **ATR** : 2.0 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.044  _(neutre)_
- **Vol ratio** : 0.5  _(volume atone)_
- **Choppiness** : 50.9  _(transition)_
- **MA** : MA20 27.62 · MA50 27.62 · MA200 28.98  _(prix < MA20)_
- **Dist MA** : MA20 -5.0% · MA50 -5.0% · MA200 -9.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (770490 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
