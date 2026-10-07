# HOOD

**Generated** : 2026-10-07T00:31:44.609491+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $112.01  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)  
> ↳ spot $112.01 (+5.0% vs entrée) · entrée $106.63 · stop $100.98 · T1 $112.96 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -1.0 % ≠ (strike 113.0 − spot 112.01)/spot = +0.9 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $105.80–$107.47 (mid $106.63)
- Spot actuel : $112.01 (+5.0% au-dessus de la zone — repli à attendre)
- Stop : $100.98 (plancher anti-bruit (R/R<2) ; -5.30 % depuis l'entree)
- Targets : T1 $112.96 · R/R 1.12 | T2 $119.28 · R/R 2.24 | T3 $125.61 · R/R 3.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $100.98


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.85 %)** : le gap seul le franchit 0.559 % des séances (7 fois sur 1253).
   - exécution **1.269 pt plus bas** dans le cas TYPIQUE (médiane), 5.74 au p90, **7.935 au pire**
   - perte réelle **12.322 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 9.85 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0138 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.416 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3051** [0.2402 ; 0.3765] _(largeur 13.6 pt, n_eff 173.1)_
   - swing : **0.5063** [0.4537 ; 0.5588] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4355** [0.384 ; 0.4881] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (25.2 pt), swing (32.5 pt), deep (32.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-5.9 %** | CVaR **-8.88 %** | vol 4.27 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.57 % contre 4.52 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7704** (β de hausse 1.6173, asymétrie 1.0946) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.402× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 107.8315 sur grid_snapped (0.44 ATR, 3.73 %) — p(stop avant cible) 0.7043 [0.65 ; 0.75], R/R 3.112, perte reelle 3.901 % (gap inclus), CVaR 6.008 %, EV 0.431 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3647 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.704, borne haute 0.751 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.44 ATR (stop 4.544 %) — p(stop avant cible) 0.6563 [0.61 ; 0.70], R/R 2.547, perte reelle 4.767 % (gap inclus), EV 0.4011 % — **REFUSE**
      - refuse : p_stop_first 0.656, borne haute 0.705 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_based a 1.5 ATR (stop 7.576 %) — p(stop avant cible) 0.4951 [0.44 ; 0.55], R/R 1.534, perte reelle 7.912 % (gap inclus), EV 0.6448 % — **REFUSE**
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 2.0 ATR (stop 12.443 %) — p(stop avant cible) 0.2561 [0.21 ; 0.30], R/R 0.924, perte reelle 13.144 % (gap inclus), EV 1.8774 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.02 % > budget 12.00 %
   - 🟢 support a 3.64 ATR (stop 20.693 %) — p(stop avant cible) 0.0691 [0.05 ; 0.10], R/R 0.577, perte reelle 21.037 % (gap inclus), EV 2.265 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.17 % > budget 12.00 %
   - 🟢 support a 5.85 ATR (stop 31.861 %) — p(stop avant cible) 0.0132 [0.00 ; 0.03], R/R 0.379, perte reelle 32.018 % (gap inclus), EV 2.3482 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.01 % > budget 12.00 %
   - ⚪ grid_snapped a 0.44 ATR (stop 3.73 %) — p(stop avant cible) 0.7043 [0.65 ; 0.75], R/R 3.112, perte reelle 3.901 % (gap inclus), EV 0.431 % — **REFUSE**
      - refuse : p_stop_first 0.704, borne haute 0.751 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 6.313 %) — p(stop avant cible) 0.5622 [0.51 ; 0.61], R/R 1.824, perte reelle 6.654 % (gap inclus), EV 0.4496 % — **REFUSE**
      - refuse : p_stop_first 0.562, borne haute 0.614 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 8.838 %) — p(stop avant cible) 0.4177 [0.37 ; 0.47], R/R 1.314, perte reelle 9.235 % (gap inclus), EV 1.1492 % — **REFUSE**
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 2.0 ATR (stop 11.63 %) — p(stop avant cible) 0.2805 [0.24 ; 0.33], R/R 0.979, perte reelle 12.398 % (gap inclus), EV 1.766 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.81 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 13.889 %) — p(stop avant cible) 0.2286 [0.19 ; 0.28], R/R 0.84, perte reelle 14.444 % (gap inclus), EV 1.7771 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.43 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 15.152 %) — p(stop avant cible) 0.1919 [0.15 ; 0.24], R/R 0.773, perte reelle 15.694 % (gap inclus), EV 1.8877 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.23 % > budget 12.00 %
   - 🟢 grid_snapped a 3.64 ATR (stop 19.88 %) — p(stop avant cible) 0.0751 [0.05 ; 0.11], R/R 0.6, perte reelle 20.246 % (gap inclus), EV 2.2637 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.43 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 22.727 %) — p(stop avant cible) 0.0463 [0.03 ; 0.07], R/R 0.524, perte reelle 23.15 % (gap inclus), EV 2.2882 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.01 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 25.253 %) — p(stop avant cible) 0.0307 [0.02 ; 0.05], R/R 0.471, perte reelle 25.785 % (gap inclus), EV 2.3055 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.50 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.778 %) — p(stop avant cible) 0.026 [0.01 ; 0.05], R/R 0.432, perte reelle 28.124 % (gap inclus), EV 2.3152 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.18 % > budget 12.00 %
   - 🟢 grid_snapped a 5.85 ATR (stop 31.048 %) — p(stop avant cible) 0.0177 [0.01 ; 0.04], R/R 0.389, perte reelle 31.211 % (gap inclus), EV 2.3312 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.38 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 32.828 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 0.367, perte reelle 33.077 % (gap inclus), EV 2.3923 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 35.354 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 0.336, perte reelle 36.161 % (gap inclus), EV 2.446 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.36 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 37.879 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.32, perte reelle 37.879 % (gap inclus), EV 2.4471 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.33 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 40.404 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.3, perte reelle 40.404 % (gap inclus), EV 2.4648 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.95 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 112.01, ATR14 5.6571 (5.051 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.373 ATR = 1.884 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.253 % | 111.7271 | 93.05 % | 95.16 % | 96.06 % | 96.56 % | 97.05 % | 98.05 % |
| 0.1 ATR | 0.505 % | 111.4443 | 85.5 % | 90.52 % | 92.23 % | 93.73 % | 94.72 % | 96.41 % |
| 0.15 ATR | 0.758 % | 111.1614 | 77.54 % | 85.18 % | 87.99 % | 90.29 % | 92.58 % | 95.07 % |
| 0.2 ATR | 1.01 % | 110.8786 | 71.4 % | 80.04 % | 83.75 % | 86.96 % | 90.35 % | 93.22 % |
| 0.25 ATR | 1.263 % | 110.5957 | 64.45 % | 74.29 % | 79.11 % | 83.42 % | 87.7 % | 90.86 % |
| 0.35 ATR | 1.768 % | 110.03 | 52.27 % | 65.22 % | 71.85 % | 77.55 % | 83.43 % | 87.89 % |
| 0.5 ATR | 2.525 % | 109.1815 | 37.16 % | 53.43 % | 61.15 % | 68.35 % | 76.42 % | 82.14 % |
| 0.75 ATR | 3.788 % | 107.7672 | 19.54 % | 35.99 % | 45.81 % | 55.61 % | 65.45 % | 72.9 % |
| 1.0 ATR | 5.051 % | 106.3529 | 9.26 % | 22.98 % | 32.8 % | 43.88 % | 54.78 % | 65.3 % |
| 1.25 ATR | 6.313 % | 104.9387 | 4.83 % | 14.52 % | 22.4 % | 33.37 % | 46.95 % | 58.73 % |
| 1.5 ATR | 7.576 % | 103.5244 | 2.52 % | 9.88 % | 16.25 % | 26.79 % | 40.04 % | 53.08 % |
| 2.0 ATR | 10.101 % | 100.6959 | 0.5 % | 3.83 % | 7.27 % | 15.37 % | 29.57 % | 43.63 % |
| 2.5 ATR | 12.626 % | 97.8673 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.44 % | 34.39 % |
| 3.0 ATR | 15.152 % | 95.0388 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.45 % | 26.28 % |
| 4.0 ATR | 20.202 % | 89.3817 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 30.303 % | 78.0676 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.68 ATR | 0.77 ATR | 1.00 ATR | 1.19 ATR | 1.35 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.98 ATR | 1.26 ATR | 1.58 ATR | 1.80 ATR | 2.37 ATR | 3.09 ATR |
| **10 s.** | 0.53 ATR | 1.15 ATR | 1.32 ATR | 1.84 ATR | 2.28 ATR | 2.62 ATR | 3.64 ATR | 4.68 ATR |
| **20 s.** | 0.69 ATR | 1.66 ATR | 1.93 ATR | 2.59 ATR | 3.11 ATR | 3.55 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.422–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.621–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.788 %, prix 107.7671), p(touche) 35.99 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.766–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.051 %, prix 106.3524), p(touche) 32.8 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (62.9 % des re-echantillons)
- **5 seance(s)** : plage utile 0.976–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.051 %, prix 106.3524), p(touche) 43.88 % (en stress 98.99 %)  ✅ optimum identifie (62.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.321–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.576 %, prix 103.5241), p(touche) 40.04 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.928–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.101 %, prix 100.6959), p(touche) 43.63 % (en stress 97.96 %)  ✅ optimum identifie (63.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.037 | EV/share : $-0.208 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 19 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 17.1 | side 77.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 400.0 (= 4 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.186% → cible +2.582% / stop −3.0%, p_fill 50%, n_eff≈54.1) : P(cible|rempli) **37%** · **EV/risk +0.014** (×p_fill ; si rempli +0.08% du capital)
  - **swing** (entrée dip −4.8% → cible +5.931% / stop −5.305%, p_fill 29%, n_eff≈33.8) : P(cible|rempli) **50%** · **EV/risk +0.032** (×p_fill ; si rempli +0.59% du capital)
  - **deep** (entrée dip −7.414% → cible +8.626% / stop −8.183%, p_fill 32%, n_eff≈34.8) : P(cible|rempli) **55%** · **EV/risk +0.053** (×p_fill ; si rempli +1.37% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→52% · +3.0%→35% · +5.0%→18% · +8.0%→6%
- Range intraday médian 4.88% (p90 8.86%) · excursion haute méd. +2.07% / basse méd. −2.24%
- Profil de vol intra : ouverture 3.683% vs midi 0.98% vs clôture 1.099% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 19% · trend ↑0%/↓2% ; spike-down 66% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.016)_ ; drift intra méd. -0.529% ; recovery-V 19%
- **σ réalisé intraday** 3.385% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 36% / bas 57% / whipsaw 6%
- POC intraday (dernière séance, temps-au-prix) : 112.89 (VA 112.546–114.438 ; dernier close 112.73)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 23% · rebond 66% · **stop −4.04%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.02% · baisse 49% (gap-down >1% 30% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.95% (p90 −2.87%) · haut méd +1.04% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −3.46%) · haut méd +1.29% · range méd 2.92%
- Excursion ouverture 30min (n=160) : bas méd −1.56% (p90 −3.72%) · haut méd +1.57% · range méd 3.42%
- Excursion ouverture 60min (n=160) : bas méd −1.9% (p90 −3.9%) · haut méd +1.67% · range méd 3.85%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 112.74 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 79% (123/159) · gap 38% · délai 0.0min · rebond 62% (72/123) (MFE +1.49%)
   - −1.0% : fill 30min 60% · séance 68% (108/159) · gap 30% · délai 0.0min · rebond 68% (67/108) (MFE +1.66%)
   - −1.5% : fill 30min 47% · séance 61% (98/159) · gap 21% · délai 1.4min · rebond 60% (56/98) (MFE +1.44%)
   - −2.0% : fill 30min 37% · séance 50% (85/159) · gap 15% · délai 2.8min · rebond 70% (56/85) (MFE +1.4%)
   - −3.0% : fill 30min 22% · séance 34% (63/159) · gap 5% · délai 12.5min · rebond 71% (45/63) (MFE +1.74%)
   - −4.0% : fill 30min 12% · séance 23% (45/159) · gap 2% · délai 32.1min · rebond 66% (32/45) (MFE +2.22%)
   - −5.0% : fill 30min 7% · séance 14% (28/159) · gap 1% · délai 30.3min · rebond 63% (20/28) (MFE +2.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.55%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −2.2%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −2.14%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=751 jambes) : jambe baissière méd −1.14% (p90 −2.74%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 92% (71/75) · rebond 60% (39/71)
      · −2.0% : fill 75% (60/75) · rebond 68% (38/60)
      · −3.0% : fill 56% (48/75) · rebond 80% (35/48)
      · −4.0% : fill 38% (35/75) · rebond 74% (27/35)
      · −5.0% : fill 25% (24/75) · rebond 67% (17/24)
   - **flat** (17 séances) :
      · −1.0% : fill 66% (11/17) · rebond 70% (7/11)
      · −2.0% : fill 47% (9/17) · rebond 53% (5/9)
      · −3.0% : fill 20% (4/17) · rebond 7% (1/4)
      · −4.0% : fill 20% (4/17) · rebond 7% (1/4)
      · −5.0% : fill 16% (2/17) · rebond 15% (1/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 46% (26/67) · rebond 82% (21/26)
      · −2.0% : fill 26% (16/67) · rebond 86% (13/16)
      · −3.0% : fill 16% (11/67) · rebond 56% (9/11)
      · −4.0% : fill 9% (6/67) · rebond 63% (4/6)
      · −5.0% : fill 2% (2/67) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 63% si les 15 1res min sont vertes (75 cas) · 26% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **26min** → P(séance verte=clôture>ouverture) 66% si début vert vs 20% si rouge (base 42% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **66%** · continue >prix actuel 46% ; creux résiduel méd -1.61% (q20 -2.72%) → **SL/trailing à −2.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +2.73% → **scale +1.69% / runner +2.73%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +1.63% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.16% .. +3.94%] · haut q95 +5.0% · bas q05 -5.03%
   - 60min (n=160) : retour [-4.26% .. +4.93%] · haut q95 +5.37% · bas q05 -5.54%
   - 2h (n=160) : retour [-4.88% .. +5.34%] · haut q95 +7.5% · bas q05 -6.04%
   - 4h (n=160) : retour [-4.77% .. +6.75%] · haut q95 +8.29% · bas q05 -6.73%
   - 6h (n=160) : retour [-6.02% .. +6.48%] · haut q95 +8.48% · bas q05 -7.25%
   - session (n=160) : retour [-5.78% .. +6.96%] · haut q95 +8.59% · bas q05 -7.61%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **31%**. Lecture précoce 30 min : signature présente → 19% vs absente 2% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.24% / p90 1.92%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **77%** (reprise méd 15.35 min, n=49)
   - −1.0% → **62%** (reprise méd 30.0 min, n=21)
   - −1.5% → **48%** (reprise méd 42.24 min, n=10)
   - −2.0% → **15%** (reprise méd None min, n=5)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.92%** (p90, défaut prudent ; serré/agressif −1.24%) ; extension open→close méd +6.2% (q75 +8.64% / q95 +11.94%), MFE méd +7.69% / q90 +13.19%
   - Échelle scale-out : +7.69% (33%) / +9.01% (33%) / +13.19% (34%)
- **DÉSARMER** : repli > **−1.92%** depuis le plus-haut = décay → P(retournement) **85%** (préavis méd 310.68 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.19% : P(retournement après) 0% (mèche méd 3.29%)
- **CONTEXTE** : la dernière heure tient les gains 73% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.62 · part idiosyncratique 0.38
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 60.0  _(momentum haussier)_
- **ADX** : 17.1  _(pas de tendance nette)_
- **MACD** : hist -1.277  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 17.7%
- **ATR** : 5.66 (45.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.27  _(distribution)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 50.9  _(transition)_
- **MA** : MA20 115.28 · MA50 106.11 · MA200 94.28  _(prix < MA20)_
- **Dist MA** : MA20 -2.8% · MA50 +5.6% · MA200 +18.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (519324 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
