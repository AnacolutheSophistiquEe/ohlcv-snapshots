# SMCI

**Generated** : 2026-10-26T01:22:25.375633+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · $32.94  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $32.94 (+0.6% vs entrée) · entrée $32.74 · stop $31.92 · T1 $34.11 · R/R 1.67  
> ↳ P(T1 av. stop) 18 % _(réel 5 s)_ · EV/risk -0.165 _(réel 5 s)_ (GBM -0.008) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.51% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 32.94 · ATR Wilder 2.55 (7.74 %)_
- **Swing** : plage **29.82 → 27.89** (-9.46 % a -15.32 % sous la cloture, 0.76 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 28.5-29.68 (B). stop INDICATIF 25.58 (-8.28 % sous le bas ; sous le support 26.86-27.75 (- 0,5 ATR)).
- **Deep** : plage **27.89 → 22.19** (-15.32 % a -32.64 % sous la cloture, 2.24 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 26.86-27.75 (B) ; 25.13-26.06 (A) ; 23.38-24.19 (A) ; 21.79-22.66 (B). stop INDICATIF 17.51 (-21.06 % sous le bas ; sous le support 18.79-20.71 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.03 ATR sous le plus haut 20 s., RSI(2) 31.4. Limite **31.66** (seance suivante), stop catastrophe 21.46, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 29.85-31.11 (A, -5.56 %) ; 28.5-29.68 (B, -9.9 %) ; 26.86-27.75 (B, -15.76 %) ; 25.13-26.06 (A, -20.89 %) ; 23.38-24.19 (A, -26.56 %) ; 21.79-22.66 (B, -31.21 %)
- Resistances reelles au-dessus : 34.94-35.88 (A, 6.07 %) ; 36.37-37.39 (A, 10.41 %) ; 37.82-39.05 (A, 14.81 %) ; 39.11-40.13 (A, 18.73 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.05 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.66 %)** : le gap seul le franchit 1.037 % des séances (13 fois sur 1254).
   - exécution **4.598 pt plus bas** dans le cas TYPIQUE (médiane), 16.759 au p90, **19.391 au pire**
   - perte réelle **16.875 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 9.66 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0748 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 13 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.817 % | p01 -10.29 % | pire -29.051 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4801** [0.4065 ; 0.5543] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3401** [0.2917 ; 0.3912] _(largeur 10.0 pt, n_eff 345.7)_
   - deep : **0.2979** [0.2515 ; 0.3476] _(largeur 9.6 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.39 %** | vol 5.85 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.89 % contre 6.56 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.53 % vs -16.84 % si l'on extrapolait par √5 _(rapport 1.041 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5317** (β de hausse 1.2087, asymétrie 1.2673) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.867× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 30.8303 sur sr_based (0.4 ATR, 6.405 %) — p(stop avant cible) 0.5975 [0.55 ; 0.65], R/R 3.627, perte reelle 7.313 % (gap inclus), CVaR 16.764 %, EV 0.9781 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 2.4708 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.598, borne haute 0.648 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 16.76 % > budget 5.21 %
- Budget de queue : **5.21 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.183 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 20.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.4 ATR (stop 6.405 %) — p(stop avant cible) 0.5975 [0.55 ; 0.65], R/R 3.627, perte reelle 7.313 % (gap inclus), EV 0.9781 % — **REFUSE**
      - refuse : cible atteinte seulement 13.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.598, borne haute 0.648 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 16.76 % > budget 5.21 %
   - ⚪ swing_based a 0.94 ATR (stop 10.912 %) — p(stop avant cible) 0.373 [0.32 ; 0.42], R/R 2.129, perte reelle 12.46 % (gap inclus), EV 1.4701 % — **REFUSE**
      - refuse : R/R 2.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.90 % > budget 5.21 %
   - 🔴 support a 1.91 ATR (stop 18.994 %) — p(stop avant cible) 0.1615 [0.13 ; 0.20], R/R 1.25, perte reelle 21.223 % (gap inclus), EV 1.9183 % — **REFUSE**
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.19 % > budget 5.21 %
      - ⚠ support DETECTE a 0.30 ATR du spot — compartiment <1, mesure a 47.8 % de casse (IC clusterise [0.449 ; 0.507] sur 1237 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 2.75 ATR (stop 25.977 %) — p(stop avant cible) 0.108 [0.08 ; 0.14], R/R 0.992, perte reelle 26.74 % (gap inclus), EV 1.6562 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.62 % > budget 5.21 %
   - 🟢 support a 3.49 ATR (stop 32.139 %) — p(stop avant cible) 0.0654 [0.04 ; 0.10], R/R 0.822, perte reelle 32.286 % (gap inclus), EV 1.4124 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.33 % > budget 5.21 %
   - ⚪ atr_grid a 1.5 ATR (stop 12.467 %) — p(stop avant cible) 0.3085 [0.26 ; 0.36], R/R 1.877, perte reelle 14.136 % (gap inclus), EV 1.6534 % — **REFUSE**
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.51 % > budget 5.21 %
   - ⚪ atr_grid a 2.5 ATR (stop 20.779 %) — p(stop avant cible) 0.1538 [0.12 ; 0.19], R/R 1.188, perte reelle 22.33 % (gap inclus), EV 1.824 % — **REFUSE**
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.44 % > budget 5.21 %
   - ⚪ atr_grid a 4.0 ATR (stop 33.247 %) — p(stop avant cible) 0.0616 [0.04 ; 0.09], R/R 0.793, perte reelle 33.434 % (gap inclus), EV 1.3737 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.48 % > budget 5.21 %
   - ⚪ atr_grid a 4.5 ATR (stop 37.402 %) — p(stop avant cible) 0.0404 [0.02 ; 0.07], R/R 0.709, perte reelle 37.426 % (gap inclus), EV 1.3444 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.42 % > budget 5.21 %
   - ⚪ atr_grid a 5.0 ATR (stop 41.558 %) — p(stop avant cible) 0.007 [0.00 ; 0.02], R/R 0.638, perte reelle 41.558 % (gap inclus), EV 1.5065 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.67 % > budget 5.21 %
   - ⚪ atr_grid a 5.5 ATR (stop 45.714 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 0.579, perte reelle 45.853 % (gap inclus), EV 1.4987 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.77 % > budget 5.21 %
   - ⚪ atr_grid a 6.0 ATR (stop 49.87 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.499, perte reelle 53.124 % (gap inclus), EV 1.4904 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.96 % > budget 5.21 %
   - ⚪ atr_grid a 6.5 ATR (stop 54.026 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.478, perte reelle 55.543 % (gap inclus), EV 1.4875 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.98 % > budget 5.21 %
   - ⚪ atr_grid a 7.0 ATR (stop 58.182 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.456, perte reelle 58.182 % (gap inclus), EV 1.4983 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.80 % > budget 5.21 %
   - ⚪ atr_grid a 7.5 ATR (stop 62.337 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.426, perte reelle 62.337 % (gap inclus), EV 1.4983 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.80 % > budget 5.21 %
   - ⚪ atr_grid a 8.0 ATR (stop 66.493 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.399, perte reelle 66.493 % (gap inclus), EV 1.4983 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.80 % > budget 5.21 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 32.94, ATR14 2.7379 (8.312 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 2.892 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.416 % | 32.8031 | 90.85 % | 93.66 % | 95.06 % | 95.56 % | 96.75 % | 97.95 % |
| 0.1 ATR | 0.831 % | 32.6662 | 82.29 % | 87.61 % | 89.62 % | 91.52 % | 93.3 % | 95.28 % |
| 0.15 ATR | 1.247 % | 32.5293 | 75.25 % | 82.58 % | 85.48 % | 88.69 % | 91.07 % | 94.05 % |
| 0.2 ATR | 1.662 % | 32.3924 | 68.41 % | 77.84 % | 81.05 % | 86.16 % | 89.54 % | 92.72 % |
| 0.25 ATR | 2.078 % | 32.2555 | 62.27 % | 73.21 % | 76.81 % | 82.93 % | 87.61 % | 91.18 % |
| 0.35 ATR | 2.909 % | 31.9817 | 49.7 % | 63.95 % | 70.26 % | 77.88 % | 83.45 % | 88.72 % |
| 0.5 ATR | 4.156 % | 31.5711 | 35.11 % | 50.35 % | 59.07 % | 69.39 % | 77.66 % | 84.21 % |
| 0.75 ATR | 6.234 % | 30.8866 | 17.51 % | 33.84 % | 43.65 % | 55.86 % | 67.11 % | 76.0 % |
| 1.0 ATR | 8.312 % | 30.2021 | 7.95 % | 21.95 % | 30.85 % | 44.34 % | 57.77 % | 69.33 % |
| 1.25 ATR | 10.39 % | 29.5177 | 3.72 % | 15.21 % | 22.58 % | 33.74 % | 48.43 % | 61.54 % |
| 1.5 ATR | 12.467 % | 28.8332 | 1.51 % | 9.67 % | 16.53 % | 26.36 % | 42.13 % | 55.18 % |
| 2.0 ATR | 16.623 % | 27.4643 | 0.3 % | 3.63 % | 8.67 % | 16.46 % | 30.25 % | 44.0 % |
| 2.5 ATR | 20.779 % | 26.0954 | 0.2 % | 1.51 % | 4.44 % | 10.0 % | 19.9 % | 32.1 % |
| 3.0 ATR | 24.935 % | 24.7264 | 0.2 % | 1.21 % | 2.62 % | 5.96 % | 14.42 % | 24.31 % |
| 4.0 ATR | 33.247 % | 21.9886 | 0.0 % | 0.6 % | 1.51 % | 2.83 % | 8.02 % | 14.46 % |
| 6.0 ATR | 49.87 % | 16.5129 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.51 ATR | 0.58 ATR | 0.77 ATR | 0.94 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.28 ATR | 0.65 ATR | 0.73 ATR | 0.96 ATR | 1.18 ATR | 1.36 ATR | 1.92 ATR | 2.43 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.99 ATR | 1.27 ATR | 1.57 ATR | 1.82 ATR | 2.50 ATR | 3.31 ATR |
| **10 s.** | 0.56 ATR | 1.21 ATR | 1.39 ATR | 1.88 ATR | 2.25 ATR | 2.50 ATR | 3.69 ATR | 5.01 ATR |
| **20 s.** | 0.79 ATR | 1.73 ATR | 1.96 ATR | 2.46 ATR | 2.96 ATR | 3.44 ATR | 5.00 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.581–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.234 %, prix 30.8865), p(touche) 33.84 % (en stress 88.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.728–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.234 %, prix 30.8865), p(touche) 43.65 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.986–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.39 %, prix 29.5175), p(touche) 33.74 % (en stress 90.91 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.386–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (12.467 %, prix 28.8334), p(touche) 42.13 % (en stress 96.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.955–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (16.623 %, prix 27.4644), p(touche) 44.0 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : $-0.006 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 66.6 | bear 5.0 | side 28.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.616% → cible +4.181% / stop −2.509%, p_fill 86%, n_eff≈91.7) : P(cible|rempli) **18%** · **EV/risk -0.165** (×p_fill ; si rempli -0.48% du capital)
  - **swing** (entrée dip −1.348% → cible +9.42% / stop −8.425%, p_fill 86%, n_eff≈99.0) : P(cible|rempli) **33%** · **EV/risk +0.001** (×p_fill ; si rempli +0.01% du capital)
  - **deep** (entrée dip −2.093% → cible +21.53% / stop −12.733%, p_fill 79%, n_eff≈87.9) : P(cible|rempli) **24%** · **EV/risk +0.115** (×p_fill ; si rempli +1.86% du capital)
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.59 · part idiosyncratique 0.41
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 26.3  _(survente)_
- **ADX** : 25.1  _(tendance etablie)_
- **MACD** : hist -0.901  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 46.7%
- **ATR** : 2.74 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.207  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 35.9  _(marche directionnel)_
- **MA** : MA20 38.7 · MA50 38.58 · MA200 32.55  _(prix < MA20)_
- **Dist MA** : MA20 -14.9% · MA50 -14.6% · MA200 +1.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (759484 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
