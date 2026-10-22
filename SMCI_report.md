# SMCI

**Generated** : 2026-10-22T22:01:18.188185+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · $33.72  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (14 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $33.72 (+1.2% vs entrée) · entrée $33.32 · stop $32.49 · T1 $34.69 · R/R 1.65  
> ↳ ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-22 : 33.72 · ATR Wilder 2.64 (7.82 %)_
- **Swing** : plage **30.5 → 28.54** (-9.56 % a -15.36 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 29.85-31.11 (B) ; 28.5-29.68 (B). stop INDICATIF 25.35 (-11.2 % sous le bas ; sous le support 26.67-27.75 (- 0,5 ATR)).
- **Deep** : plage **28.54 → 22.76** (-15.36 % a -32.52 % sous la cloture, 2.19 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 28.5-29.68 (B) ; 26.67-27.75 (B) ; 25.13-26.06 (A) ; 23.38-24.19 (A). stop INDICATIF 20.47 (-10.04 % sous le bas ; sous le support 21.79-22.66 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.57 ATR sous le plus haut 20 s., RSI(2) 44.1 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 29.85-31.11 (B, -7.74 %) ; 28.5-29.68 (B, -11.98 %) ; 26.67-27.75 (B, -17.7 %) ; 25.13-26.06 (A, -22.72 %) ; 23.38-24.19 (A, -28.26 %) ; 21.79-22.66 (B, -32.8 %)
- Resistances reelles au-dessus : 34.94-35.88 (A, 3.62 %) ; 36.37-37.39 (A, 7.86 %) ; 37.82-39.11 (A, 12.16 %) ; 39.23-40.13 (A, 16.34 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.06 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.68 %)** : le gap seul le franchit 1.038 % des séances (13 fois sur 1253).
   - exécution **3.578 pt plus bas** dans le cas TYPIQUE (médiane), 15.739 au p90, **18.371 au pire**
   - perte réelle **16.875 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 10.68 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0643 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 13 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.818 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4706** [0.3972 ; 0.5449] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3447** [0.2961 ; 0.3959] _(largeur 10.0 pt, n_eff 345.7)_
   - deep : **0.2997** [0.2532 ; 0.3495] _(largeur 9.6 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.39 %** | vol 5.85 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.74 % contre 6.56 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.54 % vs -16.84 % si l'on extrapolait par √5 _(rapport 1.041 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5351** (β de hausse 1.2087, asymétrie 1.2701) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.874× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 30.8903 sur sr_based (0.68 ATR, 8.392 %) — p(stop avant cible) 0.4626 [0.41 ; 0.52], R/R 2.493, perte reelle 9.838 % (gap inclus), CVaR 21.237 %, EV 1.311 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0368 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 2.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 21.24 % > budget 11.37 %
- Budget de queue : **11.37 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.378 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 19.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.68 ATR (stop 8.392 %) — p(stop avant cible) 0.4626 [0.41 ; 0.52], R/R 2.493, perte reelle 9.838 % (gap inclus), EV 1.311 % — **REFUSE**
      - refuse : R/R 2.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.24 % > budget 11.37 %
   - ⚪ atr_based a 1.5 ATR (stop 12.128 %) — p(stop avant cible) 0.3124 [0.27 ; 0.36], R/R 1.774, perte reelle 13.823 % (gap inclus), EV 1.563 % — **REFUSE**
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.50 % > budget 11.37 %
   - 🔴 support a 2.2 ATR (stop 20.694 %) — p(stop avant cible) 0.1489 [0.11 ; 0.19], R/R 1.098, perte reelle 22.334 % (gap inclus), EV 1.7566 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.46 % > budget 11.37 %
      - ⚠ support DETECTE a 0.58 ATR du spot — compartiment <1, mesure a 47.5 % de casse (IC clusterise [0.445 ; 0.502] sur 1274 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 3.05 ATR (stop 27.515 %) — p(stop avant cible) 0.0933 [0.07 ; 0.13], R/R 0.878, perte reelle 27.95 % (gap inclus), EV 1.5378 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.33 % > budget 11.37 %
   - 🟢 support a 3.79 ATR (stop 33.535 %) — p(stop avant cible) 0.062 [0.04 ; 0.09], R/R 0.728, perte reelle 33.702 % (gap inclus), EV 1.2835 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.74 % > budget 11.37 %
   - ⚪ atr_grid a 0.25 ATR (stop 2.021 %) — p(stop avant cible) 0.8729 [0.83 ; 0.90], R/R 10.688, perte reelle 2.295 % (gap inclus), EV 0.3204 % — **REFUSE**
      - refuse : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 10.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.873, borne haute 0.905 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 10.107 %) — p(stop avant cible) 0.4098 [0.36 ; 0.46], R/R 2.113, perte reelle 11.607 % (gap inclus), EV 1.0902 % — **REFUSE**
      - refuse : R/R 2.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.90 % > budget 11.37 %
   - ⚪ atr_grid a 1.75 ATR (stop 14.15 %) — p(stop avant cible) 0.242 [0.20 ; 0.29], R/R 1.529, perte reelle 16.037 % (gap inclus), EV 1.6319 % — **REFUSE**
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.25 % > budget 11.37 %
   - ⚪ atr_grid a 2.75 ATR (stop 22.235 %) — p(stop avant cible) 0.1362 [0.10 ; 0.18], R/R 1.038, perte reelle 23.633 % (gap inclus), EV 1.6953 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.04 % > budget 11.37 %
   - ⚪ atr_grid a 4.5 ATR (stop 36.385 %) — p(stop avant cible) 0.0489 [0.03 ; 0.08], R/R 0.673, perte reelle 36.438 % (gap inclus), EV 1.2188 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.38 % > budget 11.37 %
   - ⚪ atr_grid a 5.0 ATR (stop 40.427 %) — p(stop avant cible) 0.0111 [0.00 ; 0.03], R/R 0.607, perte reelle 40.441 % (gap inclus), EV 1.4235 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.87 % > budget 11.37 %
   - ⚪ atr_grid a 5.5 ATR (stop 44.47 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 0.548, perte reelle 44.724 % (gap inclus), EV 1.4307 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.75 % > budget 11.37 %
   - ⚪ atr_grid a 6.0 ATR (stop 48.513 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.494, perte reelle 49.666 % (gap inclus), EV 1.4255 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.88 % > budget 11.37 %
   - ⚪ atr_grid a 6.5 ATR (stop 52.556 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.442, perte reelle 55.543 % (gap inclus), EV 1.4166 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.01 % > budget 11.37 %
   - ⚪ atr_grid a 7.0 ATR (stop 56.598 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.433, perte reelle 56.598 % (gap inclus), EV 1.4207 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.00 % > budget 11.37 %
   - ⚪ atr_grid a 7.5 ATR (stop 60.641 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.404, perte reelle 60.641 % (gap inclus), EV 1.4268 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.83 % > budget 11.37 %
   - ⚪ atr_grid a 8.0 ATR (stop 64.684 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.379, perte reelle 64.684 % (gap inclus), EV 1.4268 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.83 % > budget 11.37 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 33.72, ATR14 2.7264 (8.085 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.347 ATR = 2.806 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.404 % | 33.5837 | 90.84 % | 93.65 % | 95.06 % | 95.55 % | 96.75 % | 97.95 % |
| 0.1 ATR | 0.809 % | 33.4474 | 82.28 % | 87.6 % | 89.61 % | 91.51 % | 93.29 % | 95.28 % |
| 0.15 ATR | 1.213 % | 33.311 | 75.23 % | 82.56 % | 85.47 % | 88.68 % | 91.06 % | 94.05 % |
| 0.2 ATR | 1.617 % | 33.1747 | 68.38 % | 77.82 % | 81.03 % | 86.15 % | 89.53 % | 92.71 % |
| 0.25 ATR | 2.021 % | 33.0384 | 62.24 % | 73.19 % | 76.89 % | 82.91 % | 87.6 % | 91.17 % |
| 0.35 ATR | 2.83 % | 32.7658 | 49.65 % | 63.91 % | 70.33 % | 77.86 % | 83.43 % | 88.71 % |
| 0.5 ATR | 4.043 % | 32.3568 | 35.05 % | 50.3 % | 59.13 % | 69.36 % | 77.64 % | 84.19 % |
| 0.75 ATR | 6.064 % | 31.6752 | 17.52 % | 33.77 % | 43.69 % | 55.81 % | 67.07 % | 75.98 % |
| 1.0 ATR | 8.085 % | 30.9936 | 7.96 % | 21.88 % | 30.88 % | 44.29 % | 57.72 % | 69.3 % |
| 1.25 ATR | 10.107 % | 30.312 | 3.73 % | 15.12 % | 22.6 % | 33.67 % | 48.37 % | 61.5 % |
| 1.5 ATR | 12.128 % | 29.6304 | 1.51 % | 9.68 % | 16.55 % | 26.39 % | 42.07 % | 55.13 % |
| 2.0 ATR | 16.171 % | 28.2671 | 0.3 % | 3.63 % | 8.68 % | 16.48 % | 30.18 % | 43.94 % |
| 2.5 ATR | 20.214 % | 26.9039 | 0.2 % | 1.51 % | 4.44 % | 10.01 % | 19.82 % | 32.03 % |
| 3.0 ATR | 24.256 % | 25.5407 | 0.2 % | 1.21 % | 2.62 % | 5.97 % | 14.33 % | 24.23 % |
| 4.0 ATR | 32.342 % | 22.8143 | 0.0 % | 0.6 % | 1.51 % | 2.83 % | 7.93 % | 14.37 % |
| 6.0 ATR | 48.513 % | 17.3614 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.23 ATR | 0.51 ATR | 0.58 ATR | 0.77 ATR | 0.93 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.28 ATR | 0.65 ATR | 0.73 ATR | 0.96 ATR | 1.18 ATR | 1.36 ATR | 1.92 ATR | 2.43 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.98 ATR | 1.27 ATR | 1.57 ATR | 1.82 ATR | 2.50 ATR | 3.31 ATR |
| **10 s.** | 0.56 ATR | 1.21 ATR | 1.38 ATR | 1.88 ATR | 2.25 ATR | 2.49 ATR | 3.68 ATR | 4.99 ATR |
| **20 s.** | 0.79 ATR | 1.73 ATR | 1.95 ATR | 2.46 ATR | 2.95 ATR | 3.43 ATR | 4.99 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.58–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.064 %, prix 31.6752), p(touche) 33.77 % (en stress 88.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.729–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.064 %, prix 31.6752), p(touche) 43.69 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.985–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.107 %, prix 30.3119), p(touche) 33.67 % (en stress 90.91 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.384–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (12.128 %, prix 29.6304), p(touche) 42.07 % (en stress 95.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.953–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (16.171 %, prix 28.2671), p(touche) 43.94 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : $0.026 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 — | T3 —
- Kelly (position) : f* 0.051 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 65.8 | bear 5.0 | side 29.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.179% → cible +4.091% / stop −2.5%, p_fill 75%, n_eff≈80.7) : P(cible|rempli) **16%** · **EV/risk -0.063** (×p_fill ; si rempli -0.21% du capital)
  - **swing** (entrée dip −2.595% → cible +9.281% / stop −8.301%, p_fill 61%, n_eff≈72.5) : P(cible|rempli) **33%** · **EV/risk +0.051** (×p_fill ; si rempli +0.69% du capital)
  - **deep** (entrée dip −4.001% → cible +21.095% / stop −12.635%, p_fill 60%, n_eff≈66.9) : P(cible|rempli) **25%** · **EV/risk +0.177** (×p_fill ; si rempli +3.72% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→62% · +3.0%→43% · +5.0%→22% · +8.0%→9%
- Range intraday médian 5.66% (p90 9.37%) · excursion haute méd. +2.56% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.84% vs midi 1.155% vs clôture 1.48% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 69% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.011)_ ; drift intra méd. 0.304% ; recovery-V 40%
- **σ réalisé intraday** 3.371% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 61% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 43.4066 (VA 43.1796–43.8039 ; dernier close 43.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 23% · rebond 78% · **stop −4.35%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 42% (gap-down >1% 31% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −2.5%) · haut méd +1.02% · range méd 2.13%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −3.1%) · haut méd +1.28% · range méd 2.8%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.6%) · haut méd +1.53% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.66% (p90 −4.07%) · haut méd +1.81% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.69 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 71% (116/159) · gap 37% · délai 0.0min · rebond 57% (69/116) (MFE +1.39%)
   - −1.0% : fill 30min 51% · séance 67% (109/159) · gap 31% · délai 0.0min · rebond 58% (64/109) (MFE +1.64%)
   - −1.5% : fill 30min 45% · séance 61% (99/159) · gap 20% · délai 0.2min · rebond 69% (65/99) (MFE +1.56%)
   - −2.0% : fill 30min 39% · séance 53% (86/159) · gap 16% · délai 1.1min · rebond 72% (57/86) (MFE +1.74%)
   - −3.0% : fill 30min 26% · séance 44% (72/159) · gap 8% · délai 12.8min · rebond 64% (44/72) (MFE +1.42%)
   - −4.0% : fill 30min 13% · séance 31% (52/159) · gap 4% · délai 41.3min · rebond 72% (34/52) (MFE +1.7%)
   - −5.0% : fill 30min 10% · séance 23% (41/159) · gap 3% · délai 49.2min · rebond 78% (30/41) (MFE +2.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.8%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −2.62%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.32%) → stop au-delà de −1.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=870 jambes) : jambe baissière méd −1.18% (p90 −2.77%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 98% (69/71) · rebond 48% (36/69)
      · −2.0% : fill 94% (65/71) · rebond 74% (41/65)
      · −3.0% : fill 85% (58/71) · rebond 65% (35/58)
      · −4.0% : fill 62% (43/71) · rebond 71% (28/43)
      · −5.0% : fill 46% (34/71) · rebond 76% (24/34)
   - **flat** (13 séances) :
      · −1.0% : fill 85% (12/13) · rebond 75% (9/12)
      · −2.0% : fill 36% (5/13) · rebond 50% (3/5)
      · −3.0% : fill 29% (3/13) · rebond 43% (2/3)
      · −4.0% : fill 10% (1/13) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 38% (28/75) · rebond 74% (19/28)
      · −2.0% : fill 21% (16/75) · rebond 70% (13/16)
      · −3.0% : fill 11% (11/75) · rebond 70% (7/11)
      · −4.0% : fill 8% (8/75) · rebond 72% (5/8)
      · −5.0% : fill 8% (7/75) · rebond 86% (6/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 68% si les 15 1res min sont vertes (80 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 48% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **78%** · continue >prix actuel 54% ; creux résiduel méd -1.96% (q20 -3.57%) → **SL/trailing à −3.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +4.23% → **scale +1.91% / runner +4.23%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **18%** (continue à baisser 53%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.85%** (au-delà de la MAE q10 -4.85%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.7% .. +4.13%] · haut q95 +5.15% · bas q05 -4.15%
   - 60min (n=160) : retour [-4.08% .. +5.23%] · haut q95 +6.49% · bas q05 -5.23%
   - 2h (n=160) : retour [-4.2% .. +6.08%] · haut q95 +7.25% · bas q05 -5.52%
   - 4h (n=160) : retour [-4.43% .. +6.66%] · haut q95 +7.77% · bas q05 -5.98%
   - 6h (n=160) : retour [-4.87% .. +6.53%] · haut q95 +8.68% · bas q05 -6.54%
   - session (n=160) : retour [-4.8% .. +6.89%] · haut q95 +8.93% · bas q05 -6.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.6 · part idiosyncratique 0.4
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 26.7  _(survente)_
- **ADX** : 25.6  _(tendance etablie)_
- **MACD** : hist -0.989  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 45.0%
- **ATR** : 2.73 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.142  _(distribution)_
- **Vol ratio** : 1.2  _(volume normal)_
- **Choppiness** : 35.8  _(marche directionnel)_
- **MA** : MA20 39.22 · MA50 38.71 · MA200 32.53  _(prix < MA20)_
- **Dist MA** : MA20 -14.0% · MA50 -12.9% · MA200 +3.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (763790 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
