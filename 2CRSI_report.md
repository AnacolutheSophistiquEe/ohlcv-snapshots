# AL2SI

**Generated** : 2026-10-09T00:13:42.532980+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €23.30  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (4 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €23.30 (+0.4% vs entrée) · entrée €23.21 · stop €22.75 · T1 €23.98 · R/R 1.67  
> ↳ ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 156 % hors [0,100] (R² max 0.92). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-08 : 23.3 · ATR Wilder 1.73 (7.44 %)_
- **Swing** : plage **21.34 → 20.09** (-8.42 % a -13.77 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 20.1-20.8 (B). stop INDICATIF 18.36 (-8.62 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **20.09 → 17.03** (-13.77 % a -26.9 % sous la cloture, 1.77 ATR) — touchee 41 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 15.23 (-10.56 % sous le bas ; sous le support 16.1-16.65 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.66 ATR sous le plus haut 20 s., RSI(2) 2.6. Limite **22.43** (seance suivante), stop catastrophe 15.5, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 20.1-20.8 (B, -10.73 %) ; 16.1-16.65 (A, -28.54 %) ; 14.2-15.0 (A, -35.62 %) ; 13.0-13.24 (B, -43.18 %) ; 11.76-12.4 (A, -46.78 %) ; 10.52-11.36 (A, -51.24 %)
- Resistances reelles au-dessus : 25.0-25.32 (B, 7.3 %) ; 26.38-26.7 (A, 13.22 %) ; 28.18-29.0 (B, 20.94 %) ; 30.0-30.8 (A, 28.76 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.5 %)** : le gap seul le franchit 0.938 % des séances (12 fois sur 1280).
   - exécution **3.302 pt plus bas** dans le cas TYPIQUE (médiane), 19.43 au p90, **30.617 au pire**
   - perte réelle **15.687 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 7.5 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0768 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 12 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5748** [0.5004 ; 0.6467] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4516** [0.3997 ; 0.5043] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.3403** [0.2919 ; 0.3914] _(largeur 10.0 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.24 %** | CVaR **-11.74 %** | vol 6.32 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.16 % contre 7.05 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -14.08 % si l'on extrapolait par √5 _(rapport 1.048 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2213** (β de hausse 0.9583, asymétrie 1.2744) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.074× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 22.1359 sur grid_snapped (0.45 ATR, 4.996 %) — p(stop avant cible) 0.6938 [0.64 ; 0.74], R/R 5.429, perte reelle 5.507 % (gap inclus), CVaR 12.081 %, EV 1.2294 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 3.5349 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 12.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.694, borne haute 0.741 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 12.08 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.114 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.1 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 1.85 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 0.45 ATR (stop 6.125 %) — p(stop avant cible) 0.6359 [0.58 ; 0.69], R/R 4.351, perte reelle 6.871 % (gap inclus), EV 1.5254 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.636, borne haute 0.685 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 15.60 % > budget 3.00 %
   - ⚪ atr_based a 1.5 ATR (stop 9.96 %) — p(stop avant cible) 0.4007 [0.35 ; 0.45], R/R 2.552, perte reelle 11.716 % (gap inclus), EV 2.746 % — **REFUSE**
      - refuse : R/R 2.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.99 % > budget 3.00 %
   - 🟢 support a 2.07 ATR (stop 16.855 %) — p(stop avant cible) 0.2064 [0.17 ; 0.25], R/R 1.401, perte reelle 21.338 % (gap inclus), EV 2.6264 % — **REFUSE**
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.74 % > budget 3.00 %
   - 🟢 support a 3.5 ATR (stop 26.383 %) — p(stop avant cible) 0.0936 [0.07 ; 0.13], R/R 0.886, perte reelle 33.76 % (gap inclus), EV 2.7226 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.11 % > budget 3.00 %
   - 🟢 grid_snapped a 0.45 ATR (stop 4.996 %) — p(stop avant cible) 0.6938 [0.64 ; 0.74], R/R 5.429, perte reelle 5.507 % (gap inclus), EV 1.2294 % — **REFUSE**
      - refuse : cible atteinte seulement 12.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.694, borne haute 0.741 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.08 % > budget 3.00 %
   - ⚪ atr_grid a 1.25 ATR (stop 8.3 %) — p(stop avant cible) 0.5136 [0.46 ; 0.57], R/R 3.146, perte reelle 9.504 % (gap inclus), EV 1.926 % — **REFUSE**
      - refuse : p_stop_first 0.514, borne haute 0.566 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 20.62 % > budget 3.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 11.62 %) — p(stop avant cible) 0.3143 [0.27 ; 0.36], R/R 2.192, perte reelle 13.641 % (gap inclus), EV 3.1482 % — **REFUSE**
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.33 % > budget 3.00 %
   - 🟢 grid_snapped a 2.07 ATR (stop 15.726 %) — p(stop avant cible) 0.2251 [0.18 ; 0.27], R/R 1.526, perte reelle 19.585 % (gap inclus), EV 2.7603 % — **REFUSE**
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.74 % > budget 3.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 18.26 %) — p(stop avant cible) 0.1908 [0.15 ; 0.23], R/R 1.287, perte reelle 23.237 % (gap inclus), EV 2.3737 % — **REFUSE**
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.69 % > budget 3.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 19.92 %) — p(stop avant cible) 0.1573 [0.12 ; 0.20], R/R 1.122, perte reelle 26.639 % (gap inclus), EV 2.4497 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.08 % > budget 3.00 %
   - 🟢 grid_snapped a 3.5 ATR (stop 25.254 %) — p(stop avant cible) 0.0996 [0.07 ; 0.13], R/R 0.912, perte reelle 32.79 % (gap inclus), EV 2.7491 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.08 % > budget 3.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.88 %) — p(stop avant cible) 0.0845 [0.06 ; 0.12], R/R 0.829, perte reelle 36.079 % (gap inclus), EV 2.6712 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.35 % > budget 3.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 33.2 %) — p(stop avant cible) 0.073 [0.05 ; 0.10], R/R 0.775, perte reelle 38.589 % (gap inclus), EV 2.6782 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.07 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 36.521 %) — p(stop avant cible) 0.0543 [0.03 ; 0.08], R/R 0.717, perte reelle 41.71 % (gap inclus), EV 3.0298 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.16 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.841 %) — p(stop avant cible) 0.0378 [0.02 ; 0.06], R/R 0.672, perte reelle 44.458 % (gap inclus), EV 3.3722 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.37 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 43.161 %) — p(stop avant cible) 0.0336 [0.02 ; 0.06], R/R 0.655, perte reelle 45.676 % (gap inclus), EV 3.3792 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.27 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 46.481 %) — p(stop avant cible) 0.03 [0.02 ; 0.05], R/R 0.611, perte reelle 48.918 % (gap inclus), EV 3.2864 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.06 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 49.801 %) — p(stop avant cible) 0.03 [0.02 ; 0.05], R/R 0.55, perte reelle 54.361 % (gap inclus), EV 3.1231 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.32 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 53.121 %) — p(stop avant cible) 0.0263 [0.01 ; 0.05], R/R 0.485, perte reelle 61.596 % (gap inclus), EV 2.9428 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.98 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 23.3, ATR14 1.5471 (6.64 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 2.656 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.332 % | 23.2226 | 87.06 % | 90.58 % | 92.93 % | 94.39 % | 95.55 % | 97.1 % |
| 0.1 ATR | 0.664 % | 23.1453 | 82.55 % | 87.05 % | 90.28 % | 92.13 % | 94.07 % | 96.2 % |
| 0.15 ATR | 0.996 % | 23.0679 | 78.43 % | 83.42 % | 87.23 % | 88.98 % | 92.19 % | 95.1 % |
| 0.2 ATR | 1.328 % | 22.9906 | 72.65 % | 79.29 % | 83.4 % | 85.83 % | 89.81 % | 92.91 % |
| 0.25 ATR | 1.66 % | 22.9132 | 66.67 % | 74.68 % | 79.27 % | 82.48 % | 87.54 % | 91.31 % |
| 0.35 ATR | 2.324 % | 22.7585 | 54.71 % | 65.75 % | 71.12 % | 75.69 % | 82.59 % | 87.81 % |
| 0.5 ATR | 3.32 % | 22.5264 | 40.49 % | 53.88 % | 61.98 % | 68.8 % | 78.04 % | 85.41 % |
| 0.75 ATR | 4.98 % | 22.1396 | 22.65 % | 37.59 % | 47.45 % | 55.71 % | 67.16 % | 76.72 % |
| 1.0 ATR | 6.64 % | 21.7529 | 12.84 % | 24.93 % | 33.89 % | 44.29 % | 57.17 % | 68.13 % |
| 1.25 ATR | 8.3 % | 21.3661 | 7.45 % | 17.57 % | 24.56 % | 36.32 % | 50.15 % | 61.64 % |
| 1.5 ATR | 9.96 % | 20.9793 | 3.63 % | 11.29 % | 17.29 % | 28.74 % | 42.83 % | 55.24 % |
| 2.0 ATR | 13.28 % | 20.2057 | 0.88 % | 5.1 % | 9.53 % | 16.63 % | 31.16 % | 43.46 % |
| 2.5 ATR | 16.6 % | 19.4321 | 0.1 % | 2.16 % | 4.52 % | 9.74 % | 20.97 % | 33.27 % |
| 3.0 ATR | 19.92 % | 18.6586 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 14.94 % | 25.87 % |
| 4.0 ATR | 26.56 % | 17.1114 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.18 % |
| 6.0 ATR | 39.841 % | 14.0171 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.60 ATR | 0.72 ATR | 0.82 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.60 ATR | 2.02 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.02 ATR | 1.24 ATR | 1.41 ATR | 1.97 ATR | 2.45 ATR |
| **5 s.** | 0.36 ATR | 0.88 ATR | 0.98 ATR | 1.36 ATR | 1.65 ATR | 1.86 ATR | 2.48 ATR | 3.42 ATR |
| **10 s.** | 0.57 ATR | 1.25 ATR | 1.43 ATR | 1.92 ATR | 2.30 ATR | 2.58 ATR | 3.77 ATR | 5.11 ATR |
| **20 s.** | 0.80 ATR | 1.72 ATR | 1.94 ATR | 2.52 ATR | 3.10 ATR | 3.67 ATR | 5.56 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.452–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.32 %, prix 22.5264), p(touche) 40.49 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (90.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.636–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.98 %, prix 22.1397), p(touche) 37.59 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.795–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.64 %, prix 21.7529), p(touche) 33.89 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.984–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.64 %, prix 21.7529), p(touche) 44.29 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.426–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.96 %, prix 20.9793), p(touche) 42.83 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.935–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.28 %, prix 20.2058), p(touche) 43.46 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.036 | EV/share : €0.017 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 — | T3 —
- Kelly (position) : f* 0.046 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 10.0 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.388% → cible +3.333% / stop −2.0%, p_fill 86%, n_eff≈91.7) : P(cible|rempli) **25%** · **EV/risk -0.227** (×p_fill ; si rempli -0.53% du capital)
  - **swing** (entrée dip −0.86% → cible +10.013% / stop −6.698%, p_fill 85%, n_eff≈99.2) : P(cible|rempli) **27%** · **EV/risk -0.133** (×p_fill ; si rempli -1.05% du capital)
  - **deep** (entrée dip −1.259% → cible +10.462% / stop −10.088%, p_fill 86%, n_eff≈95.5) : P(cible|rempli) **42%** · **EV/risk -0.018** (×p_fill ; si rempli -0.21% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→75% · +2.0%→68% · +3.0%→53% · +5.0%→35% · +8.0%→17%
- Range intraday médian 6.98% (p90 14.96%) · excursion haute méd. +3.32% / basse méd. −3.45%
- Profil de vol intra : ouverture 4.807% vs midi 1.539% vs clôture 1.704% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 5% · trend ↑1%/↓0% ; spike-down 74% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. -0.405% ; recovery-V 23%
- **σ réalisé intraday** 4.412% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 70% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 25.8615 (VA 25.2245–26.7435 ; dernier close 26.98)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 88% · **stop −3.68%** sous le fill (sous le bruit) · cible +2.19% · R/R 0.6 (high win-rate)
- Gaps overnight (n=158) : méd. 0.23% · baisse 41% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −3.41%) · haut méd +0.73% · range méd 2.23%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −4.07%) · haut méd +1.39% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −4.39%) · haut méd +1.93% · range méd 3.45%
- Excursion ouverture 60min (n=160) : bas méd −1.52% (p90 −5.59%) · haut méd +2.05% · range méd 3.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.82 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 80% (123/158) · gap 20% · délai 0.3min · rebond 62% (81/123) (MFE +1.87%)
   - −1.0% : fill 30min 50% · séance 75% (118/158) · gap 10% · délai 3.3min · rebond 60% (78/118) (MFE +1.56%)
   - −1.5% : fill 30min 43% · séance 69% (105/158) · gap 7% · délai 9.0min · rebond 58% (65/105) (MFE +1.52%)
   - −2.0% : fill 30min 36% · séance 63% (97/158) · gap 4% · délai 16.0min · rebond 54% (58/97) (MFE +1.11%)
   - −3.0% : fill 30min 19% · séance 46% (79/158) · gap 2% · délai 42.4min · rebond 58% (53/79) (MFE +1.4%)
   - −4.0% : fill 30min 13% · séance 39% (68/158) · gap 1% · délai 88.4min · rebond 73% (54/68) (MFE +1.57%)
   - −5.0% : fill 30min 9% · séance 28% (53/158) · gap 1% · délai 89.9min · rebond 88% (49/53) (MFE +2.19%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −3.05%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.84%) → stop au-delà de −1.98% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −3.92%) → stop au-delà de −2.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1483 jambes) : jambe baissière méd −1.21% (p90 −2.97%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 91% (45/47) · rebond 54% (26/45)
      · −2.0% : fill 84% (41/47) · rebond 49% (22/41)
      · −3.0% : fill 69% (37/47) · rebond 50% (25/37)
      · −4.0% : fill 61% (33/47) · rebond 58% (24/33)
      · −5.0% : fill 44% (27/47) · rebond 86% (24/27)
   - **flat** (34 séances) :
      · −1.0% : fill 78% (26/34) · rebond 66% (18/26)
      · −2.0% : fill 58% (20/34) · rebond 49% (12/20)
      · −3.0% : fill 43% (16/34) · rebond 60% (10/16)
      · −4.0% : fill 40% (15/34) · rebond 77% (12/15)
      · −5.0% : fill 32% (11/34) · rebond 80% (10/11)
   - **gap-up** (77 séances) :
      · −1.0% : fill 64% (47/77) · rebond 60% (34/47)
      · −2.0% : fill 54% (36/77) · rebond 62% (24/36)
      · −3.0% : fill 34% (26/77) · rebond 67% (18/26)
      · −4.0% : fill 26% (20/77) · rebond 88% (18/20)
      · −5.0% : fill 16% (15/77) · rebond 100% (15/15)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 56% si les 15 1res min sont vertes (76 cas) · 26% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:53** → P(séance verte=clôture>ouverture) 74% si début vert vs 14% si rouge (base 41% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **74%** · continue >prix actuel 50% ; creux résiduel méd -2.8% (q20 -5.42%) → **SL/trailing à −5.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.86% / q75 +3.31% → **scale +1.86% / runner +3.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **14%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.93%** (au-delà de la MAE q10 -4.93%), cible rebond +1.4% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.2% .. +5.28%] · haut q95 +6.81% · bas q05 -5.69%
   - 60min (n=160) : retour [-5.33% .. +4.89%] · haut q95 +7.28% · bas q05 -6.85%
   - 2h (n=160) : retour [-5.2% .. +7.14%] · haut q95 +8.79% · bas q05 -7.39%
   - 4h (n=160) : retour [-6.3% .. +7.38%] · haut q95 +9.96% · bas q05 -8.17%
   - 6h (n=160) : retour [-5.99% .. +8.19%] · haut q95 +11.34% · bas q05 -8.55%
   - session (n=160) : retour [-7.17% .. +9.91%] · haut q95 +12.5% · bas q05 -9.62%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.15 · part idiosyncratique 0.84
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.3  _(survente)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist -0.552  _(pas de croisement recent)_
- **BB** : %B -0.16 · largeur 24.9%
- **ATR** : 1.55 (41.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.165  _(distribution)_
- **Vol ratio** : 0.98  _(volume normal)_
- **Choppiness** : 38.5  _(transition)_
- **MA** : MA20 27.91 · MA50 27.53 · MA200 28.5  _(prix < MA20)_
- **Dist MA** : MA20 -16.5% · MA50 -15.4% · MA200 -18.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (848923 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
