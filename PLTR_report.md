# PLTR

**Generated** : 2026-10-01T00:25:47.161663+00:00  
**Santé technique** : 10/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $187.04  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $187.04 (+8.4% vs entrée) · entrée $172.59 · stop $163.55 · T1 $190.66 · R/R 2.0  
> ↳ ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 81.2 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $171.34–$173.84 (mid $172.59)
- Spot actuel : $187.04 (+8.4% au-dessus de la zone — repli à attendre)
- Stop : $163.55 (R/R 2 (resserré, parité Claude) ; -5.24 % depuis l'entree)
- Targets : T1 $190.66 · R/R 2.0 | T2 $197.04 · R/R 2.7 | T3 $203.42 · R/R 3.41
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $163.55


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.56 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **2.112 pt plus bas** dans le cas TYPIQUE (médiane), 4.72 au p90, **5.372 au pire**
   - perte réelle **15.126 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 12.56 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0061 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.861 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2463** [0.1867 ; 0.3143] _(largeur 12.8 pt, n_eff 173.1)_
   - swing : **0.4098** [0.3589 ; 0.4622] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.4442** [0.3925 ; 0.4969] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (41.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.14 %** | CVaR **-8.41 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.31 % vs -13.73 % si l'on extrapolait par √5 _(rapport 0.969 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6844** (β de hausse 1.4223, asymétrie 1.1843) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.771× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 181.3348 sur atr_grid (1.0 ATR, 3.05 %) — p(stop avant cible) 0.684 [0.63 ; 0.73], R/R 2.796, perte reelle 3.132 % (gap inclus), CVaR 4.102 %, EV 0.3999 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3976 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.684, borne haute 0.731 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.575 %) — p(stop avant cible) 0.5789 [0.53 ; 0.63], R/R 1.892, perte reelle 4.629 % (gap inclus), EV 0.431 % — **REFUSE**
      - refuse : p_stop_first 0.579, borne haute 0.630 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 4.14 ATR (stop 14.565 %) — p(stop avant cible) 0.1344 [0.10 ; 0.17], R/R 0.59, perte reelle 14.85 % (gap inclus), EV 0.6693 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.33 % > budget 12.00 %
   - ⚪ sr_based a 4.71 ATR (stop 16.284 %) — p(stop avant cible) 0.1056 [0.08 ; 0.14], R/R 0.531, perte reelle 16.503 % (gap inclus), EV 0.7238 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.75 % > budget 12.00 %
   - 🟢 support a 6.92 ATR (stop 23.039 %) — p(stop avant cible) 0.0193 [0.01 ; 0.04], R/R 0.375, perte reelle 23.372 % (gap inclus), EV 1.1068 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.24 % > budget 12.00 %
   - 🟢 support a 12.12 ATR (stop 38.902 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.222, perte reelle 39.385 % (gap inclus), EV 1.2036 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.80 % > budget 12.00 %
   - 🟢 support a 14.14 ATR (stop 45.061 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.194, perte reelle 45.061 % (gap inclus), EV 1.2028 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.79 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.763 %) — p(stop avant cible) 0.9214 [0.89 ; 0.95], R/R 11.119, perte reelle 0.787 % (gap inclus), EV -0.0424 % — **REFUSE**
      - refuse : cible atteinte seulement 7.8 % du temps (< 15 %) meme a 10 seances : le R/R de 11.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.921, borne haute 0.946 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 7.8 % x 8.76 % + P(rien) 0.1 % x 2.79 % ne couvrent pas P(stop) 92.1 % x 0.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.525 %) — p(stop avant cible) 0.821 [0.78 ; 0.86], R/R 5.609, perte reelle 1.561 % (gap inclus), EV 0.2371 % — **REFUSE**
      - refuse : p_stop_first 0.821, borne haute 0.859 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 2.288 %) — p(stop avant cible) 0.7426 [0.69 ; 0.79], R/R 3.689, perte reelle 2.373 % (gap inclus), EV 0.3983 % — **REFUSE**
      - refuse : p_stop_first 0.743, borne haute 0.786 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 3.05 %) — p(stop avant cible) 0.684 [0.63 ; 0.73], R/R 2.796, perte reelle 3.132 % (gap inclus), EV 0.3999 % — **REFUSE**
      - refuse : p_stop_first 0.684, borne haute 0.731 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 3.813 %) — p(stop avant cible) 0.6422 [0.59 ; 0.69], R/R 2.252, perte reelle 3.889 % (gap inclus), EV 0.2819 % — **REFUSE**
      - refuse : p_stop_first 0.642, borne haute 0.691 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 5.338 %) — p(stop avant cible) 0.5045 [0.45 ; 0.56], R/R 1.621, perte reelle 5.402 % (gap inclus), EV 0.6252 % — **REFUSE**
      - refuse : p_stop_first 0.504, borne haute 0.557 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 6.1 %) — p(stop avant cible) 0.458 [0.41 ; 0.51], R/R 1.42, perte reelle 6.164 % (gap inclus), EV 0.6934 % — **REFUSE**
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 6.863 %) — p(stop avant cible) 0.3973 [0.35 ; 0.45], R/R 1.262, perte reelle 6.937 % (gap inclus), EV 0.9702 % — **REFUSE**
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 7.626 %) — p(stop avant cible) 0.3582 [0.31 ; 0.41], R/R 1.133, perte reelle 7.73 % (gap inclus), EV 0.935 % — **REFUSE**
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 8.388 %) — p(stop avant cible) 0.3222 [0.27 ; 0.37], R/R 1.033, perte reelle 8.475 % (gap inclus), EV 0.8885 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.151 %) — p(stop avant cible) 0.3014 [0.25 ; 0.35], R/R 0.948, perte reelle 9.241 % (gap inclus), EV 0.7848 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 10.676 %) — p(stop avant cible) 0.2569 [0.21 ; 0.30], R/R 0.807, perte reelle 10.854 % (gap inclus), EV 0.5553 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 4.14 ATR (stop 13.549 %) — p(stop avant cible) 0.1515 [0.12 ; 0.19], R/R 0.636, perte reelle 13.768 % (gap inclus), EV 0.713 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.21 % > budget 12.00 %
   - ⚪ grid_snapped a 4.71 ATR (stop 15.269 %) — p(stop avant cible) 0.1221 [0.09 ; 0.16], R/R 0.564, perte reelle 15.525 % (gap inclus), EV 0.6801 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.89 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.776 %) — p(stop avant cible) 0.0989 [0.07 ; 0.13], R/R 0.515, perte reelle 16.986 % (gap inclus), EV 0.7654 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.19 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.301 %) — p(stop avant cible) 0.0802 [0.06 ; 0.11], R/R 0.475, perte reelle 18.45 % (gap inclus), EV 0.7667 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.54 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.826 %) — p(stop avant cible) 0.0475 [0.03 ; 0.07], R/R 0.438, perte reelle 20.012 % (gap inclus), EV 0.9704 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.92 % > budget 12.00 %
   - 🟢 grid_snapped a 6.92 ATR (stop 22.023 %) — p(stop avant cible) 0.0268 [0.01 ; 0.05], R/R 0.391, perte reelle 22.366 % (gap inclus), EV 1.0646 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.84 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 24.402 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 0.353, perte reelle 24.827 % (gap inclus), EV 1.154 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.34 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 187.04, ATR14 5.7051 (3.05 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.359 ATR = 1.095 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.153 % | 186.7547 | 92.65 % | 95.16 % | 95.96 % | 96.76 % | 98.07 % | 98.67 % |
| 0.1 ATR | 0.305 % | 186.4695 | 84.69 % | 89.31 % | 91.22 % | 93.43 % | 95.02 % | 96.41 % |
| 0.15 ATR | 0.458 % | 186.1842 | 77.04 % | 83.67 % | 85.97 % | 89.79 % | 92.38 % | 94.25 % |
| 0.2 ATR | 0.61 % | 185.899 | 69.08 % | 78.23 % | 81.74 % | 86.35 % | 90.14 % | 92.51 % |
| 0.25 ATR | 0.763 % | 185.6137 | 62.13 % | 73.49 % | 77.6 % | 82.91 % | 87.7 % | 90.97 % |
| 0.35 ATR | 1.068 % | 185.0432 | 50.86 % | 65.32 % | 71.04 % | 78.06 % | 83.64 % | 87.99 % |
| 0.5 ATR | 1.525 % | 184.1874 | 35.85 % | 52.62 % | 59.64 % | 68.86 % | 77.74 % | 83.47 % |
| 0.75 ATR | 2.288 % | 182.7611 | 19.44 % | 35.08 % | 44.5 % | 55.21 % | 66.77 % | 76.28 % |
| 1.0 ATR | 3.05 % | 181.3348 | 8.96 % | 22.78 % | 32.39 % | 43.68 % | 56.2 % | 67.35 % |
| 1.25 ATR | 3.813 % | 179.9086 | 4.43 % | 15.32 % | 23.21 % | 33.97 % | 46.34 % | 58.52 % |
| 1.5 ATR | 4.575 % | 178.4823 | 2.11 % | 10.48 % | 17.36 % | 26.59 % | 39.84 % | 54.0 % |
| 2.0 ATR | 6.1 % | 175.6297 | 0.6 % | 3.73 % | 9.38 % | 15.77 % | 29.07 % | 40.55 % |
| 2.5 ATR | 7.626 % | 172.7771 | 0.1 % | 1.51 % | 3.33 % | 9.3 % | 19.41 % | 30.29 % |
| 3.0 ATR | 9.151 % | 169.9246 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 12.201 % | 164.2194 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 18.301 % | 152.8091 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.09 ATR | 1.54 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.39 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.86 ATR | 0.97 ATR | 1.28 ATR | 1.57 ATR | 1.80 ATR | 2.45 ATR | 2.97 ATR |
| **10 s.** | 0.56 ATR | 1.16 ATR | 1.30 ATR | 1.82 ATR | 2.21 ATR | 2.47 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.79 ATR | 1.65 ATR | 1.83 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.525 %, prix 184.1876), p(touche) 35.85 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.609–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.288 %, prix 182.7605), p(touche) 35.08 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.742–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.288 %, prix 182.7605), p(touche) 44.5 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.971–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.05 %, prix 181.3353), p(touche) 43.68 % (en stress 100.0 %)  ✅ optimum identifie (82.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.302–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.575 %, prix 178.4829), p(touche) 39.84 % (en stress 100.0 %)  ✅ optimum identifie (87.2 % des re-echantillons)
- **20 seance(s)** : plage utile 1.835–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (9.151 %, prix 169.924), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.027 | EV/share : $0.245 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 10 % | T3 7 %
- Kelly (position) : f* 0.023 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 59.1 | bear 20.8 | side 20.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 495.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.508% → cible +1.581% / stop −2.5%, p_fill 16%, n_eff≈20.3) : P(cible|rempli) **29%** · **EV/risk -0.010** (×p_fill ; si rempli -0.16% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→74% · +2.0%→45% · +3.0%→24% · +5.0%→9% · +8.0%→2%
- Range intraday médian 3.72% (p90 6.89%) · excursion haute méd. +1.87% / basse méd. −1.63%
- Profil de vol intra : ouverture 2.895% vs midi 0.731% vs clôture 0.81% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑1%/↓0% ; spike-down 54% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr -0.016)_ ; drift intra méd. 0.521% ; recovery-V 34%
- **σ réalisé intraday** 2.383% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 41% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 185.9181 (VA 185.4494–186.1994 ; dernier close 186.97)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 70% · **stop −3.6%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.44 (high win-rate)
- Gaps overnight (n=156) : méd. -0.09% · baisse 53% (gap-down >1% 30% · >2% 7%)
- Excursion ouverture 5min (n=157) : bas méd −0.82% (p90 −1.93%) · haut méd +0.73% · range méd 1.74%
- Excursion ouverture 15min (n=157) : bas méd −1.02% (p90 −2.44%) · haut méd +1.07% · range méd 2.23%
- Excursion ouverture 30min (n=157) : bas méd −1.1% (p90 −2.91%) · haut méd +1.18% · range méd 2.56%
- Excursion ouverture 60min (n=157) : bas méd −1.32% (p90 −3.08%) · haut méd +1.31% · range méd 2.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 186.97 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 78% (117/156) · gap 40% · délai 0.0min · rebond 63% (68/117) (MFE +1.35%)
   - −1.0% : fill 30min 58% · séance 65% (104/156) · gap 30% · délai 0.0min · rebond 66% (61/104) (MFE +1.44%)
   - −1.5% : fill 30min 44% · séance 53% (87/156) · gap 18% · délai 0.1min · rebond 64% (53/87) (MFE +1.44%)
   - −2.0% : fill 30min 37% · séance 47% (78/156) · gap 7% · délai 1.5min · rebond 70% (50/78) (MFE +1.6%)
   - −3.0% : fill 30min 17% · séance 24% (51/156) · gap 3% · délai 6.1min · rebond 53% (24/51) (MFE +1.22%)
   - −4.0% : fill 30min 11% · séance 16% (35/156) · gap 2% · délai 15.4min · rebond 52% (17/35) (MFE +1.07%)
   - −5.0% : fill 30min 4% · séance 10% (23/156) · gap 0% · délai 45.3min · rebond 48% (12/23) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.9%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −1.84%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −1.57%) → stop au-delà de −1.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=515 jambes) : jambe baissière méd −1.04% (p90 −2.33%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 91% (70/75) · rebond 63% (41/70)
      · −2.0% : fill 75% (57/75) · rebond 72% (36/57)
      · −3.0% : fill 42% (38/75) · rebond 52% (18/38)
      · −4.0% : fill 29% (27/75) · rebond 54% (13/27)
      · −5.0% : fill 19% (19/75) · rebond 53% (11/19)
   - **flat** (24 séances) :
      · −1.0% : fill 78% (20/24) · rebond 58% (10/20)
      · −2.0% : fill 45% (14/24) · rebond 62% (9/14)
      · −3.0% : fill 25% (10/24) · rebond 55% (5/10)
      · −4.0% : fill 16% (7/24) · rebond 46% (4/7)
      · −5.0% : fill 8% (3/24) · rebond 13% (1/3)
   - **gap-up** (57 séances) :
      · −1.0% : fill 29% (14/57) · rebond 85% (10/14)
      · −2.0% : fill 14% (7/57) · rebond 67% (5/7)
      · −3.0% : fill 3% (3/57) · rebond 66% (1/3)
      · −4.0% : fill 1% (1/57) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/57) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 54% en base · 74% si les 15 1res min sont vertes (80 cas) · 31% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=157) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 89% si début vert vs 16% si rouge (base 54% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **89%** · continue >prix actuel 57% ; creux résiduel méd -0.75% (q20 -1.39%) → **SL/trailing à −1.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +2.16% → **scale +1.07% / runner +2.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **16%** (continue à baisser 51%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.64%** (au-delà de la MAE q10 -2.64%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-2.93% .. +3.81%] · haut q95 +4.05% · bas q05 -3.55%
   - 60min (n=157) : retour [-3.04% .. +3.93%] · haut q95 +4.78% · bas q05 -3.76%
   - 2h (n=157) : retour [-3.74% .. +5.37%] · haut q95 +5.78% · bas q05 -4.46%
   - 4h (n=157) : retour [-4.04% .. +5.64%] · haut q95 +6.47% · bas q05 -5.22%
   - 6h (n=157) : retour [-4.14% .. +5.76%] · haut q95 +6.83% · bas q05 -5.56%
   - session (n=157) : retour [-4.03% .. +4.91%] · haut q95 +6.83% · bas q05 -5.56%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.7% des séances sont trend-up (mild 1.3% / strong 4.5%) · base = 9 séances trend-up (n_eff 7.0)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **29%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.91% (p75 1.39% / p90 1.52%) · ~2.0 replis/séance, durée méd 77.38 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 47.34 min, n=25)
   - −1.0% → **51%** (reprise méd 65.0 min, n=11)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.52%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +4.55% (q75 +7.54% / q95 +12.13%), MFE méd +6.21% / q90 +12.4%
   - Échelle scale-out : +6.21% (33%) / +8.19% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−1.52%** depuis le plus-haut = décay → P(retournement) **65%** (préavis méd 99.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 53% du temps (retour médian dernière heure +0.12%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.6 · part idiosyncratique 0.4
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 81.2  _(surachat)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist 0.246  _(pas de croisement recent)_
- **BB** : %B 0.74 · largeur 19.3%
- **ATR** : 5.71 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.126  _(accumulation)_
- **Vol ratio** : 0.48  _(volume atone)_
- **Choppiness** : 38.0  _(marche directionnel)_
- **MA** : MA20 178.85 · MA50 167.16 · MA200 152.04  _(prix > MA20)_
- **Dist MA** : MA20 +4.6% · MA50 +11.9% · MA200 +23.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (851545 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
