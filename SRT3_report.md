# SRT3

**Generated** : 2026-11-19T21:41:48.564029+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €299.00  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 5/125 fenêtres (p_fill pondéré 4 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €299.00 (+5.5% vs entrée) · entrée €283.33 · stop €279.08 · T1 €287.26 · R/R 0.92  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 0.96 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-19 : 299.0 · ATR Wilder 8.26 (2.76 %)_
- **Swing** : plage **287.76 → 281.27** (-3.76 % a -5.93 % sous la cloture, 0.79 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 265.87 (-5.48 % sous le bas ; sous le support 270.0-272.35 (- 0,5 ATR)).
- **Deep** : plage **281.27 → 264.26** (-5.93 % a -11.62 % sous la cloture, 2.06 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 270.0-272.35 (B) ; 264.1-266.78 (C). stop INDICATIF 255.77 (-3.21 % sous le bas ; sous le support 259.9-263.11 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.77 ATR sous le plus haut 20 s., RSI(2) 96.0 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 288.55-290.03 (B, -3.0 %) ; 270.0-272.35 (B, -8.91 %) ; 264.1-266.78 (C, -10.78 %) ; 259.9-263.11 (B, -12.0 %) ; 255.36-258.01 (A, -13.71 %) ; 250.3-254.32 (B, -14.94 %)
- Resistances reelles au-dessus : 314.42-318.19 (B, 5.16 %) ; 343.17-346.24 (B, 14.77 %) ; 347.33-349.91 (A, 16.16 %) ; 352.2-354.07 (B, 17.79 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (14.16 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **0.045 pt plus bas** dans le cas TYPIQUE (médiane), 0.045 au p90, **0.045 au pire**
   - perte réelle **14.205 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 14.16 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.607 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3417** [0.2741 ; 0.4145] _(largeur 14.0 pt, n_eff 173.1)_
   - swing : **0.4671** [0.415 ; 0.5198] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4126** [0.3616 ; 0.465] _(largeur 10.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-3.72 %** | CVaR **-6.15 %** | vol 2.75 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 3.98 % contre 2.34 % aujourd'hui, rapport 1.70)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.98 % vs -9.13 % si l'on extrapolait par √5 _(rapport 1.092 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0415** (β de hausse 1.1477, asymétrie 0.9074) vs GDAXI — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.275× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 295.0714 sur atr_grid (0.5 ATR, 1.314 %) — p(stop avant cible) 0.7252 [0.68 ; 0.77], R/R 2.958, perte reelle 1.352 % (gap inclus), CVaR 1.867 %, EV 0.1186 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4143 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.725, borne haute 0.770 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.942 %) — p(stop avant cible) 0.4583 [0.41 ; 0.51], R/R 0.987, perte reelle 4.051 % (gap inclus), EV 0.1509 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 2.08 ATR (stop 6.999 %) — p(stop avant cible) 0.2468 [0.20 ; 0.29], R/R 0.565, perte reelle 7.075 % (gap inclus), EV 0.5911 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 8.08 ATR (stop 22.752 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.166, perte reelle 24.12 % (gap inclus), EV 0.8238 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.58 % > budget 12.00 %
   - 🟢 support a 12.88 ATR (stop 35.364 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.113, perte reelle 35.364 % (gap inclus), EV 0.8408 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.23 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.657 %) — p(stop avant cible) 0.811 [0.77 ; 0.85], R/R 5.881, perte reelle 0.68 % (gap inclus), EV 0.2043 % — **REFUSE**
      - refuse : p_stop_first 0.811, borne haute 0.850 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.314 %) — p(stop avant cible) 0.7252 [0.68 ; 0.77], R/R 2.958, perte reelle 1.352 % (gap inclus), EV 0.1186 % — **REFUSE**
      - refuse : p_stop_first 0.725, borne haute 0.770 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.75 ATR (stop 1.971 %) — p(stop avant cible) 0.6288 [0.58 ; 0.68], R/R 1.973, perte reelle 2.027 % (gap inclus), EV 0.21 % — **REFUSE**
      - refuse : p_stop_first 0.629, borne haute 0.678 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.0 ATR (stop 2.628 %) — p(stop avant cible) 0.5687 [0.52 ; 0.62], R/R 1.474, perte reelle 2.714 % (gap inclus), EV 0.1749 % — **REFUSE**
      - refuse : p_stop_first 0.569, borne haute 0.620 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 3.285 %) — p(stop avant cible) 0.5032 [0.45 ; 0.56], R/R 1.18, perte reelle 3.389 % (gap inclus), EV 0.2436 % — **REFUSE**
      - refuse : p_stop_first 0.503, borne haute 0.556 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 4.599 %) — p(stop avant cible) 0.404 [0.35 ; 0.46], R/R 0.852, perte reelle 4.695 % (gap inclus), EV 0.2379 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.08 ATR (stop 6.264 %) — p(stop avant cible) 0.2737 [0.23 ; 0.32], R/R 0.63, perte reelle 6.345 % (gap inclus), EV 0.6198 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 7.883 %) — p(stop avant cible) 0.1947 [0.16 ; 0.24], R/R 0.498, perte reelle 8.024 % (gap inclus), EV 0.6435 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 9.197 %) — p(stop avant cible) 0.1494 [0.11 ; 0.19], R/R 0.429, perte reelle 9.33 % (gap inclus), EV 0.611 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 10.511 %) — p(stop avant cible) 0.1185 [0.09 ; 0.16], R/R 0.377, perte reelle 10.601 % (gap inclus), EV 0.6084 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 11.825 %) — p(stop avant cible) 0.0866 [0.06 ; 0.12], R/R 0.337, perte reelle 11.862 % (gap inclus), EV 0.643 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 13.139 %) — p(stop avant cible) 0.0597 [0.04 ; 0.09], R/R 0.301, perte reelle 13.285 % (gap inclus), EV 0.681 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.31 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 14.453 %) — p(stop avant cible) 0.0387 [0.02 ; 0.06], R/R 0.272, perte reelle 14.711 % (gap inclus), EV 0.708 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.09 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 15.767 %) — p(stop avant cible) 0.023 [0.01 ; 0.04], R/R 0.246, perte reelle 16.242 % (gap inclus), EV 0.7526 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.62 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 17.081 %) — p(stop avant cible) 0.0095 [0.00 ; 0.02], R/R 0.219, perte reelle 18.251 % (gap inclus), EV 0.8068 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.78 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 18.395 %) — p(stop avant cible) 0.0092 [0.00 ; 0.02], R/R 0.208, perte reelle 19.215 % (gap inclus), EV 0.7978 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.93 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 19.709 %) — p(stop avant cible) 0.0081 [0.00 ; 0.02], R/R 0.198, perte reelle 20.194 % (gap inclus), EV 0.7985 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.95 % > budget 12.00 %
   - ⚪ grid_snapped a 8.08 ATR (stop 22.016 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.169, perte reelle 23.738 % (gap inclus), EV 0.8252 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.56 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 299.0, ATR14 7.8571 (2.628 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.379 ATR = 0.996 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.131 % | 298.6071 | 88.76 % | 92.6 % | 94.27 % | 96.04 % | 97.71 % | 98.39 % |
| 0.1 ATR | 0.263 % | 298.2143 | 82.15 % | 88.25 % | 90.71 % | 93.56 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.394 % | 297.8214 | 74.46 % | 83.42 % | 86.86 % | 90.69 % | 93.73 % | 95.08 % |
| 0.2 ATR | 0.526 % | 297.4286 | 67.95 % | 78.68 % | 82.81 % | 87.43 % | 92.14 % | 94.27 % |
| 0.25 ATR | 0.657 % | 297.0357 | 62.62 % | 74.93 % | 79.25 % | 84.95 % | 90.35 % | 92.96 % |
| 0.35 ATR | 0.92 % | 296.25 | 52.86 % | 68.41 % | 73.32 % | 80.5 % | 86.97 % | 90.85 % |
| 0.5 ATR | 1.314 % | 295.0714 | 38.17 % | 55.87 % | 63.54 % | 73.17 % | 82.09 % | 87.84 % |
| 0.75 ATR | 1.971 % | 293.1071 | 19.13 % | 36.53 % | 47.33 % | 58.71 % | 71.84 % | 80.9 % |
| 1.0 ATR | 2.628 % | 291.1429 | 9.66 % | 24.28 % | 34.49 % | 47.33 % | 62.19 % | 73.47 % |
| 1.25 ATR | 3.285 % | 289.1786 | 4.73 % | 14.81 % | 24.21 % | 37.72 % | 52.54 % | 66.33 % |
| 1.5 ATR | 3.942 % | 287.2143 | 2.17 % | 9.67 % | 17.29 % | 30.0 % | 45.17 % | 60.3 % |
| 2.0 ATR | 5.256 % | 283.2857 | 0.59 % | 4.24 % | 7.71 % | 16.34 % | 33.63 % | 50.85 % |
| 2.5 ATR | 6.57 % | 279.3572 | 0.3 % | 1.88 % | 4.45 % | 10.2 % | 23.38 % | 40.6 % |
| 3.0 ATR | 7.883 % | 275.4286 | 0.2 % | 1.38 % | 2.77 % | 6.04 % | 16.72 % | 33.27 % |
| 4.0 ATR | 10.511 % | 267.5714 | 0.0 % | 0.59 % | 1.68 % | 3.47 % | 8.66 % | 19.7 % |
| 6.0 ATR | 15.767 % | 251.8572 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 0.99 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.58 ATR | 0.64 ATR | 0.82 ATR | 0.98 ATR | 1.11 ATR | 1.48 ATR | 1.93 ATR |
| **3 s.** | 0.32 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.23 ATR | 1.40 ATR | 1.88 ATR | 2.42 ATR |
| **5 s.** | 0.46 ATR | 0.94 ATR | 1.06 ATR | 1.40 ATR | 1.68 ATR | 1.87 ATR | 2.52 ATR | 3.40 ATR |
| **10 s.** | 0.67 ATR | 1.34 ATR | 1.51 ATR | 2.03 ATR | 2.42 ATR | 2.75 ATR | 3.83 ATR | 5.11 ATR |
| **20 s.** | 0.95 ATR | 2.04 ATR | 2.29 ATR | 3.02 ATR | 3.61 ATR | 3.98 ATR | 5.53 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.43–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.314 %, prix 295.0711), p(touche) 38.17 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.641–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.971 %, prix 293.1067), p(touche) 36.53 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.795–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.628 %, prix 291.1423), p(touche) 34.49 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.061–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.285 %, prix 289.1778), p(touche) 37.72 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.507–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.256 %, prix 283.2846), p(touche) 33.63 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.285–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (6.57 %, prix 279.3557), p(touche) 40.6 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 37.6 | bear 57.4 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 598.0 (= 2 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→72% · +2.0%→45% · +3.0%→22% · +5.0%→6% · +8.0%→0%
- Range intraday médian 3.22% (p90 5.92%) · excursion haute méd. +1.84% / basse méd. −1.3%
- Profil de vol intra : ouverture 1.898% vs midi 0.79% vs clôture 0.947% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓0% ; spike-down 46% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.101 ; mean-reverting — autocorr -0.059)_ ; drift intra méd. 0.362% ; recovery-V 23%
- **σ réalisé intraday** 2.449% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 60% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 277.3675 (VA 275.7775–278.9575 ; dernier close 282.65)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 29% · rebond 55% · **stop −2.08%** sous le fill (sous le bruit) · cible +1.25% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 54% (gap-down >1% 4% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.44% (p90 −1.44%) · haut méd +0.53% · range méd 1.12%
- Excursion ouverture 15min (n=160) : bas méd −0.49% (p90 −1.58%) · haut méd +0.66% · range méd 1.32%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −1.8%) · haut méd +0.82% · range méd 1.51%
- Excursion ouverture 60min (n=160) : bas méd −0.59% (p90 −1.91%) · haut méd +0.88% · range méd 1.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 281.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 75% (121/159) · gap 23% · délai 0.4min · rebond 58% (69/121) (MFE +1.25%)
   - −1.0% : fill 30min 34% · séance 58% (98/159) · gap 4% · délai 7.2min · rebond 56% (58/98) (MFE +1.13%)
   - −1.5% : fill 30min 18% · séance 42% (74/159) · gap 1% · délai 48.7min · rebond 59% (44/74) (MFE +1.17%)
   - −2.0% : fill 30min 6% · séance 29% (54/159) · gap 0% · délai 252.9min · rebond 55% (31/54) (MFE +1.25%)
   - −3.0% : fill 30min 2% · séance 12% (24/159) · gap 0% · délai 293.1min · rebond 58% (12/24) (MFE +1.54%)
   - −4.0% : fill 30min 1% · séance 6% (12/159) · gap 0% · délai 399.3min · rebond 57% (7/12) (MFE +1.86%)
   - −5.0% : fill 30min 0% · séance 4% (8/159) · gap 0% · délai 318.6min · rebond 52% (6/8) (MFE +0.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.23% (p90 −1.59%) → stop au-delà de −0.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.17% (p90 −1.59%) → stop au-delà de −0.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.2% (p90 −1.46%) → stop au-delà de −0.98% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=438 jambes) : jambe baissière méd −1.02% (p90 −2.24%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (59 séances) :
      · −1.0% : fill 69% (45/59) · rebond 60% (29/45)
      · −2.0% : fill 33% (24/59) · rebond 43% (14/24)
      · −3.0% : fill 13% (13/59) · rebond 23% (5/13)
      · −4.0% : fill 8% (7/59) · rebond 28% (4/7)
      · −5.0% : fill 6% (5/59) · rebond 37% (4/5)
   - **flat** (40 séances) :
      · −1.0% : fill 67% (26/40) · rebond 52% (13/26)
      · −2.0% : fill 37% (16/40) · rebond 60% (8/16)
      · −3.0% : fill 12% (5/40) · rebond 75% (2/5)
      · −4.0% : fill 2% (1/40) · rebond 0% (0/1)
      · −5.0% : fill 2% (1/40) · rebond 0% (0/1)
   - **gap-up** (60 séances) :
      · −1.0% : fill 40% (27/60) · rebond 50% (16/27)
      · −2.0% : fill 19% (14/60) · rebond 70% (9/14)
      · −3.0% : fill 10% (6/60) · rebond 96% (5/6)
      · −4.0% : fill 8% (4/60) · rebond 95% (3/4)
      · −5.0% : fill 3% (2/60) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 65% si les 15 1res min sont vertes (86 cas) · 37% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 74% si début vert vs 24% si rouge (base 52% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 235min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **74%** · continue >prix actuel 56% ; creux résiduel méd -1.24% (q20 -2.3%) → **SL/trailing à −2.3%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +2.02% → **scale +1.07% / runner +2.02%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **24%** (continue à baisser 52%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.65%** (au-delà de la MAE q10 -3.65%), cible rebond +1.23% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.97% .. +2.19%] · haut q95 +2.65% · bas q05 -2.42%
   - 60min (n=160) : retour [-1.9% .. +2.34%] · haut q95 +3.27% · bas q05 -2.54%
   - 2h (n=160) : retour [-1.91% .. +2.27%] · haut q95 +3.51% · bas q05 -2.72%
   - 4h (n=160) : retour [-2.25% .. +2.8%] · haut q95 +3.79% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.48% .. +3.45%] · haut q95 +4.3% · bas q05 -3.27%
   - session (n=160) : retour [-3.0% .. +3.66%] · haut q95 +5.74% · bas q05 -4.2%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.3%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.06 · part idiosyncratique 0.94
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 57.8  _(momentum haussier)_
- **ADX** : 34.0  _(tendance etablie)_
- **MACD** : hist -0.802  _(pas de croisement recent)_
- **BB** : %B 0.96 · largeur 5.5%
- **ATR** : 7.86 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.183  _(accumulation)_
- **Vol ratio** : 0.99  _(volume normal)_
- **Choppiness** : 55.5  _(transition)_
- **MA** : MA20 291.66 · MA50 269.0 · MA200 238.16  _(prix > MA20)_
- **Dist MA** : MA20 +2.5% · MA50 +11.2% · MA200 +25.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (692507 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
