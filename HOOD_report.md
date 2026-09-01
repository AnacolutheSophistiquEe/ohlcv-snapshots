# HOOD

**Generated** : 2026-09-01T00:33:34.148355+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $104.81  

> 🟡 **WAIT-FOR-DIP** — spot +1.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $104.81 (+1.0% vs entrée) · entrée $103.81 · stop $97.62 · T1 $114.72 · R/R 1.76  
> ↳ P(T1 av. stop) 26 % _(réel 5 s)_ · EV/risk 0.077 _(réel 5 s)_ (GBM 0.035) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $102.82–$104.81 (mid $103.81)
- Spot actuel : $104.81 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $97.62 (stop swing_plan-based (-6.86%))
- Targets : T1 $114.72 · R/R 1.76 | T2 $117.84 · R/R 2.27 | T3 $120.95 · R/R 2.77
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $97.62


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.86 %)** : le gap seul le franchit 1.117 % des séances (14 fois sur 1253).
   - exécution **2.671 pt plus bas** dans le cas TYPIQUE (médiane), 6.599 au p90, **10.925 au pire**
   - perte réelle **10.236 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 6.86 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0377 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 14 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.437 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1301** [0.0862 ; 0.1862] _(largeur 10.0 pt, n_eff 173.1)_
   - swing : **0.4373** [0.3857 ; 0.4899] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4177** [0.3666 ; 0.4702] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.6 pt), swing (31.4 pt), deep (30.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.35 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.04 % contre 4.48 % aujourd'hui, rapport 0.46)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7639** (β de hausse 1.6151, asymétrie 1.0921) vs IWM — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.496× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 93.9725 sur atr_grid (1.75 ATR, 10.34 %) — p(stop avant cible) 0.3703 [0.32 ; 0.42], R/R 1.168, perte reelle 13.192 % (gap inclus), CVaR 10.351 %, EV 0.4969 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 19 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 61.4 % de la queue et il ne reste que 29.65 EUR a partager. Prix du risque 0.019 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.44 ATR (stop 5.262 %) — p(stop avant cible) 0.6208 [0.57 ; 0.67], R/R 1.809, perte reelle 8.516 % (gap inclus), EV -1.0182 % — **REFUSE**
      - refuse : p_stop_first 0.621, borne haute 0.671 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.25 ATR du spot — compartiment <1, mesure a 46.4 % de casse (IC clusterise [0.430 ; 0.496] sur 1146 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 24.1 % x 15.40 % + P(rien) 13.8 % x 4.00 % ne couvrent pas P(stop) 62.1 % x 8.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 8.863 %) — p(stop avant cible) 0.4212 [0.37 ; 0.47], R/R 1.328, perte reelle 11.595 % (gap inclus), EV 0.4484 % — **REFUSE**
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 2.16 ATR (stop 15.433 %) — p(stop avant cible) 0.1971 [0.16 ; 0.24], R/R 0.866, perte reelle 17.785 % (gap inclus), EV 1.4323 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.43 % > budget 12.00 %
   - 🟢 support a 4.18 ATR (stop 27.369 %) — p(stop avant cible) 0.0301 [0.02 ; 0.05], R/R 0.563, perte reelle 27.369 % (gap inclus), EV 1.9914 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.37 % > budget 12.00 %
   - 🔴 grid_snapped a 0.44 ATR (stop 4.358 %) — p(stop avant cible) 0.6796 [0.63 ; 0.73], R/R 2.18, perte reelle 7.064 % (gap inclus), EV -1.0093 % — **REFUSE**
      - refuse : p_stop_first 0.680, borne haute 0.727 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 21.2 % x 15.40 % + P(rien) 10.8 % x 4.82 % ne couvrent pas P(stop) 68.0 % x 7.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.386 %) — p(stop avant cible) 0.5068 [0.45 ; 0.56], R/R 1.468, perte reelle 10.494 % (gap inclus), EV -0.3884 % — **REFUSE**
      - refuse : p_stop_first 0.507, borne haute 0.559 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 27.7 % x 15.40 % + P(rien) 21.6 % x 3.05 % ne couvrent pas P(stop) 50.7 % x 10.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 10.34 %) — p(stop avant cible) 0.3703 [0.32 ; 0.42], R/R 1.168, perte reelle 13.192 % (gap inclus), EV 0.4969 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 2.16 ATR (stop 14.529 %) — p(stop avant cible) 0.2104 [0.17 ; 0.26], R/R 0.866, perte reelle 17.785 % (gap inclus), EV 1.2841 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.53 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 16.249 %) — p(stop avant cible) 0.1757 [0.14 ; 0.22], R/R 0.866, perte reelle 17.785 % (gap inclus), EV 1.5745 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.25 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.726 %) — p(stop avant cible) 0.1291 [0.10 ; 0.17], R/R 0.866, perte reelle 17.785 % (gap inclus), EV 1.9236 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.73 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.68 %) — p(stop avant cible) 0.0806 [0.06 ; 0.11], R/R 0.745, perte reelle 20.68 % (gap inclus), EV 1.9401 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.68 % > budget 12.00 %
   - 🟢 grid_snapped a 4.18 ATR (stop 26.465 %) — p(stop avant cible) 0.0352 [0.02 ; 0.06], R/R 0.582, perte reelle 26.465 % (gap inclus), EV 1.9644 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.47 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.543 %) — p(stop avant cible) 0.0253 [0.01 ; 0.05], R/R 0.521, perte reelle 29.543 % (gap inclus), EV 1.9793 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.54 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.498 %) — p(stop avant cible) 0.0106 [0.00 ; 0.03], R/R 0.474, perte reelle 32.498 % (gap inclus), EV 2.04 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.50 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.452 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.434, perte reelle 35.452 % (gap inclus), EV 2.1213 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.45 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.406 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.401, perte reelle 38.406 % (gap inclus), EV 2.1298 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.41 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 41.361 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.372, perte reelle 41.361 % (gap inclus), EV 2.1425 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.36 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 44.315 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.348, perte reelle 44.315 % (gap inclus), EV 2.1425 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.31 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 47.269 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.326, perte reelle 47.269 % (gap inclus), EV 2.1425 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.27 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 104.81, ATR14 6.1929 (5.909 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.372 ATR = 2.198 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.295 % | 104.5004 | 92.85 % | 94.96 % | 95.86 % | 96.36 % | 96.95 % | 97.95 % |
| 0.1 ATR | 0.591 % | 104.1907 | 85.5 % | 90.22 % | 91.93 % | 93.43 % | 94.51 % | 96.41 % |
| 0.15 ATR | 0.886 % | 103.8811 | 77.64 % | 84.98 % | 87.69 % | 89.89 % | 92.28 % | 94.97 % |
| 0.2 ATR | 1.182 % | 103.5714 | 71.6 % | 79.84 % | 83.45 % | 86.55 % | 90.14 % | 93.22 % |
| 0.25 ATR | 1.477 % | 103.2618 | 64.45 % | 74.09 % | 78.91 % | 83.01 % | 87.5 % | 90.86 % |
| 0.35 ATR | 2.068 % | 102.6425 | 52.27 % | 65.02 % | 71.64 % | 77.25 % | 83.13 % | 87.99 % |
| 0.5 ATR | 2.954 % | 101.7136 | 36.96 % | 53.12 % | 60.65 % | 67.95 % | 76.42 % | 82.55 % |
| 0.75 ATR | 4.431 % | 100.1654 | 19.44 % | 35.99 % | 45.71 % | 55.41 % | 65.65 % | 73.51 % |
| 1.0 ATR | 5.909 % | 98.6171 | 9.26 % | 22.78 % | 32.39 % | 43.58 % | 54.88 % | 66.02 % |
| 1.25 ATR | 7.386 % | 97.0689 | 4.83 % | 14.42 % | 22.2 % | 33.16 % | 46.85 % | 59.65 % |
| 1.5 ATR | 8.863 % | 95.5207 | 2.42 % | 9.98 % | 16.25 % | 26.69 % | 39.74 % | 53.9 % |
| 2.0 ATR | 11.817 % | 92.4243 | 0.5 % | 3.93 % | 7.37 % | 15.57 % | 29.78 % | 44.46 % |
| 2.5 ATR | 14.772 % | 89.3279 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.34 % | 34.8 % |
| 3.0 ATR | 17.726 % | 86.2314 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.35 % | 26.59 % |
| 4.0 ATR | 23.635 % | 80.0386 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 35.452 % | 67.6529 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.08 ATR | 1.50 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.18 ATR | 1.34 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.26 ATR | 1.58 ATR | 1.80 ATR | 2.38 ATR | 3.09 ATR |
| **10 s.** | 0.53 ATR | 1.15 ATR | 1.31 ATR | 1.84 ATR | 2.28 ATR | 2.61 ATR | 3.63 ATR | 4.68 ATR |
| **20 s.** | 0.71 ATR | 1.71 ATR | 1.97 ATR | 2.61 ATR | 3.14 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.421–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.619–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.431 %, prix 100.1659), p(touche) 35.99 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.763–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.909 %, prix 98.6168), p(touche) 32.39 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.6 % des re-echantillons)
- **5 seance(s)** : plage utile 0.97–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.909 %, prix 98.6168), p(touche) 43.58 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.315–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.863 %, prix 95.5207), p(touche) 39.74 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.971–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.817 %, prix 92.4246), p(touche) 44.46 % (en stress 97.96 %)  ✅ optimum identifie (62.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.035 | EV/share : $0.219 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 17 % | T3 14 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 44.0 | bear 40.7 | side 15.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 524.0 (= 5 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.432% → cible +2.461% / stop −5.0%, p_fill 88%, n_eff≈36.0) : P(cible|rempli) **39%** · **EV/risk -0.043** (×p_fill ; si rempli -0.24% du capital)
  - **swing** (entrée dip −0.951% → cible +10.505% / stop −5.965%, p_fill 85%, n_eff≈34.9) : P(cible|rempli) **26%** · **EV/risk +0.077** (×p_fill ; si rempli +0.54% du capital)
  - **deep** (entrée dip −1.397% → cible +17.733% / stop −8.988%, p_fill 86%, n_eff≈35.2) : P(cible|rempli) **30%** · **EV/risk +0.344** (×p_fill ; si rempli +3.61% du capital)
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
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 59.3  _(momentum haussier)_
- **ADX** : 19.3  _(pas de tendance nette)_
- **MACD** : hist 1.217  _(pas de croisement recent)_
- **BB** : %B 0.72 · largeur 27.4%
- **ATR** : 6.19 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.052  _(distribution)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 53.7  _(transition)_
- **MA** : MA20 98.95 · MA50 101.3 · MA200 95.27  _(prix > MA20)_
- **Dist MA** : MA20 +5.9% · MA50 +3.5% · MA200 +10.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (779027 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
