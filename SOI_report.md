# SOI

**Generated** : 2026-09-30T21:49:48.499088+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 10/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €155.95  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €155.95 (+1.2% vs entrée) · entrée €154.15 · stop €151.07 · T1 €159.23 · R/R 1.65  
> ↳ ¼-Kelly 0.017 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 10/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €153.13–€155.17 (mid €154.15)
- Spot actuel : €155.95 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €151.07 (plancher anti-bruit 5 s — stop EV-optimal −2% (first-passage 5 s réel) ; -2.00 % depuis l'entree)
- Targets : T1 €159.23 · R/R 1.65 | T2 €164.31 · R/R 3.3 | T3 €169.39 · R/R 4.95
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €151.07


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.91 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.19 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **7.529 pt plus bas** dans le cas TYPIQUE (médiane), 15.989 au p90, **18.104 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 11.19 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0241 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.675 % | p01 -5.132 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4779** [0.4044 ; 0.5522] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3478** [0.299 ; 0.3991] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.4263** [0.375 ; 0.4789] _(largeur 10.4 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-14.04 %** | vol 6.66 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 4.00 % contre 7.42 % aujourd'hui, rapport 0.54)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.4 % vs -11.44 % si l'on extrapolait par √5 _(rapport 1.084 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1106** (β de hausse 1.575, asymétrie 0.7052) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.057× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 143.9965 sur support (0.71 ATR, 7.665 %) — p(stop avant cible) 0.5473 [0.49 ; 0.60], R/R 3.644, perte reelle 8.051 % (gap inclus), CVaR 11.75 %, EV 2.3353 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0895 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.547, borne haute 0.599 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.71 ATR (stop 7.665 %) — p(stop avant cible) 0.5473 [0.49 ; 0.60], R/R 3.644, perte reelle 8.051 % (gap inclus), EV 2.3353 % — **REFUSE**
      - refuse : p_stop_first 0.547, borne haute 0.599 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.71 ATR du spot — compartiment <1, mesure a 45.4 % de casse (IC clusterise [0.423 ; 0.484] sur 1130 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 9.77 %) — p(stop avant cible) 0.4587 [0.41 ; 0.51], R/R 2.891, perte reelle 10.148 % (gap inclus), EV 2.5995 % — **REFUSE**
      - refuse : R/R 2.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.23 % > budget 12.00 %
   - 🟢 support a 3.83 ATR (stop 28.024 %) — p(stop avant cible) 0.0379 [0.02 ; 0.06], R/R 1.035, perte reelle 28.334 % (gap inclus), EV 4.17 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.15 % > budget 12.00 %
   - 🟢 support a 4.97 ATR (stop 35.398 %) — p(stop avant cible) 0.0197 [0.01 ; 0.04], R/R 0.829, perte reelle 35.398 % (gap inclus), EV 4.1184 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.47 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.628 %) — p(stop avant cible) 0.8643 [0.83 ; 0.90], R/R 16.837, perte reelle 1.742 % (gap inclus), EV 1.19 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 16.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.864, borne haute 0.897 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 grid_snapped a 0.71 ATR (stop 6.571 %) — p(stop avant cible) 0.5838 [0.53 ; 0.63], R/R 4.18, perte reelle 7.018 % (gap inclus), EV 2.7267 % — **REFUSE**
      - refuse : p_stop_first 0.584, borne haute 0.635 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.75 ATR (stop 11.398 %) — p(stop avant cible) 0.3997 [0.35 ; 0.45], R/R 2.48, perte reelle 11.829 % (gap inclus), EV 2.6588 % — **REFUSE**
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.84 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 13.026 %) — p(stop avant cible) 0.3371 [0.29 ; 0.39], R/R 2.183, perte reelle 13.437 % (gap inclus), EV 2.9328 % — **REFUSE**
      - refuse : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.80 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 14.654 %) — p(stop avant cible) 0.2998 [0.25 ; 0.35], R/R 1.943, perte reelle 15.094 % (gap inclus), EV 2.7043 % — **REFUSE**
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 16.283 %) — p(stop avant cible) 0.2373 [0.19 ; 0.28], R/R 1.765, perte reelle 16.622 % (gap inclus), EV 3.4637 % — **REFUSE**
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.89 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 17.911 %) — p(stop avant cible) 0.1931 [0.15 ; 0.24], R/R 1.596, perte reelle 18.377 % (gap inclus), EV 3.7476 % — **REFUSE**
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.71 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 19.539 %) — p(stop avant cible) 0.1688 [0.13 ; 0.21], R/R 1.476, perte reelle 19.873 % (gap inclus), EV 3.7966 % — **REFUSE**
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.67 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 22.796 %) — p(stop avant cible) 0.0847 [0.06 ; 0.12], R/R 1.254, perte reelle 23.4 % (gap inclus), EV 4.1392 % — **REFUSE**
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.82 % > budget 12.00 %
   - 🟢 grid_snapped a 3.83 ATR (stop 26.93 %) — p(stop avant cible) 0.0447 [0.03 ; 0.07], R/R 1.071, perte reelle 27.378 % (gap inclus), EV 4.1766 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.97 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.309 %) — p(stop avant cible) 0.029 [0.01 ; 0.05], R/R 0.993, perte reelle 29.535 % (gap inclus), EV 4.1968 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.86 % > budget 12.00 %
   - 🟢 grid_snapped a 4.97 ATR (stop 34.304 %) — p(stop avant cible) 0.0242 [0.01 ; 0.04], R/R 0.854, perte reelle 34.366 % (gap inclus), EV 4.1083 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.67 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.078 %) — p(stop avant cible) 0.0101 [0.00 ; 0.03], R/R 0.751, perte reelle 39.078 % (gap inclus), EV 4.1201 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.39 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 42.335 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.693, perte reelle 42.335 % (gap inclus), EV 4.1636 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.52 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 45.592 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.643, perte reelle 45.592 % (gap inclus), EV 4.1803 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.20 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 48.848 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.601, perte reelle 48.848 % (gap inclus), EV 4.1803 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.20 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 52.105 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.563, perte reelle 52.105 % (gap inclus), EV 4.1803 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.20 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 155.95, ATR14 10.1571 (6.513 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.357 ATR = 2.325 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.326 % | 155.4421 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.651 % | 154.9343 | 84.8 % | 89.79 % | 91.65 % | 94.29 % | 96.04 % | 97.3 % |
| 0.15 ATR | 0.977 % | 154.4264 | 77.84 % | 84.89 % | 87.52 % | 90.85 % | 93.57 % | 95.2 % |
| 0.2 ATR | 1.303 % | 153.9186 | 69.12 % | 79.69 % | 83.5 % | 87.8 % | 91.2 % | 93.21 % |
| 0.25 ATR | 1.628 % | 153.4107 | 62.55 % | 75.76 % | 80.26 % | 86.12 % | 89.91 % | 92.61 % |
| 0.35 ATR | 2.28 % | 152.395 | 50.69 % | 67.32 % | 73.18 % | 80.81 % | 85.56 % | 89.91 % |
| 0.5 ATR | 3.257 % | 150.8714 | 35.69 % | 55.15 % | 62.57 % | 72.83 % | 80.71 % | 87.11 % |
| 0.75 ATR | 4.885 % | 148.3321 | 16.96 % | 34.94 % | 46.46 % | 57.97 % | 72.4 % | 80.32 % |
| 1.0 ATR | 6.513 % | 145.7929 | 8.33 % | 23.75 % | 33.89 % | 47.15 % | 64.29 % | 74.83 % |
| 1.25 ATR | 8.141 % | 143.2536 | 4.12 % | 15.51 % | 24.95 % | 37.11 % | 56.08 % | 69.03 % |
| 1.5 ATR | 9.77 % | 140.7143 | 2.25 % | 10.4 % | 18.07 % | 29.43 % | 48.17 % | 62.74 % |
| 2.0 ATR | 13.026 % | 135.6357 | 0.59 % | 4.51 % | 8.84 % | 17.81 % | 34.62 % | 52.25 % |
| 2.5 ATR | 16.283 % | 130.5571 | 0.29 % | 2.45 % | 4.91 % | 11.61 % | 23.94 % | 44.36 % |
| 3.0 ATR | 19.539 % | 125.4786 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 16.42 % | 36.36 % |
| 4.0 ATR | 26.052 % | 115.3214 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.4 % | 23.18 % |
| 6.0 ATR | 39.078 % | 95.0072 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 11.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.56 ATR | 0.63 ATR | 0.79 ATR | 0.97 ATR | 1.11 ATR | 1.53 ATR | 1.96 ATR |
| **3 s.** | 0.32 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.25 ATR | 1.43 ATR | 1.94 ATR | 2.49 ATR |
| **5 s.** | 0.46 ATR | 0.93 ATR | 1.05 ATR | 1.38 ATR | 1.69 ATR | 1.91 ATR | 2.68 ATR | 3.59 ATR |
| **10 s.** | 0.67 ATR | 1.44 ATR | 1.62 ATR | 2.08 ATR | 2.45 ATR | 2.76 ATR | 3.92 ATR | 5.78 ATR |
| **20 s.** | 0.99 ATR | 2.14 ATR | 2.46 ATR | 3.25 ATR | 3.86 ATR | 4.57 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.407–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (60.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.626–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.779–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.513 %, prix 145.793), p(touche) 33.89 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.054–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.141 %, prix 143.2541), p(touche) 37.11 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.617–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.459–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.054 | EV/share : €0.167 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 — | T3 —
- Kelly (position) : f* 0.069 | ¼-Kelly 0.017 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 15.5 | bear 5.0 | side 79.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 624.0 (= 4 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.153% → cible +3.295% / stop −2.0%, p_fill 75%, n_eff≈82.0) : P(cible|rempli) **33%** · **EV/risk -0.065** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −2.535% → cible +17.761% / stop −8.88%, p_fill 61%, n_eff≈72.2) : P(cible|rempli) **21%** · **EV/risk -0.024** (×p_fill ; si rempli -0.35% du capital)
  - **deep** (entrée dip −3.92% → cible +19.458% / stop −10.169%, p_fill 64%, n_eff≈73.0) : P(cible|rempli) **26%** · **EV/risk -0.093** (×p_fill ; si rempli -1.46% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→66% · +3.0%→55% · +5.0%→37% · +8.0%→18%
- Range intraday médian 7.97% (p90 14.88%) · excursion haute méd. +3.44% / basse méd. −3.1%
- Profil de vol intra : ouverture 4.937% vs midi 1.449% vs clôture 2.153% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 11% · trend ↑1%/↓2% ; spike-down 71% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; neutre — autocorr -0.01)_ ; drift intra méd. 0.383% ; recovery-V 42%
- **σ réalisé intraday** 3.974% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 58% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 154.5362 (VA 148.2812–155.9262 ; dernier close 155.08)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 43% · rebond 75% · **stop −7.26%** sous le fill (sous le bruit) · cible +3.18% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 39% (gap-down >1% 25% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −1.05% (p90 −2.94%) · haut méd +0.83% · range méd 2.3%
- Excursion ouverture 15min (n=160) : bas méd −1.36% (p90 −4.35%) · haut méd +1.03% · range méd 3.01%
- Excursion ouverture 30min (n=160) : bas méd −1.49% (p90 −4.93%) · haut méd +1.18% · range méd 3.44%
- Excursion ouverture 60min (n=160) : bas méd −1.64% (p90 −5.03%) · haut méd +1.23% · range méd 3.66%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 155.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 74% (122/159) · gap 32% · délai 0.2min · rebond 72% (87/122) (MFE +2.14%)
   - −1.0% : fill 30min 56% · séance 71% (113/159) · gap 25% · délai 0.2min · rebond 73% (83/113) (MFE +2.02%)
   - −1.5% : fill 30min 49% · séance 61% (103/159) · gap 18% · délai 0.5min · rebond 75% (78/103) (MFE +2.32%)
   - −2.0% : fill 30min 42% · séance 59% (96/159) · gap 16% · délai 4.8min · rebond 74% (75/96) (MFE +2.42%)
   - −3.0% : fill 30min 27% · séance 43% (75/159) · gap 8% · délai 3.3min · rebond 75% (63/75) (MFE +3.18%)
   - −4.0% : fill 30min 20% · séance 36% (64/159) · gap 5% · délai 15.0min · rebond 77% (53/64) (MFE +2.54%)
   - −5.0% : fill 30min 13% · séance 28% (50/159) · gap 2% · délai 53.0min · rebond 67% (38/50) (MFE +2.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −3.4%) → stop au-delà de −2.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.39%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.91% (p90 −2.29%) → stop au-delà de −1.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1337 jambes) : jambe baissière méd −1.25% (p90 −3.04%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 98% (54/56) · rebond 67% (36/54)
      · −2.0% : fill 95% (52/56) · rebond 72% (39/52)
      · −3.0% : fill 76% (45/56) · rebond 73% (37/45)
      · −4.0% : fill 66% (39/56) · rebond 85% (35/39)
      · −5.0% : fill 53% (32/56) · rebond 74% (26/32)
   - **flat** (13 séances) :
      · −1.0% : fill 78% (11/13) · rebond 86% (9/11)
      · −2.0% : fill 68% (10/13) · rebond 88% (9/10)
      · −3.0% : fill 66% (9/13) · rebond 64% (7/9)
      · −4.0% : fill 60% (8/13) · rebond 79% (6/8)
      · −5.0% : fill 44% (7/13) · rebond 45% (5/7)
   - **gap-up** (90 séances) :
      · −1.0% : fill 54% (48/90) · rebond 77% (38/48)
      · −2.0% : fill 35% (34/90) · rebond 73% (27/34)
      · −3.0% : fill 19% (21/90) · rebond 87% (19/21)
      · −4.0% : fill 14% (17/90) · rebond 56% (12/17)
      · −5.0% : fill 11% (11/90) · rebond 60% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 66% si les 15 1res min sont vertes (76 cas) · 39% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 76% si début vert vs 31% si rouge (base 51% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **76%** · continue >prix actuel 59% ; creux résiduel méd -1.34% (q20 -3.88%) → **SL/trailing à −3.88%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.91% / q75 +5.26% → **scale +2.91% / runner +5.26%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **31%** (continue à baisser 52%) → **RÉDUIRE ~69%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.35%** (au-delà de la MAE q10 -7.35%), cible rebond +2.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.68% .. +5.83%] · haut q95 +6.54% · bas q05 -5.97%
   - 60min (n=160) : retour [-5.47% .. +4.95%] · haut q95 +7.78% · bas q05 -6.6%
   - 2h (n=160) : retour [-6.07% .. +5.62%] · haut q95 +7.85% · bas q05 -7.55%
   - 4h (n=160) : retour [-7.02% .. +7.22%] · haut q95 +8.76% · bas q05 -8.23%
   - 6h (n=160) : retour [-8.01% .. +8.63%] · haut q95 +9.19% · bas q05 -9.44%
   - session (n=160) : retour [-8.05% .. +8.95%] · haut q95 +12.03% · bas q05 -11.17%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **42%**. Lecture précoce 30 min : signature présente → 24% vs absente 2% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.39% / p90 1.98%) · ~4.89 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **90%** (reprise méd 25.0 min, n=57)
   - −1.0% → **90%** (reprise méd 45.44 min, n=31)
   - −1.5% → **80%** (reprise méd 50.92 min, n=16)
   - −2.0% → **85%** (reprise méd 52.07 min, n=12)
   - −3.0% → **100%** (reprise méd 60.96 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.98%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +8.74% (q75 +9.15% / q95 +13.89%), MFE méd +9.28% / q90 +14.1%
   - Échelle scale-out : +9.28% (33%) / +9.96% (33%) / +14.1% (34%)
- **DÉSARMER** : repli > **−1.98%** depuis le plus-haut = décay → P(retournement) **15%** (préavis méd 36.46 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.1% : P(retournement après) 0% (mèche méd 2.71%)
- **CONTEXTE** : la dernière heure tient les gains 79% du temps (retour médian dernière heure +1.27%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.5 · part idiosyncratique 0.5
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 61.9  _(momentum haussier)_
- **ADX** : 25.9  _(tendance etablie)_
- **MACD** : hist 0.705  _(pas de croisement recent)_
- **BB** : %B 0.85 · largeur 29.1%
- **ATR** : 10.16 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.117  _(accumulation)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 50.4  _(transition)_
- **MA** : MA20 141.54 · MA50 125.18 · MA200 91.44  _(prix > MA20)_
- **Dist MA** : MA20 +10.2% · MA50 +24.6% · MA200 +70.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (850046 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
