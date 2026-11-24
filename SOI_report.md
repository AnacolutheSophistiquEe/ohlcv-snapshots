# SOI

**Generated** : 2026-11-24T01:11:45.856459+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 8.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €101.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €101.60 (+3.2% vs entrée) · entrée €98.42 · stop €94.45 · T1 €106.38 · R/R 2.01  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-23 : 101.6 · ATR Wilder 10.17 (10.01 %)_
- **Swing** : plage **86.06 → 78.16** (-15.29 % a -23.07 % sous la cloture, 0.78 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 84.75-89.15 (A) ; 77.85-82.4 (A). stop INDICATIF 67.47 (-13.69 % sous le bas ; sous le support 72.55-72.9 (- 0,5 ATR)).
- **Deep** : plage **78.16 → 44.38** (-23.07 % a -56.32 % sous la cloture, 3.32 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 77.85-82.4 (A) ; 72.55-72.9 (C) ; 64.2-68.5 (B) ; 58.94-63.5 (B) ; 53.65-57.9 (B) ; 48.55-50.38 (A) ; 43.14-47.59 (A). stop INDICATIF 30.93 (-30.31 % sous le bas ; sous le support 36.01-41.03 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.3 ATR sous le plus haut 20 s., RSI(2) 55.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 91.65-96.02 (A, -5.49 %) ; 84.75-89.15 (A, -12.25 %) ; 77.85-82.4 (A, -18.9 %) ; 72.55-72.9 (C, -28.25 %) ; 64.2-68.5 (B, -32.58 %) ; 58.94-63.5 (B, -37.5 %)
- Resistances reelles au-dessus : 104.8-109.55 (A, 3.15 %) ; 110.4-114.9 (A, 8.66 %) ; 116.8-121.8 (A, 14.96 %) ; 123.3-128.0 (A, 21.36 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.53 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (17.45 %)** : le gap seul le franchit 0.156 % des séances (2 fois sur 1280).
   - exécution **6.556 pt plus bas** dans le cas TYPIQUE (médiane), 10.786 au p90, **11.844 au pire**
   - perte réelle **24.006 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 17.45 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0102 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.876 % | p01 -5.662 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3409** [0.2734 ; 0.4137] _(largeur 14.0 pt, n_eff 173.1)_
   - swing : **0.2664** [0.2219 ; 0.3148] _(largeur 9.3 pt, n_eff 345.8)_
   - deep : **0.257** [0.2131 ; 0.3049] _(largeur 9.2 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (29.2 pt), deep (28.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-9.83 %** | CVaR **-14.35 %** | vol 6.54 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.02 % contre 6.41 % aujourd'hui, rapport 0.47)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.27 % vs -12.18 % si l'on extrapolait par √5 _(rapport 1.09 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0894** (β de hausse 1.5686, asymétrie 0.6945) vs FCHI — 623 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.184× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 96.2289 sur atr_grid (0.5 ATR, 5.286 %) — p(stop avant cible) 0.6649 [0.61 ; 0.71], R/R 4.848, perte reelle 5.669 % (gap inclus), CVaR 9.515 %, EV 1.683 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4552 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 12.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.665, borne haute 0.713 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.85 ATR (stop 12.951 %) — p(stop avant cible) 0.3883 [0.34 ; 0.44], R/R 2.054, perte reelle 13.377 % (gap inclus), EV 1.0883 % — **REFUSE**
      - refuse : R/R 2.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.26 % > budget 12.00 %
   - 🟢 support a 1.18 ATR (stop 16.486 %) — p(stop avant cible) 0.2927 [0.25 ; 0.34], R/R 1.634, perte reelle 16.82 % (gap inclus), EV 1.2565 % — **REFUSE**
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.44 % > budget 12.00 %
   - 🟢 support a 1.86 ATR (stop 23.612 %) — p(stop avant cible) 0.1357 [0.10 ; 0.17], R/R 1.152, perte reelle 23.845 % (gap inclus), EV 1.3497 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.24 % > budget 12.00 %
   - 🟢 support a 3.39 ATR (stop 39.852 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.687, perte reelle 40.026 % (gap inclus), EV 1.5215 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.14 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 2.643 %) — p(stop avant cible) 0.8078 [0.76 ; 0.85], R/R 9.846, perte reelle 2.791 % (gap inclus), EV 1.3046 % — **REFUSE**
      - refuse : cible atteinte seulement 8.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.808, borne haute 0.847 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 5.286 %) — p(stop avant cible) 0.6649 [0.61 ; 0.71], R/R 4.848, perte reelle 5.669 % (gap inclus), EV 1.683 % — **REFUSE**
      - refuse : cible atteinte seulement 12.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.665, borne haute 0.713 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 2.5 ATR (stop 26.432 %) — p(stop avant cible) 0.0942 [0.07 ; 0.13], R/R 1.032, perte reelle 26.638 % (gap inclus), EV 1.3092 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.82 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 29.076 %) — p(stop avant cible) 0.0391 [0.02 ; 0.06], R/R 0.94, perte reelle 29.228 % (gap inclus), EV 1.5118 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.37 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 31.719 %) — p(stop avant cible) 0.0233 [0.01 ; 0.04], R/R 0.866, perte reelle 31.726 % (gap inclus), EV 1.5264 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.97 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 42.292 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.65, perte reelle 42.292 % (gap inclus), EV 1.5499 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.53 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 47.578 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.578, perte reelle 47.578 % (gap inclus), EV 1.5646 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.27 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 52.865 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.52, perte reelle 52.865 % (gap inclus), EV 1.5646 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.27 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 58.151 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.473, perte reelle 58.151 % (gap inclus), EV 1.5646 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.27 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 63.438 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.433, perte reelle 63.438 % (gap inclus), EV 1.5646 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.27 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 68.724 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.4, perte reelle 68.724 % (gap inclus), EV 1.5646 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.27 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 74.011 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.371, perte reelle 74.011 % (gap inclus), EV 1.5646 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.27 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 79.297 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.347, perte reelle 79.297 % (gap inclus), EV 1.5646 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.27 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 84.584 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.325, perte reelle 84.584 % (gap inclus), EV 1.5646 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.27 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 101.6, ATR14 10.7421 (10.573 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 3.785 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.529 % | 101.0629 | 91.18 % | 94.31 % | 95.58 % | 96.65 % | 97.73 % | 98.7 % |
| 0.1 ATR | 1.057 % | 100.5258 | 84.51 % | 89.89 % | 91.85 % | 94.39 % | 96.04 % | 97.2 % |
| 0.15 ATR | 1.586 % | 99.9887 | 77.45 % | 84.89 % | 87.43 % | 90.75 % | 93.47 % | 95.2 % |
| 0.2 ATR | 2.115 % | 99.4516 | 68.73 % | 79.78 % | 83.5 % | 87.8 % | 91.3 % | 93.41 % |
| 0.25 ATR | 2.643 % | 98.9145 | 62.45 % | 75.96 % | 80.06 % | 86.12 % | 90.01 % | 92.91 % |
| 0.35 ATR | 3.701 % | 97.8402 | 50.78 % | 67.42 % | 73.18 % | 81.1 % | 85.86 % | 90.41 % |
| 0.5 ATR | 5.286 % | 96.2289 | 36.27 % | 55.84 % | 62.97 % | 73.52 % | 81.31 % | 87.81 % |
| 0.75 ATR | 7.93 % | 93.5434 | 16.96 % | 35.13 % | 46.46 % | 58.37 % | 72.9 % | 81.12 % |
| 1.0 ATR | 10.573 % | 90.8579 | 8.14 % | 23.55 % | 34.09 % | 47.34 % | 64.99 % | 75.92 % |
| 1.25 ATR | 13.216 % | 88.1723 | 4.22 % | 15.9 % | 25.64 % | 37.99 % | 57.47 % | 71.03 % |
| 1.5 ATR | 15.859 % | 85.4868 | 2.35 % | 10.79 % | 18.76 % | 30.51 % | 49.95 % | 65.13 % |
| 2.0 ATR | 21.146 % | 80.1157 | 0.59 % | 4.61 % | 9.33 % | 18.6 % | 36.1 % | 54.55 % |
| 2.5 ATR | 26.432 % | 74.7446 | 0.29 % | 2.55 % | 5.21 % | 12.3 % | 25.22 % | 46.65 % |
| 3.0 ATR | 31.719 % | 69.3736 | 0.2 % | 0.88 % | 2.75 % | 7.68 % | 17.9 % | 38.46 % |
| 4.0 ATR | 42.292 % | 58.6314 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 10.29 % | 24.58 % |
| 6.0 ATR | 63.438 % | 37.1471 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.69 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.63 ATR | 0.80 ATR | 0.97 ATR | 1.12 ATR | 1.56 ATR | 1.97 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.78 ATR | 1.03 ATR | 1.27 ATR | 1.46 ATR | 1.96 ATR | 2.54 ATR |
| **5 s.** | 0.47 ATR | 0.94 ATR | 1.06 ATR | 1.42 ATR | 1.73 ATR | 1.94 ATR | 2.75 ATR | 3.65 ATR |
| **10 s.** | 0.69 ATR | 1.50 ATR | 1.68 ATR | 2.14 ATR | 2.52 ATR | 2.86 ATR | 4.10 ATR | 5.81 ATR |
| **20 s.** | 1.05 ATR | 2.29 ATR | 2.60 ATR | 3.39 ATR | 3.97 ATR | 4.77 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.41 ATR au-dessus du haut de la grille, 0.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (70.6 % des re-echantillons)
- **2 seance(s)** : plage utile VIDE (borne basse 0.631 ATR au-dessus du haut de la grille, 0.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.78 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile VIDE (borne basse 1.063 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.679 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.601 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.2 | side 77.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.125% → cible +8.083% / stop −4.041%, p_fill 51%, n_eff≈54.5) : P(cible|rempli) **2%** · **EV/risk -0.037** (×p_fill ; si rempli -0.29% du capital)
  - **swing** (entrée dip −6.877% → cible +12.435% / stop −11.353%, p_fill 32%, n_eff≈39.2) : P(cible|rempli) **30%** · **EV/risk -0.041** (×p_fill ; si rempli -1.44% du capital)
  - **deep** (entrée dip −10.62% → cible +29.408% / stop −17.745%, p_fill 34%, n_eff≈40.4) : P(cible|rempli) **12%** · **EV/risk -0.036** (×p_fill ; si rempli -1.87% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.49 · part idiosyncratique 0.51
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.4  _(momentum baissier)_
- **ADX** : 22.0  _(pas de tendance nette)_
- **MACD** : hist 0.718  _(bullish_recent)_
- **BB** : %B 0.37 · largeur 46.1%
- **ATR** : 10.74 (73.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.131  _(distribution)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 52.8  _(transition)_
- **MA** : MA20 107.85 · MA50 129.19 · MA200 109.86  _(prix < MA20)_
- **Dist MA** : MA20 -5.8% · MA50 -21.4% · MA200 -7.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (675964 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
