# HOOD

**Generated** : 2026-08-31T00:33:32.385004+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $104.26  

> 🟡 **WAIT-FOR-DIP** — spot +0.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $104.26 (+0.8% vs entrée) · entrée $103.41 · stop $97.39 · T1 $114.91 · R/R 1.91  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk 0.085 _(réel 5 s)_ (GBM 0.052) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $102.56–$104.26 (mid $103.41)
- Spot actuel : $104.26 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $97.39 (stop swing_plan-based (-6.59%))
- Targets : T1 $114.91 · R/R 1.91 | T2 $117.83 · R/R 2.4 | T3 $120.74 · R/R 2.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $97.39


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.59 %)** : le gap seul le franchit 1.196 % des séances (15 fois sur 1254).
   - exécution **2.483 pt plus bas** dans le cas TYPIQUE (médiane), 6.647 au p90, **11.195 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 6.59 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0408 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.456 % | p01 -7.299 % | pire -17.785 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1316** [0.0875 ; 0.1879] _(largeur 10.0 pt, n_eff 173.1)_
   - swing : **0.4639** [0.4118 ; 0.5166] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4196** [0.3684 ; 0.4721] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.5 pt), swing (31.4 pt), deep (31.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.35 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.02 % contre 4.48 % aujourd'hui, rapport 0.45)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.53 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.012 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7622** (β de hausse 1.6144, asymétrie 1.0915) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.483× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 93.7225 sur atr_grid (1.75 ATR, 10.107 %) — p(stop avant cible) 0.3749 [0.33 ; 0.43], R/R 1.244, perte reelle 12.711 % (gap inclus), CVaR 10.119 %, EV 0.5781 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.36 ATR (stop 5.156 %) — p(stop avant cible) 0.639 [0.59 ; 0.69], R/R 1.886, perte reelle 8.38 % (gap inclus), EV -1.3284 % — **REFUSE**
      - refuse : p_stop_first 0.639, borne haute 0.688 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.16 ATR du spot — compartiment <1, mesure a 45.9 % de casse (IC clusterise [0.428 ; 0.490] sur 1144 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.33 %) : P(cible) 21.1 % x 15.81 % + P(rien) 15.0 % x 4.61 % ne couvrent pas P(stop) 63.9 % x 8.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 8.663 %) — p(stop avant cible) 0.4412 [0.39 ; 0.49], R/R 1.363, perte reelle 11.595 % (gap inclus), EV -0.0254 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 27.0 % x 15.81 % + P(rien) 28.9 % x 2.84 % ne couvrent pas P(stop) 44.1 % x 11.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.13 ATR (stop 15.38 %) — p(stop avant cible) 0.1989 [0.16 ; 0.24], R/R 0.889, perte reelle 17.785 % (gap inclus), EV 1.364 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.38 % > budget 12.00 %
   - 🟢 support a 4.21 ATR (stop 27.379 %) — p(stop avant cible) 0.0303 [0.02 ; 0.05], R/R 0.577, perte reelle 27.379 % (gap inclus), EV 1.9204 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.38 % > budget 12.00 %
   - 🔴 grid_snapped a 0.36 ATR (stop 3.804 %) — p(stop avant cible) 0.721 [0.67 ; 0.77], R/R 2.51, perte reelle 6.298 % (gap inclus), EV -1.1103 % — **REFUSE**
      - refuse : p_stop_first 0.721, borne haute 0.766 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 17.6 % x 15.81 % + P(rien) 10.3 % x 6.27 % ne couvrent pas P(stop) 72.1 % x 6.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.219 %) — p(stop avant cible) 0.5229 [0.47 ; 0.58], R/R 1.506, perte reelle 10.494 % (gap inclus), EV -0.5951 % — **REFUSE**
      - refuse : p_stop_first 0.523, borne haute 0.575 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 25.8 % x 15.81 % + P(rien) 21.9 % x 3.71 % ne couvrent pas P(stop) 52.3 % x 10.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 10.107 %) — p(stop avant cible) 0.3749 [0.33 ; 0.43], R/R 1.244, perte reelle 12.711 % (gap inclus), EV 0.5781 % — **REFUSE**
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 2.13 ATR (stop 14.029 %) — p(stop avant cible) 0.2382 [0.20 ; 0.29], R/R 0.991, perte reelle 15.955 % (gap inclus), EV 1.3497 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.03 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.326 %) — p(stop avant cible) 0.1389 [0.11 ; 0.18], R/R 0.889, perte reelle 17.785 % (gap inclus), EV 1.7681 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.214 %) — p(stop avant cible) 0.0818 [0.06 ; 0.11], R/R 0.782, perte reelle 20.214 % (gap inclus), EV 1.9086 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.21 % > budget 12.00 %
   - 🟢 grid_snapped a 4.21 ATR (stop 26.028 %) — p(stop avant cible) 0.0355 [0.02 ; 0.06], R/R 0.607, perte reelle 26.028 % (gap inclus), EV 1.9079 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.03 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 28.877 %) — p(stop avant cible) 0.027 [0.01 ; 0.05], R/R 0.547, perte reelle 28.877 % (gap inclus), EV 1.893 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.88 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.765 %) — p(stop avant cible) 0.0153 [0.01 ; 0.03], R/R 0.498, perte reelle 31.765 % (gap inclus), EV 1.9431 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.76 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.652 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.456, perte reelle 34.652 % (gap inclus), EV 2.0446 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.65 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.54 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.421, perte reelle 37.54 % (gap inclus), EV 2.0535 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.54 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.428 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.391, perte reelle 40.428 % (gap inclus), EV 2.0736 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.43 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.315 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.365, perte reelle 43.315 % (gap inclus), EV 2.0736 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.31 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.203 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.342, perte reelle 46.203 % (gap inclus), EV 2.0736 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.20 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 104.26, ATR14 6.0214 (5.775 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.372 ATR = 2.148 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.289 % | 103.9589 | 92.86 % | 94.96 % | 95.87 % | 96.36 % | 96.95 % | 97.95 % |
| 0.1 ATR | 0.578 % | 103.6579 | 85.51 % | 90.23 % | 91.94 % | 93.43 % | 94.52 % | 96.41 % |
| 0.15 ATR | 0.866 % | 103.3568 | 77.67 % | 84.99 % | 87.7 % | 89.9 % | 92.28 % | 94.97 % |
| 0.2 ATR | 1.155 % | 103.0557 | 71.63 % | 79.86 % | 83.47 % | 86.57 % | 90.15 % | 93.23 % |
| 0.25 ATR | 1.444 % | 102.7546 | 64.49 % | 74.12 % | 78.93 % | 83.03 % | 87.51 % | 90.97 % |
| 0.35 ATR | 2.021 % | 102.1525 | 52.31 % | 65.06 % | 71.67 % | 77.27 % | 83.15 % | 88.1 % |
| 0.5 ATR | 2.888 % | 101.2493 | 36.82 % | 53.07 % | 60.58 % | 67.98 % | 76.45 % | 82.67 % |
| 0.75 ATR | 4.332 % | 99.7439 | 19.42 % | 35.95 % | 45.67 % | 55.45 % | 65.69 % | 73.64 % |
| 1.0 ATR | 5.775 % | 98.2386 | 9.26 % | 22.66 % | 32.26 % | 43.74 % | 55.03 % | 66.15 % |
| 1.25 ATR | 7.219 % | 96.7332 | 4.83 % | 14.4 % | 22.18 % | 33.23 % | 47.01 % | 59.79 % |
| 1.5 ATR | 8.663 % | 95.2279 | 2.41 % | 9.97 % | 16.23 % | 26.67 % | 39.9 % | 54.05 % |
| 2.0 ATR | 11.551 % | 92.2171 | 0.5 % | 3.93 % | 7.36 % | 15.56 % | 29.95 % | 44.62 % |
| 2.5 ATR | 14.438 % | 89.2064 | 0.1 % | 1.51 % | 3.83 % | 8.18 % | 21.52 % | 34.97 % |
| 3.0 ATR | 17.326 % | 86.1957 | 0.0 % | 0.7 % | 2.32 % | 5.25 % | 15.43 % | 26.67 % |
| 4.0 ATR | 23.102 % | 80.1743 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.9 % | 14.87 % |
| 6.0 ATR | 34.652 % | 68.1314 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.08 ATR | 1.50 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.18 ATR | 1.34 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.97 ATR | 1.26 ATR | 1.57 ATR | 1.80 ATR | 2.38 ATR | 3.08 ATR |
| **10 s.** | 0.53 ATR | 1.16 ATR | 1.32 ATR | 1.85 ATR | 2.29 ATR | 2.62 ATR | 3.64 ATR | 4.68 ATR |
| **20 s.** | 0.71 ATR | 1.72 ATR | 1.98 ATR | 2.62 ATR | 3.14 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.421–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.618–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.332 %, prix 99.7435), p(touche) 35.95 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.762–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.775 %, prix 98.239), p(touche) 32.26 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (63.6 % des re-echantillons)
- **5 seance(s)** : plage utile 0.973–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.775 %, prix 98.239), p(touche) 43.74 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.321–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.663 %, prix 95.228), p(touche) 39.9 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.98–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.551 %, prix 92.2169), p(touche) 44.62 % (en stress 97.96 %)  ✅ optimum identifie (64.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.052 | EV/share : $0.311 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 17 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 44.2 | bear 45.9 | side 9.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 521.0 (= 5 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.4% → cible +2.499% / stop −5.0%, p_fill 88%, n_eff≈36.0) : P(cible|rempli) **36%** · **EV/risk -0.052** (×p_fill ; si rempli -0.30% du capital)
  - **swing** (entrée dip −0.814% → cible +11.123% / stop −5.823%, p_fill 85%, n_eff≈34.9) : P(cible|rempli) **25%** · **EV/risk +0.085** (×p_fill ; si rempli +0.58% du capital)
  - **deep** (entrée dip −1.183% → cible +18.108% / stop −9.054%, p_fill 86%, n_eff≈35.4) : P(cible|rempli) **17%** · **EV/risk +0.318** (×p_fill ; si rempli +3.35% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→81% · +2.0%→56% · +3.0%→36% · +5.0%→24% · +8.0%→9%
- Range intraday médian 5.24% (p90 9.06%) · excursion haute méd. +2.16% / basse méd. −2.32%
- Profil de vol intra : ouverture 3.85% vs midi 1.022% vs clôture 1.164% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑1%/↓0% ; spike-down 69% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr -0.005)_ ; drift intra méd. -0.022% ; recovery-V 27%
- **σ réalisé intraday** 3.52% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 49% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 104.8754 (VA 104.2484–106.9131 ; dernier close 104.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 40% · rebond 78% · **stop −4.27%** sous le fill (sous le bruit) · cible +2.01% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. -0.05% · baisse 51% (gap-down >1% 33% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −2.76%) · haut méd +1.07% · range méd 2.2%
- Excursion ouverture 15min (n=160) : bas méd −1.28% (p90 −3.84%) · haut méd +1.37% · range méd 2.89%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.89%) · haut méd +1.65% · range méd 3.45%
- Excursion ouverture 60min (n=160) : bas méd −1.83% (p90 −4.08%) · haut méd +1.67% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 104.26 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (124/159) · gap 43% · délai 0.0min · rebond 60% (68/124) (MFE +1.43%)
   - −1.0% : fill 30min 59% · séance 68% (108/159) · gap 33% · délai 0.0min · rebond 63% (63/108) (MFE +1.62%)
   - −1.5% : fill 30min 50% · séance 59% (99/159) · gap 24% · délai 0.3min · rebond 64% (58/99) (MFE +1.32%)
   - −2.0% : fill 30min 39% · séance 50% (88/159) · gap 14% · délai 1.1min · rebond 68% (55/88) (MFE +1.41%)
   - −3.0% : fill 30min 27% · séance 40% (68/159) · gap 6% · délai 10.8min · rebond 78% (48/68) (MFE +2.01%)
   - −4.0% : fill 30min 17% · séance 30% (51/159) · gap 3% · délai 11.9min · rebond 72% (34/51) (MFE +2.29%)
   - −5.0% : fill 30min 9% · séance 17% (33/159) · gap 2% · délai 28.3min · rebond 67% (24/33) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −2.57%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.63% (p90 −2.36%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.42%) → stop au-delà de −1.66% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=771 jambes) : jambe baissière méd −1.13% (p90 −2.8%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 94% (73/76) · rebond 53% (38/73)
      · −2.0% : fill 81% (63/76) · rebond 63% (38/63)
      · −3.0% : fill 70% (53/76) · rebond 77% (37/53)
      · −4.0% : fill 52% (41/76) · rebond 71% (29/41)
      · −5.0% : fill 31% (28/76) · rebond 62% (19/28)
   - **flat** (17 séances) :
      · −1.0% : fill 62% (11/17) · rebond 80% (7/11)
      · −2.0% : fill 39% (9/17) · rebond 61% (6/9)
      · −3.0% : fill 12% (4/17) · rebond 18% (1/4)
      · −4.0% : fill 12% (4/17) · rebond 18% (1/4)
      · −5.0% : fill 5% (2/17) · rebond 100% (2/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 41% (24/66) · rebond 82% (18/24)
      · −2.0% : fill 21% (16/66) · rebond 90% (11/16)
      · −3.0% : fill 14% (11/66) · rebond 97% (10/11)
      · −4.0% : fill 10% (6/66) · rebond 91% (4/6)
      · −5.0% : fill 4% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 68% si les 15 1res min sont vertes (75 cas) · 29% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **53min** → P(séance verte=clôture>ouverture) 72% si début vert vs 22% si rouge (base 46% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **72%** · continue >prix actuel 48% ; creux résiduel méd -1.4% (q20 -2.54%) → **SL/trailing à −2.54%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.57% / q75 +3.12% → **scale +1.57% / runner +3.12%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **22%** (continue à baisser 60%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.93%** (au-delà de la MAE q10 -2.93%), cible rebond +1.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.28% .. +4.21%] · haut q95 +4.8% · bas q05 -5.1%
   - 60min (n=160) : retour [-3.71% .. +4.96%] · haut q95 +6.17% · bas q05 -5.65%
   - 2h (n=160) : retour [-4.84% .. +5.94%] · haut q95 +7.55% · bas q05 -6.07%
   - 4h (n=160) : retour [-4.91% .. +7.04%] · haut q95 +8.31% · bas q05 -6.78%
   - 6h (n=160) : retour [-5.75% .. +6.71%] · haut q95 +8.54% · bas q05 -7.11%
   - session (n=160) : retour [-5.42% .. +7.04%] · haut q95 +8.66% · bas q05 -7.15%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 8.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **36%**. Lecture précoce 30 min : signature présente → 23% vs absente 2% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.5% / p90 2.5%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **77%** (reprise méd 20.0 min, n=51)
   - −1.0% → **65%** (reprise méd 38.77 min, n=23)
   - −1.5% → **47%** (reprise méd 41.95 min, n=13)
   - −2.0% → **14%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.5%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +6.95% (q75 +9.04% / q95 +12.46%), MFE méd +8.52% / q90 +13.87%
   - Échelle scale-out : +8.52% (33%) / +9.47% (33%) / +13.87% (34%)
- **DÉSARMER** : repli > **−2.5%** depuis le plus-haut = décay → P(retournement) **81%** (préavis méd 286.42 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.87% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.38%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 58.8  _(momentum haussier)_
- **ADX** : 20.2  _(pas de tendance nette)_
- **MACD** : hist 1.567  _(pas de croisement recent)_
- **BB** : %B 0.72 · largeur 28.1%
- **ATR** : 6.02 (54.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.061  _(distribution)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 52.6  _(transition)_
- **MA** : MA20 98.22 · MA50 101.37 · MA200 95.41  _(prix > MA20)_
- **Dist MA** : MA20 +6.1% · MA50 +2.9% · MA200 +9.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (889692 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
