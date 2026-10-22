# HOOD

**Generated** : 2026-10-22T00:28:46.891928+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $101.94  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (13 séance(s) de retard, drapeau lu sur first_passage_by_horizon); usable=false (intervalle le plus large 25.2 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $101.94 (+2.2% vs entrée) · entrée $99.70 · stop $96.71 · T1 $102.42 · R/R 0.91  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +3.9 % ≠ (strike 102.0 − spot 101.94)/spot = +0.1 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.300 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-21 : 101.94 · ATR Wilder 5.79 (5.68 %)_
- **Swing** : plage **95.49 → 90.69** (-6.33 % a -11.04 % sous la cloture, 0.83 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 92.8-95.66 (A) ; 88.6-91.44 (A). stop INDICATIF 84.9 (-6.38 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **90.69 → 80.07** (-11.04 % a -21.46 % sous la cloture, 1.83 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 88.6-91.44 (A) ; 81.93-84.75 (A). stop INDICATIF 74.91 (-6.44 % sous le bas ; sous le support 77.8-79.57 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.74 ATR sous le plus haut 20 s., RSI(2) 75.8 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 96.59-99.0 (B, -2.88 %) ; 92.8-95.66 (A, -6.16 %) ; 88.6-91.44 (A, -10.3 %) ; 81.93-84.75 (A, -16.86 %) ; 77.8-79.57 (A, -21.95 %) ; 73.18-74.59 (A, -26.83 %)
- Resistances reelles au-dessus : 104.45-106.31 (A, 2.46 %) ; 108.81-111.46 (A, 6.74 %) ; 111.99-114.1 (A, 9.86 %) ; 117.46-120.05 (A, 15.22 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.26 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.17 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **1.341 pt plus bas** dans le cas TYPIQUE (médiane), 5.785 au p90, **7.615 au pire**
   - perte réelle **12.711 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 10.17 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0122 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.437 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.303** [0.2382 ; 0.3743] _(largeur 13.6 pt, n_eff 173.1)_
   - swing : **0.5127** [0.4601 ; 0.5651] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4558** [0.4039 ; 0.5085] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (25.2 pt), swing (32.5 pt), deep (32.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-6.03 %** | CVaR **-8.94 %** | vol 4.29 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.51 % contre 4.39 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.4 % vs -14.5 % si l'on extrapolait par √5 _(rapport 0.993 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7852** (β de hausse 1.6087, asymétrie 1.1098) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.437× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 93.7789 sur atr_based (1.5 ATR, 8.006 %) — p(stop avant cible) 0.504 [0.45 ; 0.56], R/R 2.322, perte reelle 8.399 % (gap inclus), CVaR 11.301 %, EV 0.9364 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2378 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.504, borne haute 0.556 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.006 %) — p(stop avant cible) 0.504 [0.45 ; 0.56], R/R 2.322, perte reelle 8.399 % (gap inclus), EV 0.9364 % — **REFUSE**
      - refuse : p_stop_first 0.504, borne haute 0.556 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 1.56 ATR (stop 10.92 %) — p(stop avant cible) 0.3504 [0.30 ; 0.40], R/R 1.701, perte reelle 11.463 % (gap inclus), EV 1.389 % — **REFUSE**
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.63 % > budget 12.00 %
   - 🟢 support a 1.93 ATR (stop 12.873 %) — p(stop avant cible) 0.2674 [0.22 ; 0.32], R/R 1.438, perte reelle 13.566 % (gap inclus), EV 1.5653 % — **REFUSE**
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.43 % > budget 12.00 %
   - 🟢 support a 4.23 ATR (stop 25.145 %) — p(stop avant cible) 0.0305 [0.02 ; 0.05], R/R 0.76, perte reelle 25.659 % (gap inclus), EV 2.0639 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.35 % > budget 12.00 %
   - 🟢 support a 6.01 ATR (stop 34.67 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.554, perte reelle 35.2 % (gap inclus), EV 2.1848 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.334 %) — p(stop avant cible) 0.9174 [0.88 ; 0.94], R/R 13.277, perte reelle 1.469 % (gap inclus), EV -0.1251 % — **REFUSE**
      - refuse : cible atteinte seulement 4.6 % du temps (< 15 %) meme a 10 seances : le R/R de 13.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.917, borne haute 0.943 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 4.6 % x 19.50 % + P(rien) 3.7 % x 8.98 % ne couvrent pas P(stop) 91.7 % x 1.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.669 %) — p(stop avant cible) 0.8029 [0.76 ; 0.84], R/R 6.833, perte reelle 2.854 % (gap inclus), EV 0.5447 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 6.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.803, borne haute 0.842 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 4.003 %) — p(stop avant cible) 0.7119 [0.66 ; 0.76], R/R 4.652, perte reelle 4.192 % (gap inclus), EV 0.8202 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.712, borne haute 0.758 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 5.337 %) — p(stop avant cible) 0.6442 [0.59 ; 0.69], R/R 3.436, perte reelle 5.676 % (gap inclus), EV 0.7417 % — **REFUSE**
      - refuse : p_stop_first 0.644, borne haute 0.693 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 6.671 %) — p(stop avant cible) 0.5932 [0.54 ; 0.64], R/R 2.798, perte reelle 6.971 % (gap inclus), EV 0.6006 % — **REFUSE**
      - refuse : p_stop_first 0.593, borne haute 0.644 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 1.56 ATR (stop 9.948 %) — p(stop avant cible) 0.4008 [0.35 ; 0.45], R/R 1.862, perte reelle 10.474 % (gap inclus), EV 1.306 % — **REFUSE**
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.84 % > budget 12.00 %
   - 🟢 grid_snapped a 1.93 ATR (stop 11.901 %) — p(stop avant cible) 0.2953 [0.25 ; 0.34], R/R 1.548, perte reelle 12.597 % (gap inclus), EV 1.6019 % — **REFUSE**
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.88 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 14.677 %) — p(stop avant cible) 0.2042 [0.16 ; 0.25], R/R 1.28, perte reelle 15.241 % (gap inclus), EV 1.6824 % — **REFUSE**
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.97 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 16.012 %) — p(stop avant cible) 0.1724 [0.14 ; 0.21], R/R 1.185, perte reelle 16.453 % (gap inclus), EV 1.743 % — **REFUSE**
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.53 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 18.68 %) — p(stop avant cible) 0.0957 [0.07 ; 0.13], R/R 1.025, perte reelle 19.023 % (gap inclus), EV 1.9315 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.34 % > budget 12.00 %
   - 🟢 grid_snapped a 4.23 ATR (stop 24.173 %) — p(stop avant cible) 0.0326 [0.02 ; 0.06], R/R 0.789, perte reelle 24.73 % (gap inclus), EV 2.0809 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.99 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 26.686 %) — p(stop avant cible) 0.0265 [0.01 ; 0.05], R/R 0.719, perte reelle 27.127 % (gap inclus), EV 2.0601 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.77 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 29.354 %) — p(stop avant cible) 0.0206 [0.01 ; 0.04], R/R 0.658, perte reelle 29.637 % (gap inclus), EV 2.0761 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.19 % > budget 12.00 %
   - 🟢 grid_snapped a 6.01 ATR (stop 33.698 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 0.573, perte reelle 34.021 % (gap inclus), EV 2.1823 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.51 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 37.36 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.522, perte reelle 37.36 % (gap inclus), EV 2.1956 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.25 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 40.029 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.487, perte reelle 40.029 % (gap inclus), EV 2.2117 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.92 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 42.697 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.457, perte reelle 42.697 % (gap inclus), EV 2.2117 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.92 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 101.94, ATR14 5.4407 (5.337 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.374 ATR = 1.996 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.267 % | 101.668 | 93.15 % | 95.26 % | 96.17 % | 96.66 % | 97.15 % | 98.05 % |
| 0.1 ATR | 0.534 % | 101.3959 | 85.5 % | 90.73 % | 92.43 % | 93.93 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.801 % | 101.1239 | 77.84 % | 85.69 % | 88.4 % | 90.7 % | 92.68 % | 95.07 % |
| 0.2 ATR | 1.067 % | 100.8519 | 71.5 % | 80.44 % | 84.26 % | 87.46 % | 90.45 % | 93.22 % |
| 0.25 ATR | 1.334 % | 100.5798 | 64.55 % | 74.7 % | 79.62 % | 83.92 % | 87.8 % | 90.86 % |
| 0.35 ATR | 1.868 % | 100.0358 | 52.47 % | 65.73 % | 72.35 % | 78.16 % | 83.64 % | 87.89 % |
| 0.5 ATR | 2.669 % | 99.2196 | 37.26 % | 53.73 % | 61.45 % | 68.96 % | 76.63 % | 82.14 % |
| 0.75 ATR | 4.003 % | 97.8595 | 19.64 % | 36.19 % | 46.01 % | 56.12 % | 65.75 % | 72.9 % |
| 1.0 ATR | 5.337 % | 96.4993 | 9.37 % | 23.29 % | 33.2 % | 44.49 % | 55.18 % | 65.3 % |
| 1.25 ATR | 6.671 % | 95.1391 | 4.93 % | 14.82 % | 22.91 % | 34.18 % | 47.46 % | 58.73 % |
| 1.5 ATR | 8.006 % | 93.7789 | 2.52 % | 10.08 % | 16.65 % | 27.4 % | 40.55 % | 52.87 % |
| 2.0 ATR | 10.674 % | 91.0586 | 0.5 % | 3.93 % | 7.47 % | 15.67 % | 29.88 % | 43.02 % |
| 2.5 ATR | 13.343 % | 88.3382 | 0.1 % | 1.61 % | 4.04 % | 8.49 % | 21.54 % | 33.88 % |
| 3.0 ATR | 16.012 % | 85.6179 | 0.0 % | 0.71 % | 2.42 % | 5.26 % | 15.14 % | 25.87 % |
| 4.0 ATR | 21.349 % | 80.1771 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.4 % | 14.48 % |
| 6.0 ATR | 32.023 % | 69.2957 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.25 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.97 ATR | 1.10 ATR | 1.51 ATR | 1.91 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.77 ATR | 1.00 ATR | 1.20 ATR | 1.37 ATR | 1.86 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.99 ATR | 1.29 ATR | 1.60 ATR | 1.81 ATR | 2.40 ATR | 3.09 ATR |
| **10 s.** | 0.54 ATR | 1.17 ATR | 1.34 ATR | 1.85 ATR | 2.29 ATR | 2.62 ATR | 3.59 ATR | 4.55 ATR |
| **20 s.** | 0.69 ATR | 1.65 ATR | 1.90 ATR | 2.56 ATR | 3.08 ATR | 3.52 ATR | 4.91 ATR | 5.92 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.424–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.669 %, prix 99.2192), p(touche) 37.26 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.003 %, prix 97.8593), p(touche) 36.19 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.77–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.337 %, prix 96.4995), p(touche) 33.2 % (en stress 92.0 %)  ✅ optimum identifie (60.2 % des re-echantillons)
- **5 seance(s)** : plage utile 0.989–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.337 %, prix 96.4995), p(touche) 44.49 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.339–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.006 %, prix 93.7787), p(touche) 40.55 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.899–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (13.343 %, prix 88.3381), p(touche) 33.88 % (en stress 93.88 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.012 | EV/share : $-0.035 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.2 | bear 85.0 | side 5.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 272.0 (= 3 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.196% → cible +2.729% / stop −3.0%, p_fill 50%, n_eff≈54.1) : P(cible|rempli) **37%** · **EV/risk +0.023** (×p_fill ; si rempli +0.14% du capital)
  - **swing** (entrée dip −4.833% → cible +6.27% / stop −5.608%, p_fill 29%, n_eff≈33.8) : P(cible|rempli) **50%** · **EV/risk +0.032** (×p_fill ; si rempli +0.63% du capital)
  - **deep** (entrée dip −7.464% → cible +9.119% / stop −8.651%, p_fill 32%, n_eff≈34.8) : P(cible|rempli) **55%** · **EV/risk +0.053** (×p_fill ; si rempli +1.44% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→52% · +3.0%→35% · +5.0%→18% · +8.0%→6%
- Range intraday médian 4.88% (p90 8.86%) · excursion haute méd. +2.07% / basse méd. −2.24%
- Profil de vol intra : ouverture 3.683% vs midi 0.98% vs clôture 1.099% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 19% · trend ↑0%/↓2% ; spike-down 66% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.016)_ ; drift intra méd. -0.529% ; recovery-V 19%
- **σ réalisé intraday** 3.385% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 36% / bas 57% / whipsaw 6%
- POC intraday (dernière séance, temps-au-prix) : 112.89 (VA 112.546–114.438 ; dernier close 112.73)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 23% · rebond 66% · **stop −4.04%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.02% · baisse 49% (gap-down >1% 30% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.95% (p90 −2.87%) · haut méd +1.04% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −3.46%) · haut méd +1.29% · range méd 2.92%
- Excursion ouverture 30min (n=160) : bas méd −1.56% (p90 −3.72%) · haut méd +1.57% · range méd 3.42%
- Excursion ouverture 60min (n=160) : bas méd −1.9% (p90 −3.9%) · haut méd +1.67% · range méd 3.85%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 112.74 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 79% (123/159) · gap 38% · délai 0.0min · rebond 62% (72/123) (MFE +1.49%)
   - −1.0% : fill 30min 60% · séance 68% (108/159) · gap 30% · délai 0.0min · rebond 68% (67/108) (MFE +1.66%)
   - −1.5% : fill 30min 47% · séance 61% (98/159) · gap 21% · délai 1.4min · rebond 60% (56/98) (MFE +1.44%)
   - −2.0% : fill 30min 37% · séance 50% (85/159) · gap 15% · délai 2.8min · rebond 70% (56/85) (MFE +1.4%)
   - −3.0% : fill 30min 22% · séance 34% (63/159) · gap 5% · délai 12.5min · rebond 71% (45/63) (MFE +1.74%)
   - −4.0% : fill 30min 12% · séance 23% (45/159) · gap 2% · délai 32.1min · rebond 66% (32/45) (MFE +2.22%)
   - −5.0% : fill 30min 7% · séance 14% (28/159) · gap 1% · délai 30.3min · rebond 63% (20/28) (MFE +2.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.55%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −2.2%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −2.14%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=751 jambes) : jambe baissière méd −1.14% (p90 −2.74%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 92% (71/75) · rebond 60% (39/71)
      · −2.0% : fill 75% (60/75) · rebond 68% (38/60)
      · −3.0% : fill 56% (48/75) · rebond 80% (35/48)
      · −4.0% : fill 38% (35/75) · rebond 74% (27/35)
      · −5.0% : fill 25% (24/75) · rebond 67% (17/24)
   - **flat** (17 séances) :
      · −1.0% : fill 66% (11/17) · rebond 70% (7/11)
      · −2.0% : fill 47% (9/17) · rebond 53% (5/9)
      · −3.0% : fill 20% (4/17) · rebond 7% (1/4)
      · −4.0% : fill 20% (4/17) · rebond 7% (1/4)
      · −5.0% : fill 16% (2/17) · rebond 15% (1/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 46% (26/67) · rebond 82% (21/26)
      · −2.0% : fill 26% (16/67) · rebond 86% (13/16)
      · −3.0% : fill 16% (11/67) · rebond 56% (9/11)
      · −4.0% : fill 9% (6/67) · rebond 63% (4/6)
      · −5.0% : fill 2% (2/67) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 63% si les 15 1res min sont vertes (75 cas) · 26% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **26min** → P(séance verte=clôture>ouverture) 66% si début vert vs 20% si rouge (base 42% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **66%** · continue >prix actuel 46% ; creux résiduel méd -1.61% (q20 -2.72%) → **SL/trailing à −2.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +2.73% → **scale +1.69% / runner +2.73%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +1.63% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.16% .. +3.94%] · haut q95 +5.0% · bas q05 -5.03%
   - 60min (n=160) : retour [-4.26% .. +4.93%] · haut q95 +5.37% · bas q05 -5.54%
   - 2h (n=160) : retour [-4.88% .. +5.34%] · haut q95 +7.5% · bas q05 -6.04%
   - 4h (n=160) : retour [-4.77% .. +6.75%] · haut q95 +8.29% · bas q05 -6.73%
   - 6h (n=160) : retour [-6.02% .. +6.48%] · haut q95 +8.48% · bas q05 -7.25%
   - session (n=160) : retour [-5.78% .. +6.96%] · haut q95 +8.59% · bas q05 -7.61%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **31%**. Lecture précoce 30 min : signature présente → 19% vs absente 2% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.24% / p90 1.92%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **77%** (reprise méd 15.35 min, n=49)
   - −1.0% → **62%** (reprise méd 30.0 min, n=21)
   - −1.5% → **48%** (reprise méd 42.24 min, n=10)
   - −2.0% → **15%** (reprise méd None min, n=5)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.92%** (p90, défaut prudent ; serré/agressif −1.24%) ; extension open→close méd +6.2% (q75 +8.64% / q95 +11.94%), MFE méd +7.69% / q90 +13.19%
   - Échelle scale-out : +7.69% (33%) / +9.01% (33%) / +13.19% (34%)
- **DÉSARMER** : repli > **−1.92%** depuis le plus-haut = décay → P(retournement) **85%** (préavis méd 310.68 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.19% : P(retournement après) 0% (mèche méd 3.29%)
- **CONTEXTE** : la dernière heure tient les gains 73% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.67 · part idiosyncratique 0.33
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-27 — HOOD earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-27 — HOOD earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 38.1  _(momentum baissier)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist -1.53  _(pas de croisement recent)_
- **BB** : %B 0.25 · largeur 25.8%
- **ATR** : 5.44 (45.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.297  _(distribution)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 42.4  _(transition)_
- **MA** : MA20 109.06 · MA50 108.92 · MA200 93.49  _(prix < MA20)_
- **Dist MA** : MA20 -6.5% · MA50 -6.4% · MA200 +9.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (776564 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
