# MSTR

**Generated** : 2026-10-06T22:03:52.875790+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $164.55  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (2 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $164.55 (+1.9% vs entrée) · entrée $161.49 · stop $155.84 · T1 $166.74 · R/R 0.93  
> ↳ ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 77.3 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $160.63–$162.35 (mid $161.49)
- Spot actuel : $164.55 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : $155.84 (plancher anti-bruit 5 s — stop EV-optimal −3.5% (first-passage 5 s réel) ; -3.50 % depuis l'entree)
- Targets : T1 $166.74 · R/R 0.93 | T2 $171.44 · R/R 1.76 | T3 $176.13 · R/R 2.59
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $155.84


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.8 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **3.513 pt plus bas** dans le cas TYPIQUE (médiane), 17.175 au p90, **17.572 au pire**
   - perte réelle **17.215 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 9.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0355 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.349 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2913** [0.2275 ; 0.362] _(largeur 13.5 pt, n_eff 173.1)_
   - swing : **0.4551** [0.4032 ; 0.5078] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4381** [0.3865 ; 0.4907] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (27.4 pt), deep (28.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.01 %** | CVaR **-9.02 %** | vol 4.9 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.02 % contre 5.32 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.67 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3593** (β de hausse 1.8274, asymétrie 1.291) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 155.1521 sur atr_grid (1.0 ATR, 5.711 %) — p(stop avant cible) 0.6213 [0.57 ; 0.67], R/R 2.753, perte reelle 5.896 % (gap inclus), CVaR 7.531 %, EV 0.481 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3026 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.621, borne haute 0.671 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.567 %) — p(stop avant cible) 0.4736 [0.42 ; 0.53], R/R 1.858, perte reelle 8.736 % (gap inclus), EV 0.7056 % — **REFUSE**
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 1.53 ATR (stop 11.39 %) — p(stop avant cible) 0.3469 [0.30 ; 0.40], R/R 1.414, perte reelle 11.484 % (gap inclus), EV 0.8671 % — **REFUSE**
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.04 % > budget 12.00 %
   - 🟢 support a 2.09 ATR (stop 14.562 %) — p(stop avant cible) 0.2553 [0.21 ; 0.30], R/R 1.101, perte reelle 14.749 % (gap inclus), EV 0.6617 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.52 % > budget 12.00 %
   - 🟢 support a 3.01 ATR (stop 19.831 %) — p(stop avant cible) 0.1475 [0.11 ; 0.19], R/R 0.806, perte reelle 20.152 % (gap inclus), EV 0.2786 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.78 % > budget 12.00 %
   - 🟢 support a 5.12 ATR (stop 31.895 %) — p(stop avant cible) 0.0278 [0.01 ; 0.05], R/R 0.501, perte reelle 32.432 % (gap inclus), EV 0.3358 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.95 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.428 %) — p(stop avant cible) 0.9308 [0.90 ; 0.95], R/R 11.136, perte reelle 1.458 % (gap inclus), EV -0.4294 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.931, borne haute 0.954 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 5.0 % x 16.23 % + P(rien) 1.9 % x 6.03 % ne couvrent pas P(stop) 93.1 % x 1.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.856 %) — p(stop avant cible) 0.8265 [0.78 ; 0.86], R/R 5.476, perte reelle 2.964 % (gap inclus), EV -0.2197 % — **REFUSE**
      - refuse : cible atteinte seulement 12.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.827, borne haute 0.864 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 12.3 % x 16.23 % + P(rien) 5.1 % x 4.67 % ne couvrent pas P(stop) 82.7 % x 2.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.283 %) — p(stop avant cible) 0.7254 [0.68 ; 0.77], R/R 3.629, perte reelle 4.474 % (gap inclus), EV 0.1021 % — **REFUSE**
      - refuse : p_stop_first 0.725, borne haute 0.770 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 5.711 %) — p(stop avant cible) 0.6213 [0.57 ; 0.67], R/R 2.753, perte reelle 5.896 % (gap inclus), EV 0.481 % — **REFUSE**
      - refuse : p_stop_first 0.621, borne haute 0.671 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 7.139 %) — p(stop avant cible) 0.5424 [0.49 ; 0.59], R/R 2.211, perte reelle 7.342 % (gap inclus), EV 0.5991 % — **REFUSE**
      - refuse : p_stop_first 0.542, borne haute 0.594 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 1.53 ATR (stop 10.47 %) — p(stop avant cible) 0.3789 [0.33 ; 0.43], R/R 1.531, perte reelle 10.604 % (gap inclus), EV 0.9102 % — **REFUSE**
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 2.09 ATR (stop 13.643 %) — p(stop avant cible) 0.2723 [0.23 ; 0.32], R/R 1.17, perte reelle 13.873 % (gap inclus), EV 0.8313 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.90 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.706 %) — p(stop avant cible) 0.2285 [0.19 ; 0.27], R/R 1.021, perte reelle 15.907 % (gap inclus), EV 0.5214 % — **REFUSE**
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.62 % > budget 12.00 %
   - 🟢 grid_snapped a 3.01 ATR (stop 18.912 %) — p(stop avant cible) 0.158 [0.12 ; 0.20], R/R 0.845, perte reelle 19.218 % (gap inclus), EV 0.3243 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.88 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.845 %) — p(stop avant cible) 0.1175 [0.09 ; 0.15], R/R 0.699, perte reelle 23.226 % (gap inclus), EV 0.2075 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.74 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 25.701 %) — p(stop avant cible) 0.0744 [0.05 ; 0.11], R/R 0.623, perte reelle 26.07 % (gap inclus), EV 0.2991 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.25 % > budget 12.00 %
   - 🟢 grid_snapped a 5.12 ATR (stop 30.975 %) — p(stop avant cible) 0.0336 [0.02 ; 0.06], R/R 0.514, perte reelle 31.587 % (gap inclus), EV 0.3382 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.73 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.267 %) — p(stop avant cible) 0.0196 [0.01 ; 0.04], R/R 0.468, perte reelle 34.678 % (gap inclus), EV 0.3565 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.74 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.123 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 0.428, perte reelle 37.972 % (gap inclus), EV 0.4822 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.17 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 39.979 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.398, perte reelle 40.788 % (gap inclus), EV 0.5234 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.39 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 42.834 %) — p(stop avant cible) 0.0004 [0.00 ; 0.01], R/R 0.378, perte reelle 42.955 % (gap inclus), EV 0.533 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.24 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 45.69 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.355, perte reelle 45.69 % (gap inclus), EV 0.5364 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.14 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 164.55, ATR14 9.3979 (5.711 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.394 ATR = 2.25 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.286 % | 164.0801 | 93.96 % | 96.47 % | 96.97 % | 97.67 % | 98.07 % | 98.67 % |
| 0.1 ATR | 0.571 % | 163.6102 | 88.22 % | 92.04 % | 93.54 % | 94.84 % | 96.54 % | 97.23 % |
| 0.15 ATR | 0.857 % | 163.1403 | 81.27 % | 87.1 % | 89.81 % | 91.91 % | 94.11 % | 95.48 % |
| 0.2 ATR | 1.142 % | 162.6704 | 73.72 % | 81.75 % | 85.07 % | 88.47 % | 91.57 % | 93.53 % |
| 0.25 ATR | 1.428 % | 162.2005 | 67.77 % | 77.92 % | 82.24 % | 86.35 % | 89.13 % | 91.89 % |
| 0.35 ATR | 1.999 % | 161.2608 | 54.98 % | 68.85 % | 75.38 % | 81.09 % | 85.67 % | 89.22 % |
| 0.5 ATR | 2.856 % | 159.8511 | 38.17 % | 55.34 % | 63.47 % | 71.49 % | 78.35 % | 84.29 % |
| 0.75 ATR | 4.283 % | 157.5016 | 19.44 % | 37.7 % | 47.02 % | 58.04 % | 67.78 % | 76.59 % |
| 1.0 ATR | 5.711 % | 155.1521 | 9.47 % | 25.2 % | 34.71 % | 46.31 % | 58.64 % | 69.51 % |
| 1.25 ATR | 7.139 % | 152.8027 | 4.13 % | 14.52 % | 24.72 % | 35.69 % | 49.7 % | 62.11 % |
| 1.5 ATR | 8.567 % | 150.4532 | 2.11 % | 8.67 % | 17.26 % | 28.82 % | 42.89 % | 56.37 % |
| 2.0 ATR | 11.422 % | 145.7543 | 0.2 % | 3.12 % | 7.37 % | 15.98 % | 30.89 % | 46.51 % |
| 2.5 ATR | 14.278 % | 141.0554 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.24 % | 37.06 % |
| 3.0 ATR | 17.134 % | 136.3564 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 27.72 % |
| 4.0 ATR | 22.845 % | 126.9586 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 17.97 % |
| 6.0 ATR | 34.267 % | 108.1628 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.58 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.12 ATR | 1.44 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.24 ATR | 1.41 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.45 ATR | 0.92 ATR | 1.03 ATR | 1.35 ATR | 1.65 ATR | 1.84 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.58 ATR | 1.24 ATR | 1.42 ATR | 1.91 ATR | 2.31 ATR | 2.59 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.81 ATR | 1.82 ATR | 2.08 ATR | 2.72 ATR | 3.28 ATR | 3.79 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.856 %, prix 159.8505), p(touche) 38.17 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.647–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.283 %, prix 157.5023), p(touche) 37.7 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.791–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.711 %, prix 155.1526), p(touche) 34.71 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.031–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.139 %, prix 152.8028), p(touche) 35.69 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.423–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.567 %, prix 150.453), p(touche) 42.89 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.08–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (14.278 %, prix 141.0556), p(touche) 37.06 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : $0.013 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 — | T3 —
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.8 | bear 5.0 | side 78.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 440.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.865% → cible +3.25% / stop −3.5%, p_fill 55%, n_eff≈60.9) : P(cible|rempli) **30%** · **EV/risk -0.040** (×p_fill ; si rempli -0.26% du capital)
  - **swing** (entrée dip −4.089% → cible +7.879% / stop −5.955%, p_fill 40%, n_eff≈47.3) : P(cible|rempli) **42%** · **EV/risk +0.040** (×p_fill ; si rempli +0.61% du capital)
  - **deep** (entrée dip −6.323% → cible +10.449% / stop −9.145%, p_fill 37%, n_eff≈44.0) : P(cible|rempli) **44%** · **EV/risk +0.012** (×p_fill ; si rempli +0.29% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.77 · part idiosyncratique 0.23
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 77.3  _(surachat)_
- **ADX** : 39.6  _(tendance etablie)_
- **MACD** : hist -0.289  _(pas de croisement recent)_
- **BB** : %B 0.74 · largeur 40.2%
- **ATR** : 9.4 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.023  _(neutre)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 42.0  _(transition)_
- **MA** : MA20 150.19 · MA50 126.38 · MA200 136.0  _(prix > MA20)_
- **Dist MA** : MA20 +9.6% · MA50 +30.2% · MA200 +21.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (532204 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
