# SMCI

**Generated** : 2026-10-01T00:24:30.691327+00:00  
**Santé technique** : 9/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $41.06  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $41.06 (+2.2% vs entrée) · entrée $40.19 · stop $37.78 · T1 $42.87 · R/R 1.11  
> ↳ ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $39.76–$40.61 (mid $40.19)
- Spot actuel : $41.06 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : $37.78 (plancher anti-bruit (R/R<2) ; -6.00 % depuis l'entree)
- Targets : T1 $42.87 · R/R 1.11 | T2 $45.56 · R/R 2.23 | T3 $48.24 · R/R 3.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $37.78


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.98 %)** : le gap seul le franchit 1.596 % des séances (20 fois sur 1253).
   - exécution **3.976 pt plus bas** dans le cas TYPIQUE (médiane), 16.897 au p90, **21.071 au pire**
   - perte réelle **14.137 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 7.98 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0983 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.795 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5093** [0.4352 ; 0.5831] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4507** [0.3988 ; 0.5034] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4333** [0.3818 ; 0.4859] _(largeur 10.4 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.34 %** | vol 5.83 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.60 % contre 6.51 % aujourd'hui, rapport 0.55)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.48 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5296** (β de hausse 1.2184, asymétrie 1.2554) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.832× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 40.4595 sur atr_grid (0.25 ATR, 1.463 %) — p(stop avant cible) 0.9091 [0.88 ; 0.94], R/R 10.423, perte reelle 1.678 % (gap inclus), CVaR 5.377 %, EV -0.0607 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.9369 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 7.5 % du temps (< 15 %) meme a 10 seances : le R/R de 10.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.909, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 5.38 % > budget 3.10 %
- Budget de queue : **3.1 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.171 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 44.7 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.66 ATR (stop 6.61 %) — p(stop avant cible) 0.5842 [0.53 ; 0.64], R/R 2.268, perte reelle 7.712 % (gap inclus), EV 0.2065 % — **REFUSE**
      - refuse : p_stop_first 0.584, borne haute 0.635 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.85 % > budget 3.10 %
      - ⚠ support DETECTE a 0.66 ATR du spot — compartiment <1, mesure a 45.4 % de casse (IC clusterise [0.423 ; 0.484] sur 1130 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 8.775 %) — p(stop avant cible) 0.449 [0.40 ; 0.50], R/R 1.696, perte reelle 10.316 % (gap inclus), EV 0.7754 % — **REFUSE**
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.34 % > budget 3.10 %
   - 🟢 support a 7.36 ATR (stop 45.797 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.381, perte reelle 45.945 % (gap inclus), EV 1.6642 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.35 % > budget 3.10 %
   - 🟢 support a 8.98 ATR (stop 55.295 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.314, perte reelle 55.79 % (gap inclus), EV 1.655 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.59 % > budget 3.10 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.463 %) — p(stop avant cible) 0.9091 [0.88 ; 0.94], R/R 10.423, perte reelle 1.678 % (gap inclus), EV -0.0607 % — **REFUSE**
      - refuse : cible atteinte seulement 7.5 % du temps (< 15 %) meme a 10 seances : le R/R de 10.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.909, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.38 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 7.5 % x 17.49 % + P(rien) 1.6 % x 9.67 % ne couvrent pas P(stop) 90.9 % x 1.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.66 ATR (stop 5.627 %) — p(stop avant cible) 0.6537 [0.60 ; 0.70], R/R 2.715, perte reelle 6.442 % (gap inclus), EV 0.1338 % — **REFUSE**
      - refuse : p_stop_first 0.654, borne haute 0.702 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.01 % > budget 3.10 %
   - ⚪ atr_grid a 1.75 ATR (stop 10.238 %) — p(stop avant cible) 0.3997 [0.35 ; 0.45], R/R 1.475, perte reelle 11.857 % (gap inclus), EV 0.8482 % — **REFUSE**
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.82 % > budget 3.10 %
   - ⚪ atr_grid a 2.0 ATR (stop 11.701 %) — p(stop avant cible) 0.3238 [0.28 ; 0.37], R/R 1.292, perte reelle 13.535 % (gap inclus), EV 1.3716 % — **REFUSE**
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.32 % > budget 3.10 %
   - ⚪ atr_grid a 2.25 ATR (stop 13.163 %) — p(stop avant cible) 0.2698 [0.23 ; 0.32], R/R 1.157, perte reelle 15.117 % (gap inclus), EV 1.505 % — **REFUSE**
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.52 % > budget 3.10 %
   - ⚪ atr_grid a 2.5 ATR (stop 14.626 %) — p(stop avant cible) 0.2292 [0.19 ; 0.28], R/R 1.042, perte reelle 16.788 % (gap inclus), EV 1.5096 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.28 % > budget 3.10 %
   - ⚪ atr_grid a 2.75 ATR (stop 16.088 %) — p(stop avant cible) 0.1974 [0.16 ; 0.24], R/R 0.944, perte reelle 18.532 % (gap inclus), EV 1.6782 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.96 % > budget 3.10 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.551 %) — p(stop avant cible) 0.1665 [0.13 ; 0.21], R/R 0.871, perte reelle 20.088 % (gap inclus), EV 1.9205 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.25 % > budget 3.10 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.476 %) — p(stop avant cible) 0.1332 [0.10 ; 0.17], R/R 0.781, perte reelle 22.394 % (gap inclus), EV 1.9902 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.56 % > budget 3.10 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.401 %) — p(stop avant cible) 0.1116 [0.08 ; 0.15], R/R 0.698, perte reelle 25.062 % (gap inclus), EV 1.9006 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.11 % > budget 3.10 %
   - ⚪ atr_grid a 4.5 ATR (stop 26.326 %) — p(stop avant cible) 0.0856 [0.06 ; 0.12], R/R 0.642, perte reelle 27.247 % (gap inclus), EV 1.8952 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.90 % > budget 3.10 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.252 %) — p(stop avant cible) 0.0789 [0.05 ; 0.11], R/R 0.594, perte reelle 29.463 % (gap inclus), EV 1.7382 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.58 % > budget 3.10 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.177 %) — p(stop avant cible) 0.0721 [0.05 ; 0.10], R/R 0.541, perte reelle 32.327 % (gap inclus), EV 1.5677 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.39 % > budget 3.10 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.102 %) — p(stop avant cible) 0.061 [0.04 ; 0.09], R/R 0.497, perte reelle 35.202 % (gap inclus), EV 1.4623 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.22 % > budget 3.10 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.027 %) — p(stop avant cible) 0.038 [0.02 ; 0.06], R/R 0.46, perte reelle 38.06 % (gap inclus), EV 1.5143 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.85 % > budget 3.10 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.952 %) — p(stop avant cible) 0.0121 [0.00 ; 0.03], R/R 0.427, perte reelle 40.952 % (gap inclus), EV 1.6578 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.55 % > budget 3.10 %
   - 🟢 grid_snapped a 7.36 ATR (stop 44.814 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.389, perte reelle 44.97 % (gap inclus), EV 1.6697 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.30 % > budget 3.10 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.803 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.37, perte reelle 47.342 % (gap inclus), EV 1.661 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.41 % > budget 3.10 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 41.06, ATR14 2.4021 (5.85 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.343 ATR = 2.007 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.293 % | 40.9399 | 90.43 % | 93.25 % | 94.65 % | 95.15 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.585 % | 40.8198 | 82.07 % | 87.2 % | 89.2 % | 91.1 % | 92.99 % | 94.87 % |
| 0.15 ATR | 0.878 % | 40.6997 | 74.92 % | 82.06 % | 84.96 % | 88.17 % | 90.65 % | 93.53 % |
| 0.2 ATR | 1.17 % | 40.5796 | 67.98 % | 77.32 % | 80.52 % | 85.64 % | 89.13 % | 92.2 % |
| 0.25 ATR | 1.463 % | 40.4595 | 61.83 % | 72.68 % | 76.29 % | 82.31 % | 87.09 % | 90.45 % |
| 0.35 ATR | 2.048 % | 40.2193 | 49.14 % | 63.31 % | 69.53 % | 77.05 % | 82.72 % | 87.78 % |
| 0.5 ATR | 2.925 % | 39.8589 | 34.94 % | 49.8 % | 58.32 % | 68.66 % | 76.93 % | 83.26 % |
| 0.75 ATR | 4.388 % | 39.2584 | 17.32 % | 33.17 % | 42.79 % | 54.9 % | 66.26 % | 75.05 % |
| 1.0 ATR | 5.85 % | 38.6579 | 7.96 % | 21.37 % | 30.27 % | 43.38 % | 56.91 % | 68.28 % |
| 1.25 ATR | 7.313 % | 38.0573 | 3.73 % | 14.72 % | 22.0 % | 32.76 % | 47.56 % | 60.68 % |
| 1.5 ATR | 8.775 % | 37.4568 | 1.51 % | 9.38 % | 16.04 % | 25.68 % | 41.36 % | 54.41 % |
| 2.0 ATR | 11.701 % | 36.2557 | 0.3 % | 3.53 % | 8.17 % | 15.87 % | 29.57 % | 43.33 % |
| 2.5 ATR | 14.626 % | 35.0546 | 0.2 % | 1.51 % | 4.24 % | 9.5 % | 19.31 % | 31.52 % |
| 3.0 ATR | 17.551 % | 33.8536 | 0.2 % | 1.21 % | 2.62 % | 5.46 % | 13.82 % | 23.72 % |
| 4.0 ATR | 23.401 % | 31.4514 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 35.102 % | 26.6471 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.57 ATR | 0.75 ATR | 0.92 ATR | 1.05 ATR | 1.47 ATR | 1.87 ATR |
| **3 s.** | 0.27 ATR | 0.63 ATR | 0.71 ATR | 0.94 ATR | 1.16 ATR | 1.33 ATR | 1.88 ATR | 2.40 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.96 ATR | 1.24 ATR | 1.53 ATR | 1.79 ATR | 2.46 ATR | 3.16 ATR |
| **10 s.** | 0.55 ATR | 1.19 ATR | 1.35 ATR | 1.85 ATR | 2.22 ATR | 2.47 ATR | 3.60 ATR | 4.90 ATR |
| **20 s.** | 0.75 ATR | 1.70 ATR | 1.93 ATR | 2.44 ATR | 2.92 ATR | 3.39 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.572–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.388 %, prix 39.2583), p(touche) 33.17 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.714–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.388 %, prix 39.2583), p(touche) 42.79 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.965–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.313 %, prix 38.0573), p(touche) 32.76 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.353–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.775 %, prix 37.457), p(touche) 41.36 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.925–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (17.551 %, prix 33.8536), p(touche) 23.72 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.052 | EV/share : $0.124 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 22 % | T3 14 %
- Kelly (position) : f* 0.04 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 83.1 | bear 5.1 | side 11.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 616.0 (= 17 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.97% → cible +2.502% / stop −2.0%, p_fill 79%, n_eff≈84.1) : P(cible|rempli) **31%** · **EV/risk -0.129** (×p_fill ; si rempli -0.33% du capital)
  - **swing** (entrée dip −2.13% → cible +6.683% / stop −5.978%, p_fill 68%, n_eff≈79.2) : P(cible|rempli) **46%** · **EV/risk -0.009** (×p_fill ; si rempli -0.08% du capital)
  - **deep** (entrée dip −3.291% → cible +18.715% / stop −9.357%, p_fill 67%, n_eff≈74.4) : P(cible|rempli) **31%** · **EV/risk +0.243** (×p_fill ; si rempli +3.38% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→62% · +3.0%→43% · +5.0%→22% · +8.0%→9%
- Range intraday médian 5.81% (p90 9.37%) · excursion haute méd. +2.54% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.806% vs midi 1.166% vs clôture 1.479% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 69% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr -0.014)_ ; drift intra méd. 0.238% ; recovery-V 35%
- **σ réalisé intraday** 3.449% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 61% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 41.2899 (VA 41.1089–41.7876 ; dernier close 41.03)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 24% · rebond 77% · **stop −4.34%** sous le fill (sous le bruit) · cible +2.19% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.18% · baisse 43% (gap-down >1% 33% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.92% (p90 −2.64%) · haut méd +1.03% · range méd 2.15%
- Excursion ouverture 15min (n=160) : bas méd −1.12% (p90 −3.11%) · haut méd +1.37% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.6%) · haut méd +1.57% · range méd 3.49%
- Excursion ouverture 60min (n=160) : bas méd −1.62% (p90 −4.12%) · haut méd +1.85% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 41.02 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 71% (117/159) · gap 39% · délai 0.0min · rebond 55% (69/117) (MFE +1.31%)
   - −1.0% : fill 30min 52% · séance 67% (109/159) · gap 33% · délai 0.0min · rebond 56% (63/109) (MFE +1.3%)
   - −1.5% : fill 30min 48% · séance 63% (100/159) · gap 21% · délai 0.2min · rebond 68% (65/100) (MFE +1.41%)
   - −2.0% : fill 30min 41% · séance 54% (87/159) · gap 16% · délai 0.7min · rebond 71% (57/87) (MFE +1.7%)
   - −3.0% : fill 30min 27% · séance 46% (74/159) · gap 8% · délai 13.1min · rebond 64% (45/74) (MFE +1.42%)
   - −4.0% : fill 30min 14% · séance 33% (54/159) · gap 4% · délai 41.4min · rebond 72% (35/54) (MFE +1.7%)
   - −5.0% : fill 30min 10% · séance 24% (43/159) · gap 3% · délai 52.5min · rebond 77% (31/43) (MFE +2.19%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −2.8%) → stop au-delà de −1.95% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.59% (p90 −2.77%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.62% (p90 −2.36%) → stop au-delà de −1.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=878 jambes) : jambe baissière méd −1.19% (p90 −2.78%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 97% (68/70) · rebond 45% (35/68)
      · −2.0% : fill 94% (64/70) · rebond 73% (40/64)
      · −3.0% : fill 88% (58/70) · rebond 65% (35/58)
      · −4.0% : fill 64% (43/70) · rebond 71% (28/43)
      · −5.0% : fill 48% (34/70) · rebond 76% (24/34)
   - **flat** (13 séances) :
      · −1.0% : fill 85% (12/13) · rebond 75% (9/12)
      · −2.0% : fill 36% (5/13) · rebond 50% (3/5)
      · −3.0% : fill 29% (3/13) · rebond 43% (2/3)
      · −4.0% : fill 10% (1/13) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 37% (29/76) · rebond 71% (19/29)
      · −2.0% : fill 23% (18/76) · rebond 70% (14/18)
      · −3.0% : fill 13% (13/76) · rebond 69% (8/13)
      · −4.0% : fill 10% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 9% (9/76) · rebond 84% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 65% si les 15 1res min sont vertes (79 cas) · 28% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 82% si début vert vs 13% si rouge (base 47% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **82%** · continue >prix actuel 52% ; creux résiduel méd -1.47% (q20 -3.22%) → **SL/trailing à −3.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.54% / q75 +2.67% → **scale +1.54% / runner +2.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **13%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.28%** (au-delà de la MAE q10 -3.28%), cible rebond +1.96% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.9% .. +4.13%] · haut q95 +5.2% · bas q05 -4.19%
   - 60min (n=160) : retour [-4.12% .. +5.43%] · haut q95 +6.58% · bas q05 -5.28%
   - 2h (n=160) : retour [-4.23% .. +6.1%] · haut q95 +7.38% · bas q05 -5.67%
   - 4h (n=160) : retour [-4.58% .. +6.73%] · haut q95 +7.83% · bas q05 -6.23%
   - 6h (n=160) : retour [-5.09% .. +6.64%] · haut q95 +8.75% · bas q05 -6.59%
   - session (n=160) : retour [-4.98% .. +6.93%] · haut q95 +9.02% · bas q05 -6.92%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.55%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.5 · part idiosyncratique 0.5
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.3  _(momentum haussier)_
- **ADX** : 26.7  _(tendance etablie)_
- **MACD** : hist 0.001  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 21.2%
- **ATR** : 2.4 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.032  _(neutre)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 52.6  _(transition)_
- **MA** : MA20 39.63 · MA50 36.04 · MA200 31.89  _(prix > MA20)_
- **Dist MA** : MA20 +3.6% · MA50 +13.9% · MA200 +28.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (846339 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
