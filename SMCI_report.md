# SMCI

**Generated** : 2026-10-07T00:24:23.518975+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 10/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $43.45  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)  
> ↳ spot $43.45 (+3.1% vs entrée) · entrée $42.16 · stop $39.66 · T1 $47.16 · R/R 2.0  
> ↳ ¼-Kelly 0.023 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -2.8 % ≠ (strike 42.0 − spot 43.45)/spot = -3.3 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 72.3 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $41.72–$42.60 (mid $42.16)
- Spot actuel : $43.45 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : $39.66 (R/R 2 (resserré, parité Claude) ; -5.93 % depuis l'entree)
- Targets : T1 $47.16 · R/R 2.0 | T2 $49.61 · R/R 2.98 | T3 $52.05 · R/R 3.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $39.66


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.73 %)** : le gap seul le franchit 1.516 % des séances (19 fois sur 1253).
   - exécution **3.672 pt plus bas** dans le cas TYPIQUE (médiane), 16.368 au p90, **20.321 au pire**
   - perte réelle **14.422 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 8.73 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0863 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.795 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.498** [0.4241 ; 0.572] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4931** [0.4406 ; 0.5457] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4686** [0.4164 ; 0.5213] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.34 %** | vol 5.83 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.91 % contre 6.46 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.48 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5326** (β de hausse 1.2187, asymétrie 1.2576) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.84× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 41.8091 sur atr_grid (0.75 ATR, 3.777 %) — p(stop avant cible) 0.7373 [0.69 ; 0.78], R/R 4.581, perte reelle 4.322 % (gap inclus), CVaR 11.339 %, EV 0.4647 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4498 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 14.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.737, borne haute 0.782 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.17 ATR (stop 8.226 %) — p(stop avant cible) 0.47 [0.42 ; 0.52], R/R 2.06, perte reelle 9.614 % (gap inclus), EV 1.1591 % — **REFUSE**
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.86 % > budget 12.00 %
   - 🟢 support a 1.82 ATR (stop 11.481 %) — p(stop avant cible) 0.3331 [0.28 ; 0.38], R/R 1.494, perte reelle 13.256 % (gap inclus), EV 1.5339 % — **REFUSE**
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.03 % > budget 12.00 %
   - 🟢 support a 9.17 ATR (stop 48.512 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.399, perte reelle 49.665 % (gap inclus), EV 1.9823 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.29 % > budget 12.00 %
   - 🟢 support a 10.96 ATR (stop 57.488 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.344, perte reelle 57.488 % (gap inclus), EV 1.9797 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.35 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.259 %) — p(stop avant cible) 0.9198 [0.89 ; 0.94], R/R 13.759, perte reelle 1.439 % (gap inclus), EV 0.0885 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 13.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.920, borne haute 0.945 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 2.518 %) — p(stop avant cible) 0.8275 [0.79 ; 0.86], R/R 6.952, perte reelle 2.848 % (gap inclus), EV 0.274 % — **REFUSE**
      - refuse : cible atteinte seulement 11.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.828, borne haute 0.865 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 3.777 %) — p(stop avant cible) 0.7373 [0.69 ; 0.78], R/R 4.581, perte reelle 4.322 % (gap inclus), EV 0.4647 % — **REFUSE**
      - refuse : cible atteinte seulement 14.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.737, borne haute 0.782 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 1.17 ATR (stop 7.415 %) — p(stop avant cible) 0.5213 [0.47 ; 0.57], R/R 2.276, perte reelle 8.7 % (gap inclus), EV 0.8948 % — **REFUSE**
      - refuse : p_stop_first 0.521, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.18 % > budget 12.00 %
   - 🟢 grid_snapped a 1.82 ATR (stop 10.671 %) — p(stop avant cible) 0.3709 [0.32 ; 0.42], R/R 1.607, perte reelle 12.323 % (gap inclus), EV 1.3577 % — **REFUSE**
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.60 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 12.588 %) — p(stop avant cible) 0.2836 [0.24 ; 0.33], R/R 1.367, perte reelle 14.487 % (gap inclus), EV 1.8278 % — **REFUSE**
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.21 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 13.847 %) — p(stop avant cible) 0.2376 [0.20 ; 0.28], R/R 1.239, perte reelle 15.984 % (gap inclus), EV 1.953 % — **REFUSE**
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.83 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 15.106 %) — p(stop avant cible) 0.2133 [0.17 ; 0.26], R/R 1.147, perte reelle 17.271 % (gap inclus), EV 1.8353 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.20 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 17.624 %) — p(stop avant cible) 0.1612 [0.13 ; 0.20], R/R 0.982, perte reelle 20.165 % (gap inclus), EV 2.2231 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.15 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 20.141 %) — p(stop avant cible) 0.1322 [0.10 ; 0.17], R/R 0.893, perte reelle 22.175 % (gap inclus), EV 2.3142 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.45 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 22.659 %) — p(stop avant cible) 0.1124 [0.08 ; 0.15], R/R 0.813, perte reelle 24.352 % (gap inclus), EV 2.2343 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.46 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 25.177 %) — p(stop avant cible) 0.0903 [0.06 ; 0.12], R/R 0.75, perte reelle 26.413 % (gap inclus), EV 2.2466 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.41 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.694 %) — p(stop avant cible) 0.08 [0.05 ; 0.11], R/R 0.703, perte reelle 28.181 % (gap inclus), EV 2.1505 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.47 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 30.212 %) — p(stop avant cible) 0.075 [0.05 ; 0.11], R/R 0.653, perte reelle 30.339 % (gap inclus), EV 2.0056 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.40 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 32.73 %) — p(stop avant cible) 0.0673 [0.04 ; 0.10], R/R 0.601, perte reelle 32.926 % (gap inclus), EV 1.861 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.99 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 35.247 %) — p(stop avant cible) 0.0596 [0.04 ; 0.09], R/R 0.56, perte reelle 35.335 % (gap inclus), EV 1.7776 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.35 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 37.765 %) — p(stop avant cible) 0.0399 [0.02 ; 0.06], R/R 0.524, perte reelle 37.802 % (gap inclus), EV 1.8157 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.89 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 40.283 %) — p(stop avant cible) 0.0119 [0.00 ; 0.03], R/R 0.491, perte reelle 40.304 % (gap inclus), EV 1.9811 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.26 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 43.45, ATR14 2.1879 (5.035 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.342 ATR = 1.722 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.252 % | 43.3406 | 90.43 % | 93.25 % | 94.65 % | 95.15 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.504 % | 43.2312 | 82.07 % | 87.2 % | 89.2 % | 91.1 % | 92.89 % | 94.87 % |
| 0.15 ATR | 0.755 % | 43.1218 | 74.92 % | 82.06 % | 84.96 % | 88.17 % | 90.55 % | 93.53 % |
| 0.2 ATR | 1.007 % | 43.0124 | 68.08 % | 77.32 % | 80.52 % | 85.64 % | 89.02 % | 92.2 % |
| 0.25 ATR | 1.259 % | 42.903 | 61.83 % | 72.58 % | 76.29 % | 82.2 % | 86.99 % | 90.45 % |
| 0.35 ATR | 1.762 % | 42.6843 | 49.04 % | 63.21 % | 69.53 % | 77.05 % | 82.62 % | 87.89 % |
| 0.5 ATR | 2.518 % | 42.3561 | 34.74 % | 49.7 % | 58.32 % | 68.66 % | 76.83 % | 83.37 % |
| 0.75 ATR | 3.777 % | 41.8091 | 17.12 % | 33.17 % | 42.89 % | 55.01 % | 66.16 % | 75.15 % |
| 1.0 ATR | 5.035 % | 41.2621 | 7.85 % | 21.27 % | 30.27 % | 43.48 % | 56.81 % | 68.48 % |
| 1.25 ATR | 6.294 % | 40.7152 | 3.73 % | 14.72 % | 22.0 % | 32.76 % | 47.56 % | 60.88 % |
| 1.5 ATR | 7.553 % | 40.1682 | 1.51 % | 9.38 % | 16.04 % | 25.68 % | 41.36 % | 54.52 % |
| 2.0 ATR | 10.071 % | 39.0743 | 0.3 % | 3.53 % | 8.17 % | 15.87 % | 29.57 % | 43.33 % |
| 2.5 ATR | 12.588 % | 37.9804 | 0.2 % | 1.51 % | 4.24 % | 9.5 % | 19.31 % | 31.52 % |
| 3.0 ATR | 15.106 % | 36.8864 | 0.2 % | 1.21 % | 2.62 % | 5.46 % | 13.82 % | 23.72 % |
| 4.0 ATR | 20.141 % | 34.6986 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 30.212 % | 30.3229 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.22 ATR | 0.50 ATR | 0.57 ATR | 0.75 ATR | 0.92 ATR | 1.05 ATR | 1.47 ATR | 1.87 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.95 ATR | 1.16 ATR | 1.33 ATR | 1.88 ATR | 2.40 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.24 ATR | 1.53 ATR | 1.79 ATR | 2.46 ATR | 3.16 ATR |
| **10 s.** | 0.54 ATR | 1.18 ATR | 1.35 ATR | 1.85 ATR | 2.22 ATR | 2.47 ATR | 3.60 ATR | 4.90 ATR |
| **20 s.** | 0.76 ATR | 1.70 ATR | 1.93 ATR | 2.44 ATR | 2.92 ATR | 3.39 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.392–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.571–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.777 %, prix 41.8089), p(touche) 33.17 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.716–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.777 %, prix 41.8089), p(touche) 42.89 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.967–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.294 %, prix 40.7153), p(touche) 32.76 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.353–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.553 %, prix 40.1682), p(touche) 41.36 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.925–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (15.106 %, prix 36.8864), p(touche) 23.72 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.161 | EV/share : $0.403 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 16 % | T3 13 %
- Kelly (position) : f* 0.093 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 84.2 | bear 5.4 | side 10.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 620.0 (= 16 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.347% → cible +2.552% / stop −2.0%, p_fill 74%, n_eff≈79.4) : P(cible|rempli) **34%** · **EV/risk -0.035** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −2.974% → cible +11.864% / stop −5.932%, p_fill 58%, n_eff≈67.7) : P(cible|rempli) **25%** · **EV/risk +0.102** (×p_fill ; si rempli +1.04% du capital)
  - **deep** (entrée dip −4.587% → cible +13.764% / stop −7.916%, p_fill 58%, n_eff≈64.9) : P(cible|rempli) **39%** · **EV/risk +0.199** (×p_fill ; si rempli +2.72% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→62% · +3.0%→43% · +5.0%→22% · +8.0%→9%
- Range intraday médian 5.66% (p90 9.37%) · excursion haute méd. +2.56% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.84% vs midi 1.155% vs clôture 1.48% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 69% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.011)_ ; drift intra méd. 0.304% ; recovery-V 40%
- **σ réalisé intraday** 3.371% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 61% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 43.4066 (VA 43.1796–43.8039 ; dernier close 43.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 23% · rebond 78% · **stop −4.35%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 42% (gap-down >1% 31% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −2.5%) · haut méd +1.02% · range méd 2.13%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −3.1%) · haut méd +1.28% · range méd 2.8%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.6%) · haut méd +1.53% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.66% (p90 −4.07%) · haut méd +1.81% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.69 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 71% (116/159) · gap 37% · délai 0.0min · rebond 57% (69/116) (MFE +1.39%)
   - −1.0% : fill 30min 51% · séance 67% (109/159) · gap 31% · délai 0.0min · rebond 58% (64/109) (MFE +1.64%)
   - −1.5% : fill 30min 45% · séance 61% (99/159) · gap 20% · délai 0.2min · rebond 69% (65/99) (MFE +1.56%)
   - −2.0% : fill 30min 39% · séance 53% (86/159) · gap 16% · délai 1.1min · rebond 72% (57/86) (MFE +1.74%)
   - −3.0% : fill 30min 26% · séance 44% (72/159) · gap 8% · délai 12.8min · rebond 64% (44/72) (MFE +1.42%)
   - −4.0% : fill 30min 13% · séance 31% (52/159) · gap 4% · délai 41.3min · rebond 72% (34/52) (MFE +1.7%)
   - −5.0% : fill 30min 10% · séance 23% (41/159) · gap 3% · délai 49.2min · rebond 78% (30/41) (MFE +2.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.8%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −2.62%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.32%) → stop au-delà de −1.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=870 jambes) : jambe baissière méd −1.18% (p90 −2.77%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 98% (69/71) · rebond 48% (36/69)
      · −2.0% : fill 94% (65/71) · rebond 74% (41/65)
      · −3.0% : fill 85% (58/71) · rebond 65% (35/58)
      · −4.0% : fill 62% (43/71) · rebond 71% (28/43)
      · −5.0% : fill 46% (34/71) · rebond 76% (24/34)
   - **flat** (13 séances) :
      · −1.0% : fill 85% (12/13) · rebond 75% (9/12)
      · −2.0% : fill 36% (5/13) · rebond 50% (3/5)
      · −3.0% : fill 29% (3/13) · rebond 43% (2/3)
      · −4.0% : fill 10% (1/13) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 38% (28/75) · rebond 74% (19/28)
      · −2.0% : fill 21% (16/75) · rebond 70% (13/16)
      · −3.0% : fill 11% (11/75) · rebond 70% (7/11)
      · −4.0% : fill 8% (8/75) · rebond 72% (5/8)
      · −5.0% : fill 8% (7/75) · rebond 86% (6/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 68% si les 15 1res min sont vertes (80 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 48% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **78%** · continue >prix actuel 54% ; creux résiduel méd -1.96% (q20 -3.57%) → **SL/trailing à −3.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +4.23% → **scale +1.91% / runner +4.23%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **18%** (continue à baisser 53%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.85%** (au-delà de la MAE q10 -4.85%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.7% .. +4.13%] · haut q95 +5.15% · bas q05 -4.15%
   - 60min (n=160) : retour [-4.08% .. +5.23%] · haut q95 +6.49% · bas q05 -5.23%
   - 2h (n=160) : retour [-4.2% .. +6.08%] · haut q95 +7.25% · bas q05 -5.52%
   - 4h (n=160) : retour [-4.43% .. +6.66%] · haut q95 +7.77% · bas q05 -5.98%
   - 6h (n=160) : retour [-4.87% .. +6.53%] · haut q95 +8.68% · bas q05 -6.54%
   - session (n=160) : retour [-4.8% .. +6.89%] · haut q95 +8.93% · bas q05 -6.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 72.3  _(surachat)_
- **ADX** : 28.1  _(tendance etablie)_
- **MACD** : hist 0.089  _(pas de croisement recent)_
- **BB** : %B 0.81 · largeur 23.4%
- **ATR** : 2.19 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.017  _(neutre)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 56.4  _(transition)_
- **MA** : MA20 40.51 · MA50 37.05 · MA200 32.13  _(prix > MA20)_
- **Dist MA** : MA20 +7.3% · MA50 +17.3% · MA200 +35.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (526919 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
