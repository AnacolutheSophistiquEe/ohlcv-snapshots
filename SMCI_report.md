# SMCI

**Generated** : 2026-10-30T01:24:37.586277+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $34.44  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (4 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $34.44 (+1.7% vs entrée) · entrée $33.86 · stop $33.12 · T1 $35.09 · R/R 1.66  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.17% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -3.7 % ≠ (strike 34.5 − spot 34.44)/spot = +0.2 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.170 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-29 : 34.44 · ATR Wilder 2.35 (6.81 %)_
- **Swing** : plage **31.53 → 29.78** (-8.44 % a -13.53 % sous la cloture, 0.75 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 30.92-32.04 (A) ; 29.68-30.65 (B). stop INDICATIF 27.33 (-8.22 % sous le bas ; sous le support 28.5-29.49 (- 0,5 ATR)).
- **Deep** : plage **29.78 → 24.41** (-13.53 % a -29.11 % sous la cloture, 2.29 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 29.68-30.65 (B) ; 28.5-29.49 (B) ; 26.86-27.75 (B) ; 25.13-26.06 (A). stop INDICATIF 22.21 (-9.04 % sous le bas ; sous le support 23.38-24.19 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 4.83 ATR sous le plus haut 20 s., RSI(2) 40.0. Limite **33.27** (seance suivante), stop catastrophe 23.89, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 32.58-33.64 (A, -2.32 %) ; 30.92-32.04 (A, -6.97 %) ; 29.68-30.65 (B, -11.0 %) ; 28.5-29.49 (B, -14.37 %) ; 26.86-27.75 (B, -19.43 %) ; 25.13-26.06 (A, -24.33 %)
- Resistances reelles au-dessus : 35.36-36.37 (A, 2.67 %) ; 36.8-37.85 (A, 6.85 %) ; 38.28-39.23 (A, 11.15 %) ; 39.47-40.13 (A, 14.61 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.06 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.84 %)** : le gap seul le franchit 1.038 % des séances (13 fois sur 1253).
   - exécution **3.418 pt plus bas** dans le cas TYPIQUE (médiane), 15.579 au p90, **18.211 au pire**
   - perte réelle **16.875 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 10.84 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0626 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 13 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.818 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5215** [0.4472 ; 0.595] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4083** [0.3574 ; 0.4607] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3595** [0.3103 ; 0.4111] _(largeur 10.1 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : deep (25.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-7.98 %** | CVaR **-12.63 %** | vol 5.95 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 3.73 % contre 6.20 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.54 % vs -16.84 % si l'on extrapolait par √5 _(rapport 1.041 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5352** (β de hausse 1.2166, asymétrie 1.2619) vs IWM — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.848× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 33.8266 sur atr_grid (0.25 ATR, 1.781 %) — p(stop avant cible) 0.8981 [0.86 ; 0.93], R/R 10.004, perte reelle 2.017 % (gap inclus), CVaR 6.004 %, EV -0.0362 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.1829 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 7.5 % du temps (< 15 %) meme a 10 seances : le R/R de 10.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.898, borne haute 0.927 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **6.1 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.202 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 19.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.96 ATR (stop 9.062 %) — p(stop avant cible) 0.4539 [0.40 ; 0.51], R/R 1.933, perte reelle 10.437 % (gap inclus), EV 0.5546 % — **REFUSE**
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.18 % > budget 6.10 %
   - 🔴 support a 2.74 ATR (stop 21.778 %) — p(stop avant cible) 0.1507 [0.12 ; 0.19], R/R 0.876, perte reelle 23.024 % (gap inclus), EV 0.9684 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.53 % > budget 6.10 %
      - ⚠ support DETECTE a 0.95 ATR du spot — compartiment <1, mesure a 48.9 % de casse (IC clusterise [0.458 ; 0.522] sur 1149 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 3.68 ATR (stop 28.456 %) — p(stop avant cible) 0.0825 [0.06 ; 0.12], R/R 0.702, perte reelle 28.727 % (gap inclus), EV 0.7544 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.90 % > budget 6.10 %
   - 🟢 support a 4.51 ATR (stop 34.351 %) — p(stop avant cible) 0.0565 [0.04 ; 0.08], R/R 0.585, perte reelle 34.504 % (gap inclus), EV 0.5624 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.52 % > budget 6.10 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.781 %) — p(stop avant cible) 0.8981 [0.86 ; 0.93], R/R 10.004, perte reelle 2.017 % (gap inclus), EV -0.0362 % — **REFUSE**
      - refuse : cible atteinte seulement 7.5 % du temps (< 15 %) meme a 10 seances : le R/R de 10.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.898, borne haute 0.927 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 7.5 % x 20.18 % + P(rien) 2.7 % x 9.62 % ne couvrent pas P(stop) 89.8 % x 2.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.562 %) — p(stop avant cible) 0.7688 [0.72 ; 0.81], R/R 5.012, perte reelle 4.026 % (gap inclus), EV 0.195 % — **REFUSE**
      - refuse : cible atteinte seulement 13.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.769, borne haute 0.811 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 10.29 % > budget 6.10 %
   - ⚪ atr_grid a 1.5 ATR (stop 10.686 %) — p(stop avant cible) 0.3921 [0.34 ; 0.44], R/R 1.661, perte reelle 12.148 % (gap inclus), EV 0.6124 % — **REFUSE**
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.64 % > budget 6.10 %
   - ⚪ atr_grid a 1.75 ATR (stop 12.467 %) — p(stop avant cible) 0.3173 [0.27 ; 0.37], R/R 1.436, perte reelle 14.052 % (gap inclus), EV 0.9454 % — **REFUSE**
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.30 % > budget 6.10 %
   - ⚪ atr_grid a 2.0 ATR (stop 14.248 %) — p(stop avant cible) 0.2564 [0.21 ; 0.30], R/R 1.26, perte reelle 16.022 % (gap inclus), EV 0.9525 % — **REFUSE**
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.24 % > budget 6.10 %
   - ⚪ atr_grid a 2.25 ATR (stop 16.029 %) — p(stop avant cible) 0.2298 [0.19 ; 0.28], R/R 1.125, perte reelle 17.937 % (gap inclus), EV 0.8621 % — **REFUSE**
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.33 % > budget 6.10 %
   - ⚪ atr_grid a 5.0 ATR (stop 35.621 %) — p(stop avant cible) 0.0538 [0.03 ; 0.08], R/R 0.565, perte reelle 35.701 % (gap inclus), EV 0.521 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.71 % > budget 6.10 %
   - ⚪ atr_grid a 5.5 ATR (stop 39.183 %) — p(stop avant cible) 0.0137 [0.01 ; 0.03], R/R 0.515, perte reelle 39.206 % (gap inclus), EV 0.7157 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.87 % > budget 6.10 %
   - ⚪ atr_grid a 6.0 ATR (stop 42.745 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 0.472, perte reelle 42.745 % (gap inclus), EV 0.7319 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.54 % > budget 6.10 %
   - ⚪ atr_grid a 6.5 ATR (stop 46.307 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.428, perte reelle 47.157 % (gap inclus), EV 0.726 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.67 % > budget 6.10 %
   - ⚪ atr_grid a 7.0 ATR (stop 49.869 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.38, perte reelle 53.124 % (gap inclus), EV 0.7168 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.82 % > budget 6.10 %
   - ⚪ atr_grid a 7.5 ATR (stop 53.431 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.363, perte reelle 55.543 % (gap inclus), EV 0.72 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.83 % > budget 6.10 %
   - ⚪ atr_grid a 8.0 ATR (stop 56.994 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.354, perte reelle 56.994 % (gap inclus), EV 0.7204 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.75 % > budget 6.10 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 34.44, ATR14 2.4536 (7.124 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.347 ATR = 2.472 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.356 % | 34.3173 | 90.84 % | 93.65 % | 95.06 % | 95.55 % | 96.75 % | 97.95 % |
| 0.1 ATR | 0.712 % | 34.1946 | 82.28 % | 87.6 % | 89.61 % | 91.51 % | 93.29 % | 95.28 % |
| 0.15 ATR | 1.069 % | 34.072 | 75.23 % | 82.56 % | 85.47 % | 88.68 % | 91.06 % | 94.05 % |
| 0.2 ATR | 1.425 % | 33.9493 | 68.28 % | 77.72 % | 81.03 % | 86.25 % | 89.63 % | 92.81 % |
| 0.25 ATR | 1.781 % | 33.8266 | 62.13 % | 73.08 % | 76.79 % | 82.91 % | 87.7 % | 91.27 % |
| 0.35 ATR | 2.493 % | 33.5812 | 49.65 % | 63.81 % | 70.23 % | 77.86 % | 83.54 % | 88.81 % |
| 0.5 ATR | 3.562 % | 33.2132 | 34.84 % | 50.2 % | 59.03 % | 69.46 % | 77.85 % | 84.39 % |
| 0.75 ATR | 5.343 % | 32.5998 | 17.42 % | 33.77 % | 43.69 % | 56.02 % | 67.48 % | 76.39 % |
| 1.0 ATR | 7.124 % | 31.9864 | 7.85 % | 21.88 % | 30.88 % | 44.39 % | 58.13 % | 69.71 % |
| 1.25 ATR | 8.905 % | 31.373 | 3.73 % | 15.22 % | 22.7 % | 33.87 % | 48.88 % | 62.01 % |
| 1.5 ATR | 10.686 % | 30.7596 | 1.51 % | 9.68 % | 16.55 % | 26.39 % | 42.48 % | 55.65 % |
| 2.0 ATR | 14.248 % | 29.5329 | 0.3 % | 3.63 % | 8.68 % | 16.48 % | 30.59 % | 44.46 % |
| 2.5 ATR | 17.81 % | 28.3061 | 0.2 % | 1.51 % | 4.44 % | 10.01 % | 20.22 % | 32.55 % |
| 3.0 ATR | 21.373 % | 27.0793 | 0.2 % | 1.21 % | 2.62 % | 5.97 % | 14.74 % | 24.74 % |
| 4.0 ATR | 28.497 % | 24.6257 | 0.0 % | 0.6 % | 1.51 % | 2.83 % | 8.13 % | 14.89 % |
| 6.0 ATR | 42.745 % | 19.7186 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.58 ATR | 0.77 ATR | 0.93 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.28 ATR | 0.65 ATR | 0.73 ATR | 0.96 ATR | 1.18 ATR | 1.36 ATR | 1.92 ATR | 2.43 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.99 ATR | 1.28 ATR | 1.57 ATR | 1.82 ATR | 2.50 ATR | 3.31 ATR |
| **10 s.** | 0.57 ATR | 1.22 ATR | 1.40 ATR | 1.90 ATR | 2.27 ATR | 2.52 ATR | 3.72 ATR | 5.03 ATR |
| **20 s.** | 0.80 ATR | 1.75 ATR | 1.98 ATR | 2.48 ATR | 2.98 ATR | 3.48 ATR | 5.05 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.397–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.579–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.343 %, prix 32.5999), p(touche) 33.77 % (en stress 88.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.729–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.343 %, prix 32.5999), p(touche) 43.69 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.987–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.905 %, prix 31.3731), p(touche) 33.87 % (en stress 90.91 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.402–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.686 %, prix 30.7597), p(touche) 42.48 % (en stress 96.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.976–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.81 %, prix 28.3062), p(touche) 32.55 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.015 | EV/share : $-0.011 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 47.5 | bear 5.0 | side 47.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 154.0 (= 5 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.693% → cible +3.623% / stop −2.174%, p_fill 68%, n_eff≈72.5) : P(cible|rempli) **17%** · **EV/risk -0.154** (×p_fill ; si rempli -0.49% du capital)
  - **swing** (entrée dip −3.716% → cible +8.272% / stop −7.399%, p_fill 54%, n_eff≈63.3) : P(cible|rempli) **47%** · **EV/risk +0.053** (×p_fill ; si rempli +0.72% du capital)
  - **deep** (entrée dip −5.744% → cible +20.831% / stop −11.337%, p_fill 49%, n_eff≈56.0) : P(cible|rempli) **23%** · **EV/risk +0.109** (×p_fill ; si rempli +2.50% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.55 · part idiosyncratique 0.45
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-03 — SMCI earnings (J-3 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-03 — SMCI earnings (J-3 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 32.8  _(momentum baissier)_
- **ADX** : 20.5  _(pas de tendance nette)_
- **MACD** : hist -0.196  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 48.8%
- **ATR** : 2.45 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.174  _(distribution)_
- **Vol ratio** : 0.58  _(volume atone)_
- **Choppiness** : 45.1  _(transition)_
- **MA** : MA20 37.31 · MA50 38.3 · MA200 32.64  _(prix < MA20)_
- **Dist MA** : MA20 -7.7% · MA50 -10.1% · MA200 +5.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (788818 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
