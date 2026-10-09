# PLTR

**Generated** : 2026-10-09T00:26:44.073294+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 10/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $198.72  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $198.72 (+1.2% vs entrée) · entrée $196.41 · stop $190.58 · T1 $202.93 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -3.4 % ≠ (strike 187.5 − spot 198.72)/spot = -5.6 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 80.2 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-08 : 198.72 · ATR Wilder 6.31 (3.18 %)_
- **Swing** : plage **191.32 → 185.79** (-3.72 % a -6.51 % sous la cloture, 0.88 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 188.2-190.39 (B) ; 184.81-187.62 (A). stop INDICATIF 177.02 (-4.72 % sous le bas ; sous le support 180.18-182.44 (- 0,5 ATR)).
- **Deep** : plage **185.79 → 174.37** (-6.51 % a -12.26 % sous la cloture, 1.81 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 184.81-187.62 (A) ; 180.18-182.44 (B) ; 174.29-176.5 (B). stop INDICATIF 165.74 (-4.94 % sous le bas ; sous le support 168.9-172.0 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.91 ATR sous le plus haut 20 s., RSI(2) 98.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 194.68-194.93 (B, -1.91 %) ; 188.2-190.39 (B, -4.19 %) ; 184.81-187.62 (A, -5.59 %) ; 180.18-182.44 (B, -8.19 %) ; 174.29-176.5 (B, -11.18 %) ; 168.9-172.0 (B, -13.45 %)
- Resistances reelles au-dessus : 207.52-207.52 (C, 4.43 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (4.1 %)** : le gap seul le franchit 2.314 % des séances (29 fois sur 1253).
   - exécution **1.551 pt plus bas** dans le cas TYPIQUE (médiane), 8.155 au p90, **13.832 au pire**
   - perte réelle **7.196 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 4.1 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0716 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.861 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2271** [0.1695 ; 0.2937] _(largeur 12.4 pt, n_eff 173.1)_
   - swing : **0.4793** [0.427 ; 0.532] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4527** [0.4008 ; 0.5054] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.14 %** | CVaR **-8.41 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.31 % vs -13.73 % si l'on extrapolait par √5 _(rapport 0.969 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6877** (β de hausse 1.4235, asymétrie 1.1855) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.785× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 192.1885 sur grid_snapped (0.82 ATR, 3.287 %) — p(stop avant cible) 0.6506 [0.60 ; 0.70], R/R 2.58, perte reelle 3.363 % (gap inclus), CVaR 4.257 %, EV 0.5216 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4116 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.651, borne haute 0.699 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.82 ATR (stop 4.132 %) — p(stop avant cible) 0.5967 [0.54 ; 0.65], R/R 2.065, perte reelle 4.201 % (gap inclus), EV 0.4287 % — **REFUSE**
      - refuse : p_stop_first 0.597, borne haute 0.647 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 1.96 ATR (stop 7.482 %) — p(stop avant cible) 0.3512 [0.30 ; 0.40], R/R 1.147, perte reelle 7.565 % (gap inclus), EV 1.0929 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 2.59 ATR (stop 9.311 %) — p(stop avant cible) 0.2841 [0.24 ; 0.33], R/R 0.924, perte reelle 9.392 % (gap inclus), EV 0.9058 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 13.87 ATR (stop 42.4 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.205, perte reelle 42.4 % (gap inclus), EV 1.3256 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.67 % > budget 12.00 %
   - 🟢 support a 15.84 ATR (stop 48.197 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.18, perte reelle 48.197 % (gap inclus), EV 1.3256 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.67 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.733 %) — p(stop avant cible) 0.924 [0.89 ; 0.95], R/R 11.447, perte reelle 0.758 % (gap inclus), EV -0.0472 % — **REFUSE**
      - refuse : cible atteinte seulement 7.5 % du temps (< 15 %) meme a 10 seances : le R/R de 11.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.924, borne haute 0.948 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 7.5 % x 8.68 % + P(rien) 0.1 % x 2.78 % ne couvrent pas P(stop) 92.4 % x 0.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.467 %) — p(stop avant cible) 0.8236 [0.78 ; 0.86], R/R 5.771, perte reelle 1.503 % (gap inclus), EV 0.2462 % — **REFUSE**
      - refuse : p_stop_first 0.824, borne haute 0.861 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 0.82 ATR (stop 3.287 %) — p(stop avant cible) 0.6506 [0.60 ; 0.70], R/R 2.58, perte reelle 3.363 % (gap inclus), EV 0.5216 % — **REFUSE**
      - refuse : p_stop_first 0.651, borne haute 0.699 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 3.666 %) — p(stop avant cible) 0.6263 [0.57 ; 0.68], R/R 2.315, perte reelle 3.748 % (gap inclus), EV 0.4822 % — **REFUSE**
      - refuse : p_stop_first 0.626, borne haute 0.676 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 1.96 ATR (stop 6.637 %) — p(stop avant cible) 0.4033 [0.35 ; 0.46], R/R 1.295, perte reelle 6.702 % (gap inclus), EV 0.9944 % — **REFUSE**
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.59 ATR (stop 8.466 %) — p(stop avant cible) 0.3106 [0.26 ; 0.36], R/R 1.011, perte reelle 8.579 % (gap inclus), EV 0.9952 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 10.266 %) — p(stop avant cible) 0.2649 [0.22 ; 0.31], R/R 0.834, perte reelle 10.402 % (gap inclus), EV 0.7334 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 11.733 %) — p(stop avant cible) 0.2003 [0.16 ; 0.24], R/R 0.73, perte reelle 11.888 % (gap inclus), EV 0.8663 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.35 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 13.199 %) — p(stop avant cible) 0.1595 [0.12 ; 0.20], R/R 0.648, perte reelle 13.394 % (gap inclus), EV 0.8643 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.82 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 14.666 %) — p(stop avant cible) 0.1298 [0.10 ; 0.17], R/R 0.581, perte reelle 14.936 % (gap inclus), EV 0.7992 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.37 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.132 %) — p(stop avant cible) 0.1021 [0.07 ; 0.14], R/R 0.531, perte reelle 16.349 % (gap inclus), EV 0.8774 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.57 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 17.599 %) — p(stop avant cible) 0.0863 [0.06 ; 0.12], R/R 0.489, perte reelle 17.756 % (gap inclus), EV 0.9153 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.87 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.065 %) — p(stop avant cible) 0.0606 [0.04 ; 0.09], R/R 0.452, perte reelle 19.185 % (gap inclus), EV 1.0255 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.21 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 20.532 %) — p(stop avant cible) 0.0442 [0.03 ; 0.07], R/R 0.419, perte reelle 20.683 % (gap inclus), EV 1.077 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.32 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 21.998 %) — p(stop avant cible) 0.0259 [0.01 ; 0.05], R/R 0.388, perte reelle 22.344 % (gap inclus), EV 1.1922 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.65 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 23.465 %) — p(stop avant cible) 0.0141 [0.01 ; 0.03], R/R 0.364, perte reelle 23.837 % (gap inclus), EV 1.2493 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.76 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 198.72, ATR14 5.8287 (2.933 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.359 ATR = 1.053 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.147 % | 198.4286 | 92.85 % | 95.36 % | 96.17 % | 96.97 % | 98.27 % | 98.67 % |
| 0.1 ATR | 0.293 % | 198.1371 | 84.89 % | 89.52 % | 91.42 % | 93.63 % | 95.22 % | 96.41 % |
| 0.15 ATR | 0.44 % | 197.8457 | 77.14 % | 83.87 % | 86.18 % | 89.99 % | 92.58 % | 94.25 % |
| 0.2 ATR | 0.587 % | 197.5543 | 69.08 % | 78.33 % | 81.94 % | 86.55 % | 90.35 % | 92.51 % |
| 0.25 ATR | 0.733 % | 197.2628 | 62.24 % | 73.49 % | 77.6 % | 82.91 % | 87.91 % | 90.97 % |
| 0.35 ATR | 1.027 % | 196.68 | 50.86 % | 65.22 % | 70.94 % | 78.06 % | 83.74 % | 87.89 % |
| 0.5 ATR | 1.467 % | 195.8056 | 35.95 % | 52.42 % | 59.43 % | 68.76 % | 77.64 % | 83.37 % |
| 0.75 ATR | 2.2 % | 194.3485 | 19.44 % | 34.98 % | 44.3 % | 55.01 % | 66.46 % | 76.18 % |
| 1.0 ATR | 2.933 % | 192.8913 | 8.86 % | 22.68 % | 32.29 % | 43.68 % | 56.1 % | 67.15 % |
| 1.25 ATR | 3.666 % | 191.4341 | 4.33 % | 15.22 % | 23.11 % | 33.97 % | 46.24 % | 58.11 % |
| 1.5 ATR | 4.4 % | 189.9769 | 2.01 % | 10.38 % | 17.26 % | 26.49 % | 39.74 % | 53.59 % |
| 2.0 ATR | 5.866 % | 187.0626 | 0.6 % | 3.73 % | 9.38 % | 15.77 % | 29.07 % | 40.14 % |
| 2.5 ATR | 7.333 % | 184.1482 | 0.1 % | 1.51 % | 3.33 % | 9.3 % | 19.41 % | 29.98 % |
| 3.0 ATR | 8.799 % | 181.2339 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.48 % |
| 4.0 ATR | 11.733 % | 175.4051 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 17.599 % | 163.7477 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.21 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.09 ATR | 1.53 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.98 ATR | 1.20 ATR | 1.38 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.86 ATR | 0.97 ATR | 1.28 ATR | 1.57 ATR | 1.80 ATR | 2.45 ATR | 2.97 ATR |
| **10 s.** | 0.56 ATR | 1.16 ATR | 1.30 ATR | 1.82 ATR | 2.21 ATR | 2.47 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.78 ATR | 1.63 ATR | 1.82 ATR | 2.35 ATR | 2.83 ATR | 3.23 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.467 %, prix 195.8048), p(touche) 35.95 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.606–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.2 %, prix 194.3482), p(touche) 34.98 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.738–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.2 %, prix 194.3482), p(touche) 44.3 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.971–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.933 %, prix 192.8915), p(touche) 43.68 % (en stress 100.0 %)  ✅ optimum identifie (83.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.298–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.4 %, prix 189.9763), p(touche) 39.74 % (en stress 100.0 %)  ✅ optimum identifie (87.0 % des re-echantillons)
- **20 seance(s)** : plage utile 1.819–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (8.799 %, prix 181.2346), p(touche) 22.48 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.006 | EV/share : $-0.033 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 25 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 9.8 | bear 40.4 | side 49.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 532.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.533% → cible +1.474% / stop −2.5%, p_fill 83%, n_eff≈88.7) : P(cible|rempli) **52%** · **EV/risk +0.016** (×p_fill ; si rempli +0.05% du capital)
  - **swing** (entrée dip −1.167% → cible +3.318% / stop −2.968%, p_fill 75%, n_eff≈87.7) : P(cible|rempli) **52%** · **EV/risk +0.080** (×p_fill ; si rempli +0.32% du capital)
  - **deep** (entrée dip −1.8% → cible +4.723% / stop −4.48%, p_fill 74%, n_eff≈83.9) : P(cible|rempli) **51%** · **EV/risk +0.059** (×p_fill ; si rempli +0.36% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→73% · +2.0%→44% · +3.0%→24% · +5.0%→9% · +8.0%→2%
- Range intraday médian 3.72% (p90 6.89%) · excursion haute méd. +1.85% / basse méd. −1.67%
- Profil de vol intra : ouverture 2.899% vs midi 0.725% vs clôture 0.809% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; neutre — autocorr -0.02)_ ; drift intra méd. 0.326% ; recovery-V 29%
- **σ réalisé intraday** 2.336% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 40% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 189.3098 (VA 188.5023–190.9247 ; dernier close 188.79)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 70% · **stop −3.61%** sous le fill (sous le bruit) · cible +1.61% · R/R 0.45 (high win-rate)
- Gaps overnight (n=156) : méd. -0.06% · baisse 51% (gap-down >1% 29% · >2% 6%)
- Excursion ouverture 5min (n=157) : bas méd −0.81% (p90 −1.9%) · haut méd +0.74% · range méd 1.73%
- Excursion ouverture 15min (n=157) : bas méd −1.0% (p90 −2.43%) · haut méd +0.97% · range méd 2.2%
- Excursion ouverture 30min (n=157) : bas méd −1.11% (p90 −2.9%) · haut méd +1.17% · range méd 2.56%
- Excursion ouverture 60min (n=157) : bas méd −1.33% (p90 −3.06%) · haut méd +1.29% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 188.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 75% (117/156) · gap 38% · délai 0.0min · rebond 61% (67/117) (MFE +1.35%)
   - −1.0% : fill 30min 55% · séance 62% (103/156) · gap 29% · délai 0.0min · rebond 66% (60/103) (MFE +1.43%)
   - −1.5% : fill 30min 42% · séance 50% (86/156) · gap 17% · délai 0.1min · rebond 64% (52/86) (MFE +1.42%)
   - −2.0% : fill 30min 35% · séance 44% (77/156) · gap 6% · délai 1.5min · rebond 70% (49/77) (MFE +1.61%)
   - −3.0% : fill 30min 16% · séance 23% (50/156) · gap 3% · délai 6.1min · rebond 53% (23/50) (MFE +1.19%)
   - −4.0% : fill 30min 10% · séance 15% (34/156) · gap 2% · délai 15.4min · rebond 52% (16/34) (MFE +1.04%)
   - −5.0% : fill 30min 4% · séance 10% (23/156) · gap 0% · délai 45.3min · rebond 48% (12/23) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.9%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −1.84%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −1.57%) → stop au-delà de −1.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=515 jambes) : jambe baissière méd −1.06% (p90 −2.33%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 91% (70/75) · rebond 63% (41/70)
      · −2.0% : fill 75% (57/75) · rebond 72% (36/57)
      · −3.0% : fill 42% (38/75) · rebond 52% (18/38)
      · −4.0% : fill 29% (27/75) · rebond 54% (13/27)
      · −5.0% : fill 19% (19/75) · rebond 53% (11/19)
   - **flat** (23 séances) :
      · −1.0% : fill 78% (19/23) · rebond 58% (9/19)
      · −2.0% : fill 45% (13/23) · rebond 61% (8/13)
      · −3.0% : fill 24% (9/23) · rebond 54% (4/9)
      · −4.0% : fill 15% (6/23) · rebond 43% (3/6)
      · −5.0% : fill 8% (3/23) · rebond 13% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 25% (14/58) · rebond 85% (10/14)
      · −2.0% : fill 12% (7/58) · rebond 67% (5/7)
      · −3.0% : fill 3% (3/58) · rebond 66% (1/3)
      · −4.0% : fill 1% (1/58) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 51% en base · 71% si les 15 1res min sont vertes (80 cas) · 29% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=157) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 86% si début vert vs 15% si rouge (base 51% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **86%** · continue >prix actuel 55% ; creux résiduel méd -0.8% (q20 -1.44%) → **SL/trailing à −1.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +2.11% → **scale +1.07% / runner +2.11%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **15%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.53%** (au-delà de la MAE q10 -2.53%), cible rebond +1.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-2.87% .. +3.73%] · haut q95 +4.0% · bas q05 -3.52%
   - 60min (n=157) : retour [-3.01% .. +3.93%] · haut q95 +4.71% · bas q05 -3.64%
   - 2h (n=157) : retour [-3.61% .. +5.08%] · haut q95 +5.27% · bas q05 -4.46%
   - 4h (n=157) : retour [-3.99% .. +5.64%] · haut q95 +6.27% · bas q05 -5.01%
   - 6h (n=157) : retour [-4.0% .. +5.46%] · haut q95 +6.81% · bas q05 -5.37%
   - session (n=157) : retour [-3.98% .. +4.77%] · haut q95 +6.81% · bas q05 -5.37%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.7% des séances sont trend-up (mild 1.3% / strong 4.5%) · base = 9 séances trend-up (n_eff 7.0)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.91% (p75 1.39% / p90 1.52%) · ~2.0 replis/séance, durée méd 77.38 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 47.34 min, n=25)
   - −1.0% → **51%** (reprise méd 65.0 min, n=11)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.52%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +4.55% (q75 +7.54% / q95 +12.13%), MFE méd +6.21% / q90 +12.4%
   - Échelle scale-out : +6.21% (33%) / +8.19% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−1.52%** depuis le plus-haut = décay → P(retournement) **65%** (préavis méd 99.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 53% du temps (retour médian dernière heure +0.12%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.63 · part idiosyncratique 0.37
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 80.2  _(surachat)_
- **ADX** : 31.2  _(tendance etablie)_
- **MACD** : hist 0.423  _(pas de croisement recent)_
- **BB** : %B 0.91 · largeur 18.4%
- **ATR** : 5.83 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.214  _(accumulation)_
- **Vol ratio** : 1.69  _(volume au-dessus de la moyenne)_
- **Choppiness** : 41.0  _(transition)_
- **MA** : MA20 184.9 · MA50 175.24 · MA200 152.26  _(prix > MA20)_
- **Dist MA** : MA20 +7.5% · MA50 +13.4% · MA200 +30.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (859012 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
