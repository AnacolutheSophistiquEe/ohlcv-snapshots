# AL2SI

**Generated** : 2026-10-26T01:11:56.602367+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €26.62  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €26.62 (+2.2% vs entrée) · entrée €26.04 · stop €24.01 · T1 €29.09 · R/R 1.5  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.088 _(réel 5 s)_ (GBM 0.12) · ¼-Kelly 0.023 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 26.62 · ATR Wilder 1.88 (7.05 %)_
- **Swing** : plage **24.49 → 23.15** (-8.02 % a -13.05 % sous la cloture, 0.71 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 22.6-23.38 (A). stop INDICATIF 21.27 (-8.11 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **23.15 → 19.86** (-13.05 % a -25.39 % sous la cloture, 1.75 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 22.6-23.38 (A) ; 20.1-20.8 (B). stop INDICATIF 17.99 (-9.45 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (1.99 ATR sous le plus haut 20 s., RSI(2) 27.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 25.0-25.4 (A, -4.58 %) ; 22.6-23.38 (A, -12.17 %) ; 20.1-20.8 (B, -21.86 %) ; 16.1-16.65 (A, -37.45 %) ; 14.2-15.0 (A, -43.65 %) ; 13.0-13.24 (B, -50.26 %)
- Resistances reelles au-dessus : 28.18-29.0 (B, 5.86 %) ; 30.0-30.8 (A, 12.7 %) ; 30.94-31.54 (B, 16.23 %) ; 33.02-33.02 (C, 24.04 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.52 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.82 %)** : le gap seul le franchit 0.547 % des séances (7 fois sur 1280).
   - exécution **8.14 pt plus bas** dans le cas TYPIQUE (médiane), 21.726 au p90, **28.297 au pire**
   - perte réelle **20.706 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 9.82 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0595 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.401 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4905** [0.4167 ; 0.5646] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4331** [0.3816 ; 0.4857] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3162** [0.2689 ; 0.3666] _(largeur 9.8 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.41 %** | CVaR **-12.97 %** | vol 6.53 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 4.38 % contre 7.27 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -14.08 % si l'on extrapolait par √5 _(rapport 1.048 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2078** (β de hausse 0.9561, asymétrie 1.2633) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.024× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 25.6025 sur atr_grid (0.5 ATR, 3.822 %) — p(stop avant cible) 0.769 [0.72 ; 0.81], R/R 6.2, perte reelle 4.254 % (gap inclus), CVaR 10.465 %, EV 0.6628 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6787 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 6.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.769, borne haute 0.811 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.8 ATR (stop 8.952 %) — p(stop avant cible) 0.4972 [0.44 ; 0.55], R/R 2.6, perte reelle 10.144 % (gap inclus), EV 1.5452 % — **REFUSE**
      - refuse : R/R 2.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.81 % > budget 12.00 %
      - ⚠ support DETECTE a 0.52 ATR du spot — compartiment <1, mesure a 47.8 % de casse (IC clusterise [0.449 ; 0.507] sur 1237 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 11.467 %) — p(stop avant cible) 0.352 [0.30 ; 0.40], R/R 1.997, perte reelle 13.208 % (gap inclus), EV 2.3669 % — **REFUSE**
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.71 % > budget 12.00 %
   - 🟢 support a 1.98 ATR (stop 17.968 %) — p(stop avant cible) 0.2012 [0.16 ; 0.25], R/R 1.173, perte reelle 22.493 % (gap inclus), EV 1.8651 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.76 % > budget 12.00 %
   - 🟢 support a 3.2 ATR (stop 27.36 %) — p(stop avant cible) 0.0875 [0.06 ; 0.12], R/R 0.771, perte reelle 34.202 % (gap inclus), EV 2.3021 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.33 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.911 %) — p(stop avant cible) 0.8687 [0.83 ; 0.90], R/R 12.55, perte reelle 2.102 % (gap inclus), EV 0.6705 % — **REFUSE**
      - refuse : cible atteinte seulement 7.6 % du temps (< 15 %) meme a 10 seances : le R/R de 12.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.869, borne haute 0.901 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.822 %) — p(stop avant cible) 0.769 [0.72 ; 0.81], R/R 6.2, perte reelle 4.254 % (gap inclus), EV 0.6628 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 6.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.769, borne haute 0.811 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 2.5 ATR (stop 19.112 %) — p(stop avant cible) 0.1781 [0.14 ; 0.22], R/R 1.055, perte reelle 24.994 % (gap inclus), EV 1.8903 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.28 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 21.023 %) — p(stop avant cible) 0.14 [0.11 ; 0.18], R/R 0.954, perte reelle 27.637 % (gap inclus), EV 2.0924 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.28 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 30.579 %) — p(stop avant cible) 0.0786 [0.05 ; 0.11], R/R 0.723, perte reelle 36.474 % (gap inclus), EV 2.2671 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.85 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 34.401 %) — p(stop avant cible) 0.0595 [0.04 ; 0.09], R/R 0.66, perte reelle 39.967 % (gap inclus), EV 2.3353 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.03 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 38.223 %) — p(stop avant cible) 0.043 [0.03 ; 0.07], R/R 0.612, perte reelle 43.124 % (gap inclus), EV 2.6823 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.32 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 42.045 %) — p(stop avant cible) 0.0355 [0.02 ; 0.06], R/R 0.585, perte reelle 45.056 % (gap inclus), EV 2.8941 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.97 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 45.868 %) — p(stop avant cible) 0.0281 [0.01 ; 0.05], R/R 0.563, perte reelle 46.855 % (gap inclus), EV 2.8968 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.98 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 49.69 %) — p(stop avant cible) 0.0281 [0.01 ; 0.05], R/R 0.501, perte reelle 52.645 % (gap inclus), EV 2.7341 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.23 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 53.512 %) — p(stop avant cible) 0.0247 [0.01 ; 0.05], R/R 0.416, perte reelle 63.341 % (gap inclus), EV 2.4693 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.49 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 57.335 %) — p(stop avant cible) 0.0247 [0.01 ; 0.05], R/R 0.416, perte reelle 63.341 % (gap inclus), EV 2.4693 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.49 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 61.157 %) — p(stop avant cible) 0.0247 [0.01 ; 0.05], R/R 0.416, perte reelle 63.478 % (gap inclus), EV 2.466 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.56 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 26.62, ATR14 2.035 (7.645 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.401 ATR = 3.065 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.382 % | 26.5183 | 87.25 % | 90.78 % | 93.03 % | 94.49 % | 95.55 % | 97.2 % |
| 0.1 ATR | 0.764 % | 26.4165 | 82.65 % | 87.14 % | 90.28 % | 92.22 % | 94.07 % | 96.3 % |
| 0.15 ATR | 1.147 % | 26.3148 | 78.43 % | 83.51 % | 87.33 % | 89.07 % | 92.19 % | 95.2 % |
| 0.2 ATR | 1.529 % | 26.213 | 72.75 % | 79.39 % | 83.6 % | 86.02 % | 89.81 % | 93.01 % |
| 0.25 ATR | 1.911 % | 26.1113 | 66.76 % | 74.78 % | 79.47 % | 82.68 % | 87.54 % | 91.41 % |
| 0.35 ATR | 2.676 % | 25.9078 | 54.71 % | 65.65 % | 71.22 % | 75.89 % | 82.69 % | 87.91 % |
| 0.5 ATR | 3.822 % | 25.6025 | 40.78 % | 53.88 % | 62.08 % | 69.09 % | 78.24 % | 85.51 % |
| 0.75 ATR | 5.733 % | 25.0938 | 22.75 % | 37.88 % | 47.64 % | 55.91 % | 67.46 % | 76.92 % |
| 1.0 ATR | 7.645 % | 24.585 | 12.75 % | 25.02 % | 33.99 % | 44.39 % | 57.47 % | 68.63 % |
| 1.25 ATR | 9.556 % | 24.0763 | 7.45 % | 17.76 % | 24.85 % | 36.71 % | 50.54 % | 62.24 % |
| 1.5 ATR | 11.467 % | 23.5675 | 3.63 % | 11.38 % | 17.49 % | 29.13 % | 43.32 % | 55.94 % |
| 2.0 ATR | 15.289 % | 22.55 | 0.88 % | 5.2 % | 9.72 % | 17.03 % | 31.75 % | 44.26 % |
| 2.5 ATR | 19.112 % | 21.5325 | 0.1 % | 2.16 % | 4.62 % | 9.84 % | 21.56 % | 34.27 % |
| 3.0 ATR | 22.934 % | 20.515 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 15.23 % | 26.57 % |
| 4.0 ATR | 30.579 % | 18.48 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.28 % |
| 6.0 ATR | 45.868 % | 14.41 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.46 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.03 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.98 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 0.99 ATR | 1.37 ATR | 1.67 ATR | 1.88 ATR | 2.49 ATR | 3.42 ATR |
| **10 s.** | 0.57 ATR | 1.27 ATR | 1.44 ATR | 1.95 ATR | 2.33 ATR | 2.62 ATR | 3.78 ATR | 5.11 ATR |
| **20 s.** | 0.81 ATR | 1.75 ATR | 1.97 ATR | 2.58 ATR | 3.17 ATR | 3.71 ATR | 5.57 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.455–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.822 %, prix 25.6026), p(touche) 40.78 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (90.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.639–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.733 %, prix 25.0939), p(touche) 37.88 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.798–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.645 %, prix 24.5849), p(touche) 33.99 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.987–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.645 %, prix 24.5849), p(touche) 44.39 % (en stress 97.06 %)  ✅ optimum identifie (60.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.442–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.467 %, prix 23.5675), p(touche) 43.32 % (en stress 97.06 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.968–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (15.289 %, prix 22.5501), p(touche) 44.26 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.12 | EV/share : €0.243 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 16 % | T3 7 %
- Kelly (position) : f* 0.092 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 80.7 | side 14.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 160.0 (= 6 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.988% → cible +6.146% / stop −3.073%, p_fill 79%, n_eff≈85.3) : P(cible|rempli) **13%** · **EV/risk -0.191** (×p_fill ; si rempli -0.74% du capital)
  - **swing** (entrée dip −2.175% → cible +11.717% / stop −7.815%, p_fill 71%, n_eff≈81.8) : P(cible|rempli) **25%** · **EV/risk -0.088** (×p_fill ; si rempli -0.97% du capital)
  - **deep** (entrée dip −3.363% → cible +13.089% / stop −11.866%, p_fill 69%, n_eff≈76.5) : P(cible|rempli) **35%** · **EV/risk -0.084** (×p_fill ; si rempli -1.45% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→74% · +2.0%→66% · +3.0%→50% · +5.0%→34% · +8.0%→17%
- Range intraday médian 6.93% (p90 16.1%) · excursion haute méd. +2.93% / basse méd. −3.31%
- Profil de vol intra : ouverture 4.806% vs midi 1.518% vs clôture 1.661% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑1%/↓0% ; spike-down 74% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. 0.151% ; recovery-V 25%
- **σ réalisé intraday** 4.419% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 71% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 26.6325 (VA 26.2575–26.7325 ; dernier close 26.53)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 91% · **stop −3.21%** sous le fill (sous le bruit) · cible +2.26% · R/R 0.7 (high win-rate)
- Gaps overnight (n=158) : méd. -0.0% · baisse 51% (gap-down >1% 16% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −3.16%) · haut méd +0.82% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.92%) · haut méd +1.23% · range méd 2.91%
- Excursion ouverture 30min (n=160) : bas méd −1.42% (p90 −4.38%) · haut méd +1.57% · range méd 3.4%
- Excursion ouverture 60min (n=160) : bas méd −1.64% (p90 −5.26%) · haut méd +2.01% · range méd 4.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.62 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 81% (125/158) · gap 30% · délai 0.1min · rebond 61% (81/125) (MFE +1.75%)
   - −1.0% : fill 30min 56% · séance 76% (120/158) · gap 16% · délai 0.4min · rebond 61% (79/120) (MFE +1.71%)
   - −1.5% : fill 30min 50% · séance 72% (107/158) · gap 8% · délai 2.4min · rebond 63% (68/107) (MFE +1.74%)
   - −2.0% : fill 30min 42% · séance 66% (98/158) · gap 6% · délai 7.8min · rebond 59% (60/98) (MFE +1.61%)
   - −3.0% : fill 30min 26% · séance 51% (79/158) · gap 3% · délai 31.2min · rebond 59% (53/79) (MFE +1.59%)
   - −4.0% : fill 30min 16% · séance 39% (65/158) · gap 2% · délai 55.8min · rebond 71% (49/65) (MFE +1.67%)
   - −5.0% : fill 30min 11% · séance 28% (50/158) · gap 2% · délai 48.7min · rebond 91% (46/50) (MFE +2.26%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.9%) → stop au-delà de −1.95% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.91%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.34% (p90 −3.18%) → stop au-delà de −2.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1398 jambes) : jambe baissière méd −1.21% (p90 −2.94%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 95% (51/53) · rebond 58% (30/51)
      · −2.0% : fill 87% (46/53) · rebond 59% (26/46)
      · −3.0% : fill 76% (41/53) · rebond 59% (28/41)
      · −4.0% : fill 58% (34/53) · rebond 61% (23/34)
      · −5.0% : fill 44% (27/53) · rebond 92% (24/27)
   - **flat** (34 séances) :
      · −1.0% : fill 72% (25/34) · rebond 66% (17/25)
      · −2.0% : fill 54% (19/34) · rebond 49% (11/19)
      · −3.0% : fill 40% (15/34) · rebond 60% (9/15)
      · −4.0% : fill 37% (14/34) · rebond 77% (11/14)
      · −5.0% : fill 30% (11/34) · rebond 80% (10/11)
   - **gap-up** (71 séances) :
      · −1.0% : fill 61% (44/71) · rebond 63% (32/44)
      · −2.0% : fill 52% (33/71) · rebond 65% (23/33)
      · −3.0% : fill 34% (23/71) · rebond 59% (16/23)
      · −4.0% : fill 23% (17/71) · rebond 88% (15/17)
      · −5.0% : fill 13% (12/71) · rebond 100% (12/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 56% si les 15 1res min sont vertes (77 cas) · 29% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:03** → P(séance verte=clôture>ouverture) 76% si début vert vs 15% si rouge (base 42% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -2.0% (q20 -4.42%) → **SL/trailing à −4.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.14% / q75 +3.25% → **scale +2.14% / runner +3.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **15%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.15%** (au-delà de la MAE q10 -4.15%), cible rebond +1.5% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.12% .. +5.57%] · haut q95 +6.82% · bas q05 -5.16%
   - 60min (n=160) : retour [-4.85% .. +7.25%] · haut q95 +8.2% · bas q05 -6.05%
   - 2h (n=160) : retour [-4.79% .. +9.19%] · haut q95 +9.95% · bas q05 -6.15%
   - 4h (n=160) : retour [-5.98% .. +9.6%] · haut q95 +9.98% · bas q05 -7.39%
   - 6h (n=160) : retour [-5.66% .. +10.41%] · haut q95 +12.17% · bas q05 -8.1%
   - session (n=160) : retour [-7.13% .. +9.93%] · haut q95 +12.72% · bas q05 -8.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 4.85%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.08 · part idiosyncratique 0.92
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.0  _(neutre)_
- **ADX** : 12.2  _(pas de tendance nette)_
- **MACD** : hist 0.069  _(bullish_recent)_
- **BB** : %B 0.43 · largeur 21.2%
- **ATR** : 2.04 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.039  _(neutre)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 52.2  _(transition)_
- **MA** : MA20 27.04 · MA50 27.54 · MA200 29.39  _(prix < MA20)_
- **Dist MA** : MA20 -1.5% · MA50 -3.3% · MA200 -9.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (773775 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
