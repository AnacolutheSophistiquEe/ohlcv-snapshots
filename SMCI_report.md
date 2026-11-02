# SMCI

**Generated** : 2026-11-02T01:24:17.346258+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $32.95  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-03 — SMCI earnings (J-1 sess · earnings)  
> ↳ spot $32.95 (+1.4% vs entrée) · entrée $32.49 · stop $30.00 · T1 $35.27 · R/R 1.12  
> ↳ ¼-Kelly 0.015 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.150 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-30 : 32.95 · ATR Wilder 2.4 (7.28 %)_
- **Swing** : plage **29.98 → 28.18** (-9.02 % a -14.47 % sous la cloture, 0.75 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 29.85-31.03 (A) ; 28.5-29.68 (B). stop INDICATIF 25.66 (-8.95 % sous le bas ; sous le support 26.86-27.75 (- 0,5 ATR)).
- **Deep** : plage **28.18 → 22.43** (-14.47 % a -31.92 % sous la cloture, 2.4 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 26.86-27.75 (B) ; 25.13-26.06 (A) ; 23.38-24.19 (A). stop INDICATIF 19.51 (-13.03 % sous le bas ; sous le support 20.71-21.79 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.34 ATR sous le plus haut 20 s., RSI(2) 18.4. Limite **31.75** (seance suivante), stop catastrophe 22.15, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 31.11-32.04 (B, -2.76 %) ; 29.85-31.03 (A, -5.83 %) ; 28.5-29.68 (B, -9.92 %) ; 26.86-27.75 (B, -15.78 %) ; 25.13-26.06 (A, -20.91 %) ; 23.38-24.19 (A, -26.59 %)
- Resistances reelles au-dessus : 33.86-34.98 (A, 2.76 %) ; 35.36-36.37 (A, 7.31 %) ; 36.8-37.85 (A, 11.68 %) ; 38.28-39.47 (A, 16.18 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.13 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.95 %)** : le gap seul le franchit 1.356 % des séances (17 fois sur 1254).
   - exécution **4.603 pt plus bas** dans le cas TYPIQUE (médiane), 16.588 au p90, **20.101 au pire**
   - perte réelle **15.075 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 8.95 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.083 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.856 % | p01 -10.29 % | pire -29.051 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5133** [0.4391 ; 0.587] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3794** [0.3294 ; 0.4314] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3561** [0.307 ; 0.4076] _(largeur 10.1 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-7.98 %** | CVaR **-12.63 %** | vol 5.95 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 3.73 % contre 6.19 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.53 % vs -16.84 % si l'on extrapolait par √5 _(rapport 1.041 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5376** (β de hausse 1.2166, asymétrie 1.2639) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.842× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 31.3659 sur swing_based (0.35 ATR, 4.808 %) — p(stop avant cible) 0.7068 [0.66 ; 0.75], R/R 4.625, perte reelle 5.396 % (gap inclus), CVaR 12.6 %, EV 0.4819 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 2.1328 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 12.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.707, borne haute 0.753 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 12.60 % > budget 4.89 %
- Budget de queue : **4.89 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.164 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 20.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.35 ATR (stop 4.808 %) — p(stop avant cible) 0.7068 [0.66 ; 0.75], R/R 4.625, perte reelle 5.396 % (gap inclus), EV 0.4819 % — **REFUSE**
      - refuse : cible atteinte seulement 12.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.707, borne haute 0.753 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.60 % > budget 4.89 %
   - ⚪ atr_based a 1.5 ATR (stop 11.326 %) — p(stop avant cible) 0.3575 [0.31 ; 0.41], R/R 1.946, perte reelle 12.824 % (gap inclus), EV 1.1975 % — **REFUSE**
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.65 % > budget 4.89 %
   - 🔴 support a 2.11 ATR (stop 18.077 %) — p(stop avant cible) 0.1821 [0.14 ; 0.23], R/R 1.237, perte reelle 20.18 % (gap inclus), EV 1.4205 % — **REFUSE**
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.85 % > budget 4.89 %
      - ⚠ support DETECTE a 0.34 ATR du spot — compartiment <1, mesure a 47.3 % de casse (IC clusterise [0.442 ; 0.505] sur 1151 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 3.03 ATR (stop 25.058 %) — p(stop avant cible) 0.1162 [0.09 ; 0.15], R/R 0.962, perte reelle 25.948 % (gap inclus), EV 1.2597 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.13 % > budget 4.89 %
   - 🟢 support a 3.85 ATR (stop 31.219 %) — p(stop avant cible) 0.0649 [0.04 ; 0.09], R/R 0.796, perte reelle 31.337 % (gap inclus), EV 1.0413 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.37 % > budget 4.89 %
   - ⚪ atr_grid a 1.0 ATR (stop 7.55 %) — p(stop avant cible) 0.5435 [0.49 ; 0.60], R/R 2.863, perte reelle 8.718 % (gap inclus), EV 0.8703 % — **REFUSE**
      - refuse : p_stop_first 0.543, borne haute 0.596 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.47 % > budget 4.89 %
   - ⚪ atr_grid a 1.25 ATR (stop 9.438 %) — p(stop avant cible) 0.4474 [0.40 ; 0.50], R/R 2.31, perte reelle 10.804 % (gap inclus), EV 0.8752 % — **REFUSE**
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.34 % > budget 4.89 %
   - ⚪ atr_grid a 1.75 ATR (stop 13.213 %) — p(stop avant cible) 0.2867 [0.24 ; 0.34], R/R 1.673, perte reelle 14.914 % (gap inclus), EV 1.2915 % — **REFUSE**
      - refuse : R/R 1.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.77 % > budget 4.89 %
   - ⚪ atr_grid a 2.75 ATR (stop 20.764 %) — p(stop avant cible) 0.1551 [0.12 ; 0.20], R/R 1.121, perte reelle 22.265 % (gap inclus), EV 1.3928 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.32 % > budget 4.89 %
   - ⚪ atr_grid a 3.5 ATR (stop 26.426 %) — p(stop avant cible) 0.1026 [0.07 ; 0.14], R/R 0.922, perte reelle 27.071 % (gap inclus), EV 1.2109 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.75 % > budget 4.89 %
   - ⚪ atr_grid a 4.5 ATR (stop 33.977 %) — p(stop avant cible) 0.0562 [0.04 ; 0.08], R/R 0.731, perte reelle 34.132 % (gap inclus), EV 0.9349 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.15 % > budget 4.89 %
   - ⚪ atr_grid a 5.0 ATR (stop 37.752 %) — p(stop avant cible) 0.0359 [0.02 ; 0.06], R/R 0.661, perte reelle 37.774 % (gap inclus), EV 0.9309 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.20 % > budget 4.89 %
   - ⚪ atr_grid a 5.5 ATR (stop 41.527 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 0.601, perte reelle 41.527 % (gap inclus), EV 1.079 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.57 % > budget 4.89 %
   - ⚪ atr_grid a 6.0 ATR (stop 45.302 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.548, perte reelle 45.528 % (gap inclus), EV 1.0812 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.58 % > budget 4.89 %
   - ⚪ atr_grid a 6.5 ATR (stop 49.078 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.486, perte reelle 51.362 % (gap inclus), EV 1.0709 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.72 % > budget 4.89 %
   - ⚪ atr_grid a 7.0 ATR (stop 52.853 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.449, perte reelle 55.543 % (gap inclus), EV 1.0713 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.80 % > budget 4.89 %
   - ⚪ atr_grid a 7.5 ATR (stop 56.628 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.441, perte reelle 56.628 % (gap inclus), EV 1.0704 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.78 % > budget 4.89 %
   - ⚪ atr_grid a 8.0 ATR (stop 60.403 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.413, perte reelle 60.403 % (gap inclus), EV 1.0784 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.62 % > budget 4.89 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 32.95, ATR14 2.4879 (7.55 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 2.628 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.378 % | 32.8256 | 90.85 % | 93.66 % | 94.96 % | 95.56 % | 96.75 % | 97.95 % |
| 0.1 ATR | 0.755 % | 32.7012 | 82.29 % | 87.61 % | 89.52 % | 91.52 % | 93.3 % | 95.28 % |
| 0.15 ATR | 1.133 % | 32.5768 | 75.25 % | 82.58 % | 85.38 % | 88.69 % | 91.07 % | 94.05 % |
| 0.2 ATR | 1.51 % | 32.4524 | 68.31 % | 77.74 % | 80.95 % | 86.26 % | 89.64 % | 92.82 % |
| 0.25 ATR | 1.888 % | 32.328 | 62.17 % | 73.11 % | 76.71 % | 82.93 % | 87.72 % | 91.28 % |
| 0.35 ATR | 2.643 % | 32.0793 | 49.7 % | 63.85 % | 70.16 % | 77.88 % | 83.55 % | 88.82 % |
| 0.5 ATR | 3.775 % | 31.7061 | 34.81 % | 50.25 % | 58.97 % | 69.39 % | 77.87 % | 84.41 % |
| 0.75 ATR | 5.663 % | 31.0841 | 17.4 % | 33.74 % | 43.65 % | 55.96 % | 67.51 % | 76.41 % |
| 1.0 ATR | 7.55 % | 30.4621 | 7.85 % | 21.85 % | 30.85 % | 44.34 % | 58.17 % | 69.74 % |
| 1.25 ATR | 9.438 % | 29.8402 | 3.72 % | 15.21 % | 22.68 % | 33.84 % | 48.93 % | 62.05 % |
| 1.5 ATR | 11.326 % | 29.2182 | 1.51 % | 9.67 % | 16.53 % | 26.36 % | 42.44 % | 55.69 % |
| 2.0 ATR | 15.101 % | 27.9743 | 0.3 % | 3.63 % | 8.67 % | 16.46 % | 30.56 % | 44.51 % |
| 2.5 ATR | 18.876 % | 26.7304 | 0.2 % | 1.51 % | 4.44 % | 10.0 % | 20.2 % | 32.62 % |
| 3.0 ATR | 22.651 % | 25.4864 | 0.2 % | 1.21 % | 2.62 % | 5.96 % | 14.72 % | 24.82 % |
| 4.0 ATR | 30.202 % | 22.9986 | 0.0 % | 0.6 % | 1.51 % | 2.83 % | 8.12 % | 14.97 % |
| 6.0 ATR | 45.302 % | 18.0229 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.58 ATR | 0.77 ATR | 0.93 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.28 ATR | 0.65 ATR | 0.73 ATR | 0.96 ATR | 1.18 ATR | 1.36 ATR | 1.92 ATR | 2.43 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.99 ATR | 1.28 ATR | 1.57 ATR | 1.82 ATR | 2.50 ATR | 3.31 ATR |
| **10 s.** | 0.57 ATR | 1.22 ATR | 1.40 ATR | 1.90 ATR | 2.27 ATR | 2.52 ATR | 3.71 ATR | 5.03 ATR |
| **20 s.** | 0.80 ATR | 1.75 ATR | 1.98 ATR | 2.48 ATR | 2.99 ATR | 3.49 ATR | 5.05 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.397–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.579–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.663 %, prix 31.084), p(touche) 33.74 % (en stress 88.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.728–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.663 %, prix 31.084), p(touche) 43.65 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.986–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.438 %, prix 29.8402), p(touche) 33.84 % (en stress 90.91 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.401–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.326 %, prix 29.2181), p(touche) 42.44 % (en stress 96.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.978–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (18.876 %, prix 26.7304), p(touche) 32.62 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.064 | EV/share : $0.160 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 15 % | T3 10 %
- Kelly (position) : f* 0.06 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 29.0 | bear 5.1 | side 65.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 148.0 (= 5 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.635% → cible +3.799% / stop −2.28%, p_fill 86%, n_eff≈91.7) : P(cible|rempli) **20%** · **EV/risk -0.192** (×p_fill ; si rempli -0.51% du capital)
  - **swing** (entrée dip −1.4% → cible +8.561% / stop −7.657%, p_fill 84%, n_eff≈97.1) : P(cible|rempli) **35%** · **EV/risk -0.016** (×p_fill ; si rempli -0.14% du capital)
  - **deep** (entrée dip −2.154% → cible +21.658% / stop −11.575%, p_fill 78%, n_eff≈86.9) : P(cible|rempli) **24%** · **EV/risk +0.144** (×p_fill ; si rempli +2.14% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→57% · +3.0%→40% · +5.0%→22% · +8.0%→8%
- Range intraday médian 5.72% (p90 9.37%) · excursion haute méd. +2.42% / basse méd. −2.68%
- Profil de vol intra : ouverture 3.884% vs midi 1.151% vs clôture 1.47% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.077)_ ; drift intra méd. -0.659% ; recovery-V 28%
- **σ réalisé intraday** 3.524% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 33.7346 (VA 33.3821–34.0871 ; dernier close 32.95)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 74% · **stop −4.61%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 50% (gap-down >1% 38% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.11% (p90 −2.79%) · haut méd +0.93% · range méd 2.16%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.55%) · haut méd +1.01% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.65% (p90 −3.98%) · haut méd +1.23% · range méd 3.58%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −4.46%) · haut méd +1.48% · range méd 4.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (116/159) · gap 42% · délai 0.0min · rebond 49% (64/116) (MFE +0.98%)
   - −1.0% : fill 30min 58% · séance 70% (109/159) · gap 38% · délai 0.0min · rebond 51% (60/109) (MFE +1.09%)
   - −1.5% : fill 30min 52% · séance 66% (100/159) · gap 28% · délai 0.0min · rebond 56% (62/100) (MFE +1.13%)
   - −2.0% : fill 30min 47% · séance 59% (87/159) · gap 23% · délai 0.1min · rebond 56% (54/87) (MFE +1.2%)
   - −3.0% : fill 30min 34% · séance 48% (73/159) · gap 11% · délai 2.7min · rebond 62% (43/73) (MFE +1.34%)
   - −4.0% : fill 30min 21% · séance 35% (54/159) · gap 5% · délai 12.5min · rebond 72% (36/54) (MFE +1.72%)
   - −5.0% : fill 30min 15% · séance 29% (44/159) · gap 2% · délai 21.5min · rebond 74% (31/44) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.69% (p90 −2.8%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.84%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.25%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=876 jambes) : jambe baissière méd −1.19% (p90 −2.78%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 98% (68/70) · rebond 39% (32/68)
      · −2.0% : fill 96% (64/70) · rebond 57% (37/64)
      · −3.0% : fill 86% (58/70) · rebond 60% (33/58)
      · −4.0% : fill 64% (44/70) · rebond 70% (29/44)
      · −5.0% : fill 53% (36/70) · rebond 71% (24/36)
   - **flat** (14 séances) :
      · −1.0% : fill 90% (13/14) · rebond 84% (10/13)
      · −2.0% : fill 57% (6/14) · rebond 47% (4/6)
      · −3.0% : fill 20% (3/14) · rebond 43% (2/3)
      · −4.0% : fill 7% (1/14) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/14) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 36% (28/75) · rebond 66% (18/28)
      · −2.0% : fill 21% (17/75) · rebond 58% (13/17)
      · −3.0% : fill 13% (12/75) · rebond 78% (8/12)
      · −4.0% : fill 11% (9/75) · rebond 81% (6/9)
      · −5.0% : fill 10% (8/75) · rebond 91% (7/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 67% si les 15 1res min sont vertes (78 cas) · 24% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 83% si début vert vs 11% si rouge (base 43% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **83%** · continue >prix actuel 59% ; creux résiduel méd -1.33% (q20 -2.94%) → **SL/trailing à −2.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +2.72% → **scale +1.67% / runner +2.72%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **11%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.93%** (au-delà de la MAE q10 -3.93%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.17% .. +4.1%] · haut q95 +5.04% · bas q05 -5.27%
   - 60min (n=160) : retour [-4.12% .. +4.96%] · haut q95 +6.21% · bas q05 -5.43%
   - 2h (n=160) : retour [-4.55% .. +5.52%] · haut q95 +7.12% · bas q05 -5.93%
   - 4h (n=160) : retour [-4.91% .. +6.39%] · haut q95 +7.24% · bas q05 -6.41%
   - 6h (n=160) : retour [-5.14% .. +6.41%] · haut q95 +7.8% · bas q05 -6.61%
   - session (n=160) : retour [-6.33% .. +6.37%] · haut q95 +7.95% · bas q05 -6.95%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.59%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-03 — SMCI earnings (J-1 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-03 — SMCI earnings (J-1 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-03 — SMCI earnings (J-1 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 33.4  _(momentum baissier)_
- **ADX** : 20.3  _(pas de tendance nette)_
- **MACD** : hist -0.209  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 47.8%
- **ATR** : 2.49 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.151  _(distribution)_
- **Vol ratio** : 1.09  _(volume normal)_
- **Choppiness** : 53.1  _(transition)_
- **MA** : MA20 36.78 · MA50 38.23 · MA200 32.67  _(prix < MA20)_
- **Dist MA** : MA20 -10.4% · MA50 -13.8% · MA200 +0.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (788149 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
