# SAF

**Generated** : 2026-10-01T00:09:03.988277+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €334.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €334.30 (+6.8% vs entrée) · entrée €312.93 · stop €305.08 · T1 €321.71 · R/R 1.12  
> ↳ ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.090 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €311.74–€314.12 (mid €312.93)
- Spot actuel : €334.30 (+6.8% au-dessus de la zone — repli à attendre)
- Stop : €305.08 (plancher anti-bruit (R/R<2) ; -2.51 % depuis l'entree)
- Targets : T1 €321.71 · R/R 1.12 | T2 €330.48 · R/R 2.24 | T3 €339.26 · R/R 3.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €305.08


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.74 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **1.246 pt plus bas** dans le cas TYPIQUE (médiane), 1.246 au p90, **1.246 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 8.74 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.001 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.396 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0** [0.0 ; 0.0144] _(largeur 1.4 pt, n_eff 173.1)_
   - swing : **0.4236** [0.3723 ; 0.4761] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3764** [0.3265 ; 0.4283] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 13.9 observations effectives », dont la borne haute a 95 % vaut environ 21.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (48.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.21 %** | CVaR **-4.01 %** | vol 2.08 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.35 % contre 2.20 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.06 % si l'on extrapolait par √5 _(rapport 0.934 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3874** (β de hausse 1.3517, asymétrie 1.0264) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 324.4875 sur atr_grid (1.25 ATR, 2.935 %) — p(stop avant cible) 0.5117 [0.46 ; 0.56], R/R 2.653, perte reelle 3.043 % (gap inclus), CVaR 3.932 %, EV 0.6257 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1412 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.512, borne haute 0.564 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.522 %) — p(stop avant cible) 0.4277 [0.38 ; 0.48], R/R 2.234, perte reelle 3.614 % (gap inclus), EV 0.7031 % — **REFUSE**
      - refuse : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 2.16 ATR (stop 6.563 %) — p(stop avant cible) 0.1918 [0.15 ; 0.24], R/R 1.218, perte reelle 6.631 % (gap inclus), EV 0.8815 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 5.05 ATR (stop 13.343 %) — p(stop avant cible) 0.0302 [0.02 ; 0.05], R/R 0.57, perte reelle 14.161 % (gap inclus), EV 0.6865 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.73 % > budget 12.00 %
   - 🟢 support a 9.51 ATR (stop 23.807 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.339, perte reelle 23.807 % (gap inclus), EV 0.7286 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.25 ATR (stop 0.587 %) — p(stop avant cible) 0.8893 [0.85 ; 0.92], R/R 13.222, perte reelle 0.611 % (gap inclus), EV 0.1186 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 13.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.889, borne haute 0.919 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.174 %) — p(stop avant cible) 0.7714 [0.72 ; 0.81], R/R 6.575, perte reelle 1.228 % (gap inclus), EV 0.3001 % — **REFUSE**
      - refuse : cible atteinte seulement 9.6 % du temps (< 15 %) meme a 10 seances : le R/R de 6.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.771, borne haute 0.813 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 1.761 %) — p(stop avant cible) 0.6757 [0.63 ; 0.72], R/R 4.395, perte reelle 1.837 % (gap inclus), EV 0.395 % — **REFUSE**
      - refuse : cible atteinte seulement 12.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.676, borne haute 0.723 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 2.348 %) — p(stop avant cible) 0.6039 [0.55 ; 0.65], R/R 3.304, perte reelle 2.444 % (gap inclus), EV 0.4757 % — **REFUSE**
      - refuse : p_stop_first 0.604, borne haute 0.654 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 2.935 %) — p(stop avant cible) 0.5117 [0.46 ; 0.56], R/R 2.653, perte reelle 3.043 % (gap inclus), EV 0.6257 % — **REFUSE**
      - refuse : p_stop_first 0.512, borne haute 0.564 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 4.109 %) — p(stop avant cible) 0.3604 [0.31 ; 0.41], R/R 1.923, perte reelle 4.198 % (gap inclus), EV 0.8378 % — **REFUSE**
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.16 ATR (stop 5.781 %) — p(stop avant cible) 0.2397 [0.20 ; 0.29], R/R 1.38, perte reelle 5.852 % (gap inclus), EV 0.9468 % — **REFUSE**
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 7.045 %) — p(stop avant cible) 0.1577 [0.12 ; 0.20], R/R 1.136, perte reelle 7.105 % (gap inclus), EV 0.8655 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 8.219 %) — p(stop avant cible) 0.1101 [0.08 ; 0.15], R/R 0.96, perte reelle 8.415 % (gap inclus), EV 0.8176 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 9.393 %) — p(stop avant cible) 0.0853 [0.06 ; 0.12], R/R 0.837, perte reelle 9.649 % (gap inclus), EV 0.7501 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 10.567 %) — p(stop avant cible) 0.0671 [0.04 ; 0.10], R/R 0.742, perte reelle 10.88 % (gap inclus), EV 0.7158 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 5.05 ATR (stop 12.561 %) — p(stop avant cible) 0.0389 [0.02 ; 0.06], R/R 0.605, perte reelle 13.346 % (gap inclus), EV 0.7012 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.43 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 12.915 %) — p(stop avant cible) 0.0388 [0.02 ; 0.06], R/R 0.592, perte reelle 13.633 % (gap inclus), EV 0.6913 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.65 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 14.089 %) — p(stop avant cible) 0.021 [0.01 ; 0.04], R/R 0.525, perte reelle 15.393 % (gap inclus), EV 0.6801 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.87 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 15.263 %) — p(stop avant cible) 0.0119 [0.00 ; 0.03], R/R 0.466, perte reelle 17.325 % (gap inclus), EV 0.6901 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.66 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 16.437 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 0.414, perte reelle 19.493 % (gap inclus), EV 0.7019 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.42 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 17.611 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.408, perte reelle 19.773 % (gap inclus), EV 0.702 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.45 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 18.786 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 0.396, perte reelle 20.416 % (gap inclus), EV 0.7131 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.20 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 334.3, ATR14 7.85 (2.348 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 0.808 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.117 % | 333.9075 | 89.22 % | 92.54 % | 93.71 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.235 % | 333.515 | 81.37 % | 87.14 % | 89.1 % | 91.34 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.352 % | 333.1225 | 75.0 % | 83.22 % | 86.15 % | 88.58 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.47 % | 332.73 | 67.94 % | 77.92 % | 82.42 % | 85.14 % | 88.82 % | 90.91 % |
| 0.25 ATR | 0.587 % | 332.3375 | 60.88 % | 73.41 % | 78.78 % | 83.07 % | 87.54 % | 90.01 % |
| 0.35 ATR | 0.822 % | 331.5525 | 49.31 % | 63.3 % | 69.65 % | 76.77 % | 82.59 % | 87.01 % |
| 0.5 ATR | 1.174 % | 330.375 | 35.2 % | 51.72 % | 58.94 % | 68.31 % | 75.87 % | 81.52 % |
| 0.75 ATR | 1.761 % | 328.4125 | 20.49 % | 35.23 % | 42.53 % | 52.85 % | 63.01 % | 70.93 % |
| 1.0 ATR | 2.348 % | 326.45 | 9.8 % | 23.55 % | 32.22 % | 41.83 % | 53.51 % | 61.64 % |
| 1.25 ATR | 2.935 % | 324.4875 | 4.41 % | 15.21 % | 23.67 % | 32.87 % | 46.09 % | 54.85 % |
| 1.5 ATR | 3.522 % | 322.525 | 2.25 % | 9.91 % | 16.4 % | 24.7 % | 37.88 % | 46.95 % |
| 2.0 ATR | 4.696 % | 318.6 | 0.98 % | 4.42 % | 7.47 % | 15.16 % | 26.71 % | 37.16 % |
| 2.5 ATR | 5.87 % | 314.675 | 0.2 % | 1.47 % | 3.63 % | 8.56 % | 18.2 % | 28.47 % |
| 3.0 ATR | 7.045 % | 310.75 | 0.0 % | 0.88 % | 2.06 % | 5.71 % | 12.07 % | 22.28 % |
| 4.0 ATR | 9.393 % | 302.9 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 4.55 % | 10.89 % |
| 6.0 ATR | 14.089 % | 287.2 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.67 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.50 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.71 ATR | 0.98 ATR | 1.21 ATR | 1.38 ATR | 1.86 ATR | 2.32 ATR |
| **5 s.** | 0.38 ATR | 0.81 ATR | 0.93 ATR | 1.25 ATR | 1.49 ATR | 1.75 ATR | 2.39 ATR | 3.15 ATR |
| **10 s.** | 0.52 ATR | 1.12 ATR | 1.28 ATR | 1.72 ATR | 2.10 ATR | 2.39 ATR | 3.27 ATR | 3.94 ATR |
| **20 s.** | 0.65 ATR | 1.40 ATR | 1.60 ATR | 2.24 ATR | 2.78 ATR | 3.20 ATR | 4.23 ATR | 5.49 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.602–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.761 %, prix 328.413), p(touche) 35.23 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.712–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.761 %, prix 328.413), p(touche) 42.53 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.928–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.348 %, prix 326.4506), p(touche) 41.83 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.283–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.522 %, prix 322.5259), p(touche) 37.88 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.6–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.696 %, prix 318.6013), p(touche) 37.16 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.006 | EV/share : €0.050 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 16 % | T3 9 %
- Kelly (position) : f* 0.005 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 42.0 | bear 53.0 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 334.0 (= 1 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.902% → cible +1.209% / stop −8.0%, p_fill 11%, n_eff≈13.9) : P(cible|rempli) **47%** · **EV/risk +0.002** (×p_fill ; si rempli +0.17% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→49% · +2.0%→25% · +3.0%→9% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.49% (p90 4.12%) · excursion haute méd. +0.95% / basse méd. −0.99%
- Profil de vol intra : ouverture 1.514% vs midi 0.548% vs clôture 0.689% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 40% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.105 ; mean-reverting — autocorr -0.058)_ ; drift intra méd. -0.3% ; recovery-V 22%
- **σ réalisé intraday** 1.487% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 69% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 337.0263 (VA 335.0512–338.6063 ; dernier close 335.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 23% · rebond 32% · **stop −1.5%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. 0.3% · baisse 32% (gap-down >1% 1% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.39%) · haut méd +0.19% · range méd 0.78%
- Excursion ouverture 15min (n=160) : bas méd −0.44% (p90 −1.6%) · haut méd +0.33% · range méd 1.01%
- Excursion ouverture 30min (n=160) : bas méd −0.47% (p90 −1.7%) · haut méd +0.48% · range méd 1.09%
- Excursion ouverture 60min (n=160) : bas méd −0.62% (p90 −1.83%) · haut méd +0.52% · range méd 1.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 335.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 47% · séance 58% (90/159) · gap 9% · délai 0.5min · rebond 38% (35/90) (MFE +0.81%)
   - −1.0% : fill 30min 23% · séance 48% (73/159) · gap 1% · délai 32.9min · rebond 45% (35/73) (MFE +0.83%)
   - −1.5% : fill 30min 9% · séance 27% (45/159) · gap 0% · délai 71.0min · rebond 30% (18/45) (MFE +0.56%)
   - −2.0% : fill 30min 3% · séance 23% (37/159) · gap 0% · délai 173.6min · rebond 32% (14/37) (MFE +0.74%)
   - −3.0% : fill 30min 1% · séance 9% (16/159) · gap 0% · délai 398.1min · rebond 20% (6/16) (MFE +0.54%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 282.8min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −0.99%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.68%) → stop au-delà de −0.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.09% (p90 −0.98%) → stop au-delà de −0.66% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=200 jambes) : jambe baissière méd −1.1% (p90 −2.5%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 80% (18/22) · rebond 18% (5/18)
      · −2.0% : fill 47% (12/22) · rebond 31% (5/12)
      · −3.0% : fill 24% (6/22) · rebond 18% (2/6)
      · −4.0% : fill 5% (2/22) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/22) · rebond 0% (0/0)
   - **flat** (43 séances) :
      · −1.0% : fill 58% (24/43) · rebond 48% (13/24)
      · −2.0% : fill 32% (11/43) · rebond 23% (2/11)
      · −3.0% : fill 12% (4/43) · rebond 19% (1/4)
      · −4.0% : fill 0% (0/43) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/43) · rebond 0% (0/0)
   - **gap-up** (94 séances) :
      · −1.0% : fill 31% (31/94) · rebond 60% (17/31)
      · −2.0% : fill 9% (14/94) · rebond 56% (7/14)
      · −3.0% : fill 4% (6/94) · rebond 27% (3/6)
      · −4.0% : fill 1% (2/94) · rebond 38% (1/2)
      · −5.0% : fill 0% (1/94) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 70% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 81% si début vert vs 21% si rouge (base 47% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 34min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **81%** · continue >prix actuel 61% ; creux résiduel méd -0.73% (q20 -1.18%) → **SL/trailing à −1.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.0% / q75 +1.3% → **scale +1.0% / runner +1.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **21%** (continue à baisser 57%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.26%** (au-delà de la MAE q10 -2.26%), cible rebond +0.84% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.5% .. +1.32%] · haut q95 +1.8% · bas q05 -1.97%
   - 60min (n=160) : retour [-1.64% .. +1.64%] · haut q95 +1.93% · bas q05 -1.99%
   - 2h (n=160) : retour [-1.84% .. +1.77%] · haut q95 +2.38% · bas q05 -2.49%
   - 4h (n=160) : retour [-1.87% .. +1.84%] · haut q95 +2.54% · bas q05 -2.75%
   - 6h (n=160) : retour [-2.1% .. +2.06%] · haut q95 +2.56% · bas q05 -2.82%
   - session (n=160) : retour [-2.88% .. +2.04%] · haut q95 +2.85% · bas q05 -3.47%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.67%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.5 · part idiosyncratique 0.5
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 60.5  _(momentum haussier)_
- **ADX** : 12.7  _(pas de tendance nette)_
- **MACD** : hist 1.339  _(pas de croisement recent)_
- **BB** : %B 0.7 · largeur 6.2%
- **ATR** : 7.85 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.092  _(distribution)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 62.2  _(marche en range (choppy))_
- **MA** : MA20 330.16 · MA50 340.08 · MA200 314.97  _(prix > MA20)_
- **Dist MA** : MA20 +1.3% · MA50 -1.7% · MA200 +6.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (841641 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
