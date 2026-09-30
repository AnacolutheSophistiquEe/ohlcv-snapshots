# PLTR

**Generated** : 2026-09-30T00:28:08.919437+00:00  
**Santé technique** : 10/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $186.97  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $186.97 (+13.5% vs entrée) · entrée $164.67 · stop $158.90 · T1 $170.87 · R/R 1.07  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 73.2 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $163.43–$165.91 (mid $164.67)
- Spot actuel : $186.97 (+13.5% au-dessus de la zone — repli à attendre)
- Stop : $158.90 (plancher anti-bruit (R/R<2) ; -3.50 % depuis l'entree)
- Targets : T1 $170.87 · R/R 1.07 | T2 $177.06 · R/R 2.15 | T3 $183.25 · R/R 3.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $158.90


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.01 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **2.922 pt plus bas** dans le cas TYPIQUE (médiane), 2.922 au p90, **2.922 au pire**
   - perte réelle **17.932 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 15.01 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0023 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.861 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4719** [0.3985 ; 0.5462] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4806** [0.4283 ; 0.5332] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4091** [0.3582 ; 0.4615] _(largeur 10.3 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-5.78 %** | CVaR **-8.09 %** | vol 4.15 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 2.64 % contre 4.31 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.31 % vs -13.73 % si l'on extrapolait par √5 _(rapport 0.969 ; < 1 = le √5 surestime)_
- **β de baisse : 1.684** (β de hausse 1.421, asymétrie 1.1851) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.769× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 185.5266 sur atr_grid (0.25 ATR, 0.772 %) — p(stop avant cible) 0.7754 [0.73 ; 0.82], R/R 3.977, perte reelle 0.778 % (gap inclus), CVaR 0.868 %, EV 0.0917 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4855 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.775, borne haute 0.817 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.632 %) — p(stop avant cible) 0.3697 [0.32 ; 0.42], R/R 0.66, perte reelle 4.692 % (gap inclus), EV 0.1934 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 4.08 ATR (stop 14.406 %) — p(stop avant cible) 0.0876 [0.06 ; 0.12], R/R 0.211, perte reelle 14.689 % (gap inclus), EV 0.3113 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.90 % > budget 12.00 %
   - ⚪ sr_based a 7.12 ATR (stop 23.789 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.126, perte reelle 24.58 % (gap inclus), EV 0.5247 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.34 % > budget 12.00 %
   - 🟢 support a 11.96 ATR (stop 38.744 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.079, perte reelle 38.949 % (gap inclus), EV 0.5842 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.66 % > budget 12.00 %
   - 🟢 support a 13.96 ATR (stop 44.906 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.069, perte reelle 44.906 % (gap inclus), EV 0.5836 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.66 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.772 %) — p(stop avant cible) 0.7754 [0.73 ; 0.82], R/R 3.977, perte reelle 0.778 % (gap inclus), EV 0.0917 % — **REFUSE**
      - refuse : p_stop_first 0.775, borne haute 0.817 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.544 %) — p(stop avant cible) 0.662 [0.61 ; 0.71], R/R 1.985, perte reelle 1.559 % (gap inclus), EV 0.0141 % — **REFUSE**
      - refuse : p_stop_first 0.662, borne haute 0.710 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.75 ATR (stop 2.316 %) — p(stop avant cible) 0.5457 [0.49 ; 0.60], R/R 1.291, perte reelle 2.397 % (gap inclus), EV 0.0982 % — **REFUSE**
      - refuse : p_stop_first 0.546, borne haute 0.598 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.0 ATR (stop 3.088 %) — p(stop avant cible) 0.494 [0.44 ; 0.55], R/R 0.974, perte reelle 3.176 % (gap inclus), EV -0.0029 % — **REFUSE**
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 50.6 % x 3.10 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 49.4 % x 3.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 3.86 %) — p(stop avant cible) 0.4391 [0.39 ; 0.49], R/R 0.788, perte reelle 3.93 % (gap inclus), EV 0.0104 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 5.404 %) — p(stop avant cible) 0.3233 [0.28 ; 0.37], R/R 0.565, perte reelle 5.478 % (gap inclus), EV 0.2894 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 6.176 %) — p(stop avant cible) 0.284 [0.24 ; 0.33], R/R 0.496, perte reelle 6.24 % (gap inclus), EV 0.3987 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 6.948 %) — p(stop avant cible) 0.2455 [0.20 ; 0.29], R/R 0.441, perte reelle 7.018 % (gap inclus), EV 0.5615 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 7.72 %) — p(stop avant cible) 0.2326 [0.19 ; 0.28], R/R 0.396, perte reelle 7.816 % (gap inclus), EV 0.4791 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 8.492 %) — p(stop avant cible) 0.2168 [0.18 ; 0.26], R/R 0.36, perte reelle 8.595 % (gap inclus), EV 0.4403 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.264 %) — p(stop avant cible) 0.1996 [0.16 ; 0.24], R/R 0.332, perte reelle 9.333 % (gap inclus), EV 0.3965 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 10.808 %) — p(stop avant cible) 0.178 [0.14 ; 0.22], R/R 0.283, perte reelle 10.919 % (gap inclus), EV 0.2588 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 4.08 ATR (stop 13.535 %) — p(stop avant cible) 0.102 [0.07 ; 0.14], R/R 0.226, perte reelle 13.723 % (gap inclus), EV 0.3088 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.92 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 15.44 %) — p(stop avant cible) 0.0706 [0.05 ; 0.10], R/R 0.197, perte reelle 15.694 % (gap inclus), EV 0.4038 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.80 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.984 %) — p(stop avant cible) 0.0643 [0.04 ; 0.09], R/R 0.18, perte reelle 17.184 % (gap inclus), EV 0.3459 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.24 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.528 %) — p(stop avant cible) 0.0608 [0.04 ; 0.09], R/R 0.166, perte reelle 18.631 % (gap inclus), EV 0.28 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.65 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 20.072 %) — p(stop avant cible) 0.0402 [0.02 ; 0.06], R/R 0.153, perte reelle 20.233 % (gap inclus), EV 0.3665 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.47 % > budget 12.00 %
   - ⚪ grid_snapped a 7.12 ATR (stop 22.918 %) — p(stop avant cible) 0.0189 [0.01 ; 0.04], R/R 0.133, perte reelle 23.271 % (gap inclus), EV 0.4569 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.63 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 24.704 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 0.122, perte reelle 25.296 % (gap inclus), EV 0.533 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.18 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 186.97, ATR14 5.7737 (3.088 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.359 ATR = 1.109 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.154 % | 186.6813 | 92.65 % | 95.16 % | 95.96 % | 96.76 % | 98.07 % | 98.67 % |
| 0.1 ATR | 0.309 % | 186.3926 | 84.69 % | 89.31 % | 91.22 % | 93.43 % | 95.02 % | 96.41 % |
| 0.15 ATR | 0.463 % | 186.1039 | 77.04 % | 83.67 % | 85.97 % | 89.79 % | 92.38 % | 94.25 % |
| 0.2 ATR | 0.618 % | 185.8153 | 69.08 % | 78.23 % | 81.74 % | 86.35 % | 90.24 % | 92.51 % |
| 0.25 ATR | 0.772 % | 185.5266 | 62.13 % | 73.59 % | 77.6 % | 82.91 % | 87.8 % | 90.97 % |
| 0.35 ATR | 1.081 % | 184.9492 | 50.86 % | 65.42 % | 71.04 % | 78.06 % | 83.74 % | 87.99 % |
| 0.5 ATR | 1.544 % | 184.0831 | 35.95 % | 52.72 % | 59.64 % | 68.96 % | 77.85 % | 83.47 % |
| 0.75 ATR | 2.316 % | 182.6397 | 19.44 % | 35.18 % | 44.5 % | 55.31 % | 66.87 % | 76.28 % |
| 1.0 ATR | 3.088 % | 181.1963 | 8.96 % | 22.88 % | 32.39 % | 43.78 % | 56.3 % | 67.35 % |
| 1.25 ATR | 3.86 % | 179.7529 | 4.43 % | 15.42 % | 23.21 % | 34.07 % | 46.44 % | 58.52 % |
| 1.5 ATR | 4.632 % | 178.3094 | 2.11 % | 10.48 % | 17.36 % | 26.59 % | 39.84 % | 54.0 % |
| 2.0 ATR | 6.176 % | 175.4226 | 0.6 % | 3.73 % | 9.38 % | 15.77 % | 29.07 % | 40.55 % |
| 2.5 ATR | 7.72 % | 172.5357 | 0.1 % | 1.51 % | 3.33 % | 9.3 % | 19.41 % | 30.29 % |
| 3.0 ATR | 9.264 % | 169.6489 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 12.352 % | 163.8751 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 18.528 % | 152.3277 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.96 ATR | 1.10 ATR | 1.54 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.39 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.86 ATR | 0.97 ATR | 1.29 ATR | 1.57 ATR | 1.80 ATR | 2.45 ATR | 2.97 ATR |
| **10 s.** | 0.56 ATR | 1.16 ATR | 1.30 ATR | 1.82 ATR | 2.21 ATR | 2.47 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.79 ATR | 1.65 ATR | 1.83 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.544 %, prix 184.0832), p(touche) 35.95 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.61–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.316 %, prix 182.6398), p(touche) 35.18 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.742–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.316 %, prix 182.6398), p(touche) 44.5 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.974–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.088 %, prix 181.1964), p(touche) 43.78 % (en stress 100.0 %)  ✅ optimum identifie (82.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.305–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.632 %, prix 178.3096), p(touche) 39.84 % (en stress 100.0 %)  ✅ optimum identifie (87.9 % des re-echantillons)
- **20 seance(s)** : plage utile 1.835–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (9.264 %, prix 169.6491), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (97.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.012 | EV/share : $-0.067 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 23 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 57.7 | bear 22.5 | side 19.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 495.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=8, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→74% · +2.0%→47% · +3.0%→28% · +5.0%→10% · +8.0%→2%
- Range intraday médian 3.94% (p90 6.95%) · excursion haute méd. +1.91% / basse méd. −1.51%
- Profil de vol intra : ouverture 2.952% vs midi 0.758% vs clôture 0.839% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (155 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 74% · range 25% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.151 ; neutre — autocorr 0.002)_ ; drift intra méd. 0.507% ; recovery-V 20%
- **σ réalisé intraday** 2.604% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 49% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 174.1906 (VA 173.9824–176.0649 ; dernier close 174.31)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 21% · rebond 52% · **stop −3.4%** sous le fill (sous le bruit) · cible +1.07% · R/R 0.31 (high win-rate)
- Gaps overnight (n=154) : méd. -0.29% · baisse 56% (gap-down >1% 30% · >2% 9%)
- Excursion ouverture 5min (n=155) : bas méd −0.83% (p90 −2.04%) · haut méd +0.97% · range méd 1.91%
- Excursion ouverture 15min (n=155) : bas méd −0.89% (p90 −2.74%) · haut méd +1.17% · range méd 2.37%
- Excursion ouverture 30min (n=155) : bas méd −1.01% (p90 −3.26%) · haut méd +1.29% · range méd 2.68%
- Excursion ouverture 60min (n=155) : bas méd −1.16% (p90 −3.5%) · haut méd +1.37% · range méd 2.98%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 174.33 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 76% (116/154) · gap 43% · délai 0.0min · rebond 55% (66/116) (MFE +1.21%)
   - −1.0% : fill 30min 56% · séance 66% (105/154) · gap 30% · délai 0.0min · rebond 60% (59/105) (MFE +1.27%)
   - −1.5% : fill 30min 44% · séance 54% (87/154) · gap 20% · délai 0.1min · rebond 60% (50/87) (MFE +1.25%)
   - −2.0% : fill 30min 38% · séance 50% (77/154) · gap 9% · délai 1.4min · rebond 62% (47/77) (MFE +1.32%)
   - −3.0% : fill 30min 22% · séance 33% (54/154) · gap 4% · délai 6.3min · rebond 52% (24/54) (MFE +1.14%)
   - −4.0% : fill 30min 14% · séance 21% (37/154) · gap 2% · délai 15.5min · rebond 52% (18/37) (MFE +1.07%)
   - −5.0% : fill 30min 6% · séance 14% (24/154) · gap 0% · délai 46.0min · rebond 47% (12/24) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.71%) → stop au-delà de −1.01% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.59% (p90 −1.39%) → stop au-delà de −1.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −1.17%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=516 jambes) : jambe baissière méd −1.07% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 89% (66/71) · rebond 61% (39/66)
      · −2.0% : fill 74% (54/71) · rebond 64% (33/54)
      · −3.0% : fill 52% (38/71) · rebond 52% (18/38)
      · −4.0% : fill 36% (27/71) · rebond 54% (13/27)
      · −5.0% : fill 24% (19/71) · rebond 53% (11/19)
   - **flat** (29 séances) :
      · −1.0% : fill 72% (24/29) · rebond 39% (12/24)
      · −2.0% : fill 57% (14/29) · rebond 62% (9/14)
      · −3.0% : fill 32% (10/29) · rebond 55% (5/10)
      · −4.0% : fill 20% (7/29) · rebond 46% (4/7)
      · −5.0% : fill 10% (3/29) · rebond 13% (1/3)
   - **gap-up** (54 séances) :
      · −1.0% : fill 30% (15/54) · rebond 75% (8/15)
      · −2.0% : fill 15% (9/54) · rebond 50% (5/9)
      · −3.0% : fill 6% (6/54) · rebond 52% (1/6)
      · −4.0% : fill 2% (3/54) · rebond 24% (1/3)
      · −5.0% : fill 1% (2/54) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=155) : 52% en base · 71% si les 15 1res min sont vertes (78 cas) · 30% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=155) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 84% si début vert vs 18% si rouge (base 52% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **84%** · continue >prix actuel 55% ; creux résiduel méd -0.84% (q20 -1.56%) → **SL/trailing à −1.56%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +2.17% → **scale +1.06% / runner +2.17%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **18%** (continue à baisser 53%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.01%** (au-delà de la MAE q10 -3.01%), cible rebond +1.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=155) : retour [-3.34% .. +4.64%] · haut q95 +5.01% · bas q05 -3.61%
   - 60min (n=155) : retour [-3.6% .. +5.96%] · haut q95 +6.34% · bas q05 -4.16%
   - 2h (n=155) : retour [-4.14% .. +6.21%] · haut q95 +6.98% · bas q05 -4.52%
   - 4h (n=155) : retour [-4.47% .. +5.89%] · haut q95 +6.98% · bas q05 -5.94%
   - 6h (n=155) : retour [-4.59% .. +6.53%] · haut q95 +7.4% · bas q05 -6.33%
   - session (n=155) : retour [-4.28% .. +5.85%] · haut q95 +7.71% · bas q05 -6.33%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.8% des séances sont trend-up (mild 1.3% / strong 4.5%) · base = 9 séances trend-up (n_eff 7.0)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **36%**. Lecture précoce 30 min : signature présente → 17% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.91% (p75 1.39% / p90 1.52%) · ~2.0 replis/séance, durée méd 77.38 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 47.34 min, n=25)
   - −1.0% → **51%** (reprise méd 65.0 min, n=11)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.52%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +4.55% (q75 +7.54% / q95 +12.13%), MFE méd +6.21% / q90 +12.4%
   - Échelle scale-out : +6.21% (33%) / +8.19% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−1.52%** depuis le plus-haut = décay → P(retournement) **65%** (préavis méd 99.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 53% du temps (retour médian dernière heure +0.12%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.59 · part idiosyncratique 0.41
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 73.2  _(surachat)_
- **ADX** : 25.9  _(tendance etablie)_
- **MACD** : hist 0.492  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 18.9%
- **ATR** : 5.77 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.1  _(accumulation)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 37.4  _(marche directionnel)_
- **MA** : MA20 178.49 · MA50 166.07 · MA200 152.05  _(prix > MA20)_
- **Dist MA** : MA20 +4.8% · MA50 +12.6% · MA200 +23.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (847494 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
