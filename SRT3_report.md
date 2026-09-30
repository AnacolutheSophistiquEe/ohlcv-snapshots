# SRT3

**Generated** : 2026-09-30T00:08:42.994535+00:00  
**Santé technique** : 10/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €260.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €260.80 (+6.9% vs entrée) · entrée €243.87 · stop €235.59 · T1 €250.53 · R/R 0.8  
> ↳ ¼-Kelly 0.012 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €242.54–€245.20 (mid €243.87)
- Spot actuel : €260.80 (+6.9% au-dessus de la zone — repli à attendre)
- Stop : €235.59 (plancher anti-bruit (R/R<2) ; -3.40 % depuis l'entree)
- Targets : T1 €250.53 · R/R 0.8 | T2 €257.19 · R/R 1.61 | T3 €263.85 · R/R 2.41
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €235.59


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.67 %)** : le gap seul le franchit 0.157 % des séances (2 fois sur 1274).
   - exécution **2.418 pt plus bas** dans le cas TYPIQUE (médiane), 4.112 au p90, **4.535 au pire**
   - perte réelle **12.088 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 9.67 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0038 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3754** [0.3058 ; 0.4491] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.4119** [0.3609 ; 0.4643] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3777** [0.3278 ; 0.4296] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (41.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.09 %** | CVaR **-6.57 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.98 % vs -9.16 % si l'on extrapolait par √5 _(rapport 1.089 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0816** (β de hausse 1.1662, asymétrie 0.9274) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.308× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 258.7303 sur atr_grid (0.25 ATR, 0.794 %) — p(stop avant cible) 0.5516 [0.50 ; 0.60], R/R 1.475, perte reelle 0.794 % (gap inclus), CVaR 0.795 %, EV 0.087 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6056 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.552, borne haute 0.603 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.761 %) — p(stop avant cible) 0.1896 [0.15 ; 0.23], R/R 0.241, perte reelle 4.856 % (gap inclus), EV 0.0203 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 3.82 ATR (stop 13.966 %) — p(stop avant cible) 0.0284 [0.01 ; 0.05], R/R 0.084, perte reelle 13.971 % (gap inclus), EV 0.1745 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.35 % > budget 12.00 %
   - ⚪ swing_based a 4.38 ATR (stop 15.749 %) — p(stop avant cible) 0.0152 [0.01 ; 0.03], R/R 0.073, perte reelle 16.025 % (gap inclus), EV 0.1818 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.24 % > budget 12.00 %
   - 🟢 support a 7.61 ATR (stop 25.997 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.044, perte reelle 26.883 % (gap inclus), EV 0.2163 % — **REFUSE**
      - refuse : R/R 0.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.25 ATR (stop 0.794 %) — p(stop avant cible) 0.5516 [0.50 ; 0.60], R/R 1.475, perte reelle 0.794 % (gap inclus), EV 0.087 % — **REFUSE**
      - refuse : p_stop_first 0.552, borne haute 0.603 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.5 ATR (stop 1.587 %) — p(stop avant cible) 0.4418 [0.39 ; 0.49], R/R 0.731, perte reelle 1.603 % (gap inclus), EV -0.0545 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 55.8 % x 1.17 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 44.2 % x 1.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.381 %) — p(stop avant cible) 0.3293 [0.28 ; 0.38], R/R 0.483, perte reelle 2.422 % (gap inclus), EV -0.0123 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 67.1 % x 1.17 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 32.9 % x 2.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.174 %) — p(stop avant cible) 0.2739 [0.23 ; 0.32], R/R 0.364, perte reelle 3.216 % (gap inclus), EV -0.0307 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 72.6 % x 1.17 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 27.4 % x 3.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 3.968 %) — p(stop avant cible) 0.2288 [0.19 ; 0.28], R/R 0.29, perte reelle 4.04 % (gap inclus), EV -0.0267 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 76.9 % x 1.17 % + P(rien) 0.2 % x -1.13 % ne couvrent pas P(stop) 22.9 % x 4.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 5.555 %) — p(stop avant cible) 0.1652 [0.13 ; 0.21], R/R 0.207, perte reelle 5.663 % (gap inclus), EV 0.032 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 6.349 %) — p(stop avant cible) 0.1484 [0.11 ; 0.19], R/R 0.182, perte reelle 6.423 % (gap inclus), EV 0.0291 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 7.142 %) — p(stop avant cible) 0.1404 [0.11 ; 0.18], R/R 0.163, perte reelle 7.181 % (gap inclus), EV -0.0282 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 85.1 % x 1.17 % + P(rien) 0.8 % x -1.99 % ne couvrent pas P(stop) 14.0 % x 7.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 7.936 %) — p(stop avant cible) 0.1174 [0.09 ; 0.15], R/R 0.146, perte reelle 7.995 % (gap inclus), EV 0.023 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 8.729 %) — p(stop avant cible) 0.0979 [0.07 ; 0.13], R/R 0.133, perte reelle 8.791 % (gap inclus), EV 0.0537 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.523 %) — p(stop avant cible) 0.0776 [0.05 ; 0.11], R/R 0.122, perte reelle 9.61 % (gap inclus), EV 0.126 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 11.11 %) — p(stop avant cible) 0.0554 [0.03 ; 0.08], R/R 0.105, perte reelle 11.192 % (gap inclus), EV 0.1867 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.82 ATR (stop 13.071 %) — p(stop avant cible) 0.0423 [0.02 ; 0.07], R/R 0.09, perte reelle 13.081 % (gap inclus), EV 0.1269 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.71 % > budget 12.00 %
   - ⚪ grid_snapped a 4.38 ATR (stop 14.854 %) — p(stop avant cible) 0.0187 [0.01 ; 0.04], R/R 0.079, perte reelle 14.859 % (gap inclus), EV 0.1768 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.32 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.459 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 0.065, perte reelle 18.091 % (gap inclus), EV 0.2224 % — **REFUSE**
      - refuse : R/R 0.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 6.0 ATR (stop 19.046 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.06, perte reelle 19.492 % (gap inclus), EV 0.2184 % — **REFUSE**
      - refuse : R/R 0.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 6.5 ATR (stop 20.633 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.054, perte reelle 21.751 % (gap inclus), EV 0.2084 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 7.0 ATR (stop 22.22 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 0.047, perte reelle 24.801 % (gap inclus), EV 0.2115 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 7.61 ATR (stop 25.102 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.044, perte reelle 26.651 % (gap inclus), EV 0.2145 % — **REFUSE**
      - refuse : R/R 0.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 260.8, ATR14 8.2786 (3.174 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.381 ATR = 1.209 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.159 % | 260.3861 | 89.05 % | 92.89 % | 94.27 % | 96.14 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.317 % | 259.9721 | 82.45 % | 88.45 % | 90.71 % | 93.56 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.476 % | 259.5582 | 74.75 % | 83.61 % | 86.66 % | 90.4 % | 93.53 % | 94.97 % |
| 0.2 ATR | 0.635 % | 259.1443 | 68.24 % | 78.78 % | 82.81 % | 87.33 % | 92.24 % | 94.37 % |
| 0.25 ATR | 0.794 % | 258.7303 | 62.92 % | 75.42 % | 79.55 % | 84.95 % | 90.45 % | 93.07 % |
| 0.35 ATR | 1.111 % | 257.9025 | 53.06 % | 69.1 % | 73.81 % | 80.59 % | 87.16 % | 90.95 % |
| 0.5 ATR | 1.587 % | 256.6607 | 38.26 % | 56.56 % | 64.23 % | 73.76 % | 82.69 % | 88.24 % |
| 0.75 ATR | 2.381 % | 254.5911 | 19.23 % | 36.72 % | 47.63 % | 59.11 % | 72.54 % | 81.71 % |
| 1.0 ATR | 3.174 % | 252.5214 | 9.86 % | 24.48 % | 34.58 % | 47.72 % | 63.28 % | 74.67 % |
| 1.25 ATR | 3.968 % | 250.4518 | 4.73 % | 14.91 % | 24.6 % | 38.42 % | 53.63 % | 67.54 % |
| 1.5 ATR | 4.761 % | 248.3821 | 2.27 % | 9.87 % | 17.69 % | 30.89 % | 46.27 % | 61.71 % |
| 2.0 ATR | 6.349 % | 244.2428 | 0.69 % | 4.54 % | 8.2 % | 17.23 % | 34.83 % | 51.86 % |
| 2.5 ATR | 7.936 % | 240.1036 | 0.3 % | 1.97 % | 4.74 % | 10.69 % | 24.48 % | 42.01 % |
| 3.0 ATR | 9.523 % | 235.9643 | 0.2 % | 1.48 % | 2.96 % | 6.34 % | 17.51 % | 34.47 % |
| 4.0 ATR | 12.697 % | 227.6857 | 0.0 % | 0.69 % | 1.78 % | 3.56 % | 8.96 % | 20.2 % |
| 6.0 ATR | 19.046 % | 211.1286 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.49 ATR | 1.96 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.24 ATR | 1.42 ATR | 1.91 ATR | 2.46 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.72 ATR | 1.90 ATR | 2.58 ATR | 3.48 ATR |
| **10 s.** | 0.69 ATR | 1.37 ATR | 1.56 ATR | 2.09 ATR | 2.48 ATR | 2.82 ATR | 3.88 ATR | 5.15 ATR |
| **20 s.** | 0.99 ATR | 2.09 ATR | 2.35 ATR | 3.10 ATR | 3.66 ATR | 4.03 ATR | 5.55 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.587 %, prix 256.6611), p(touche) 38.26 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.381 %, prix 254.5903), p(touche) 36.72 % (en stress 89.22 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.8–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.174 %, prix 252.5222), p(touche) 34.58 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.073–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.968 %, prix 250.4514), p(touche) 38.42 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.556–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.349 %, prix 244.2418), p(touche) 34.83 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.348–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.936 %, prix 240.1029), p(touche) 42.01 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.045 | EV/share : €0.371 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 30 % | T3 13 %
- Kelly (position) : f* 0.048 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 56.6 | bear 9.2 | side 34.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 522.0 (= 2 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.954% → cible +1.221% / stop −1.5%, p_fill 15%, n_eff≈19.4) : P(cible|rempli) **49%** · **EV/risk -0.006** (×p_fill ; si rempli -0.06% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=10))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→73% · +2.0%→42% · +3.0%→24% · +5.0%→6% · +8.0%→0%
- Range intraday médian 3.48% (p90 6.44%) · excursion haute méd. +1.75% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.014% vs midi 0.882% vs clôture 1.003% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.093 ; neutre — autocorr -0.022)_ ; drift intra méd. 0.167% ; recovery-V 26%
- **σ réalisé intraday** 2.314% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 71% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 242.1875 (VA 239.7375–242.8875 ; dernier close 238.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 34% · rebond 64% · **stop −2.21%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 54% (gap-down >1% 6% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.35% (p90 −1.53%) · haut méd +0.61% · range méd 1.07%
- Excursion ouverture 15min (n=160) : bas méd −0.46% (p90 −1.75%) · haut méd +0.77% · range méd 1.38%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −1.93%) · haut méd +0.82% · range méd 1.56%
- Excursion ouverture 60min (n=160) : bas méd −0.72% (p90 −2.13%) · haut méd +0.87% · range méd 1.77%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 237.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 77% (120/159) · gap 26% · délai 0.4min · rebond 50% (64/120) (MFE +1.01%)
   - −1.0% : fill 30min 40% · séance 67% (104/159) · gap 6% · délai 10.0min · rebond 59% (59/104) (MFE +1.22%)
   - −1.5% : fill 30min 24% · séance 47% (82/159) · gap 3% · délai 28.8min · rebond 58% (46/82) (MFE +1.25%)
   - −2.0% : fill 30min 8% · séance 34% (61/159) · gap 0% · délai 165.7min · rebond 64% (34/61) (MFE +1.4%)
   - −3.0% : fill 30min 4% · séance 12% (31/159) · gap 0% · délai 115.8min · rebond 63% (17/31) (MFE +1.43%)
   - −4.0% : fill 30min 2% · séance 7% (16/159) · gap 0% · délai 56.4min · rebond 64% (11/16) (MFE +1.82%)
   - −5.0% : fill 30min 0% · séance 5% (9/159) · gap 0% · délai 141.3min · rebond 85% (8/9) (MFE +2.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.81%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −2.01%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.44% (p90 −2.53%) → stop au-delà de −1.42% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=454 jambes) : jambe baissière méd −1.02% (p90 −2.25%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 83% (47/56) · rebond 65% (29/47)
      · −2.0% : fill 40% (26/56) · rebond 67% (15/26)
      · −3.0% : fill 13% (16/56) · rebond 52% (8/16)
      · −4.0% : fill 9% (10/56) · rebond 63% (8/10)
      · −5.0% : fill 4% (5/56) · rebond 100% (5/5)
   - **flat** (39 séances) :
      · −1.0% : fill 66% (25/39) · rebond 47% (11/25)
      · −2.0% : fill 35% (16/39) · rebond 53% (8/16)
      · −3.0% : fill 9% (6/39) · rebond 38% (2/6)
      · −4.0% : fill 3% (2/39) · rebond 0% (0/2)
      · −5.0% : fill 3% (1/39) · rebond 0% (0/1)
   - **gap-up** (64 séances) :
      · −1.0% : fill 48% (32/64) · rebond 60% (19/32)
      · −2.0% : fill 26% (19/64) · rebond 71% (11/19)
      · −3.0% : fill 13% (9/64) · rebond 90% (7/9)
      · −4.0% : fill 8% (4/64) · rebond 90% (3/4)
      · −5.0% : fill 7% (3/64) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 54% si les 15 1res min sont vertes (82 cas) · 41% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 63% si début vert vs 30% si rouge (base 47% · écart 33 pts) ; prédictivité sature ensuite (plafond brut 254min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **63%** · continue >prix actuel 46% ; creux résiduel méd -1.48% (q20 -2.23%) → **SL/trailing à −2.23%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.01% / q75 +1.86% → **scale +1.01% / runner +1.86%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **30%** (continue à baisser 44%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.57%** (au-delà de la MAE q10 -2.57%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.33% .. +1.99%] · haut q95 +2.57% · bas q05 -2.91%
   - 60min (n=160) : retour [-2.32% .. +2.33%] · haut q95 +2.71% · bas q05 -3.28%
   - 2h (n=160) : retour [-2.18% .. +2.24%] · haut q95 +2.93% · bas q05 -3.72%
   - 4h (n=160) : retour [-2.27% .. +2.29%] · haut q95 +3.1% · bas q05 -3.67%
   - 6h (n=160) : retour [-2.48% .. +2.59%] · haut q95 +3.29% · bas q05 -3.82%
   - session (n=160) : retour [-3.37% .. +3.72%] · haut q95 +4.76% · bas q05 -4.07%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.07 · part idiosyncratique 0.93
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 67.9  _(momentum haussier)_
- **ADX** : 24.7  _(pas de tendance nette)_
- **MACD** : hist 2.086  _(pas de croisement recent)_
- **BB** : %B 0.85 · largeur 18.0%
- **ATR** : 8.28 (40.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.052  _(accumulation)_
- **Vol ratio** : 0.35  _(volume atone)_
- **Choppiness** : 36.9  _(marche directionnel)_
- **MA** : MA20 245.37 · MA50 238.61 · MA200 233.13  _(prix > MA20)_
- **Dist MA** : MA20 +6.3% · MA50 +9.3% · MA200 +11.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (845710 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
