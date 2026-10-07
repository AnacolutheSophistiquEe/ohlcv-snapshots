# AL2SI

**Generated** : 2026-10-07T00:13:16.079562+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.62  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (2 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €27.62 (+1.9% vs entrée) · entrée €27.11 · stop €26.63 · T1 €28.02 · R/R 1.9  
> ↳ ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.75% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -179 % hors [0,100] (R² max 0.46). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €26.99–€27.22 (mid €27.11)
- Spot actuel : €27.62 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : €26.63 (plancher anti-bruit (R/R<2) ; -1.77 % depuis l'entree)
- Targets : T1 €28.02 · R/R 1.9 | T2 €28.81 · R/R 3.54 | T3 €29.60 · R/R 5.19
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €26.63


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.82 %)** : le gap seul le franchit 0.547 % des séances (7 fois sur 1280).
   - exécution **8.14 pt plus bas** dans le cas TYPIQUE (médiane), 21.726 au p90, **28.297 au pire**
   - perte réelle **20.706 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 9.82 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0595 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.6134** [0.5395 ; 0.6836] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.4515** [0.3996 ; 0.5042] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4043** [0.3535 ; 0.4566] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.4 pt), deep (25.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.3 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.18 % contre 7.00 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2135** (β de hausse 0.9554, asymétrie 1.2702) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.89× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 26.8286 sur atr_grid (0.5 ATR, 2.865 %) — p(stop avant cible) 0.797 [0.75 ; 0.84], R/R 5.588, perte reelle 3.094 % (gap inclus), CVaR 6.509 %, EV 0.4959 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5215 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.797, borne haute 0.837 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.98 ATR (stop 8.278 %) — p(stop avant cible) 0.4814 [0.43 ; 0.53], R/R 1.858, perte reelle 9.304 % (gap inclus), EV 1.2463 % — **REFUSE**
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.16 % > budget 12.00 %
   - ⚪ sr_based a 1.4 ATR (stop 10.649 %) — p(stop avant cible) 0.3391 [0.29 ; 0.39], R/R 1.399, perte reelle 12.358 % (gap inclus), EV 2.05 % — **REFUSE**
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.23 % > budget 12.00 %
   - 🟢 support a 1.66 ATR (stop 12.128 %) — p(stop avant cible) 0.2733 [0.23 ; 0.32], R/R 1.193, perte reelle 14.495 % (gap inclus), EV 2.1922 % — **REFUSE**
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.07 % > budget 12.00 %
   - 🟢 support a 3.17 ATR (stop 20.817 %) — p(stop avant cible) 0.142 [0.11 ; 0.18], R/R 0.629, perte reelle 27.472 % (gap inclus), EV 1.3422 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.37 % > budget 12.00 %
   - 🟢 support a 4.75 ATR (stop 29.869 %) — p(stop avant cible) 0.0817 [0.06 ; 0.11], R/R 0.481, perte reelle 35.955 % (gap inclus), EV 1.5086 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.82 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.433 %) — p(stop avant cible) 0.8827 [0.85 ; 0.91], R/R 11.133, perte reelle 1.553 % (gap inclus), EV 0.4212 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 11.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.883, borne haute 0.913 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 2.865 %) — p(stop avant cible) 0.797 [0.75 ; 0.84], R/R 5.588, perte reelle 3.094 % (gap inclus), EV 0.4959 % — **REFUSE**
      - refuse : p_stop_first 0.797, borne haute 0.837 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 0.98 ATR (stop 7.355 %) — p(stop avant cible) 0.546 [0.49 ; 0.60], R/R 2.129, perte reelle 8.12 % (gap inclus), EV 0.9427 % — **REFUSE**
      - refuse : p_stop_first 0.546, borne haute 0.598 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.71 % > budget 12.00 %
   - ⚪ grid_snapped a 1.4 ATR (stop 9.726 %) — p(stop avant cible) 0.395 [0.34 ; 0.45], R/R 1.535, perte reelle 11.259 % (gap inclus), EV 1.5595 % — **REFUSE**
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.83 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 12.894 %) — p(stop avant cible) 0.26 [0.22 ; 0.31], R/R 1.066, perte reelle 16.21 % (gap inclus), EV 1.9023 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.14 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 14.327 %) — p(stop avant cible) 0.2385 [0.20 ; 0.29], R/R 0.967, perte reelle 17.875 % (gap inclus), EV 1.7514 % — **REFUSE**
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.03 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.76 %) — p(stop avant cible) 0.218 [0.18 ; 0.26], R/R 0.891, perte reelle 19.391 % (gap inclus), EV 1.683 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.48 % > budget 12.00 %
   - 🟢 grid_snapped a 3.17 ATR (stop 19.894 %) — p(stop avant cible) 0.1559 [0.12 ; 0.20], R/R 0.657, perte reelle 26.317 % (gap inclus), EV 1.3321 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.37 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.923 %) — p(stop avant cible) 0.1145 [0.08 ; 0.15], R/R 0.573, perte reelle 30.163 % (gap inclus), EV 1.5572 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.37 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 25.789 %) — p(stop avant cible) 0.0941 [0.07 ; 0.13], R/R 0.523, perte reelle 33.026 % (gap inclus), EV 1.574 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.38 % > budget 12.00 %
   - 🟢 grid_snapped a 4.75 ATR (stop 28.946 %) — p(stop avant cible) 0.082 [0.06 ; 0.11], R/R 0.488, perte reelle 35.451 % (gap inclus), EV 1.5434 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.61 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.52 %) — p(stop avant cible) 0.0794 [0.05 ; 0.11], R/R 0.467, perte reelle 37.001 % (gap inclus), EV 1.4723 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.22 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.385 %) — p(stop avant cible) 0.0605 [0.04 ; 0.09], R/R 0.432, perte reelle 40.039 % (gap inclus), EV 1.5576 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.22 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.25 %) — p(stop avant cible) 0.0512 [0.03 ; 0.08], R/R 0.409, perte reelle 42.228 % (gap inclus), EV 1.8065 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.35 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.116 %) — p(stop avant cible) 0.0345 [0.02 ; 0.06], R/R 0.384, perte reelle 44.989 % (gap inclus), EV 2.1212 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.67 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 42.981 %) — p(stop avant cible) 0.0303 [0.02 ; 0.05], R/R 0.376, perte reelle 45.961 % (gap inclus), EV 2.1403 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.29 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 45.847 %) — p(stop avant cible) 0.0303 [0.02 ; 0.05], R/R 0.369, perte reelle 46.845 % (gap inclus), EV 2.1136 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.83 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 27.62, ATR14 1.5829 (5.731 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 2.292 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.287 % | 27.5409 | 87.06 % | 90.58 % | 92.93 % | 94.39 % | 95.55 % | 97.1 % |
| 0.1 ATR | 0.573 % | 27.4617 | 82.45 % | 86.95 % | 90.18 % | 92.13 % | 94.07 % | 96.2 % |
| 0.15 ATR | 0.86 % | 27.3826 | 78.43 % | 83.32 % | 87.13 % | 88.98 % | 92.19 % | 95.1 % |
| 0.2 ATR | 1.146 % | 27.3034 | 72.65 % | 79.2 % | 83.3 % | 85.83 % | 89.81 % | 92.91 % |
| 0.25 ATR | 1.433 % | 27.2243 | 66.67 % | 74.58 % | 79.17 % | 82.48 % | 87.54 % | 91.31 % |
| 0.35 ATR | 2.006 % | 27.066 | 54.71 % | 65.65 % | 71.02 % | 75.69 % | 82.59 % | 87.81 % |
| 0.5 ATR | 2.865 % | 26.8286 | 40.49 % | 53.88 % | 61.89 % | 68.7 % | 77.94 % | 85.31 % |
| 0.75 ATR | 4.298 % | 26.4329 | 22.55 % | 37.49 % | 47.35 % | 55.61 % | 67.06 % | 76.62 % |
| 1.0 ATR | 5.731 % | 26.0371 | 12.75 % | 24.83 % | 33.79 % | 44.19 % | 57.07 % | 68.03 % |
| 1.25 ATR | 7.164 % | 25.6414 | 7.45 % | 17.47 % | 24.56 % | 36.22 % | 50.05 % | 61.54 % |
| 1.5 ATR | 8.596 % | 25.2457 | 3.63 % | 11.29 % | 17.29 % | 28.54 % | 42.63 % | 55.04 % |
| 2.0 ATR | 11.462 % | 24.4543 | 0.88 % | 5.1 % | 9.53 % | 16.63 % | 30.96 % | 43.26 % |
| 2.5 ATR | 14.327 % | 23.6629 | 0.1 % | 2.16 % | 4.52 % | 9.74 % | 20.87 % | 33.27 % |
| 3.0 ATR | 17.193 % | 22.8714 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 14.94 % | 25.87 % |
| 4.0 ATR | 22.923 % | 21.2886 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.18 % |
| 6.0 ATR | 34.385 % | 18.1229 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.60 ATR | 0.72 ATR | 0.81 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.60 ATR | 2.02 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.24 ATR | 1.41 ATR | 1.97 ATR | 2.45 ATR |
| **5 s.** | 0.36 ATR | 0.87 ATR | 0.98 ATR | 1.35 ATR | 1.65 ATR | 1.86 ATR | 2.48 ATR | 3.42 ATR |
| **10 s.** | 0.57 ATR | 1.25 ATR | 1.42 ATR | 1.91 ATR | 2.29 ATR | 2.57 ATR | 3.77 ATR | 5.11 ATR |
| **20 s.** | 0.80 ATR | 1.71 ATR | 1.93 ATR | 2.52 ATR | 3.10 ATR | 3.67 ATR | 5.56 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.452–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.865 %, prix 26.8287), p(touche) 40.49 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (91.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.635–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.298 %, prix 26.4329), p(touche) 37.49 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.793–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.731 %, prix 26.0371), p(touche) 33.79 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.982–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.731 %, prix 26.0371), p(touche) 44.19 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.42–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.596 %, prix 25.2458), p(touche) 42.63 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.926–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.462 %, prix 24.4542), p(touche) 43.26 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.038 | EV/share : €0.018 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 — | T3 —
- Kelly (position) : f* 0.042 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 10.0 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.861% → cible +3.376% / stop −1.752%, p_fill 67%, n_eff≈70.9) : P(cible|rempli) **15%** · **EV/risk -0.300** (×p_fill ; si rempli -0.79% du capital)
  - **swing** (entrée dip −4.089% → cible +8.926% / stop −5.975%, p_fill 48%, n_eff≈57.0) : P(cible|rempli) **37%** · **EV/risk -0.030** (×p_fill ; si rempli -0.37% du capital)
  - **deep** (entrée dip −6.324% → cible +11.519% / stop −9.176%, p_fill 50%, n_eff≈57.3) : P(cible|rempli) **41%** · **EV/risk -0.044** (×p_fill ; si rempli -0.82% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.19 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.5  _(momentum baissier)_
- **ADX** : 16.8  _(pas de tendance nette)_
- **MACD** : hist -0.249  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 16.9%
- **ATR** : 1.58 (42.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.041  _(neutre)_
- **Vol ratio** : 0.19  _(volume atone)_
- **Choppiness** : 48.4  _(transition)_
- **MA** : MA20 28.45 · MA50 27.58 · MA200 28.37  _(prix < MA20)_
- **Dist MA** : MA20 -2.9% · MA50 +0.1% · MA200 -2.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (521199 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
