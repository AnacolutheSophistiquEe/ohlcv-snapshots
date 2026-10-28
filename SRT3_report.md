# SRT3

**Generated** : 2026-10-28T21:41:28.318454+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 10/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · €292.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €292.50 (+12.5% vs entrée) · entrée €260.11 · stop €250.74 · T1 €270.58 · R/R 1.12  
> ↳ ¼-Kelly 0.032 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 153 % hors [0,100] (R² max 0.83). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 88.6 > 70 (surachat) ; %B 1.01 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-28 : 292.5 · ATR Wilder 9.6 (3.28 %)_
- **Swing** : plage **279.44 → 271.91** (-4.46 % a -7.04 % sous la cloture, 0.79 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 271.9-275.96 (B). stop INDICATIF 261.98 (-3.65 % sous le bas ; sous le support 266.78-270.86 (- 0,5 ATR)).
- **Deep** : plage **271.91 → 252.15** (-7.04 % a -13.79 % sous la cloture, 2.06 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 271.9-275.96 (B) ; 266.78-270.86 (B) ; 259.9-264.1 (B) ; 254.32-258.01 (A) ; 249.2-252.98 (B). stop INDICATIF 238.76 (-5.31 % sous le bas ; sous le support 243.56-247.91 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.52 ATR sous le plus haut 20 s., RSI(2) 98.1 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 271.9-275.96 (B, -5.65 %) ; 266.78-270.86 (B, -7.4 %) ; 259.9-264.1 (B, -9.71 %) ; 254.32-258.01 (A, -11.79 %) ; 249.2-252.98 (B, -13.51 %) ; 243.56-247.91 (A, -15.24 %)
- Resistances reelles au-dessus : 314.42-318.19 (B, 7.5 %) ; 343.17-347.33 (A, 17.32 %) ; 349.71-354.07 (A, 19.56 %) ; 359.03-359.03 (C, 22.75 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (14.28 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1274).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 14.28 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.602 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3739** [0.3044 ; 0.4476] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.4212** [0.37 ; 0.4737] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.352** [0.3031 ; 0.4034] _(largeur 10.0 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.09 %** | CVaR **-6.53 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.98 % vs -9.16 % si l'on extrapolait par √5 _(rapport 1.089 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0744** (β de hausse 1.1717, asymétrie 0.9169) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.354× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 287.8179 sur atr_grid (0.5 ATR, 1.601 %) — p(stop avant cible) 0.6758 [0.63 ; 0.72], R/R 2.466, perte reelle 1.622 % (gap inclus), CVaR 1.887 %, EV 0.2006 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4935 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.676, borne haute 0.724 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.802 %) — p(stop avant cible) 0.4157 [0.36 ; 0.47], R/R 0.819, perte reelle 4.882 % (gap inclus), EV 0.1069 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 4.14 ATR (stop 15.295 %) — p(stop avant cible) 0.0343 [0.02 ; 0.06], R/R 0.255, perte reelle 15.678 % (gap inclus), EV 0.5739 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.55 % > budget 12.00 %
   - ⚪ sr_based a 6.39 ATR (stop 22.494 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.167, perte reelle 23.984 % (gap inclus), EV 0.7014 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.83 % > budget 12.00 %
   - 🟢 support a 10.11 ATR (stop 34.409 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.116, perte reelle 34.409 % (gap inclus), EV 0.721 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.45 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.8 %) — p(stop avant cible) 0.7905 [0.75 ; 0.83], R/R 4.922, perte reelle 0.813 % (gap inclus), EV 0.1956 % — **REFUSE**
      - refuse : p_stop_first 0.790, borne haute 0.831 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.601 %) — p(stop avant cible) 0.6758 [0.63 ; 0.72], R/R 2.466, perte reelle 1.622 % (gap inclus), EV 0.2006 % — **REFUSE**
      - refuse : p_stop_first 0.676, borne haute 0.724 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.75 ATR (stop 2.401 %) — p(stop avant cible) 0.5874 [0.54 ; 0.64], R/R 1.636, perte reelle 2.445 % (gap inclus), EV 0.2124 % — **REFUSE**
      - refuse : p_stop_first 0.587, borne haute 0.638 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.0 ATR (stop 3.201 %) — p(stop avant cible) 0.5292 [0.48 ; 0.58], R/R 1.221, perte reelle 3.277 % (gap inclus), EV 0.128 % — **REFUSE**
      - refuse : p_stop_first 0.529, borne haute 0.581 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 4.002 %) — p(stop avant cible) 0.4612 [0.41 ; 0.51], R/R 0.976, perte reelle 4.1 % (gap inclus), EV 0.121 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 5.603 %) — p(stop avant cible) 0.3343 [0.29 ; 0.39], R/R 0.701, perte reelle 5.702 % (gap inclus), EV 0.4477 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 6.403 %) — p(stop avant cible) 0.2919 [0.25 ; 0.34], R/R 0.616, perte reelle 6.493 % (gap inclus), EV 0.4853 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 7.203 %) — p(stop avant cible) 0.2597 [0.22 ; 0.31], R/R 0.549, perte reelle 7.286 % (gap inclus), EV 0.4626 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 8.004 %) — p(stop avant cible) 0.2118 [0.17 ; 0.26], R/R 0.491, perte reelle 8.153 % (gap inclus), EV 0.4832 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 8.804 %) — p(stop avant cible) 0.1696 [0.13 ; 0.21], R/R 0.446, perte reelle 8.96 % (gap inclus), EV 0.4839 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.604 %) — p(stop avant cible) 0.1487 [0.11 ; 0.19], R/R 0.412, perte reelle 9.709 % (gap inclus), EV 0.5251 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 11.205 %) — p(stop avant cible) 0.1083 [0.08 ; 0.14], R/R 0.355, perte reelle 11.261 % (gap inclus), EV 0.5171 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 4.14 ATR (stop 14.216 %) — p(stop avant cible) 0.0473 [0.03 ; 0.07], R/R 0.278, perte reelle 14.369 % (gap inclus), EV 0.5716 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.29 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.007 %) — p(stop avant cible) 0.0216 [0.01 ; 0.04], R/R 0.242, perte reelle 16.536 % (gap inclus), EV 0.6343 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.76 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.608 %) — p(stop avant cible) 0.0104 [0.00 ; 0.03], R/R 0.215, perte reelle 18.627 % (gap inclus), EV 0.6803 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.12 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 19.209 %) — p(stop avant cible) 0.009 [0.00 ; 0.02], R/R 0.201, perte reelle 19.852 % (gap inclus), EV 0.677 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.19 % > budget 12.00 %
   - ⚪ grid_snapped a 6.39 ATR (stop 21.415 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 0.175, perte reelle 22.85 % (gap inclus), EV 0.6895 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.08 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.011 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.156, perte reelle 25.622 % (gap inclus), EV 0.7134 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.63 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 25.612 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.15, perte reelle 26.734 % (gap inclus), EV 0.7158 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.55 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 292.5, ATR14 9.3643 (3.201 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 1.223 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.16 % | 292.0318 | 88.86 % | 92.69 % | 94.27 % | 96.14 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.32 % | 291.5636 | 82.35 % | 88.25 % | 90.71 % | 93.47 % | 95.62 % | 96.98 % |
| 0.15 ATR | 0.48 % | 291.0954 | 74.85 % | 83.42 % | 86.76 % | 90.5 % | 93.53 % | 94.97 % |
| 0.2 ATR | 0.64 % | 290.6271 | 68.34 % | 78.68 % | 82.81 % | 87.33 % | 92.14 % | 94.37 % |
| 0.25 ATR | 0.8 % | 290.1589 | 63.12 % | 75.32 % | 79.64 % | 84.95 % | 90.35 % | 93.07 % |
| 0.35 ATR | 1.121 % | 289.2225 | 53.16 % | 68.81 % | 73.72 % | 80.5 % | 86.87 % | 90.95 % |
| 0.5 ATR | 1.601 % | 287.8179 | 38.26 % | 56.17 % | 63.83 % | 73.47 % | 82.29 % | 88.24 % |
| 0.75 ATR | 2.401 % | 285.4768 | 19.13 % | 36.53 % | 47.43 % | 58.81 % | 71.84 % | 81.41 % |
| 1.0 ATR | 3.201 % | 283.1357 | 9.76 % | 24.38 % | 34.49 % | 47.33 % | 62.39 % | 74.07 % |
| 1.25 ATR | 4.002 % | 280.7946 | 4.73 % | 14.91 % | 24.41 % | 37.92 % | 52.84 % | 66.93 % |
| 1.5 ATR | 4.802 % | 278.4536 | 2.17 % | 9.87 % | 17.49 % | 30.4 % | 45.47 % | 61.11 % |
| 2.0 ATR | 6.403 % | 273.7714 | 0.59 % | 4.34 % | 7.81 % | 16.63 % | 34.03 % | 51.26 % |
| 2.5 ATR | 8.004 % | 269.0893 | 0.3 % | 1.88 % | 4.55 % | 10.3 % | 23.58 % | 41.01 % |
| 3.0 ATR | 9.604 % | 264.4071 | 0.2 % | 1.38 % | 2.77 % | 6.04 % | 16.82 % | 33.57 % |
| 4.0 ATR | 12.806 % | 255.0429 | 0.0 % | 0.59 % | 1.68 % | 3.47 % | 8.66 % | 19.8 % |
| 6.0 ATR | 19.209 % | 236.3143 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 0.99 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.64 ATR | 0.82 ATR | 0.99 ATR | 1.12 ATR | 1.49 ATR | 1.94 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.24 ATR | 1.41 ATR | 1.89 ATR | 2.43 ATR |
| **5 s.** | 0.47 ATR | 0.94 ATR | 1.06 ATR | 1.41 ATR | 1.70 ATR | 1.88 ATR | 2.54 ATR | 3.40 ATR |
| **10 s.** | 0.67 ATR | 1.35 ATR | 1.52 ATR | 2.05 ATR | 2.43 ATR | 2.77 ATR | 3.84 ATR | 5.11 ATR |
| **20 s.** | 0.97 ATR | 2.06 ATR | 2.31 ATR | 3.04 ATR | 3.62 ATR | 3.98 ATR | 5.54 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.601 %, prix 287.8171), p(touche) 38.26 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.642–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.401 %, prix 285.4771), p(touche) 36.53 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.797–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.201 %, prix 283.1371), p(touche) 34.49 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.062–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.002 %, prix 280.7942), p(touche) 37.92 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.521–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.403 %, prix 273.7712), p(touche) 34.03 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.305–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.004 %, prix 269.0883), p(touche) 41.01 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.142 | EV/share : €1.326 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 16 % | T3 3 %
- Kelly (position) : f* 0.128 | ¼-Kelly 0.032 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 36.4 | bear 5.4 | side 58.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 585.0 (= 2 part(s) × prix) · cible 640.0


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

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.17 · part idiosyncratique 0.83
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 88.6  _(surachat)_
- **ADX** : 34.6  _(tendance etablie)_
- **MACD** : hist 3.352  _(pas de croisement recent)_
- **BB** : %B 1.01 · largeur 21.6%
- **ATR** : 9.36 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.118  _(accumulation)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 38.0  _(marche directionnel)_
- **MA** : MA20 263.65 · MA50 253.38 · MA200 234.55  _(prix > MA20)_
- **Dist MA** : MA20 +10.9% · MA50 +15.4% · MA200 +24.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (814572 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
