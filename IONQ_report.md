# IONQ

**Generated** : 2026-10-16T00:26:24.322077+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $34.35  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (9 séance(s) de retard, drapeau lu sur first_passage_by_horizon); usable=false (intervalle le plus large 27.6 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $34.35 (+2.8% vs entrée) · entrée $33.42 · stop $32.61 · T1 $34.78 · R/R 1.68  
> ↳ ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.43% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +27.3 % ≠ (strike 40.0 − spot 34.35)/spot = +16.5 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-15 : 34.35 · ATR Wilder 2.8 (8.14 %)_
- **Swing** : plage **30.9 → 28.78** (-10.03 % a -16.21 % sous la cloture, 0.76 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 29.99-31.33 (B). stop INDICATIF 26.43 (-8.15 % sous le bas ; sous le support 27.83-28.32 (- 0,5 ATR)).
- **Deep** : plage **28.78 → 24.15** (-16.21 % a -29.69 % sous la cloture, 1.65 ATR) — touchee 47 % → 15 % du temps en 20 seances ; supports reels dans la plage : 27.83-28.32 (B) ; 25.5-26.33 (A). stop INDICATIF 20.87 (-13.57 % sous le bas ; sous le support 22.27-23.49 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 4.85 ATR sous le plus haut 20 s., RSI(2) 53.3. Limite **32.95** (seance suivante), stop catastrophe 21.76, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 31.81-31.85 (A, -7.26 %) ; 29.99-31.33 (B, -8.78 %) ; 27.83-28.32 (B, -17.54 %) ; 25.5-26.33 (A, -23.34 %) ; 22.27-23.49 (B, -31.62 %) ; 20.61-21.5 (B, -37.4 %)
- Resistances reelles au-dessus : 36.57-37.28 (A, 6.48 %) ; 38.0-38.46 (A, 10.64 %) ; 39.76-40.84 (A, 15.78 %) ; 41.29-41.9 (A, 20.22 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.8 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **8.059 pt plus bas** dans le cas TYPIQUE (médiane), 8.059 au p90, **8.059 au pire**
   - perte réelle **21.859 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 13.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0064 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.087 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.52** [0.4458 ; 0.5936] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4517** [0.3998 ; 0.5044] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4161** [0.365 ; 0.4686] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (27.6 pt), swing (28.5 pt), deep (31.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.85 %** | CVaR **-10.55 %** | vol 6.14 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 10.39 % contre 5.48 % aujourd'hui, rapport 1.90)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.88 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.899 ; < 1 = le √5 surestime)_
- **β de baisse : 2.1831** (β de hausse 2.0106, asymétrie 1.0858) vs IWM — 605 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 31.6333 sur atr_grid (1.0 ATR, 7.896 %) — p(stop avant cible) 0.6421 [0.59 ; 0.69], R/R 3.209, perte reelle 8.02 % (gap inclus), CVaR 9.493 %, EV 0.6889 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2569 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.642, borne haute 0.691 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 11.843 %) — p(stop avant cible) 0.4663 [0.41 ; 0.52], R/R 2.154, perte reelle 11.947 % (gap inclus), EV 0.4014 % — **REFUSE**
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.81 % > budget 12.00 %
   - 🟢 support a 1.61 ATR (stop 15.317 %) — p(stop avant cible) 0.3097 [0.26 ; 0.36], R/R 1.67, perte reelle 15.417 % (gap inclus), EV 0.315 % — **REFUSE**
      - refuse : R/R 1.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.94 % > budget 12.00 %
   - 🟢 support a 3.12 ATR (stop 27.255 %) — p(stop avant cible) 0.0702 [0.05 ; 0.10], R/R 0.942, perte reelle 27.32 % (gap inclus), EV 0.5958 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.35 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.974 %) — p(stop avant cible) 0.8897 [0.85 ; 0.92], R/R 12.849, perte reelle 2.003 % (gap inclus), EV 0.3404 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 12.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.890, borne haute 0.919 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.948 %) — p(stop avant cible) 0.8105 [0.77 ; 0.85], R/R 6.35, perte reelle 4.053 % (gap inclus), EV 0.346 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 6.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.810, borne haute 0.849 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 5.922 %) — p(stop avant cible) 0.7458 [0.70 ; 0.79], R/R 4.286, perte reelle 6.005 % (gap inclus), EV 0.1122 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.746, borne haute 0.789 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 7.896 %) — p(stop avant cible) 0.6421 [0.59 ; 0.69], R/R 3.209, perte reelle 8.02 % (gap inclus), EV 0.6889 % — **REFUSE**
      - refuse : p_stop_first 0.642, borne haute 0.691 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 9.869 %) — p(stop avant cible) 0.5694 [0.52 ; 0.62], R/R 2.589, perte reelle 9.942 % (gap inclus), EV 0.4508 % — **REFUSE**
      - refuse : p_stop_first 0.569, borne haute 0.621 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 17.765 %) — p(stop avant cible) 0.2467 [0.20 ; 0.29], R/R 1.444, perte reelle 17.82 % (gap inclus), EV 0.4141 % — **REFUSE**
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.04 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 19.739 %) — p(stop avant cible) 0.1964 [0.16 ; 0.24], R/R 1.296, perte reelle 19.854 % (gap inclus), EV 0.5621 % — **REFUSE**
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.19 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 21.713 %) — p(stop avant cible) 0.1615 [0.13 ; 0.20], R/R 1.177, perte reelle 21.859 % (gap inclus), EV 0.5554 % — **REFUSE**
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.19 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 31.582 %) — p(stop avant cible) 0.0348 [0.02 ; 0.06], R/R 0.815, perte reelle 31.583 % (gap inclus), EV 0.5413 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.57 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 35.53 %) — p(stop avant cible) 0.0127 [0.00 ; 0.03], R/R 0.722, perte reelle 35.66 % (gap inclus), EV 0.6093 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.22 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 39.478 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 0.651, perte reelle 39.511 % (gap inclus), EV 0.6102 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.24 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 43.425 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.593, perte reelle 43.425 % (gap inclus), EV 0.6284 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.02 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 47.373 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.543, perte reelle 47.373 % (gap inclus), EV 0.6428 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.87 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 51.321 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.502, perte reelle 51.321 % (gap inclus), EV 0.6571 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.66 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 55.269 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.466, perte reelle 55.269 % (gap inclus), EV 0.6571 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.66 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 59.216 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.435, perte reelle 59.216 % (gap inclus), EV 0.6571 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.66 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 63.164 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.407, perte reelle 63.164 % (gap inclus), EV 0.6571 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.66 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 34.345, ATR14 2.7117 (7.896 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 3.016 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.395 % | 34.2094 | 93.76 % | 95.46 % | 96.17 % | 97.57 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.79 % | 34.0738 | 86.2 % | 91.23 % | 92.33 % | 94.64 % | 95.83 % | 96.82 % |
| 0.15 ATR | 1.184 % | 33.9382 | 78.95 % | 86.39 % | 88.4 % | 91.61 % | 93.6 % | 95.59 % |
| 0.2 ATR | 1.579 % | 33.8027 | 71.4 % | 80.65 % | 84.36 % | 88.47 % | 90.85 % | 93.43 % |
| 0.25 ATR | 1.974 % | 33.6671 | 65.36 % | 76.51 % | 80.83 % | 85.95 % | 88.82 % | 91.89 % |
| 0.35 ATR | 2.763 % | 33.3959 | 53.17 % | 67.54 % | 74.27 % | 79.47 % | 84.15 % | 88.3 % |
| 0.5 ATR | 3.948 % | 32.9891 | 38.17 % | 54.64 % | 62.36 % | 71.18 % | 78.66 % | 84.39 % |
| 0.75 ATR | 5.922 % | 32.3112 | 22.56 % | 39.52 % | 48.64 % | 59.05 % | 69.31 % | 76.8 % |
| 1.0 ATR | 7.896 % | 31.6333 | 10.27 % | 25.0 % | 35.12 % | 46.21 % | 58.33 % | 68.17 % |
| 1.25 ATR | 9.869 % | 30.9554 | 3.83 % | 14.62 % | 24.32 % | 35.09 % | 50.51 % | 61.81 % |
| 1.5 ATR | 11.843 % | 30.2774 | 1.11 % | 7.26 % | 15.94 % | 25.78 % | 41.46 % | 56.16 % |
| 2.0 ATR | 15.791 % | 28.9216 | 0.1 % | 1.92 % | 5.25 % | 14.46 % | 28.46 % | 45.28 % |
| 2.5 ATR | 19.739 % | 27.5657 | 0.0 % | 0.2 % | 1.31 % | 5.97 % | 18.29 % | 34.29 % |
| 3.0 ATR | 23.687 % | 26.2099 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.59 % | 25.98 % |
| 4.0 ATR | 31.582 % | 23.4981 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 3.05 % | 10.57 % |
| 6.0 ATR | 47.373 % | 18.0747 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.01 ATR | 1.21 ATR |
| **2 s.** | 0.27 ATR | 0.58 ATR | 0.66 ATR | 0.86 ATR | 1.00 ATR | 1.12 ATR | 1.41 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.82 ATR | 1.05 ATR | 1.23 ATR | 1.38 ATR | 1.78 ATR | 2.03 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.03 ATR | 1.31 ATR | 1.53 ATR | 1.75 ATR | 2.26 ATR | 2.65 ATR |
| **10 s.** | 0.60 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.17 ATR | 2.42 ATR | 3.19 ATR | 3.77 ATR |
| **20 s.** | 0.80 ATR | 1.78 ATR | 2.01 ATR | 2.58 ATR | 3.06 ATR | 3.39 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.659–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.922 %, prix 32.3111), p(touche) 39.52 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.817–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.896 %, prix 31.6331), p(touche) 35.12 % (en stress 92.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.027–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.869 %, prix 30.9555), p(touche) 35.09 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.402–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.843 %, prix 30.2775), p(touche) 41.46 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.013–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (68.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.052 | EV/share : $0.042 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 — | T3 —
- Kelly (position) : f* 0.072 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 51.3 | bear 8.3 | side 40.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.681% → cible +4.057% / stop −2.434%, p_fill 40%, n_eff≈47.2) : P(cible|rempli) **20%** · **EV/risk -0.107** (×p_fill ; si rempli -0.65% du capital)
  - **swing** (entrée dip −5.904% → cible +14.868% / stop −8.391%, p_fill 36%, n_eff≈43.4) : P(cible|rempli) **27%** · **EV/risk -0.001** (×p_fill ; si rempli -0.03% du capital)
  - **deep** (entrée dip −9.127% → cible +18.941% / stop −13.033%, p_fill 30%, n_eff≈36.2) : P(cible|rempli) **18%** · **EV/risk -0.046** (×p_fill ; si rempli -1.96% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→80% · +2.0%→64% · +3.0%→54% · +5.0%→28% · +8.0%→13%
- Range intraday médian 7.05% (p90 11.57%) · excursion haute méd. +3.57% / basse méd. −2.49%
- Profil de vol intra : ouverture 4.841% vs midi 1.378% vs clôture 1.552% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 62% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr 0.011)_ ; drift intra méd. -0.232% ; recovery-V 26%
- **σ réalisé intraday** 4.05% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 57% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 44.6406 (VA 44.2714–45.1154 ; dernier close 43.77)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 78% · **stop −4.38%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 49% (gap-down >1% 34% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.73%) · haut méd +1.28% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −3.76%) · haut méd +1.47% · range méd 3.38%
- Excursion ouverture 30min (n=160) : bas méd −1.31% (p90 −4.62%) · haut méd +1.81% · range méd 4.16%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −5.28%) · haut méd +1.87% · range méd 4.67%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (126/159) · gap 43% · délai 0.0min · rebond 61% (83/126) (MFE +1.81%)
   - −1.0% : fill 30min 60% · séance 70% (119/159) · gap 34% · délai 0.0min · rebond 67% (85/119) (MFE +1.91%)
   - −1.5% : fill 30min 53% · séance 65% (112/159) · gap 30% · délai 0.0min · rebond 70% (78/112) (MFE +2.06%)
   - −2.0% : fill 30min 46% · séance 54% (100/159) · gap 21% · délai 0.0min · rebond 69% (70/100) (MFE +2.17%)
   - −3.0% : fill 30min 37% · séance 43% (81/159) · gap 10% · délai 4.1min · rebond 70% (59/81) (MFE +2.38%)
   - −4.0% : fill 30min 22% · séance 33% (64/159) · gap 4% · délai 15.3min · rebond 69% (48/64) (MFE +2.23%)
   - −5.0% : fill 30min 11% · séance 25% (50/159) · gap 1% · délai 32.0min · rebond 78% (41/50) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.62%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −2.65%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.35%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1047 jambes) : jambe baissière méd −1.26% (p90 −2.97%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (80 séances) :
      · −1.0% : fill 100% (80/80) · rebond 69% (56/80)
      · −2.0% : fill 87% (73/80) · rebond 75% (54/73)
      · −3.0% : fill 72% (61/80) · rebond 72% (44/61)
      · −4.0% : fill 54% (47/80) · rebond 67% (34/47)
      · −5.0% : fill 38% (37/80) · rebond 70% (28/37)
   - **flat** (15 séances) :
      · −1.0% : fill 62% (10/15) · rebond 84% (9/10)
      · −2.0% : fill 43% (8/15) · rebond 90% (6/8)
      · −3.0% : fill 27% (5/15) · rebond 64% (4/5)
      · −4.0% : fill 23% (4/15) · rebond 57% (3/4)
      · −5.0% : fill 16% (3/15) · rebond 100% (3/3)
   - **gap-up** (64 séances) :
      · −1.0% : fill 41% (29/64) · rebond 55% (20/29)
      · −2.0% : fill 22% (19/64) · rebond 31% (10/19)
      · −3.0% : fill 15% (15/64) · rebond 60% (11/15)
      · −4.0% : fill 14% (13/64) · rebond 84% (11/13)
      · −5.0% : fill 12% (10/64) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 59% si les 15 1res min sont vertes (90 cas) · 26% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **56min** → P(séance verte=clôture>ouverture) 66% si début vert vs 19% si rouge (base 46% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=86) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.76% (q20 -4.14%) → **SL/trailing à −4.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.64% / q75 +3.31% → **scale +1.64% / runner +3.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **19%** (continue à baisser 59%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.23%** (au-delà de la MAE q10 -4.23%), cible rebond +1.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +5.46%] · haut q95 +7.35% · bas q05 -5.49%
   - 60min (n=160) : retour [-5.25% .. +5.86%] · haut q95 +7.69% · bas q05 -6.74%
   - 2h (n=160) : retour [-6.37% .. +5.93%] · haut q95 +8.07% · bas q05 -7.06%
   - 4h (n=160) : retour [-6.75% .. +6.86%] · haut q95 +8.75% · bas q05 -7.93%
   - 6h (n=160) : retour [-6.62% .. +7.19%] · haut q95 +9.75% · bas q05 -7.92%
   - session (n=160) : retour [-6.36% .. +8.14%] · haut q95 +9.8% · bas q05 -8.19%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0% / strong 7.5%) · base = 12 séances trend-up (n_eff 7.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **35%**. Lecture précoce 30 min : signature présente → 13% vs absente 5% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.3% (p75 2.44% / p90 3.18%) · ~4.0 replis/séance, durée méd 70.31 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 30.0 min, n=48)
   - −1.0% → **77%** (reprise méd 34.75 min, n=35)
   - −1.5% → **67%** (reprise méd 44.94 min, n=18)
   - −2.0% → **61%** (reprise méd 64.1 min, n=13)
   - −3.0% → **74%** (reprise méd 175.76 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.18%** (p90, défaut prudent ; serré/agressif −2.44%) ; extension open→close méd +8.16% (q75 +8.39% / q95 +13.57%), MFE méd +9.48% / q90 +12.4%
   - Échelle scale-out : +9.48% (33%) / +10.45% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−3.18%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 167.77 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 2.07%)
- **CONTEXTE** : la dernière heure tient les gains 70% du temps (retour médian dernière heure +0.1%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.51 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 20.3  _(survente)_
- **ADX** : 21.9  _(pas de tendance nette)_
- **MACD** : hist -1.181  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 38.8%
- **ATR** : 2.71 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.256  _(distribution)_
- **Vol ratio** : 1.6  _(volume au-dessus de la moyenne)_
- **Choppiness** : 28.5  _(marche directionnel)_
- **MA** : MA20 40.86 · MA50 40.93 · MA200 42.99  _(prix < MA20)_
- **Dist MA** : MA20 -15.9% · MA50 -16.1% · MA200 -20.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (834437 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
