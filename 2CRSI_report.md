# AL2SI

**Generated** : 2026-10-15T00:11:48.731000+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.80  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (8 séance(s) de retard, drapeau lu sur first_passage_by_horizon); usable=false (intervalle le plus large 26.0 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €27.80 (+4.6% vs entrée) · entrée €26.57 · stop €24.59 · T1 €28.75 · R/R 1.1  
> ↳ ¼-Kelly 0.025 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.150 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 27.8 · ATR Wilder 2.04 (7.34 %)_
- **Swing** : plage **25.49 → 24.02** (-8.31 % a -13.59 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 25.0-25.32 (C). stop INDICATIF 21.58 (-10.17 % sous le bas ; sous le support 22.6-23.55 (- 0,5 ATR)).
- **Deep** : plage **24.02 → 20.49** (-13.59 % a -26.31 % sous la cloture, 1.73 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 22.6-23.55 (A) ; 20.1-21.05 (A). stop INDICATIF 18.45 (-9.96 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (1.75 ATR sous le plus haut 20 s., RSI(2) 53.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 25.92-26.7 (B, -3.96 %) ; 25.0-25.32 (C, -8.92 %) ; 22.6-23.55 (A, -15.29 %) ; 20.1-21.05 (A, -24.28 %) ; 16.1-16.65 (A, -40.11 %) ; 14.2-15.0 (A, -46.04 %)
- Resistances reelles au-dessus : 30.0-30.94 (A, 7.91 %) ; 31.38-31.54 (B, 12.88 %) ; 33.02-33.02 (C, 18.78 %) ; 34.5-35.02 (A, 24.1 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.56 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **9.826 pt plus bas** dans le cas TYPIQUE (médiane), 21.081 au p90, **26.557 au pire**
   - perte réelle **22.515 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 11.56 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0513 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5015** [0.4275 ; 0.5754] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4129** [0.3619 ; 0.4653] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3238** [0.2761 ; 0.3744] _(largeur 9.8 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (26.0 pt), deep (25.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.41 %** | CVaR **-12.97 %** | vol 6.52 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 4.25 % contre 7.22 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -14.08 % si l'on extrapolait par √5 _(rapport 1.048 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2079** (β de hausse 0.9438, asymétrie 1.2798) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.091× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 26.3107 sur atr_grid (0.75 ATR, 5.357 %) — p(stop avant cible) 0.6707 [0.62 ; 0.72], R/R 3.374, perte reelle 5.747 % (gap inclus), CVaR 10.594 %, EV 0.6781 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3067 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.671, borne haute 0.719 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 27.9 % de la queue et il ne reste que 13.84 EUR a partager. Prix du risque 0.004 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.41 ATR (stop 12.372 %) — p(stop avant cible) 0.2975 [0.25 ; 0.35], R/R 1.341, perte reelle 14.46 % (gap inclus), EV 2.1165 % — **REFUSE**
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.80 % > budget 12.00 %
   - 🟢 support a 2.62 ATR (stop 21.005 %) — p(stop avant cible) 0.1422 [0.11 ; 0.18], R/R 0.709, perte reelle 27.348 % (gap inclus), EV 1.4088 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.91 % > budget 12.00 %
   - 🟢 support a 3.88 ATR (stop 29.998 %) — p(stop avant cible) 0.079 [0.05 ; 0.11], R/R 0.538, perte reelle 36.021 % (gap inclus), EV 1.5747 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.51 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.786 %) — p(stop avant cible) 0.8704 [0.83 ; 0.90], R/R 9.949, perte reelle 1.949 % (gap inclus), EV 0.4441 % — **REFUSE**
      - refuse : cible atteinte seulement 10.2 % du temps (< 15 %) meme a 10 seances : le R/R de 9.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.870, borne haute 0.903 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.571 %) — p(stop avant cible) 0.7542 [0.71 ; 0.80], R/R 5.053, perte reelle 3.837 % (gap inclus), EV 0.7804 % — **REFUSE**
      - refuse : p_stop_first 0.754, borne haute 0.797 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 5.357 %) — p(stop avant cible) 0.6707 [0.62 ; 0.72], R/R 3.374, perte reelle 5.747 % (gap inclus), EV 0.6781 % — **REFUSE**
      - refuse : p_stop_first 0.671, borne haute 0.719 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 7.143 %) — p(stop avant cible) 0.5714 [0.52 ; 0.62], R/R 2.458, perte reelle 7.888 % (gap inclus), EV 1.0313 % — **REFUSE**
      - refuse : p_stop_first 0.571, borne haute 0.623 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.66 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 14.286 %) — p(stop avant cible) 0.2647 [0.22 ; 0.31], R/R 1.113, perte reelle 17.426 % (gap inclus), EV 1.6577 % — **REFUSE**
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.52 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 16.071 %) — p(stop avant cible) 0.2308 [0.19 ; 0.28], R/R 1.003, perte reelle 19.328 % (gap inclus), EV 1.6178 % — **REFUSE**
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.04 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 25.0 %) — p(stop avant cible) 0.0938 [0.07 ; 0.13], R/R 0.598, perte reelle 32.442 % (gap inclus), EV 1.6702 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.94 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 32.143 %) — p(stop avant cible) 0.0716 [0.05 ; 0.10], R/R 0.514, perte reelle 37.72 % (gap inclus), EV 1.5807 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.13 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 35.714 %) — p(stop avant cible) 0.051 [0.03 ; 0.08], R/R 0.468, perte reelle 41.421 % (gap inclus), EV 1.8759 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.54 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 39.286 %) — p(stop avant cible) 0.0371 [0.02 ; 0.06], R/R 0.437, perte reelle 44.32 % (gap inclus), EV 1.9727 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.02 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 42.857 %) — p(stop avant cible) 0.0293 [0.02 ; 0.05], R/R 0.422, perte reelle 45.946 % (gap inclus), EV 2.2092 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.82 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 46.429 %) — p(stop avant cible) 0.0293 [0.02 ; 0.05], R/R 0.397, perte reelle 48.898 % (gap inclus), EV 2.1227 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.55 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 50.0 %) — p(stop avant cible) 0.0293 [0.02 ; 0.05], R/R 0.345, perte reelle 56.123 % (gap inclus), EV 1.911 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.78 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 53.571 %) — p(stop avant cible) 0.0257 [0.01 ; 0.05], R/R 0.306, perte reelle 63.341 % (gap inclus), EV 1.7406 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.22 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 57.143 %) — p(stop avant cible) 0.0257 [0.01 ; 0.05], R/R 0.306, perte reelle 63.341 % (gap inclus), EV 1.7406 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.22 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 27.8, ATR14 1.9857 (7.143 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.399 ATR = 2.85 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.357 % | 27.7007 | 87.06 % | 90.58 % | 92.93 % | 94.49 % | 95.65 % | 97.2 % |
| 0.1 ATR | 0.714 % | 27.6014 | 82.55 % | 87.05 % | 90.28 % | 92.22 % | 94.16 % | 96.3 % |
| 0.15 ATR | 1.071 % | 27.5021 | 78.43 % | 83.42 % | 87.23 % | 89.07 % | 92.28 % | 95.2 % |
| 0.2 ATR | 1.429 % | 27.4029 | 72.65 % | 79.29 % | 83.4 % | 85.93 % | 89.91 % | 93.01 % |
| 0.25 ATR | 1.786 % | 27.3036 | 66.67 % | 74.68 % | 79.27 % | 82.58 % | 87.64 % | 91.41 % |
| 0.35 ATR | 2.5 % | 27.105 | 54.61 % | 65.55 % | 71.12 % | 75.79 % | 82.69 % | 87.91 % |
| 0.5 ATR | 3.571 % | 26.8071 | 40.59 % | 53.78 % | 61.98 % | 68.9 % | 78.14 % | 85.51 % |
| 0.75 ATR | 5.357 % | 26.3107 | 22.75 % | 37.68 % | 47.54 % | 55.91 % | 67.36 % | 76.92 % |
| 1.0 ATR | 7.143 % | 25.8143 | 12.84 % | 25.02 % | 33.99 % | 44.59 % | 57.47 % | 68.43 % |
| 1.25 ATR | 8.929 % | 25.3179 | 7.45 % | 17.66 % | 24.75 % | 36.71 % | 50.54 % | 62.04 % |
| 1.5 ATR | 10.714 % | 24.8214 | 3.63 % | 11.38 % | 17.49 % | 29.13 % | 43.22 % | 55.64 % |
| 2.0 ATR | 14.286 % | 23.8286 | 0.88 % | 5.2 % | 9.72 % | 17.03 % | 31.55 % | 43.86 % |
| 2.5 ATR | 17.857 % | 22.8357 | 0.1 % | 2.16 % | 4.62 % | 9.84 % | 21.36 % | 33.57 % |
| 3.0 ATR | 21.429 % | 21.8429 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 15.23 % | 26.07 % |
| 4.0 ATR | 28.571 % | 19.8571 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.28 % |
| 6.0 ATR | 42.857 % | 15.8857 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.03 ATR | 1.24 ATR | 1.41 ATR | 1.98 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 0.99 ATR | 1.37 ATR | 1.67 ATR | 1.88 ATR | 2.49 ATR | 3.42 ATR |
| **10 s.** | 0.57 ATR | 1.27 ATR | 1.44 ATR | 1.94 ATR | 2.32 ATR | 2.61 ATR | 3.78 ATR | 5.11 ATR |
| **20 s.** | 0.81 ATR | 1.74 ATR | 1.95 ATR | 2.54 ATR | 3.12 ATR | 3.69 ATR | 5.57 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.453–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.571 %, prix 26.8073), p(touche) 40.59 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (91.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.636–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.357 %, prix 26.3108), p(touche) 37.68 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.797–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.143 %, prix 25.8142), p(touche) 33.99 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.991–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.143 %, prix 25.8142), p(touche) 44.59 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.439–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.714 %, prix 24.8215), p(touche) 43.22 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.952–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.286 %, prix 23.8285), p(touche) 43.86 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.112 | EV/share : €0.223 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 21 % | T3 11 %
- Kelly (position) : f* 0.098 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 22.1 | side 72.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 389.0 (= 14 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.007% → cible +5.538% / stop −2.769%, p_fill 65%, n_eff≈69.3) : P(cible|rempli) **8%** · **EV/risk -0.246** (×p_fill ; si rempli -1.04% du capital)
  - **swing** (entrée dip −4.417% → cible +8.199% / stop −7.473%, p_fill 45%, n_eff≈54.2) : P(cible|rempli) **45%** · **EV/risk -0.059** (×p_fill ; si rempli -0.97% du capital)
  - **deep** (entrée dip −6.825% → cible +17.874% / stop −11.5%, p_fill 48%, n_eff≈55.4) : P(cible|rempli) **23%** · **EV/risk -0.068** (×p_fill ; si rempli -1.62% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.11 · part idiosyncratique 0.89
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 42.2  _(momentum baissier)_
- **ADX** : 16.3  _(pas de tendance nette)_
- **MACD** : hist 0.034  _(bullish_recent)_
- **BB** : %B 0.5 · largeur 26.2%
- **ATR** : 1.99 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.149  _(distribution)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 50.7  _(transition)_
- **MA** : MA20 27.83 · MA50 27.67 · MA200 28.82  _(prix < MA20)_
- **Dist MA** : MA20 -0.1% · MA50 +0.5% · MA200 -3.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (889070 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
