# SAF

**Generated** : 2026-09-30T00:12:06.166451+00:00  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €335.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €335.60 (+7.0% vs entrée) · entrée €313.52 · stop €305.82 · T1 €319.52 · R/R 0.78  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €312.31–€314.72 (mid €313.52)
- Spot actuel : €335.60 (+7.0% au-dessus de la zone — repli à attendre)
- Stop : €305.82 (plancher anti-bruit (R/R<2) ; -2.46 % depuis l'entree)
- Targets : T1 €319.52 · R/R 0.78 | T2 €325.53 · R/R 1.56 | T3 €331.54 · R/R 2.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €305.82


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.87 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **1.116 pt plus bas** dans le cas TYPIQUE (médiane), 1.116 au p90, **1.116 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 8.87 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0009 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.396 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3973** [0.3266 ; 0.4714] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.3893** [0.339 ; 0.4414] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3434** [0.2948 ; 0.3946] _(largeur 10.0 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (48.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.21 %** | CVaR **-4.01 %** | vol 2.08 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.36 % contre 2.21 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.06 % si l'on extrapolait par √5 _(rapport 0.934 ; < 1 = le √5 surestime)_
- **β de baisse : 1.386** (β de hausse 1.3517, asymétrie 1.0254) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 325.9839 sur atr_grid (1.25 ATR, 2.865 %) — p(stop avant cible) 0.5243 [0.47 ; 0.58], R/R 2.576, perte reelle 2.977 % (gap inclus), CVaR 3.906 %, EV 0.5665 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1896 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.524, borne haute 0.577 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.438 %) — p(stop avant cible) 0.4408 [0.39 ; 0.49], R/R 2.184, perte reelle 3.512 % (gap inclus), EV 0.67 % — **REFUSE**
      - refuse : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 2.37 ATR (stop 6.769 %) — p(stop avant cible) 0.1845 [0.15 ; 0.23], R/R 1.123, perte reelle 6.83 % (gap inclus), EV 0.8074 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 5.32 ATR (stop 13.528 %) — p(stop avant cible) 0.0304 [0.02 ; 0.05], R/R 0.536, perte reelle 14.311 % (gap inclus), EV 0.6275 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.85 % > budget 12.00 %
   - 🟢 support a 9.87 ATR (stop 23.956 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.32, perte reelle 23.956 % (gap inclus), EV 0.6747 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.25 ATR (stop 0.573 %) — p(stop avant cible) 0.8908 [0.85 ; 0.92], R/R 12.838, perte reelle 0.597 % (gap inclus), EV 0.1186 % — **REFUSE**
      - refuse : cible atteinte seulement 6.0 % du temps (< 15 %) meme a 10 seances : le R/R de 12.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.891, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.146 %) — p(stop avant cible) 0.7766 [0.73 ; 0.82], R/R 6.382, perte reelle 1.202 % (gap inclus), EV 0.2912 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 6.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.777, borne haute 0.818 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 1.719 %) — p(stop avant cible) 0.6928 [0.64 ; 0.74], R/R 4.267, perte reelle 1.797 % (gap inclus), EV 0.3437 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.693, borne haute 0.740 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 2.292 %) — p(stop avant cible) 0.6117 [0.56 ; 0.66], R/R 3.218, perte reelle 2.384 % (gap inclus), EV 0.4488 % — **REFUSE**
      - refuse : p_stop_first 0.612, borne haute 0.662 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 2.865 %) — p(stop avant cible) 0.5243 [0.47 ; 0.58], R/R 2.576, perte reelle 2.977 % (gap inclus), EV 0.5665 % — **REFUSE**
      - refuse : p_stop_first 0.524, borne haute 0.577 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 4.011 %) — p(stop avant cible) 0.3805 [0.33 ; 0.43], R/R 1.868, perte reelle 4.105 % (gap inclus), EV 0.7735 % — **REFUSE**
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 4.585 %) — p(stop avant cible) 0.3256 [0.28 ; 0.38], R/R 1.645, perte reelle 4.663 % (gap inclus), EV 0.7892 % — **REFUSE**
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.37 ATR (stop 6.122 %) — p(stop avant cible) 0.224 [0.18 ; 0.27], R/R 1.239, perte reelle 6.188 % (gap inclus), EV 0.8777 % — **REFUSE**
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 8.023 %) — p(stop avant cible) 0.1303 [0.10 ; 0.17], R/R 0.94, perte reelle 8.156 % (gap inclus), EV 0.7597 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 9.169 %) — p(stop avant cible) 0.0892 [0.06 ; 0.12], R/R 0.81, perte reelle 9.471 % (gap inclus), EV 0.7101 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 10.315 %) — p(stop avant cible) 0.0676 [0.04 ; 0.10], R/R 0.73, perte reelle 10.5 % (gap inclus), EV 0.6864 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 11.461 %) — p(stop avant cible) 0.0558 [0.04 ; 0.08], R/R 0.652, perte reelle 11.763 % (gap inclus), EV 0.6476 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 5.32 ATR (stop 12.881 %) — p(stop avant cible) 0.039 [0.02 ; 0.06], R/R 0.564, perte reelle 13.606 % (gap inclus), EV 0.6386 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.65 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 14.9 %) — p(stop avant cible) 0.0147 [0.01 ; 0.03], R/R 0.459, perte reelle 16.723 % (gap inclus), EV 0.6244 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.92 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 16.046 %) — p(stop avant cible) 0.0088 [0.00 ; 0.02], R/R 0.417, perte reelle 18.376 % (gap inclus), EV 0.6362 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.68 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 17.192 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 0.39, perte reelle 19.677 % (gap inclus), EV 0.6474 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.46 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 18.338 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.381, perte reelle 20.148 % (gap inclus), EV 0.6527 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.36 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 335.6, ATR14 7.6929 (2.292 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 0.789 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.115 % | 335.2154 | 89.22 % | 92.54 % | 93.71 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.229 % | 334.8307 | 81.37 % | 87.14 % | 89.1 % | 91.34 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.344 % | 334.4461 | 75.0 % | 83.22 % | 86.15 % | 88.58 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.458 % | 334.0614 | 67.94 % | 77.92 % | 82.42 % | 85.14 % | 88.82 % | 90.91 % |
| 0.25 ATR | 0.573 % | 333.6768 | 60.98 % | 73.41 % | 78.78 % | 83.07 % | 87.54 % | 90.01 % |
| 0.35 ATR | 0.802 % | 332.9075 | 49.31 % | 63.3 % | 69.65 % | 76.77 % | 82.59 % | 87.01 % |
| 0.5 ATR | 1.146 % | 331.7536 | 35.2 % | 51.72 % | 58.94 % | 68.41 % | 75.87 % | 81.52 % |
| 0.75 ATR | 1.719 % | 329.8304 | 20.49 % | 35.33 % | 42.53 % | 52.95 % | 63.11 % | 70.93 % |
| 1.0 ATR | 2.292 % | 327.9071 | 9.8 % | 23.55 % | 32.22 % | 41.83 % | 53.51 % | 61.54 % |
| 1.25 ATR | 2.865 % | 325.9839 | 4.41 % | 15.21 % | 23.67 % | 32.87 % | 46.09 % | 54.75 % |
| 1.5 ATR | 3.438 % | 324.0607 | 2.25 % | 9.91 % | 16.4 % | 24.7 % | 37.88 % | 46.85 % |
| 2.0 ATR | 4.585 % | 320.2143 | 0.98 % | 4.42 % | 7.47 % | 15.16 % | 26.71 % | 37.16 % |
| 2.5 ATR | 5.731 % | 316.3679 | 0.2 % | 1.47 % | 3.63 % | 8.56 % | 18.2 % | 28.47 % |
| 3.0 ATR | 6.877 % | 312.5214 | 0.0 % | 0.88 % | 2.06 % | 5.71 % | 12.07 % | 22.28 % |
| 4.0 ATR | 9.169 % | 304.8286 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 4.55 % | 10.89 % |
| 6.0 ATR | 13.754 % | 289.4428 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.67 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.50 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.71 ATR | 0.98 ATR | 1.21 ATR | 1.38 ATR | 1.86 ATR | 2.32 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.25 ATR | 1.49 ATR | 1.75 ATR | 2.39 ATR | 3.15 ATR |
| **10 s.** | 0.52 ATR | 1.12 ATR | 1.28 ATR | 1.72 ATR | 2.10 ATR | 2.39 ATR | 3.27 ATR | 3.94 ATR |
| **20 s.** | 0.65 ATR | 1.40 ATR | 1.59 ATR | 2.24 ATR | 2.78 ATR | 3.20 ATR | 4.23 ATR | 5.49 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.719 %, prix 329.831), p(touche) 35.33 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.712–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.719 %, prix 329.831), p(touche) 42.53 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.929–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.292 %, prix 327.9081), p(touche) 41.83 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.283–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.438 %, prix 324.0621), p(touche) 37.88 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.595–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.585 %, prix 320.2127), p(touche) 37.16 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : €-0.103 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 29 % | T3 16 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 44.0 | bear 51.0 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 336.0 (= 1 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.99% → cible +0.857% / stop −1.0%, p_fill 10%, n_eff≈14.0) : P(cible|rempli) **55%** · **EV/risk -0.001** (×p_fill ; si rempli -0.01% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→50% · +2.0%→26% · +3.0%→10% · +5.0%→3% · +8.0%→2%
- Range intraday médian 2.57% (p90 4.49%) · excursion haute méd. +1.01% / basse méd. −1.07%
- Profil de vol intra : ouverture 1.554% vs midi 0.586% vs clôture 0.715% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 42% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; mean-reverting — autocorr -0.072)_ ; drift intra méd. -0.3% ; recovery-V 12%
- **σ réalisé intraday** 1.555% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 61% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 331.8075 (VA 331.3325–332.7575 ; dernier close 333.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 22% · rebond 35% · **stop −1.26%** sous le fill (sous le bruit) · cible +0.73% · R/R 0.58 (high win-rate)
- Gaps overnight (n=159) : méd. 0.3% · baisse 30% (gap-down >1% 1% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.58%) · haut méd +0.18% · range méd 0.85%
- Excursion ouverture 15min (n=160) : bas méd −0.47% (p90 −1.76%) · haut méd +0.31% · range méd 1.02%
- Excursion ouverture 30min (n=160) : bas méd −0.48% (p90 −1.78%) · haut méd +0.44% · range méd 1.22%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.84%) · haut méd +0.53% · range méd 1.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 333.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 60% (86/159) · gap 10% · délai 0.4min · rebond 38% (34/86) (MFE +0.84%)
   - −1.0% : fill 30min 24% · séance 48% (69/159) · gap 1% · délai 28.0min · rebond 43% (32/69) (MFE +0.83%)
   - −1.5% : fill 30min 10% · séance 28% (43/159) · gap 0% · délai 148.6min · rebond 30% (17/43) (MFE +0.52%)
   - −2.0% : fill 30min 4% · séance 22% (35/159) · gap 0% · délai 278.4min · rebond 35% (15/35) (MFE +0.73%)
   - −3.0% : fill 30min 1% · séance 6% (13/159) · gap 0% · délai 351.3min · rebond 40% (6/13) (MFE +0.55%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 282.8min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −0.76%) → stop au-delà de −0.67% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.09% (p90 −0.69%) → stop au-delà de −0.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.09% (p90 −0.98%) → stop au-delà de −0.66% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=208 jambes) : jambe baissière méd −1.06% (p90 −2.26%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (20 séances) :
      · −1.0% : fill 75% (16/20) · rebond 26% (5/16)
      · −2.0% : fill 47% (11/20) · rebond 39% (5/11)
      · −3.0% : fill 17% (5/20) · rebond 31% (2/5)
      · −4.0% : fill 7% (2/20) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/20) · rebond 0% (0/0)
   - **flat** (37 séances) :
      · −1.0% : fill 48% (19/37) · rebond 40% (10/19)
      · −2.0% : fill 25% (8/37) · rebond 13% (1/8)
      · −3.0% : fill 4% (2/37) · rebond 76% (1/2)
      · −4.0% : fill 0% (0/37) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/37) · rebond 0% (0/0)
   - **gap-up** (102 séances) :
      · −1.0% : fill 39% (34/102) · rebond 54% (17/34)
      · −2.0% : fill 13% (16/102) · rebond 58% (9/16)
      · −3.0% : fill 5% (6/102) · rebond 27% (3/6)
      · −4.0% : fill 2% (2/102) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/102) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 70% si les 15 1res min sont vertes (73 cas) · 26% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 76% si début vert vs 21% si rouge (base 47% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **76%** · continue >prix actuel 50% ; creux résiduel méd -0.72% (q20 -1.35%) → **SL/trailing à −1.35%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.93% / q75 +1.39% → **scale +0.93% / runner +1.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **21%** (continue à baisser 60%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.3%** (au-delà de la MAE q10 -2.3%), cible rebond +0.78% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.49% .. +1.54%] · haut q95 +1.94% · bas q05 -2.06%
   - 60min (n=160) : retour [-1.63% .. +1.82%] · haut q95 +1.99% · bas q05 -2.34%
   - 2h (n=160) : retour [-2.33% .. +2.07%] · haut q95 +2.49% · bas q05 -2.93%
   - 4h (n=160) : retour [-1.87% .. +2.02%] · haut q95 +2.65% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.07% .. +2.22%] · haut q95 +2.76% · bas q05 -2.99%
   - session (n=160) : retour [-2.7% .. +2.25%] · haut q95 +3.27% · bas q05 -3.82%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.56 · part idiosyncratique 0.44
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 60.9  _(momentum haussier)_
- **ADX** : 13.6  _(pas de tendance nette)_
- **MACD** : hist 1.459  _(pas de croisement recent)_
- **BB** : %B 0.78 · largeur 6.1%
- **ATR** : 7.69 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.122  _(distribution)_
- **Vol ratio** : 0.43  _(volume atone)_
- **Choppiness** : 61.2  _(transition)_
- **MA** : MA20 329.91 · MA50 339.95 · MA200 314.75  _(prix > MA20)_
- **Dist MA** : MA20 +1.7% · MA50 -1.3% · MA200 +6.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (842925 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
