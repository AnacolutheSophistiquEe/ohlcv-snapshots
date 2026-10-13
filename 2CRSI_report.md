# AL2SI

**Generated** : 2026-10-13T21:49:07.794329+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €28.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €28.30 (+0.5% vs entrée) · entrée €28.17 · stop €26.99 · T1 €30.53 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-13 : 28.3 · ATR Wilder 2.09 (7.4 %)_
- **Swing** : plage **25.93 → 24.42** (-8.38 % a -13.7 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 25.92-26.7 (B) ; 25.0-25.32 (C). stop INDICATIF 21.55 (-11.75 % sous le bas ; sous le support 22.6-23.55 (- 0,5 ATR)).
- **Deep** : plage **24.42 → 20.77** (-13.7 % a -26.61 % sous la cloture, 1.74 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 22.6-23.55 (A) ; 20.1-21.05 (A). stop INDICATIF 18.68 (-10.08 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (1.47 ATR sous le plus haut 20 s., RSI(2) 67.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 25.92-26.7 (B, -5.65 %) ; 25.0-25.32 (C, -10.53 %) ; 22.6-23.55 (A, -16.78 %) ; 20.1-21.05 (A, -25.62 %) ; 16.1-16.65 (A, -41.17 %) ; 14.2-15.0 (A, -47.0 %)
- Resistances reelles au-dessus : 30.0-30.94 (A, 6.01 %) ; 31.38-31.54 (B, 10.88 %) ; 33.02-33.02 (C, 16.68 %) ; 34.5-35.02 (A, 21.91 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.88 %)** : le gap seul le franchit 0.859 % des séances (11 fois sur 1280).
   - exécution **3.868 pt plus bas** dans le cas TYPIQUE (médiane), 19.285 au p90, **30.237 au pire**
   - perte réelle **16.422 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 7.88 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0734 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3811** [0.3112 ; 0.4549] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.4346** [0.3831 ; 0.4872] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3579** [0.3087 ; 0.4094] _(largeur 10.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.41 %** | CVaR **-12.97 %** | vol 6.53 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 4.26 % contre 7.25 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -14.08 % si l'on extrapolait par √5 _(rapport 1.048 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2079** (β de hausse 0.9375, asymétrie 1.2883) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.091× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 26.8043 sur atr_grid (0.75 ATR, 5.285 %) — p(stop avant cible) 0.6796 [0.63 ; 0.73], R/R 4.191, perte reelle 5.692 % (gap inclus), CVaR 10.817 %, EV 1.1066 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.322 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.680, borne haute 0.727 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 38.9 % de la queue et il ne reste que -829.92 EUR a partager. Prix du risque -0.253 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.06 ATR (stop 2.433 %) — p(stop avant cible) 0.839 [0.80 ; 0.87], R/R 9.015, perte reelle 2.646 % (gap inclus), EV 0.6142 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 9.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.839, borne haute 0.875 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.06 ATR du spot — compartiment <1, mesure a 46.6 % de casse (IC clusterise [0.434 ; 0.497] sur 1119 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ swing_based a 1.16 ATR (stop 10.202 %) — p(stop avant cible) 0.3917 [0.34 ; 0.44], R/R 2.041, perte reelle 11.684 % (gap inclus), EV 2.5604 % — **REFUSE**
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.78 % > budget 12.00 %
   - 🟢 support a 1.65 ATR (stop 13.669 %) — p(stop avant cible) 0.268 [0.22 ; 0.32], R/R 1.424, perte reelle 16.747 % (gap inclus), EV 2.5305 % — **REFUSE**
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.16 % > budget 12.00 %
   - 🟢 support a 2.86 ATR (stop 22.15 %) — p(stop avant cible) 0.1341 [0.10 ; 0.17], R/R 0.839, perte reelle 28.447 % (gap inclus), EV 2.0815 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.99 % > budget 12.00 %
   - ⚪ atr_grid a 0.5 ATR (stop 3.523 %) — p(stop avant cible) 0.7585 [0.71 ; 0.80], R/R 6.255, perte reelle 3.813 % (gap inclus), EV 1.1783 % — **REFUSE**
      - refuse : cible atteinte seulement 14.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.758, borne haute 0.801 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 5.285 %) — p(stop avant cible) 0.6796 [0.63 ; 0.73], R/R 4.191, perte reelle 5.692 % (gap inclus), EV 1.1066 % — **REFUSE**
      - refuse : p_stop_first 0.680, borne haute 0.727 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 2.25 ATR (stop 15.856 %) — p(stop avant cible) 0.2346 [0.19 ; 0.28], R/R 1.248, perte reelle 19.118 % (gap inclus), EV 2.3315 % — **REFUSE**
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.09 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 17.617 %) — p(stop avant cible) 0.2107 [0.17 ; 0.26], R/R 1.089, perte reelle 21.9 % (gap inclus), EV 1.9941 % — **REFUSE**
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.18 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 24.664 %) — p(stop avant cible) 0.0948 [0.07 ; 0.13], R/R 0.74, perte reelle 32.247 % (gap inclus), EV 2.3836 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.01 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 28.188 %) — p(stop avant cible) 0.08 [0.05 ; 0.11], R/R 0.68, perte reelle 35.063 % (gap inclus), EV 2.3469 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.19 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 31.711 %) — p(stop avant cible) 0.077 [0.05 ; 0.11], R/R 0.643, perte reelle 37.117 % (gap inclus), EV 2.2419 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.04 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 35.235 %) — p(stop avant cible) 0.0549 [0.03 ; 0.08], R/R 0.584, perte reelle 40.826 % (gap inclus), EV 2.5351 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.38 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 38.758 %) — p(stop avant cible) 0.0413 [0.02 ; 0.07], R/R 0.546, perte reelle 43.678 % (gap inclus), EV 2.6856 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.29 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 42.282 %) — p(stop avant cible) 0.0335 [0.02 ; 0.06], R/R 0.525, perte reelle 45.436 % (gap inclus), EV 2.9161 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.58 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 45.805 %) — p(stop avant cible) 0.0294 [0.02 ; 0.05], R/R 0.509, perte reelle 46.823 % (gap inclus), EV 2.9252 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.42 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 49.329 %) — p(stop avant cible) 0.0294 [0.02 ; 0.05], R/R 0.47, perte reelle 50.718 % (gap inclus), EV 2.8107 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 52.852 %) — p(stop avant cible) 0.0294 [0.02 ; 0.05], R/R 0.394, perte reelle 60.497 % (gap inclus), EV 2.5232 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.47 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 56.376 %) — p(stop avant cible) 0.0259 [0.01 ; 0.05], R/R 0.377, perte reelle 63.341 % (gap inclus), EV 2.4734 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.36 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 28.3, ATR14 1.9943 (7.047 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.398 ATR = 2.805 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.352 % | 28.2003 | 86.96 % | 90.48 % | 92.93 % | 94.39 % | 95.55 % | 97.1 % |
| 0.1 ATR | 0.705 % | 28.1006 | 82.45 % | 86.95 % | 90.28 % | 92.13 % | 94.07 % | 96.2 % |
| 0.15 ATR | 1.057 % | 28.0009 | 78.33 % | 83.32 % | 87.23 % | 88.98 % | 92.19 % | 95.1 % |
| 0.2 ATR | 1.409 % | 27.9011 | 72.55 % | 79.2 % | 83.4 % | 85.83 % | 89.81 % | 92.91 % |
| 0.25 ATR | 1.762 % | 27.8014 | 66.57 % | 74.58 % | 79.27 % | 82.48 % | 87.54 % | 91.31 % |
| 0.35 ATR | 2.466 % | 27.602 | 54.51 % | 65.55 % | 71.12 % | 75.69 % | 82.59 % | 87.81 % |
| 0.5 ATR | 3.523 % | 27.3029 | 40.49 % | 53.78 % | 61.98 % | 68.8 % | 78.04 % | 85.41 % |
| 0.75 ATR | 5.285 % | 26.8043 | 22.75 % | 37.68 % | 47.54 % | 55.81 % | 67.26 % | 76.82 % |
| 1.0 ATR | 7.047 % | 26.3057 | 12.84 % | 25.02 % | 33.99 % | 44.49 % | 57.37 % | 68.33 % |
| 1.25 ATR | 8.809 % | 25.8071 | 7.45 % | 17.66 % | 24.75 % | 36.61 % | 50.45 % | 61.94 % |
| 1.5 ATR | 10.57 % | 25.3086 | 3.63 % | 11.38 % | 17.49 % | 29.04 % | 43.13 % | 55.54 % |
| 2.0 ATR | 14.094 % | 24.3114 | 0.88 % | 5.2 % | 9.72 % | 16.93 % | 31.45 % | 43.76 % |
| 2.5 ATR | 17.617 % | 23.3143 | 0.1 % | 2.16 % | 4.62 % | 9.84 % | 21.27 % | 33.47 % |
| 3.0 ATR | 21.141 % | 22.3171 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 15.23 % | 25.97 % |
| 4.0 ATR | 28.188 % | 20.3229 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.28 % |
| 6.0 ATR | 42.282 % | 16.3343 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.03 ATR | 1.24 ATR | 1.41 ATR | 1.98 ATR | 2.46 ATR |
| **5 s.** | 0.36 ATR | 0.88 ATR | 0.99 ATR | 1.37 ATR | 1.67 ATR | 1.87 ATR | 2.49 ATR | 3.42 ATR |
| **10 s.** | 0.57 ATR | 1.26 ATR | 1.44 ATR | 1.93 ATR | 2.32 ATR | 2.60 ATR | 3.78 ATR | 5.11 ATR |
| **20 s.** | 0.80 ATR | 1.74 ATR | 1.95 ATR | 2.53 ATR | 3.11 ATR | 3.69 ATR | 5.57 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.452–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.523 %, prix 27.303), p(touche) 40.49 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (91.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.636–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.285 %, prix 26.8043), p(touche) 37.68 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.797–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.047 %, prix 26.3057), p(touche) 33.99 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.989–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.047 %, prix 26.3057), p(touche) 44.49 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.436–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.57 %, prix 25.3087), p(touche) 43.13 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.947–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.094 %, prix 24.3114), p(touche) 43.76 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 74.7 | bear 20.3 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 283.0 (= 10 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.452% → cible +8.374% / stop −4.187%, p_fill 85%, n_eff≈90.9) : P(cible|rempli) **8%** · **EV/risk -0.287** (×p_fill ; si rempli -1.41% du capital)
  - **swing** (entrée dip −0.834% → cible +8.785% / stop −7.106%, p_fill 85%, n_eff≈99.2) : P(cible|rempli) **31%** · **EV/risk -0.166** (×p_fill ; si rempli -1.39% du capital)
  - **deep** (entrée dip −1.139% → cible +17.312% / stop −10.693%, p_fill 86%, n_eff≈95.5) : P(cible|rempli) **24%** · **EV/risk -0.016** (×p_fill ; si rempli -0.20% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.1 · part idiosyncratique 0.91
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.5  _(momentum baissier)_
- **ADX** : 16.9  _(pas de tendance nette)_
- **MACD** : hist -0.04  _(pas de croisement recent)_
- **BB** : %B 0.56 · largeur 26.5%
- **ATR** : 1.99 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.076  _(distribution)_
- **Vol ratio** : 1.26  _(volume normal)_
- **Choppiness** : 50.2  _(transition)_
- **MA** : MA20 27.89 · MA50 27.66 · MA200 28.74  _(prix > MA20)_
- **Dist MA** : MA20 +1.5% · MA50 +2.3% · MA200 -1.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (892884 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
