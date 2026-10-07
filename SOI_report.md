# SOI

**Generated** : 2026-10-07T00:12:09.437334+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 10/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €167.45  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)  
> ↳ spot €167.45 (+5.1% vs entrée) · entrée €159.32 · stop €149.42 · T1 €179.13 · R/R 2.0  
> ↳ ¼-Kelly 0.046 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 73.1 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €157.08–€161.57 (mid €159.32)
- Spot actuel : €167.45 (+5.1% au-dessus de la zone — repli à attendre)
- Stop : €149.42 (R/R 2 (resserré, parité Claude) ; -6.21 % depuis l'entree)
- Targets : T1 €179.13 · R/R 2.0 | T2 €188.86 · R/R 2.98 | T3 €198.60 · R/R 3.97
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €149.42


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.91 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.77 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **7.949 pt plus bas** dans le cas TYPIQUE (médiane), 16.409 au p90, **18.524 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 10.77 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.025 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.675 % | p01 -5.132 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4204** [0.3487 ; 0.4948] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4289** [0.3775 ; 0.4815] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4921** [0.4397 ; 0.5447] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (26.5 pt), deep (25.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-14.04 %** | vol 6.65 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.97 % contre 7.27 % aujourd'hui, rapport 0.55)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.4 % vs -11.44 % si l'on extrapolait par √5 _(rapport 1.084 ; < 1 = le √5 surestime)_
- **β de baisse : 1.104** (β de hausse 1.5764, asymétrie 0.7003) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.009× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 158.7429 sur atr_grid (1.0 ATR, 5.2 %) — p(stop avant cible) 0.6201 [0.57 ; 0.67], R/R 3.331, perte reelle 5.585 % (gap inclus), CVaR 9.564 %, EV 1.7426 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2184 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.620, borne haute 0.670 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.8 %) — p(stop avant cible) 0.5209 [0.47 ; 0.57], R/R 2.271, perte reelle 8.192 % (gap inclus), EV 1.4705 % — **REFUSE**
      - refuse : p_stop_first 0.521, borne haute 0.573 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 1.8 ATR (stop 11.741 %) — p(stop avant cible) 0.3769 [0.33 ; 0.43], R/R 1.533, perte reelle 12.131 % (gap inclus), EV 1.6106 % — **REFUSE**
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.68 % > budget 12.00 %
   - 🟢 support a 2.15 ATR (stop 13.565 %) — p(stop avant cible) 0.3115 [0.26 ; 0.36], R/R 1.334, perte reelle 13.941 % (gap inclus), EV 1.6828 % — **REFUSE**
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.91 % > budget 12.00 %
   - ⚪ swing_based a 3.43 ATR (stop 20.248 %) — p(stop avant cible) 0.1304 [0.10 ; 0.17], R/R 0.899, perte reelle 20.697 % (gap inclus), EV 2.7222 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.42 % > budget 12.00 %
   - 🟢 support a 5.79 ATR (stop 32.526 %) — p(stop avant cible) 0.0283 [0.01 ; 0.05], R/R 0.571, perte reelle 32.592 % (gap inclus), EV 2.9445 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.47 % > budget 12.00 %
   - 🟢 support a 7.11 ATR (stop 39.393 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 0.472, perte reelle 39.393 % (gap inclus), EV 2.9589 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.19 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.3 %) — p(stop avant cible) 0.8929 [0.86 ; 0.92], R/R 13.411, perte reelle 1.387 % (gap inclus), EV 0.482 % — **REFUSE**
      - refuse : cible atteinte seulement 8.1 % du temps (< 15 %) meme a 10 seances : le R/R de 13.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.893, borne haute 0.922 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 2.6 %) — p(stop avant cible) 0.7883 [0.74 ; 0.83], R/R 6.739, perte reelle 2.76 % (gap inclus), EV 1.1661 % — **REFUSE**
      - refuse : p_stop_first 0.788, borne haute 0.829 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 3.9 %) — p(stop avant cible) 0.7038 [0.65 ; 0.75], R/R 4.45, perte reelle 4.18 % (gap inclus), EV 1.3918 % — **REFUSE**
      - refuse : p_stop_first 0.704, borne haute 0.750 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 5.2 %) — p(stop avant cible) 0.6201 [0.57 ; 0.67], R/R 3.331, perte reelle 5.585 % (gap inclus), EV 1.7426 % — **REFUSE**
      - refuse : p_stop_first 0.620, borne haute 0.670 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 6.5 %) — p(stop avant cible) 0.5636 [0.51 ; 0.62], R/R 2.672, perte reelle 6.961 % (gap inclus), EV 1.7912 % — **REFUSE**
      - refuse : p_stop_first 0.564, borne haute 0.615 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 1.8 ATR (stop 10.903 %) — p(stop avant cible) 0.3981 [0.35 ; 0.45], R/R 1.64, perte reelle 11.34 % (gap inclus), EV 1.7003 % — **REFUSE**
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.38 % > budget 12.00 %
   - 🟢 grid_snapped a 2.15 ATR (stop 12.727 %) — p(stop avant cible) 0.3372 [0.29 ; 0.39], R/R 1.419, perte reelle 13.112 % (gap inclus), EV 1.6514 % — **REFUSE**
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.32 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 14.3 %) — p(stop avant cible) 0.2998 [0.25 ; 0.35], R/R 1.266, perte reelle 14.692 % (gap inclus), EV 1.5922 % — **REFUSE**
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.65 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 15.6 %) — p(stop avant cible) 0.2397 [0.20 ; 0.29], R/R 1.165, perte reelle 15.964 % (gap inclus), EV 2.028 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.34 % > budget 12.00 %
   - ⚪ grid_snapped a 3.43 ATR (stop 19.411 %) — p(stop avant cible) 0.165 [0.13 ; 0.21], R/R 0.941, perte reelle 19.765 % (gap inclus), EV 2.4749 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.58 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 23.399 %) — p(stop avant cible) 0.0689 [0.05 ; 0.10], R/R 0.775, perte reelle 24.0 % (gap inclus), EV 3.0522 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.23 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 25.999 %) — p(stop avant cible) 0.0477 [0.03 ; 0.07], R/R 0.7, perte reelle 26.571 % (gap inclus), EV 3.0284 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.44 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 28.599 %) — p(stop avant cible) 0.0327 [0.02 ; 0.06], R/R 0.644, perte reelle 28.872 % (gap inclus), EV 3.0082 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.96 % > budget 12.00 %
   - 🟢 grid_snapped a 5.79 ATR (stop 31.688 %) — p(stop avant cible) 0.0283 [0.01 ; 0.05], R/R 0.587, perte reelle 31.695 % (gap inclus), EV 2.9698 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.96 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 33.799 %) — p(stop avant cible) 0.0247 [0.01 ; 0.05], R/R 0.55, perte reelle 33.799 % (gap inclus), EV 2.9476 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.39 % > budget 12.00 %
   - 🟢 grid_snapped a 7.11 ATR (stop 38.556 %) — p(stop avant cible) 0.0098 [0.00 ; 0.02], R/R 0.482, perte reelle 38.556 % (gap inclus), EV 2.9627 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.13 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 41.599 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.447, perte reelle 41.599 % (gap inclus), EV 3.0012 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.36 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 167.45, ATR14 8.7071 (5.2 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.357 ATR = 1.856 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.26 % | 167.0146 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.52 % | 166.5793 | 84.8 % | 89.89 % | 91.75 % | 94.29 % | 96.04 % | 97.3 % |
| 0.15 ATR | 0.78 % | 166.1439 | 77.84 % | 84.99 % | 87.62 % | 90.85 % | 93.57 % | 95.2 % |
| 0.2 ATR | 1.04 % | 165.7086 | 69.12 % | 79.59 % | 83.4 % | 87.7 % | 91.2 % | 93.21 % |
| 0.25 ATR | 1.3 % | 165.2732 | 62.55 % | 75.66 % | 80.06 % | 85.93 % | 89.91 % | 92.61 % |
| 0.35 ATR | 1.82 % | 164.4025 | 50.69 % | 67.22 % | 72.99 % | 80.61 % | 85.46 % | 89.91 % |
| 0.5 ATR | 2.6 % | 163.0964 | 35.69 % | 55.05 % | 62.38 % | 72.64 % | 80.61 % | 87.01 % |
| 0.75 ATR | 3.9 % | 160.9196 | 17.06 % | 34.84 % | 46.27 % | 57.87 % | 72.11 % | 80.12 % |
| 1.0 ATR | 5.2 % | 158.7429 | 8.33 % | 23.65 % | 33.79 % | 46.95 % | 64.0 % | 74.63 % |
| 1.25 ATR | 6.5 % | 156.5661 | 4.12 % | 15.51 % | 24.85 % | 36.91 % | 55.89 % | 68.93 % |
| 1.5 ATR | 7.8 % | 154.3893 | 2.25 % | 10.4 % | 17.98 % | 29.23 % | 47.87 % | 62.54 % |
| 2.0 ATR | 10.4 % | 150.0357 | 0.59 % | 4.51 % | 8.84 % | 17.72 % | 34.32 % | 52.05 % |
| 2.5 ATR | 13.0 % | 145.6821 | 0.29 % | 2.45 % | 4.91 % | 11.61 % | 23.74 % | 44.26 % |
| 3.0 ATR | 15.6 % | 141.3286 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 16.32 % | 36.26 % |
| 4.0 ATR | 20.799 % | 132.6214 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.4 % | 23.18 % |
| 6.0 ATR | 31.199 % | 115.2072 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 11.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.56 ATR | 0.62 ATR | 0.79 ATR | 0.97 ATR | 1.11 ATR | 1.53 ATR | 1.96 ATR |
| **3 s.** | 0.32 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.25 ATR | 1.43 ATR | 1.94 ATR | 2.49 ATR |
| **5 s.** | 0.46 ATR | 0.93 ATR | 1.05 ATR | 1.38 ATR | 1.68 ATR | 1.90 ATR | 2.68 ATR | 3.59 ATR |
| **10 s.** | 0.67 ATR | 1.43 ATR | 1.61 ATR | 2.06 ATR | 2.44 ATR | 2.75 ATR | 3.91 ATR | 5.78 ATR |
| **20 s.** | 0.98 ATR | 2.13 ATR | 2.45 ATR | 3.25 ATR | 3.86 ATR | 4.57 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.407–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (63.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.624–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.775–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.2 %, prix 158.7426), p(touche) 33.79 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.049–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.5 %, prix 156.5657), p(touche) 36.91 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.606–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.453–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (13.0 %, prix 145.6815), p(touche) 44.26 % (en stress 93.07 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.322 | EV/share : €3.188 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 21 % | T3 15 %
- Kelly (position) : f* 0.183 | ¼-Kelly 0.046 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.5 | bear 9.5 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 502.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.205% → cible +2.659% / stop −2.5%, p_fill 54%, n_eff≈60.8) : P(cible|rempli) **43%** · **EV/risk -0.011** (×p_fill ; si rempli -0.05% du capital)
  - **swing** (entrée dip −4.856% → cible +12.431% / stop −6.215%, p_fill 42%, n_eff≈50.4) : P(cible|rempli) **28%** · **EV/risk -0.023** (×p_fill ; si rempli -0.34% du capital)
  - **deep** (entrée dip −7.5% → cible +15.648% / stop −8.432%, p_fill 45%, n_eff≈52.6) : P(cible|rempli) **33%** · **EV/risk -0.002** (×p_fill ; si rempli -0.04% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→79% · +2.0%→66% · +3.0%→55% · +5.0%→38% · +8.0%→18%
- Range intraday médian 7.97% (p90 14.88%) · excursion haute méd. +3.44% / basse méd. −3.03%
- Profil de vol intra : ouverture 4.948% vs midi 1.438% vs clôture 2.123% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 12% · trend ↑1%/↓2% ; spike-down 69% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.021)_ ; drift intra méd. 0.659% ; recovery-V 45%
- **σ réalisé intraday** 3.905% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 55% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 164.595 (VA 162.435–167.025 ; dernier close 169.06)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 41% · rebond 75% · **stop −7.26%** sous le fill (sous le bruit) · cible +3.18% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.49% · baisse 39% (gap-down >1% 24% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.97% (p90 −2.92%) · haut méd +0.92% · range méd 2.17%
- Excursion ouverture 15min (n=160) : bas méd −1.24% (p90 −4.28%) · haut méd +1.17% · range méd 2.96%
- Excursion ouverture 30min (n=160) : bas méd −1.48% (p90 −4.65%) · haut méd +1.29% · range méd 3.39%
- Excursion ouverture 60min (n=160) : bas méd −1.63% (p90 −4.95%) · haut méd +1.46% · range méd 3.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 170.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 74% (121/159) · gap 30% · délai 0.2min · rebond 74% (87/121) (MFE +2.15%)
   - −1.0% : fill 30min 53% · séance 69% (112/159) · gap 24% · délai 0.2min · rebond 74% (82/112) (MFE +2.11%)
   - −1.5% : fill 30min 46% · séance 60% (102/159) · gap 17% · délai 1.4min · rebond 76% (77/102) (MFE +2.4%)
   - −2.0% : fill 30min 40% · séance 55% (94/159) · gap 15% · délai 4.7min · rebond 74% (73/94) (MFE +2.54%)
   - −3.0% : fill 30min 26% · séance 41% (75/159) · gap 8% · délai 3.3min · rebond 75% (63/75) (MFE +3.18%)
   - −4.0% : fill 30min 19% · séance 34% (64/159) · gap 5% · délai 15.0min · rebond 77% (53/64) (MFE +2.54%)
   - −5.0% : fill 30min 12% · séance 27% (50/159) · gap 2% · délai 53.0min · rebond 67% (38/50) (MFE +2.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −3.21%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −2.3%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.8% (p90 −2.29%) → stop au-delà de −1.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1335 jambes) : jambe baissière méd −1.24% (p90 −3.03%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 93% (53/56) · rebond 67% (35/53)
      · −2.0% : fill 90% (51/56) · rebond 72% (38/51)
      · −3.0% : fill 73% (45/56) · rebond 73% (37/45)
      · −4.0% : fill 63% (39/56) · rebond 85% (35/39)
      · −5.0% : fill 50% (32/56) · rebond 74% (26/32)
   - **flat** (13 séances) :
      · −1.0% : fill 78% (11/13) · rebond 86% (9/11)
      · −2.0% : fill 68% (10/13) · rebond 88% (9/10)
      · −3.0% : fill 66% (9/13) · rebond 64% (7/9)
      · −4.0% : fill 60% (8/13) · rebond 79% (6/8)
      · −5.0% : fill 44% (7/13) · rebond 45% (5/7)
   - **gap-up** (90 séances) :
      · −1.0% : fill 54% (48/90) · rebond 78% (38/48)
      · −2.0% : fill 33% (33/90) · rebond 73% (26/33)
      · −3.0% : fill 18% (21/90) · rebond 87% (19/21)
      · −4.0% : fill 13% (17/90) · rebond 56% (12/17)
      · −5.0% : fill 10% (11/90) · rebond 60% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 68% si les 15 1res min sont vertes (77 cas) · 41% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 78% si début vert vs 33% si rouge (base 54% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **78%** · continue >prix actuel 62% ; creux résiduel méd -1.36% (q20 -3.77%) → **SL/trailing à −3.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.91% / q75 +4.81% → **scale +2.91% / runner +4.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **33%** (continue à baisser 50%) → **RÉDUIRE ~67%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.35%** (au-delà de la MAE q10 -7.35%), cible rebond +2.38% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.59% .. +5.74%] · haut q95 +6.51% · bas q05 -5.93%
   - 60min (n=160) : retour [-5.37% .. +4.91%] · haut q95 +7.61% · bas q05 -6.55%
   - 2h (n=160) : retour [-6.01% .. +5.57%] · haut q95 +7.84% · bas q05 -7.41%
   - 4h (n=160) : retour [-6.76% .. +7.19%] · haut q95 +8.48% · bas q05 -8.09%
   - 6h (n=160) : retour [-7.59% .. +8.57%] · haut q95 +9.11% · bas q05 -9.35%
   - session (n=160) : retour [-7.86% .. +8.91%] · haut q95 +11.32% · bas q05 -10.78%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **37%**. Lecture précoce 30 min : signature présente → 21% vs absente 2% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.39% / p90 1.98%) · ~4.89 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **90%** (reprise méd 25.0 min, n=57)
   - −1.0% → **90%** (reprise méd 45.44 min, n=31)
   - −1.5% → **80%** (reprise méd 50.92 min, n=16)
   - −2.0% → **85%** (reprise méd 52.07 min, n=12)
   - −3.0% → **100%** (reprise méd 60.96 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.98%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +8.74% (q75 +9.15% / q95 +13.89%), MFE méd +9.28% / q90 +14.1%
   - Échelle scale-out : +9.28% (33%) / +9.96% (33%) / +14.1% (34%)
- **DÉSARMER** : repli > **−1.98%** depuis le plus-haut = décay → P(retournement) **15%** (préavis méd 36.46 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.1% : P(retournement après) 0% (mèche méd 2.71%)
- **CONTEXTE** : la dernière heure tient les gains 79% du temps (retour médian dernière heure +1.27%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.5 · part idiosyncratique 0.5
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 73.1  _(surachat)_
- **ADX** : 30.3  _(tendance etablie)_
- **MACD** : hist 1.703  _(pas de croisement recent)_
- **BB** : %B 0.88 · largeur 35.3%
- **ATR** : 8.71 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.096  _(accumulation)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 44.4  _(transition)_
- **MA** : MA20 147.67 · MA50 129.7 · MA200 94.29  _(prix > MA20)_
- **Dist MA** : MA20 +13.4% · MA50 +29.1% · MA200 +77.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (536351 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
