# SRT3

**Generated** : 2026-10-01T00:05:31.212696+00:00  
**Santé technique** : 10/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · €257.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €257.00 (+6.1% vs entrée) · entrée €242.17 · stop €233.84 · T1 €251.49 · R/R 1.12  
> ↳ ¼-Kelly 0.018 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 70.0 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €240.83–€243.52 (mid €242.17)
- Spot actuel : €257.00 (+6.1% au-dessus de la zone — repli à attendre)
- Stop : €233.84 (plancher anti-bruit (R/R<2) ; -3.44 % depuis l'entree)
- Targets : T1 €251.49 · R/R 1.12 | T2 €260.81 · R/R 2.24 | T3 €270.13 · R/R 3.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €233.84


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.01 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **0.962 pt plus bas** dans le cas TYPIQUE (médiane), 4.349 au p90, **5.195 au pire**
   - perte réelle **11.278 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 9.01 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0053 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4018** [0.3309 ; 0.476] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.4487** [0.3969 ; 0.5014] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4102** [0.3593 ; 0.4626] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (39.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.09 %** | CVaR **-6.57 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.98 % vs -9.16 % si l'on extrapolait par √5 _(rapport 1.089 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0809** (β de hausse 1.1689, asymétrie 0.9247) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.308× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 252.8321 sur atr_grid (0.5 ATR, 1.622 %) — p(stop avant cible) 0.7757 [0.73 ; 0.82], R/R 3.105, perte reelle 1.646 % (gap inclus), CVaR 1.991 %, EV -0.1403 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.486 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.776, borne haute 0.817 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.865 %) — p(stop avant cible) 0.4563 [0.40 ; 0.51], R/R 1.031, perte reelle 4.956 % (gap inclus), EV 0.0739 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 3.33 ATR (stop 12.866 %) — p(stop avant cible) 0.0803 [0.06 ; 0.11], R/R 0.395, perte reelle 12.948 % (gap inclus), EV 0.4489 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.00 % > budget 12.00 %
   - ⚪ swing_based a 3.89 ATR (stop 14.686 %) — p(stop avant cible) 0.0443 [0.03 ; 0.07], R/R 0.342, perte reelle 14.948 % (gap inclus), EV 0.4798 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.72 % > budget 12.00 %
   - 🟢 support a 7.1 ATR (stop 25.081 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.193, perte reelle 26.442 % (gap inclus), EV 0.6395 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.00 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.811 %) — p(stop avant cible) 0.8447 [0.80 ; 0.88], R/R 6.14, perte reelle 0.832 % (gap inclus), EV 0.0906 % — **REFUSE**
      - refuse : p_stop_first 0.845, borne haute 0.880 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.622 %) — p(stop avant cible) 0.7757 [0.73 ; 0.82], R/R 3.105, perte reelle 1.646 % (gap inclus), EV -0.1403 % — **REFUSE**
      - refuse : p_stop_first 0.776, borne haute 0.817 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 22.2 % x 5.11 % + P(rien) 0.2 % x 0.40 % ne couvrent pas P(stop) 77.6 % x 1.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.433 %) — p(stop avant cible) 0.6824 [0.63 ; 0.73], R/R 2.055, perte reelle 2.486 % (gap inclus), EV -0.1015 % — **REFUSE**
      - refuse : p_stop_first 0.682, borne haute 0.730 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 31.0 % x 5.11 % + P(rien) 0.8 % x 1.49 % ne couvrent pas P(stop) 68.2 % x 2.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.243 %) — p(stop avant cible) 0.6011 [0.55 ; 0.65], R/R 1.538, perte reelle 3.322 % (gap inclus), EV -0.08 % — **REFUSE**
      - refuse : p_stop_first 0.601, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 37.0 % x 5.11 % + P(rien) 2.9 % x 0.95 % ne couvrent pas P(stop) 60.1 % x 3.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 4.054 %) — p(stop avant cible) 0.5197 [0.47 ; 0.57], R/R 1.227, perte reelle 4.164 % (gap inclus), EV -0.0365 % — **REFUSE**
      - refuse : p_stop_first 0.520, borne haute 0.572 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 41.7 % x 5.11 % + P(rien) 6.3 % x -0.07 % ne couvrent pas P(stop) 52.0 % x 4.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 5.676 %) — p(stop avant cible) 0.3776 [0.33 ; 0.43], R/R 0.884, perte reelle 5.782 % (gap inclus), EV 0.2897 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 6.487 %) — p(stop avant cible) 0.3278 [0.28 ; 0.38], R/R 0.773, perte reelle 6.606 % (gap inclus), EV 0.3349 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 7.298 %) — p(stop avant cible) 0.2889 [0.24 ; 0.34], R/R 0.692, perte reelle 7.383 % (gap inclus), EV 0.3749 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 8.109 %) — p(stop avant cible) 0.2434 [0.20 ; 0.29], R/R 0.619, perte reelle 8.257 % (gap inclus), EV 0.3442 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 8.92 %) — p(stop avant cible) 0.2029 [0.16 ; 0.25], R/R 0.564, perte reelle 9.061 % (gap inclus), EV 0.3185 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.73 %) — p(stop avant cible) 0.1717 [0.13 ; 0.21], R/R 0.519, perte reelle 9.841 % (gap inclus), EV 0.4144 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.33 ATR (stop 11.786 %) — p(stop avant cible) 0.1124 [0.08 ; 0.15], R/R 0.432, perte reelle 11.822 % (gap inclus), EV 0.3897 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.89 ATR (stop 13.606 %) — p(stop avant cible) 0.0635 [0.04 ; 0.09], R/R 0.371, perte reelle 13.757 % (gap inclus), EV 0.4876 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.80 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.217 %) — p(stop avant cible) 0.0199 [0.01 ; 0.04], R/R 0.3, perte reelle 17.052 % (gap inclus), EV 0.5609 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.12 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.839 %) — p(stop avant cible) 0.0123 [0.00 ; 0.03], R/R 0.273, perte reelle 18.741 % (gap inclus), EV 0.5999 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.60 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 19.461 %) — p(stop avant cible) 0.0107 [0.00 ; 0.03], R/R 0.256, perte reelle 19.986 % (gap inclus), EV 0.5953 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.69 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 21.083 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 0.23, perte reelle 22.264 % (gap inclus), EV 0.5907 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.75 % > budget 12.00 %
   - 🟢 grid_snapped a 7.1 ATR (stop 24.001 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.2, perte reelle 25.571 % (gap inclus), EV 0.6359 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.06 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 25.948 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.191, perte reelle 26.768 % (gap inclus), EV 0.6412 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.98 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 257.0, ATR14 8.3357 (3.243 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 1.239 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.162 % | 256.5832 | 89.05 % | 92.79 % | 94.27 % | 96.14 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.324 % | 256.1664 | 82.54 % | 88.45 % | 90.81 % | 93.56 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.487 % | 255.7496 | 74.85 % | 83.61 % | 86.76 % | 90.4 % | 93.43 % | 94.97 % |
| 0.2 ATR | 0.649 % | 255.3329 | 68.34 % | 78.78 % | 82.91 % | 87.33 % | 92.14 % | 94.37 % |
| 0.25 ATR | 0.811 % | 254.9161 | 63.02 % | 75.42 % | 79.64 % | 84.95 % | 90.35 % | 93.07 % |
| 0.35 ATR | 1.135 % | 254.0825 | 53.16 % | 69.1 % | 73.91 % | 80.59 % | 87.06 % | 90.95 % |
| 0.5 ATR | 1.622 % | 252.8321 | 38.26 % | 56.56 % | 64.33 % | 73.86 % | 82.59 % | 88.24 % |
| 0.75 ATR | 2.433 % | 250.7482 | 19.23 % | 36.72 % | 47.73 % | 59.11 % | 72.44 % | 81.71 % |
| 1.0 ATR | 3.243 % | 248.6643 | 9.86 % | 24.48 % | 34.68 % | 47.72 % | 63.18 % | 74.67 % |
| 1.25 ATR | 4.054 % | 246.5804 | 4.73 % | 14.91 % | 24.6 % | 38.42 % | 53.53 % | 67.54 % |
| 1.5 ATR | 4.865 % | 244.4964 | 2.27 % | 9.87 % | 17.69 % | 30.89 % | 46.17 % | 61.71 % |
| 2.0 ATR | 6.487 % | 240.3286 | 0.69 % | 4.54 % | 8.2 % | 17.23 % | 34.83 % | 51.86 % |
| 2.5 ATR | 8.109 % | 236.1607 | 0.3 % | 1.97 % | 4.74 % | 10.69 % | 24.48 % | 41.91 % |
| 3.0 ATR | 9.73 % | 231.9929 | 0.2 % | 1.48 % | 2.96 % | 6.34 % | 17.51 % | 34.37 % |
| 4.0 ATR | 12.974 % | 223.6571 | 0.0 % | 0.69 % | 1.78 % | 3.56 % | 8.96 % | 20.2 % |
| 6.0 ATR | 19.461 % | 206.9857 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.49 ATR | 1.96 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.80 ATR | 1.04 ATR | 1.24 ATR | 1.42 ATR | 1.91 ATR | 2.46 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.72 ATR | 1.90 ATR | 2.58 ATR | 3.48 ATR |
| **10 s.** | 0.69 ATR | 1.37 ATR | 1.55 ATR | 2.09 ATR | 2.48 ATR | 2.82 ATR | 3.88 ATR | 5.15 ATR |
| **20 s.** | 0.99 ATR | 2.09 ATR | 2.35 ATR | 3.10 ATR | 3.66 ATR | 4.03 ATR | 5.55 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.622 %, prix 252.8315), p(touche) 38.26 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.433 %, prix 250.7472), p(touche) 36.72 % (en stress 89.22 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.802–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.243 %, prix 248.6655), p(touche) 34.68 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.073–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.054 %, prix 246.5812), p(touche) 38.42 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.552–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.487 %, prix 240.3284), p(touche) 34.83 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.345–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.109 %, prix 236.1599), p(touche) 41.91 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.081 | EV/share : €0.674 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 16 % | T3 4 %
- Kelly (position) : f* 0.073 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 49.5 | bear 11.3 | side 39.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 514.0 (= 2 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.619% → cible +1.665% / stop −1.5%, p_fill 16%, n_eff≈22.4) : P(cible|rempli) **35%** · **EV/risk +0.014** (×p_fill ; si rempli +0.13% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=12))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→74% · +2.0%→45% · +3.0%→24% · +5.0%→7% · +8.0%→0%
- Range intraday médian 3.34% (p90 6.12%) · excursion haute méd. +1.81% / basse méd. −1.46%
- Profil de vol intra : ouverture 1.956% vs midi 0.823% vs clôture 0.965% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 46% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. 0.561% ; recovery-V 24%
- **σ réalisé intraday** 2.248% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 60% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 266.745 (VA 263.295–267.205 ; dernier close 260.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 45% · rebond 55% · **stop −1.51%** sous le fill (sous le bruit) · cible +1.14% · R/R 0.75 (high win-rate)
- Gaps overnight (n=159) : méd. -0.14% · baisse 59% (gap-down >1% 6% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.22% (p90 −1.53%) · haut méd +0.61% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.29% (p90 −1.75%) · haut méd +0.82% · range méd 1.36%
- Excursion ouverture 30min (n=160) : bas méd −0.41% (p90 −1.78%) · haut méd +0.91% · range méd 1.54%
- Excursion ouverture 60min (n=160) : bas méd −0.49% (p90 −1.91%) · haut méd +0.96% · range méd 1.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 260.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 79% (121/159) · gap 24% · délai 0.6min · rebond 52% (66/121) (MFE +1.07%)
   - −1.0% : fill 30min 37% · séance 65% (101/159) · gap 6% · délai 10.5min · rebond 57% (58/101) (MFE +1.23%)
   - −1.5% : fill 30min 22% · séance 45% (77/159) · gap 2% · délai 46.5min · rebond 55% (43/77) (MFE +1.14%)
   - −2.0% : fill 30min 7% · séance 32% (57/159) · gap 0% · délai 220.2min · rebond 53% (29/57) (MFE +1.19%)
   - −3.0% : fill 30min 3% · séance 9% (26/159) · gap 0% · délai 97.9min · rebond 62% (13/26) (MFE +1.26%)
   - −4.0% : fill 30min 1% · séance 5% (13/159) · gap 0% · délai 55.4min · rebond 62% (8/13) (MFE +1.73%)
   - −5.0% : fill 30min 0% · séance 3% (7/159) · gap 0% · délai 141.9min · rebond 84% (6/7) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −1.59%) → stop au-delà de −1.0% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.06% (p90 −1.59%) → stop au-delà de −1.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.15% (p90 −1.98%) → stop au-delà de −1.15% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=436 jambes) : jambe baissière méd −1.01% (p90 −2.28%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 77% (48/60) · rebond 59% (29/48)
      · −2.0% : fill 34% (26/60) · rebond 54% (14/26)
      · −3.0% : fill 9% (14/60) · rebond 52% (7/14)
      · −4.0% : fill 6% (8/60) · rebond 60% (6/8)
      · −5.0% : fill 3% (4/60) · rebond 100% (4/4)
   - **flat** (41 séances) :
      · −1.0% : fill 61% (25/41) · rebond 53% (12/25)
      · −2.0% : fill 34% (16/41) · rebond 49% (7/16)
      · −3.0% : fill 6% (5/41) · rebond 34% (1/5)
      · −4.0% : fill 2% (2/41) · rebond 0% (0/2)
      · −5.0% : fill 2% (1/41) · rebond 0% (0/1)
   - **gap-up** (58 séances) :
      · −1.0% : fill 50% (28/58) · rebond 58% (17/28)
      · −2.0% : fill 26% (15/58) · rebond 58% (8/15)
      · −3.0% : fill 11% (7/58) · rebond 89% (5/7)
      · −4.0% : fill 6% (3/58) · rebond 89% (2/3)
      · −5.0% : fill 6% (2/58) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 58% si les 15 1res min sont vertes (89 cas) · 41% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 64% si début vert vs 32% si rouge (base 51% · écart 32 pts) ; prédictivité sature ensuite (plafond brut 265min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **64%** · continue >prix actuel 46% ; creux résiduel méd -1.37% (q20 -2.3%) → **SL/trailing à −2.3%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.99% / q75 +2.08% → **scale +0.99% / runner +2.08%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **32%** (continue à baisser 40%) → **RÉDUIRE ~68%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.6%** (au-delà de la MAE q10 -2.6%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.08%] · haut q95 +2.54% · bas q05 -2.82%
   - 60min (n=160) : retour [-2.29% .. +2.34%] · haut q95 +2.82% · bas q05 -2.95%
   - 2h (n=160) : retour [-2.18% .. +2.3%] · haut q95 +2.94% · bas q05 -3.04%
   - 4h (n=160) : retour [-2.25% .. +2.51%] · haut q95 +3.2% · bas q05 -3.15%
   - 6h (n=160) : retour [-2.48% .. +2.9%] · haut q95 +3.61% · bas q05 -3.19%
   - session (n=160) : retour [-3.04% .. +4.5%] · haut q95 +5.23% · bas q05 -3.83%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.08 · part idiosyncratique 0.92
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 70.0  _(surachat)_
- **ADX** : 25.7  _(tendance etablie)_
- **MACD** : hist 1.525  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 18.4%
- **ATR** : 8.34 (42.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.01  _(neutre)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 37.1  _(marche directionnel)_
- **MA** : MA20 245.88 · MA50 239.31 · MA200 233.21  _(prix > MA20)_
- **Dist MA** : MA20 +4.5% · MA50 +7.4% · MA200 +10.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (847363 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
