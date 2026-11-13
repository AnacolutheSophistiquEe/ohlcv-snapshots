# SOI

**Generated** : 2026-11-13T01:10:34.343372+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 7.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €106.55  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (14 séance(s) de retard, drapeau lu sur first_passage_by_horizon); usable=false (intervalle le plus large 28.9 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €106.55 (+4.3% vs entrée) · entrée €102.14 · stop €99.01 · T1 €106.41 · R/R 1.36  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.07% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-12 : 106.55 · ATR Wilder 10.17 (9.54 %)_
- **Swing** : plage **91.39 → 83.35** (-14.22 % a -21.78 % sous la cloture, 0.79 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 84.75-89.15 (A). stop INDICATIF 72.77 (-12.69 % sous le bas ; sous le support 77.85-82.4 (- 0,5 ATR)).
- **Deep** : plage **83.35 → 49.33** (-21.78 % a -53.7 % sous la cloture, 3.35 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 77.85-82.4 (A) ; 72.55-72.9 (C) ; 64.2-68.5 (B) ; 58.94-63.5 (B) ; 53.65-57.9 (B) ; 48.55-50.38 (A). stop INDICATIF 38.06 (-22.85 % sous le bas ; sous le support 43.14-47.59 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.81 ATR sous le plus haut 20 s., RSI(2) 66.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 97.95-102.4 (B, -3.89 %) ; 91.65-96.02 (A, -9.88 %) ; 84.75-89.15 (A, -16.33 %) ; 77.85-82.4 (A, -22.67 %) ; 72.55-72.9 (C, -31.58 %) ; 64.2-68.5 (B, -35.71 %)
- Resistances reelles au-dessus : 110.4-114.9 (A, 3.61 %) ; 116.8-121.8 (A, 9.62 %) ; 123.3-128.0 (A, 15.72 %) ; 132.0-136.1 (A, 23.89 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.38 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (18.91 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **10.384 pt plus bas** dans le cas TYPIQUE (médiane), 10.384 au p90, **10.384 au pire**
   - perte réelle **29.294 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 18.91 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0081 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.839 % | p01 -5.347 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4308** [0.3587 ; 0.5052] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3047** [0.258 ; 0.3547] _(largeur 9.7 pt, n_eff 345.8)_
   - deep : **0.2615** [0.2173 ; 0.3097] _(largeur 9.2 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (28.9 pt), swing (35.8 pt), deep (35.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-9.6 %** | CVaR **-14.22 %** | vol 6.47 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 2.76 % contre 6.53 % aujourd'hui, rapport 0.42)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.27 % vs -12.04 % si l'on extrapolait par √5 _(rapport 1.102 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0581** (β de hausse 1.5562, asymétrie 0.6799) vs FCHI — 622 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.058× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 96.1093 sur atr_grid (1.0 ATR, 9.799 %) — p(stop avant cible) 0.495 [0.44 ; 0.55], R/R 3.179, perte reelle 10.138 % (gap inclus), CVaR 13.086 %, EV 1.5936 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2338 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 12.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 13.09 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 14.698 %) — p(stop avant cible) 0.3342 [0.29 ; 0.39], R/R 2.118, perte reelle 15.214 % (gap inclus), EV 1.4873 % — **REFUSE**
      - refuse : cible atteinte seulement 14.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.89 % > budget 12.00 %
   - 🟢 support a 1.69 ATR (stop 19.838 %) — p(stop avant cible) 0.2062 [0.17 ; 0.25], R/R 1.594, perte reelle 20.211 % (gap inclus), EV 2.2064 % — **REFUSE**
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.38 % > budget 12.00 %
   - 🟢 support a 2.38 ATR (stop 26.633 %) — p(stop avant cible) 0.0752 [0.05 ; 0.11], R/R 1.199, perte reelle 26.883 % (gap inclus), EV 2.2452 % — **REFUSE**
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.01 % > budget 12.00 %
   - 🟢 support a 3.96 ATR (stop 42.118 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.765, perte reelle 42.118 % (gap inclus), EV 2.3398 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.73 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 2.45 %) — p(stop avant cible) 0.815 [0.77 ; 0.85], R/R 12.39, perte reelle 2.601 % (gap inclus), EV 1.6003 % — **REFUSE**
      - refuse : cible atteinte seulement 6.9 % du temps (< 15 %) meme a 10 seances : le R/R de 12.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.815, borne haute 0.853 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 4.899 %) — p(stop avant cible) 0.6867 [0.64 ; 0.73], R/R 6.116, perte reelle 5.269 % (gap inclus), EV 1.941 % — **REFUSE**
      - refuse : cible atteinte seulement 10.3 % du temps (< 15 %) meme a 10 seances : le R/R de 6.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.687, borne haute 0.734 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 7.349 %) — p(stop avant cible) 0.5955 [0.54 ; 0.65], R/R 4.18, perte reelle 7.71 % (gap inclus), EV 1.6057 % — **REFUSE**
      - refuse : cible atteinte seulement 11.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.596, borne haute 0.646 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 9.799 %) — p(stop avant cible) 0.495 [0.44 ; 0.55], R/R 3.179, perte reelle 10.138 % (gap inclus), EV 1.5936 % — **REFUSE**
      - refuse : cible atteinte seulement 12.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.09 % > budget 12.00 %
   - ⚪ atr_grid a 1.25 ATR (stop 12.249 %) — p(stop avant cible) 0.4124 [0.36 ; 0.46], R/R 2.534, perte reelle 12.719 % (gap inclus), EV 1.4796 % — **REFUSE**
      - refuse : cible atteinte seulement 14.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.12 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 29.397 %) — p(stop avant cible) 0.0349 [0.02 ; 0.06], R/R 1.091, perte reelle 29.547 % (gap inclus), EV 2.3635 % — **REFUSE**
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.17 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 34.296 %) — p(stop avant cible) 0.0203 [0.01 ; 0.04], R/R 0.938, perte reelle 34.358 % (gap inclus), EV 2.29 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.68 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 44.095 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.731, perte reelle 44.095 % (gap inclus), EV 2.3526 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.46 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 48.994 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.658, perte reelle 48.994 % (gap inclus), EV 2.3526 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.46 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 53.894 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.598, perte reelle 53.894 % (gap inclus), EV 2.3526 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.46 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 58.793 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.548, perte reelle 58.793 % (gap inclus), EV 2.3526 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.46 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 63.693 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.506, perte reelle 63.693 % (gap inclus), EV 2.3526 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.46 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 68.592 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.47, perte reelle 68.592 % (gap inclus), EV 2.3526 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.46 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 73.492 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.438, perte reelle 73.492 % (gap inclus), EV 2.3526 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.46 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 78.391 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.411, perte reelle 78.391 % (gap inclus), EV 2.3526 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.46 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 106.55, ATR14 10.4407 (9.799 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.359 ATR = 3.518 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.49 % | 106.028 | 91.08 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.98 % | 105.5059 | 84.51 % | 89.89 % | 91.75 % | 94.29 % | 96.04 % | 97.2 % |
| 0.15 ATR | 1.47 % | 104.9839 | 77.55 % | 84.89 % | 87.43 % | 90.85 % | 93.67 % | 95.2 % |
| 0.2 ATR | 1.96 % | 104.4619 | 68.82 % | 79.78 % | 83.5 % | 87.89 % | 91.49 % | 93.41 % |
| 0.25 ATR | 2.45 % | 103.9398 | 62.45 % | 75.96 % | 80.06 % | 86.22 % | 90.21 % | 92.91 % |
| 0.35 ATR | 3.43 % | 102.8958 | 50.88 % | 67.62 % | 73.28 % | 81.2 % | 86.05 % | 90.41 % |
| 0.5 ATR | 4.899 % | 101.3296 | 36.37 % | 55.94 % | 63.16 % | 73.62 % | 81.4 % | 87.71 % |
| 0.75 ATR | 7.349 % | 98.7195 | 17.06 % | 35.43 % | 46.86 % | 58.66 % | 73.0 % | 81.02 % |
| 1.0 ATR | 9.799 % | 96.1093 | 8.24 % | 23.75 % | 34.28 % | 47.74 % | 64.89 % | 75.62 % |
| 1.25 ATR | 12.249 % | 93.4991 | 4.22 % | 15.9 % | 25.64 % | 38.09 % | 57.27 % | 70.63 % |
| 1.5 ATR | 14.698 % | 90.8889 | 2.35 % | 10.79 % | 18.76 % | 30.51 % | 49.46 % | 64.44 % |
| 2.0 ATR | 19.598 % | 85.6686 | 0.59 % | 4.61 % | 9.33 % | 18.6 % | 35.71 % | 53.85 % |
| 2.5 ATR | 24.497 % | 80.4482 | 0.29 % | 2.55 % | 5.21 % | 12.3 % | 24.83 % | 46.05 % |
| 3.0 ATR | 29.397 % | 75.2279 | 0.2 % | 0.88 % | 2.75 % | 7.68 % | 17.51 % | 37.96 % |
| 4.0 ATR | 39.196 % | 64.7872 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 10.29 % | 24.38 % |
| 6.0 ATR | 58.793 % | 43.9057 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.69 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.63 ATR | 0.80 ATR | 0.97 ATR | 1.12 ATR | 1.56 ATR | 1.97 ATR |
| **3 s.** | 0.33 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.27 ATR | 1.46 ATR | 1.96 ATR | 2.54 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.42 ATR | 1.73 ATR | 1.94 ATR | 2.75 ATR | 3.65 ATR |
| **10 s.** | 0.69 ATR | 1.48 ATR | 1.66 ATR | 2.12 ATR | 2.49 ATR | 2.83 ATR | 4.10 ATR | 5.81 ATR |
| **20 s.** | 1.03 ATR | 2.25 ATR | 2.56 ATR | 3.37 ATR | 3.95 ATR | 4.75 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.411 ATR au-dessus du haut de la grille, 0.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (65.5 % des re-echantillons)
- **2 seance(s)** : plage utile VIDE (borne basse 0.633 ATR au-dessus du haut de la grille, 0.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.787 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile VIDE (borne basse 1.071 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.662 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.565 ATR au-dessus du haut de la grille, 2.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.038 | EV/share : €-0.118 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 80.9 | bear 7.3 | side 11.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.14% → cible +4.183% / stop −3.067%, p_fill 38%, n_eff≈41.0) : P(cible|rempli) **27%** · **EV/risk -0.002** (×p_fill ; si rempli -0.01% du capital)
  - **swing** (entrée dip −9.111% → cible +21.372% / stop −10.781%, p_fill 21%, n_eff≈26.9) : P(cible|rempli) **15%** · **EV/risk +0.008** (×p_fill ; si rempli +0.40% du capital)
  - **deep** (entrée dip −14.082% → cible +28.391% / stop −17.107%, p_fill 23%, n_eff≈27.3) : P(cible|rempli) **20%** · **EV/risk +0.051** (×p_fill ; si rempli +3.85% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→83% · +1.0%→74% · +2.0%→62% · +3.0%→46% · +5.0%→29% · +8.0%→10%
- Range intraday médian 7.0% (p90 13.76%) · excursion haute méd. +2.7% / basse méd. −3.24%
- Profil de vol intra : ouverture 4.423% vs midi 1.287% vs clôture 1.954% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑1%/↓1% ; spike-down 73% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.002)_ ; drift intra méd. -0.88% ; recovery-V 29%
- **σ réalisé intraday** 3.81% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 78% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 111.4765 (VA 109.8045–114.4025 ; dernier close 111.96)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 66% · **stop −6.95%** sous le fill (sous le bruit) · cible +2.1% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. 0.56% · baisse 40% (gap-down >1% 26% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.01% (p90 −3.1%) · haut méd +0.82% · range méd 2.14%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −3.34%) · haut méd +1.06% · range méd 2.95%
- Excursion ouverture 30min (n=160) : bas méd −1.56% (p90 −3.74%) · haut méd +1.13% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.76% (p90 −4.51%) · haut méd +1.44% · range méd 3.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 111.65 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 77% (120/159) · gap 33% · délai 0.2min · rebond 61% (78/120) (MFE +1.63%)
   - −1.0% : fill 30min 55% · séance 73% (114/159) · gap 26% · délai 0.2min · rebond 63% (76/114) (MFE +1.69%)
   - −1.5% : fill 30min 48% · séance 65% (104/159) · gap 21% · délai 1.3min · rebond 58% (72/104) (MFE +1.84%)
   - −2.0% : fill 30min 44% · séance 62% (98/159) · gap 18% · délai 4.5min · rebond 66% (72/98) (MFE +1.89%)
   - −3.0% : fill 30min 30% · séance 47% (80/159) · gap 9% · délai 8.9min · rebond 73% (66/80) (MFE +1.88%)
   - −4.0% : fill 30min 21% · séance 39% (68/159) · gap 6% · délai 15.4min · rebond 72% (54/68) (MFE +1.92%)
   - −5.0% : fill 30min 14% · séance 30% (53/159) · gap 3% · délai 38.9min · rebond 66% (39/53) (MFE +2.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −3.17%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −3.07%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.7% (p90 −2.29%) → stop au-delà de −1.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1324 jambes) : jambe baissière méd −1.26% (p90 −3.04%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (59 séances) :
      · −1.0% : fill 95% (56/59) · rebond 52% (33/56)
      · −2.0% : fill 93% (54/59) · rebond 60% (37/54)
      · −3.0% : fill 80% (49/59) · rebond 64% (38/49)
      · −4.0% : fill 68% (42/59) · rebond 70% (35/42)
      · −5.0% : fill 59% (35/59) · rebond 68% (27/35)
   - **flat** (11 séances) :
      · −1.0% : fill 83% (10/11) · rebond 66% (7/10)
      · −2.0% : fill 74% (9/11) · rebond 65% (7/9)
      · −3.0% : fill 74% (9/11) · rebond 73% (7/9)
      · −4.0% : fill 68% (8/11) · rebond 85% (6/8)
      · −5.0% : fill 55% (7/11) · rebond 63% (5/7)
   - **gap-up** (89 séances) :
      · −1.0% : fill 58% (48/89) · rebond 74% (36/48)
      · −2.0% : fill 40% (35/89) · rebond 74% (28/35)
      · −3.0% : fill 22% (22/89) · rebond 92% (21/22)
      · −4.0% : fill 16% (18/89) · rebond 72% (13/18)
      · −5.0% : fill 8% (11/89) · rebond 60% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 62% si les 15 1res min sont vertes (75 cas) · 31% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **10min** → P(séance verte=clôture>ouverture) 63% si début vert vs 28% si rouge (base 44% · écart 34 pts) ; prédictivité sature ensuite (plafond brut 284min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **63%** · continue >prix actuel 51% ; creux résiduel méd -2.33% (q20 -4.61%) → **SL/trailing à −4.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.95% / q75 +5.39% → **scale +2.95% / runner +5.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **28%** (continue à baisser 61%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.99%** (au-delà de la MAE q10 -6.99%), cible rebond +2.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.33% .. +4.1%] · haut q95 +5.94% · bas q05 -5.72%
   - 60min (n=160) : retour [-4.39% .. +4.55%] · haut q95 +6.48% · bas q05 -5.91%
   - 2h (n=160) : retour [-5.15% .. +5.34%] · haut q95 +7.16% · bas q05 -6.63%
   - 4h (n=160) : retour [-5.33% .. +6.48%] · haut q95 +7.84% · bas q05 -7.2%
   - 6h (n=160) : retour [-6.3% .. +7.83%] · haut q95 +8.85% · bas q05 -7.75%
   - session (n=160) : retour [-7.87% .. +8.67%] · haut q95 +10.28% · bas q05 -9.9%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **38%**. Lecture précoce 30 min : signature présente → 16% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.4% / p90 1.99%) · ~5.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **90%** (reprise méd 24.99 min, n=53)
   - −1.0% → **91%** (reprise méd 44.55 min, n=28)
   - −1.5% → **80%** (reprise méd 50.92 min, n=16)
   - −2.0% → **85%** (reprise méd 52.07 min, n=12)
   - −3.0% → **100%** (reprise méd 60.96 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.99%** (p90, défaut prudent ; serré/agressif −1.4%) ; extension open→close méd +8.74% (q75 +9.27% / q95 +13.89%), MFE méd +9.37% / q90 +14.21%
   - Échelle scale-out : +9.37% (33%) / +10.06% (33%) / +14.21% (34%)
- **DÉSARMER** : repli > **−1.99%** depuis le plus-haut = décay → P(retournement) **15%** (préavis méd 36.46 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.21% : P(retournement après) 0% (mèche méd 2.71%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +1.29%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 47.4  _(neutre)_
- **ADX** : 25.5  _(tendance etablie)_
- **MACD** : hist -0.964  _(pas de croisement recent)_
- **BB** : %B 0.32 · largeur 43.0%
- **ATR** : 10.44 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.043  _(neutre)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 43.6  _(transition)_
- **MA** : MA20 115.32 · MA50 134.41 · MA200 107.47  _(prix < MA20)_
- **Dist MA** : MA20 -7.6% · MA50 -20.7% · MA200 -0.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (698826 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
