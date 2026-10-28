# AL2SI

**Generated** : 2026-10-28T21:51:22.060636+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.52  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €27.52 (+1.9% vs entrée) · entrée €27.02 · stop €26.16 · T1 €28.75 · R/R 2.01  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-28 : 27.52 · ATR Wilder 1.78 (6.47 %)_
- **Swing** : plage **25.49 → 24.22** (-7.38 % a -11.98 % sous la cloture, 0.71 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 25.0-25.4 (A). stop INDICATIF 21.71 (-10.38 % sous le bas ; sous le support 22.6-23.38 (- 0,5 ATR)).
- **Deep** : plage **24.22 → 21.11** (-11.98 % a -23.3 % sous la cloture, 1.75 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 22.6-23.38 (A). stop INDICATIF 19.21 (-8.99 % sous le bas ; sous le support 20.1-20.8 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.53 ATR sous le plus haut 20 s., RSI(2) 48.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 26.38-26.7 (B, -2.98 %) ; 25.0-25.4 (A, -7.7 %) ; 22.6-23.38 (A, -15.04 %) ; 20.1-20.8 (B, -24.42 %) ; 16.1-16.65 (A, -39.5 %) ; 14.2-15.0 (A, -45.49 %)
- Resistances reelles au-dessus : 28.18-29.04 (A, 2.4 %) ; 30.0-30.8 (A, 9.01 %) ; 30.94-31.54 (B, 12.43 %) ; 33.02-33.02 (C, 19.99 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.52 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.16 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **10.226 pt plus bas** dans le cas TYPIQUE (médiane), 21.481 au p90, **26.957 au pire**
   - perte réelle **22.515 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 11.16 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0532 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.401 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.468** [0.3947 ; 0.5423] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.403** [0.3523 ; 0.4553] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3301** [0.2821 ; 0.3809] _(largeur 9.9 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.0 pt), deep (25.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.3 %** | CVaR **-11.71 %** | vol 6.31 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 4.35 % contre 7.24 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -14.08 % si l'on extrapolait par √5 _(rapport 1.048 ; < 1 = le √5 surestime)_
- **β de baisse : 1.199** (β de hausse 0.9528, asymétrie 1.2584) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.105× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 26.5332 sur atr_grid (0.5 ATR, 3.586 %) — p(stop avant cible) 0.7639 [0.72 ; 0.81], R/R 5.351, perte reelle 3.833 % (gap inclus), CVaR 7.362 %, EV 0.7508 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.016 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.764, borne haute 0.806 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 7.36 % > budget 4.75 %
- Budget de queue : **4.75 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.17 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 21.7 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.28 ATR (stop 11.71 %) — p(stop avant cible) 0.3354 [0.29 ; 0.39], R/R 1.554, perte reelle 13.202 % (gap inclus), EV 1.9402 % — **REFUSE**
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.72 % > budget 4.75 %
   - 🟢 support a 2.49 ATR (stop 20.431 %) — p(stop avant cible) 0.1468 [0.11 ; 0.19], R/R 0.776, perte reelle 26.442 % (gap inclus), EV 1.5393 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.00 % > budget 4.75 %
   - 🟢 support a 3.76 ATR (stop 29.515 %) — p(stop avant cible) 0.0746 [0.05 ; 0.11], R/R 0.573, perte reelle 35.772 % (gap inclus), EV 1.8286 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.85 % > budget 4.75 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.793 %) — p(stop avant cible) 0.8737 [0.84 ; 0.91], R/R 10.531, perte reelle 1.948 % (gap inclus), EV 0.456 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 10.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.874, borne haute 0.906 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.586 %) — p(stop avant cible) 0.7639 [0.72 ; 0.81], R/R 5.351, perte reelle 3.833 % (gap inclus), EV 0.7508 % — **REFUSE**
      - refuse : p_stop_first 0.764, borne haute 0.806 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 7.36 % > budget 4.75 %
   - ⚪ atr_grid a 0.75 ATR (stop 5.379 %) — p(stop avant cible) 0.6841 [0.63 ; 0.73], R/R 3.566, perte reelle 5.752 % (gap inclus), EV 0.5865 % — **REFUSE**
      - refuse : p_stop_first 0.684, borne haute 0.731 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 10.48 % > budget 4.75 %
   - ⚪ atr_grid a 1.0 ATR (stop 7.171 %) — p(stop avant cible) 0.5834 [0.53 ; 0.63], R/R 2.599, perte reelle 7.892 % (gap inclus), EV 0.9548 % — **REFUSE**
      - refuse : p_stop_first 0.583, borne haute 0.634 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.54 % > budget 4.75 %
   - ⚪ atr_grid a 2.0 ATR (stop 14.343 %) — p(stop avant cible) 0.261 [0.22 ; 0.31], R/R 1.183, perte reelle 17.335 % (gap inclus), EV 1.7242 % — **REFUSE**
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.68 % > budget 4.75 %
   - ⚪ atr_grid a 3.0 ATR (stop 21.514 %) — p(stop avant cible) 0.1313 [0.10 ; 0.17], R/R 0.738, perte reelle 27.806 % (gap inclus), EV 1.6333 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.00 % > budget 4.75 %
   - ⚪ atr_grid a 3.5 ATR (stop 25.1 %) — p(stop avant cible) 0.0885 [0.06 ; 0.12], R/R 0.631, perte reelle 32.502 % (gap inclus), EV 1.8942 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.18 % > budget 4.75 %
   - ⚪ atr_grid a 4.5 ATR (stop 32.271 %) — p(stop avant cible) 0.0676 [0.04 ; 0.10], R/R 0.543, perte reelle 37.788 % (gap inclus), EV 1.8099 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.73 % > budget 4.75 %
   - ⚪ atr_grid a 5.0 ATR (stop 35.857 %) — p(stop avant cible) 0.0482 [0.03 ; 0.07], R/R 0.494, perte reelle 41.482 % (gap inclus), EV 2.0928 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.11 % > budget 4.75 %
   - ⚪ atr_grid a 5.5 ATR (stop 39.443 %) — p(stop avant cible) 0.035 [0.02 ; 0.06], R/R 0.462, perte reelle 44.353 % (gap inclus), EV 2.1894 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.30 % > budget 4.75 %
   - ⚪ atr_grid a 6.0 ATR (stop 43.028 %) — p(stop avant cible) 0.0276 [0.01 ; 0.05], R/R 0.446, perte reelle 45.967 % (gap inclus), EV 2.417 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.98 % > budget 4.75 %
   - ⚪ atr_grid a 6.5 ATR (stop 46.614 %) — p(stop avant cible) 0.0276 [0.01 ; 0.05], R/R 0.419, perte reelle 48.968 % (gap inclus), EV 2.3342 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.64 % > budget 4.75 %
   - ⚪ atr_grid a 7.0 ATR (stop 50.2 %) — p(stop avant cible) 0.0276 [0.01 ; 0.05], R/R 0.365, perte reelle 56.222 % (gap inclus), EV 2.134 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.65 % > budget 4.75 %
   - ⚪ atr_grid a 7.5 ATR (stop 53.786 %) — p(stop avant cible) 0.0243 [0.01 ; 0.04], R/R 0.324, perte reelle 63.341 % (gap inclus), EV 1.9701 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.85 % > budget 4.75 %
   - ⚪ atr_grid a 8.0 ATR (stop 57.371 %) — p(stop avant cible) 0.0243 [0.01 ; 0.04], R/R 0.324, perte reelle 63.341 % (gap inclus), EV 1.9701 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.85 % > budget 4.75 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 27.52, ATR14 1.9736 (7.171 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 2.869 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.359 % | 27.4213 | 87.25 % | 90.78 % | 93.03 % | 94.49 % | 95.55 % | 97.2 % |
| 0.1 ATR | 0.717 % | 27.3226 | 82.55 % | 87.14 % | 90.28 % | 92.13 % | 94.07 % | 96.3 % |
| 0.15 ATR | 1.076 % | 27.224 | 78.33 % | 83.51 % | 87.33 % | 88.98 % | 92.19 % | 95.2 % |
| 0.2 ATR | 1.434 % | 27.1253 | 72.65 % | 79.29 % | 83.6 % | 85.93 % | 89.81 % | 93.01 % |
| 0.25 ATR | 1.793 % | 27.0266 | 66.57 % | 74.68 % | 79.47 % | 82.58 % | 87.54 % | 91.41 % |
| 0.35 ATR | 2.51 % | 26.8293 | 54.61 % | 65.65 % | 71.22 % | 75.79 % | 82.69 % | 87.91 % |
| 0.5 ATR | 3.586 % | 26.5332 | 40.69 % | 53.78 % | 62.08 % | 68.9 % | 78.24 % | 85.51 % |
| 0.75 ATR | 5.379 % | 26.0398 | 22.65 % | 37.78 % | 47.45 % | 55.61 % | 67.46 % | 76.92 % |
| 1.0 ATR | 7.171 % | 25.5464 | 12.75 % | 24.93 % | 33.79 % | 44.09 % | 57.37 % | 68.63 % |
| 1.25 ATR | 8.964 % | 25.053 | 7.45 % | 17.76 % | 24.75 % | 36.52 % | 50.54 % | 62.34 % |
| 1.5 ATR | 10.757 % | 24.5596 | 3.63 % | 11.38 % | 17.49 % | 28.94 % | 43.32 % | 56.04 % |
| 2.0 ATR | 14.343 % | 23.5729 | 0.88 % | 5.2 % | 9.72 % | 17.03 % | 31.75 % | 44.56 % |
| 2.5 ATR | 17.929 % | 22.5861 | 0.1 % | 2.16 % | 4.62 % | 9.84 % | 21.56 % | 34.57 % |
| 3.0 ATR | 21.514 % | 21.5993 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 15.23 % | 26.77 % |
| 4.0 ATR | 28.686 % | 19.6257 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.28 % |
| 6.0 ATR | 43.028 % | 15.6786 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.02 ATR | 1.24 ATR | 1.41 ATR | 1.98 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.87 ATR | 0.98 ATR | 1.37 ATR | 1.67 ATR | 1.88 ATR | 2.49 ATR | 3.42 ATR |
| **10 s.** | 0.57 ATR | 1.27 ATR | 1.44 ATR | 1.95 ATR | 2.33 ATR | 2.62 ATR | 3.78 ATR | 5.11 ATR |
| **20 s.** | 0.81 ATR | 1.76 ATR | 1.98 ATR | 2.60 ATR | 3.19 ATR | 3.71 ATR | 5.57 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.454–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.586 %, prix 26.5331), p(touche) 40.69 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (89.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.637–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.379 %, prix 26.0397), p(touche) 37.78 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.795–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.171 %, prix 25.5465), p(touche) 33.79 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.98–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.171 %, prix 25.5465), p(touche) 44.09 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.442–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.757 %, prix 24.5597), p(touche) 43.32 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.981–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.343 %, prix 23.5728), p(touche) 44.56 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 83.3 | side 11.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 385.0 (= 14 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.816% → cible +6.403% / stop −3.202%, p_fill 69%, n_eff≈73.2) : P(cible|rempli) **6%** · **EV/risk -0.186** (×p_fill ; si rempli -0.86% du capital)
  - **swing** (entrée dip −3.989% → cible +8.813% / stop −7.469%, p_fill 51%, n_eff≈58.8) : P(cible|rempli) **36%** · **EV/risk -0.080** (×p_fill ; si rempli -1.18% du capital)
  - **deep** (entrée dip −6.163% → cible +11.335% / stop −11.464%, p_fill 50%, n_eff≈56.2) : P(cible|rempli) **40%** · **EV/risk -0.106** (×p_fill ; si rempli -2.44% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→74% · +2.0%→66% · +3.0%→50% · +5.0%→34% · +8.0%→17%
- Range intraday médian 6.93% (p90 16.1%) · excursion haute méd. +2.93% / basse méd. −3.31%
- Profil de vol intra : ouverture 4.806% vs midi 1.518% vs clôture 1.661% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑1%/↓0% ; spike-down 74% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. 0.151% ; recovery-V 25%
- **σ réalisé intraday** 4.419% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 71% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 26.6325 (VA 26.2575–26.7325 ; dernier close 26.53)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 91% · **stop −3.21%** sous le fill (sous le bruit) · cible +2.26% · R/R 0.7 (high win-rate)
- Gaps overnight (n=158) : méd. -0.0% · baisse 51% (gap-down >1% 16% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −3.16%) · haut méd +0.82% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.92%) · haut méd +1.23% · range méd 2.91%
- Excursion ouverture 30min (n=160) : bas méd −1.42% (p90 −4.38%) · haut méd +1.57% · range méd 3.4%
- Excursion ouverture 60min (n=160) : bas méd −1.64% (p90 −5.26%) · haut méd +2.01% · range méd 4.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.62 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 81% (125/158) · gap 30% · délai 0.1min · rebond 61% (81/125) (MFE +1.75%)
   - −1.0% : fill 30min 56% · séance 76% (120/158) · gap 16% · délai 0.4min · rebond 61% (79/120) (MFE +1.71%)
   - −1.5% : fill 30min 50% · séance 72% (107/158) · gap 8% · délai 2.4min · rebond 63% (68/107) (MFE +1.74%)
   - −2.0% : fill 30min 42% · séance 66% (98/158) · gap 6% · délai 7.8min · rebond 59% (60/98) (MFE +1.61%)
   - −3.0% : fill 30min 26% · séance 51% (79/158) · gap 3% · délai 31.2min · rebond 59% (53/79) (MFE +1.59%)
   - −4.0% : fill 30min 16% · séance 39% (65/158) · gap 2% · délai 55.8min · rebond 71% (49/65) (MFE +1.67%)
   - −5.0% : fill 30min 11% · séance 28% (50/158) · gap 2% · délai 48.7min · rebond 91% (46/50) (MFE +2.26%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.9%) → stop au-delà de −1.95% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.91%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.34% (p90 −3.18%) → stop au-delà de −2.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1398 jambes) : jambe baissière méd −1.21% (p90 −2.94%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 95% (51/53) · rebond 58% (30/51)
      · −2.0% : fill 87% (46/53) · rebond 59% (26/46)
      · −3.0% : fill 76% (41/53) · rebond 59% (28/41)
      · −4.0% : fill 58% (34/53) · rebond 61% (23/34)
      · −5.0% : fill 44% (27/53) · rebond 92% (24/27)
   - **flat** (34 séances) :
      · −1.0% : fill 72% (25/34) · rebond 66% (17/25)
      · −2.0% : fill 54% (19/34) · rebond 49% (11/19)
      · −3.0% : fill 40% (15/34) · rebond 60% (9/15)
      · −4.0% : fill 37% (14/34) · rebond 77% (11/14)
      · −5.0% : fill 30% (11/34) · rebond 80% (10/11)
   - **gap-up** (71 séances) :
      · −1.0% : fill 61% (44/71) · rebond 63% (32/44)
      · −2.0% : fill 52% (33/71) · rebond 65% (23/33)
      · −3.0% : fill 34% (23/71) · rebond 59% (16/23)
      · −4.0% : fill 23% (17/71) · rebond 88% (15/17)
      · −5.0% : fill 13% (12/71) · rebond 100% (12/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 56% si les 15 1res min sont vertes (77 cas) · 29% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:03** → P(séance verte=clôture>ouverture) 76% si début vert vs 15% si rouge (base 42% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -2.0% (q20 -4.42%) → **SL/trailing à −4.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.14% / q75 +3.25% → **scale +2.14% / runner +3.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **15%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.15%** (au-delà de la MAE q10 -4.15%), cible rebond +1.5% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.12% .. +5.57%] · haut q95 +6.82% · bas q05 -5.16%
   - 60min (n=160) : retour [-4.85% .. +7.25%] · haut q95 +8.2% · bas q05 -6.05%
   - 2h (n=160) : retour [-4.79% .. +9.19%] · haut q95 +9.95% · bas q05 -6.15%
   - 4h (n=160) : retour [-5.98% .. +9.6%] · haut q95 +9.98% · bas q05 -7.39%
   - 6h (n=160) : retour [-5.66% .. +10.41%] · haut q95 +12.17% · bas q05 -8.1%
   - session (n=160) : retour [-7.13% .. +9.93%] · haut q95 +12.72% · bas q05 -8.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 4.85%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.19 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 63.0  _(momentum haussier)_
- **ADX** : 12.3  _(pas de tendance nette)_
- **MACD** : hist 0.117  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 20.0%
- **ATR** : 1.97 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.013  _(neutre)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 51.1  _(transition)_
- **MA** : MA20 26.9 · MA50 27.61 · MA200 29.62  _(prix > MA20)_
- **Dist MA** : MA20 +2.3% · MA50 -0.3% · MA200 -7.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (788955 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
