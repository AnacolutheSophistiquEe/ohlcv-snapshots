# MSTR

**Generated** : 2026-10-05T00:23:33.178162+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $160.01  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $160.01 (+1.2% vs entrée) · entrée $158.08 · stop $153.83 · T1 $166.58 · R/R 2.0  
> ↳ P(T1 av. stop) 10 % _(réel 5 s)_ · EV/risk -0.043 _(réel 5 s)_ · _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $157.22–$158.95 (mid $158.08)
- Spot actuel : $160.01 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $153.83 (R/R 2 (resserré, parité Claude) ; -2.69 % depuis l'entree)
- Targets : T1 $166.58 · R/R 2.0 | T2 $171.53 · R/R 3.16 | T3 $176.47 · R/R 4.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $153.83


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.45 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.83 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1254).
   - exécution **2.569 pt plus bas** dans le cas TYPIQUE (médiane), 17.907 au p90, **18.542 au pire**
   - perte réelle **14.455 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 8.83 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0404 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.344 % | p01 -7.774 % | pire -27.372 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4337** [0.3615 ; 0.5081] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4228** [0.3715 ; 0.4753] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4205** [0.3693 ; 0.473] _(largeur 10.4 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.01 %** | CVaR **-9.02 %** | vol 4.89 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.03 % contre 5.34 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.67 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3634** (β de hausse 1.8198, asymétrie 1.2987) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 148.3519 sur grid_snapped (0.88 ATR, 7.286 %) — p(stop avant cible) 0.5376 [0.48 ; 0.59], R/R 2.397, perte reelle 7.477 % (gap inclus), CVaR 9.191 %, EV 0.5947 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2731 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.538, borne haute 0.590 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **25.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 1.02 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 61.0 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 27.09 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.88 ATR (stop 8.324 %) — p(stop avant cible) 0.4924 [0.44 ; 0.55], R/R 2.113, perte reelle 8.483 % (gap inclus), EV 0.6161 % — **REFUSE**
      - refuse : R/R 2.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 support a 1.53 ATR (stop 12.322 %) — p(stop avant cible) 0.333 [0.28 ; 0.38], R/R 1.442, perte reelle 12.434 % (gap inclus), EV 0.5906 % — **REFUSE**
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.78 ATR du spot — compartiment <1, mesure a 46.3 % de casse (IC clusterise [0.432 ; 0.495] sur 1140 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 2.4 ATR (stop 17.741 %) — p(stop avant cible) 0.1862 [0.15 ; 0.23], R/R 0.994, perte reelle 18.033 % (gap inclus), EV 0.253 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 3.91 ATR (stop 27.051 %) — p(stop avant cible) 0.0625 [0.04 ; 0.09], R/R 0.651, perte reelle 27.53 % (gap inclus), EV 0.0538 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.65 % > budget 25.00 %
   - 🟢 support a 4.41 ATR (stop 30.146 %) — p(stop avant cible) 0.0416 [0.02 ; 0.07], R/R 0.586, perte reelle 30.576 % (gap inclus), EV 0.068 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.94 % > budget 25.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.545 %) — p(stop avant cible) 0.9313 [0.90 ; 0.95], R/R 11.389, perte reelle 1.574 % (gap inclus), EV -0.4699 % — **REFUSE**
      - refuse : cible atteinte seulement 4.8 % du temps (< 15 %) meme a 10 seances : le R/R de 11.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.931, borne haute 0.954 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 4.8 % x 17.93 % + P(rien) 2.1 % x 6.40 % ne couvrent pas P(stop) 93.1 % x 1.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.09 %) — p(stop avant cible) 0.8282 [0.79 ; 0.87], R/R 5.601, perte reelle 3.201 % (gap inclus), EV -0.4306 % — **REFUSE**
      - refuse : cible atteinte seulement 10.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.828, borne haute 0.865 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 10.5 % x 17.93 % + P(rien) 6.7 % x 4.97 % ne couvrent pas P(stop) 82.8 % x 3.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.88 ATR (stop 7.286 %) — p(stop avant cible) 0.5376 [0.48 ; 0.59], R/R 2.397, perte reelle 7.477 % (gap inclus), EV 0.5947 % — **REFUSE**
      - refuse : p_stop_first 0.538, borne haute 0.590 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 grid_snapped a 1.53 ATR (stop 11.284 %) — p(stop avant cible) 0.3621 [0.31 ; 0.41], R/R 1.573, perte reelle 11.398 % (gap inclus), EV 0.75 % — **REFUSE**
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 2.4 ATR (stop 16.703 %) — p(stop avant cible) 0.2072 [0.17 ; 0.25], R/R 1.057, perte reelle 16.953 % (gap inclus), EV 0.3015 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 18.537 %) — p(stop avant cible) 0.1778 [0.14 ; 0.22], R/R 0.953, perte reelle 18.816 % (gap inclus), EV 0.1479 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 21.627 %) — p(stop avant cible) 0.1309 [0.10 ; 0.17], R/R 0.815, perte reelle 21.989 % (gap inclus), EV 0.0817 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.91 ATR (stop 26.013 %) — p(stop avant cible) 0.0732 [0.05 ; 0.10], R/R 0.679, perte reelle 26.383 % (gap inclus), EV 0.0852 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.55 % > budget 25.00 %
   - 🟢 grid_snapped a 4.41 ATR (stop 29.108 %) — p(stop avant cible) 0.0491 [0.03 ; 0.08], R/R 0.605, perte reelle 29.619 % (gap inclus), EV 0.0165 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.59 % > budget 25.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 33.985 %) — p(stop avant cible) 0.0198 [0.01 ; 0.04], R/R 0.521, perte reelle 34.427 % (gap inclus), EV 0.1363 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.91 % > budget 25.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 37.074 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.472, perte reelle 37.967 % (gap inclus), EV 0.256 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.54 % > budget 25.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 40.164 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.439, perte reelle 40.879 % (gap inclus), EV 0.2991 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.75 % > budget 25.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 43.254 %) — p(stop avant cible) 0.0004 [0.00 ; 0.01], R/R 0.414, perte reelle 43.333 % (gap inclus), EV 0.3085 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.60 % > budget 25.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 46.343 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.387, perte reelle 46.343 % (gap inclus), EV 0.3124 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.50 % > budget 25.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 49.433 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.362, perte reelle 49.546 % (gap inclus), EV 0.3117 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.51 % > budget 25.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 160.01, ATR14 9.8871 (6.179 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.394 ATR = 2.435 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.309 % | 159.5156 | 93.96 % | 96.48 % | 96.98 % | 97.68 % | 98.07 % | 98.67 % |
| 0.1 ATR | 0.618 % | 159.0213 | 88.13 % | 91.94 % | 93.45 % | 94.85 % | 96.55 % | 97.23 % |
| 0.15 ATR | 0.927 % | 158.5269 | 81.19 % | 87.11 % | 89.82 % | 91.92 % | 94.11 % | 95.49 % |
| 0.2 ATR | 1.236 % | 158.0326 | 73.64 % | 81.77 % | 85.08 % | 88.38 % | 91.47 % | 93.54 % |
| 0.25 ATR | 1.545 % | 157.5382 | 67.71 % | 77.95 % | 82.26 % | 86.26 % | 89.04 % | 91.9 % |
| 0.35 ATR | 2.163 % | 156.5495 | 54.93 % | 68.88 % | 75.4 % | 81.01 % | 85.58 % | 89.23 % |
| 0.5 ATR | 3.09 % | 155.0664 | 38.23 % | 55.39 % | 63.51 % | 71.41 % | 78.27 % | 84.31 % |
| 0.75 ATR | 4.634 % | 152.5946 | 19.42 % | 37.66 % | 46.98 % | 58.08 % | 67.72 % | 76.62 % |
| 1.0 ATR | 6.179 % | 150.1229 | 9.36 % | 25.08 % | 34.68 % | 46.16 % | 58.38 % | 69.54 % |
| 1.25 ATR | 7.724 % | 147.6511 | 4.12 % | 14.5 % | 24.7 % | 35.66 % | 49.54 % | 62.15 % |
| 1.5 ATR | 9.269 % | 145.1793 | 2.11 % | 8.66 % | 17.24 % | 28.79 % | 42.74 % | 56.62 % |
| 2.0 ATR | 12.358 % | 140.2357 | 0.2 % | 3.12 % | 7.36 % | 15.96 % | 30.86 % | 46.77 % |
| 2.5 ATR | 15.448 % | 135.2921 | 0.1 % | 0.91 % | 2.42 % | 8.69 % | 21.22 % | 37.33 % |
| 3.0 ATR | 18.537 % | 130.3486 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.52 % | 28.0 % |
| 4.0 ATR | 24.716 % | 120.4614 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.19 % | 18.05 % |
| 6.0 ATR | 37.074 % | 100.6871 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.58 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.12 ATR | 1.44 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.24 ATR | 1.41 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.92 ATR | 1.03 ATR | 1.35 ATR | 1.65 ATR | 1.84 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.58 ATR | 1.24 ATR | 1.42 ATR | 1.91 ATR | 2.30 ATR | 2.59 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.81 ATR | 1.84 ATR | 2.09 ATR | 2.73 ATR | 3.30 ATR | 3.80 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.09 %, prix 155.0657), p(touche) 38.23 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.647–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.634 %, prix 152.5951), p(touche) 37.66 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.79–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.179 %, prix 150.123), p(touche) 34.68 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.028–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.724 %, prix 147.6508), p(touche) 35.66 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.417–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.269 %, prix 145.1787), p(touche) 42.74 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.094–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.448 %, prix 135.2917), p(touche) 37.33 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 13.3 | bear 5.0 | side 81.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 426.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.204% → cible +5.377% / stop −2.689%, p_fill 72%, n_eff≈79.4) : P(cible|rempli) **10%** · **EV/risk -0.043** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −2.651% → cible +6.94% / stop −6.347%, p_fill 63%, n_eff≈74.1) : P(cible|rempli) **44%** · **EV/risk +0.037** (×p_fill ; si rempli +0.38% du capital)
  - **deep** (entrée dip −4.091% → cible +10.908% / stop −9.664%, p_fill 57%, n_eff≈64.9) : P(cible|rempli) **57%** · **EV/risk +0.149** (×p_fill ; si rempli +2.51% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→78% · +2.0%→58% · +3.0%→41% · +5.0%→18% · +8.0%→9%
- Range intraday médian 5.36% (p90 9.67%) · excursion haute méd. +2.57% / basse méd. −2.28%
- Profil de vol intra : ouverture 3.353% vs midi 1.137% vs clôture 1.289% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 14% · trend ↑3%/↓0% ; spike-down 68% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.141 ; neutre — autocorr -0.029)_ ; drift intra méd. 0.341% ; recovery-V 26%
- **σ réalisé intraday** 3.531% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 56% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 157.5016 (VA 156.1046–160.2956 ; dernier close 160.03)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 22% · rebond 79% · **stop −3.87%** sous le fill (sous le bruit) · cible +2.49% · R/R 0.64 (high win-rate)
- Gaps overnight (n=159) : méd. 0.06% · baisse 49% (gap-down >1% 35% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.12%) · haut méd +0.84% · range méd 1.88%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.9%) · haut méd +1.24% · range méd 2.6%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.22%) · haut méd +1.51% · range méd 3.04%
- Excursion ouverture 60min (n=160) : bas méd −1.52% (p90 −3.66%) · haut méd +1.86% · range méd 3.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 160.01 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 72% (118/159) · gap 42% · délai 0.0min · rebond 43% (54/118) (MFE +0.52%)
   - −1.0% : fill 30min 53% · séance 67% (112/159) · gap 35% · délai 0.0min · rebond 45% (58/112) (MFE +0.78%)
   - −1.5% : fill 30min 45% · séance 64% (105/159) · gap 28% · délai 0.0min · rebond 54% (59/105) (MFE +1.16%)
   - −2.0% : fill 30min 38% · séance 57% (94/159) · gap 24% · délai 0.1min · rebond 61% (57/94) (MFE +1.35%)
   - −3.0% : fill 30min 26% · séance 42% (74/159) · gap 14% · délai 1.2min · rebond 59% (42/74) (MFE +1.56%)
   - −4.0% : fill 30min 19% · séance 32% (59/159) · gap 4% · délai 11.3min · rebond 76% (41/59) (MFE +1.92%)
   - −5.0% : fill 30min 13% · séance 22% (42/159) · gap 3% · délai 17.2min · rebond 79% (32/42) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.16%) → stop au-delà de −1.63% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −2.2%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.87% (p90 −2.26%) → stop au-delà de −1.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=927 jambes) : jambe baissière méd −1.1% (p90 −2.68%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 96% (75/76) · rebond 41% (33/75)
      · −2.0% : fill 91% (69/76) · rebond 60% (40/69)
      · −3.0% : fill 74% (60/76) · rebond 56% (34/60)
      · −4.0% : fill 63% (51/76) · rebond 76% (36/51)
      · −5.0% : fill 46% (38/76) · rebond 81% (30/38)
   - **flat** (18 séances) :
      · −1.0% : fill 69% (13/18) · rebond 68% (10/13)
      · −2.0% : fill 52% (9/18) · rebond 54% (5/9)
      · −3.0% : fill 43% (7/18) · rebond 71% (4/7)
      · −4.0% : fill 20% (4/18) · rebond 80% (3/4)
      · −5.0% : fill 6% (2/18) · rebond 0% (0/2)
   - **gap-up** (65 séances) :
      · −1.0% : fill 37% (24/65) · rebond 41% (15/24)
      · −2.0% : fill 24% (16/65) · rebond 70% (12/16)
      · −3.0% : fill 9% (7/65) · rebond 67% (4/7)
      · −4.0% : fill 4% (4/65) · rebond 58% (2/4)
      · −5.0% : fill 2% (2/65) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 57% si les 15 1res min sont vertes (86 cas) · 31% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 74% si début vert vs 8% si rouge (base 46% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=90) : tient le vert **74%** · continue >prix actuel 52% ; creux résiduel méd -1.25% (q20 -2.9%) → **SL/trailing à −2.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +2.9% → **scale +2.05% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **8%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.61%** (au-delà de la MAE q10 -4.61%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.19% .. +3.97%] · haut q95 +4.43% · bas q05 -3.67%
   - 60min (n=160) : retour [-3.97% .. +5.6%] · haut q95 +5.88% · bas q05 -4.75%
   - 2h (n=160) : retour [-4.57% .. +8.48%] · haut q95 +8.77% · bas q05 -5.63%
   - 4h (n=160) : retour [-5.17% .. +9.39%] · haut q95 +10.33% · bas q05 -6.01%
   - 6h (n=160) : retour [-5.25% .. +8.5%] · haut q95 +11.08% · bas q05 -6.13%
   - session (n=160) : retour [-4.99% .. +8.27%] · haut q95 +11.08% · bas q05 -6.31%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0.6% / strong 5.6%) · base = 10 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **39%**. Lecture précoce 30 min : signature présente → 22% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.77% (p75 1.13% / p90 2.71%) · ~4.0 replis/séance, durée méd 34.08 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 20.0 min, n=37)
   - −1.0% → **60%** (reprise méd 31.69 min, n=14)
   - −1.5% → **43%** (reprise méd 42.45 min, n=10)
   - −2.0% → **19%** (reprise méd None min, n=7)
   - −3.0% → **38%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.71%** (p90, défaut prudent ; serré/agressif −1.13%) ; extension open→close méd +9.11% (q75 +12.7% / q95 +13.17%), MFE méd +11.91% / q90 +13.21%
   - Échelle scale-out : +11.91% (33%) / +13.03% (33%) / +13.21% (34%)
- **DÉSARMER** : repli > **−2.71%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 182.05 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.21% : P(retournement après) 0% (mèche méd 0.05%)
- **CONTEXTE** : la dernière heure tient les gains 84% du temps (retour médian dernière heure +0.85%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.78 · part idiosyncratique 0.22
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 65.1  _(momentum haussier)_
- **ADX** : 39.2  _(tendance etablie)_
- **MACD** : hist -0.409  _(bearish_recent)_
- **BB** : %B 0.71 · largeur 39.4%
- **ATR** : 9.89 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.004  _(neutre)_
- **Vol ratio** : 1.2  _(volume normal)_
- **Choppiness** : 40.2  _(transition)_
- **MA** : MA20 147.7 · MA50 123.61 · MA200 135.99  _(prix > MA20)_
- **Dist MA** : MA20 +8.3% · MA50 +29.5% · MA200 +17.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (836982 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
