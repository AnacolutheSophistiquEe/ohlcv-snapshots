# SOI

**Generated** : 2026-09-30T00:14:23.642575+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €155.07  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €155.07 (+1.0% vs entrée) · entrée €153.49 · stop €149.66 · T1 €156.60 · R/R 0.81  
> ↳ ¼-Kelly 0.017 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €152.87–€154.12 (mid €153.49)
- Spot actuel : €155.07 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : €149.66 (plancher anti-bruit 5 s — stop EV-optimal −2.5% (first-passage 5 s réel) ; -2.50 % depuis l'entree)
- Targets : T1 €156.60 · R/R 0.81 | T2 €162.98 · R/R 2.48 | T3 €169.36 · R/R 4.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €149.66


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.91 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.4 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **7.319 pt plus bas** dans le cas TYPIQUE (médiane), 15.779 au p90, **17.894 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 11.4 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0236 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.675 % | p01 -5.132 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3979** [0.3272 ; 0.472] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.3153** [0.268 ; 0.3657] _(largeur 9.8 pt, n_eff 345.8)_
   - deep : **0.3782** [0.3283 ; 0.4302] _(largeur 10.2 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-14.04 %** | vol 6.66 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.89 % contre 7.48 % aujourd'hui, rapport 0.52)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.4 % vs -11.44 % si l'on extrapolait par √5 _(rapport 1.084 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1058** (β de hausse 1.575, asymétrie 0.7021) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.046× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 144.2854 sur support (0.59 ATR, 6.958 %) — p(stop avant cible) 0.5666 [0.51 ; 0.62], R/R 2.763, perte reelle 7.365 % (gap inclus), CVaR 11.364 %, EV 1.5832 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2028 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.567, borne haute 0.618 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.59 ATR (stop 6.958 %) — p(stop avant cible) 0.5666 [0.51 ; 0.62], R/R 2.763, perte reelle 7.365 % (gap inclus), EV 1.5832 % — **REFUSE**
      - refuse : p_stop_first 0.567, borne haute 0.618 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.59 ATR du spot — compartiment <1, mesure a 49.1 % de casse (IC clusterise [0.457 ; 0.522] sur 1123 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 10.381 %) — p(stop avant cible) 0.4208 [0.37 ; 0.47], R/R 1.884, perte reelle 10.802 % (gap inclus), EV 1.6357 % — **REFUSE**
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.90 % > budget 12.00 %
   - 🟢 support a 3.55 ATR (stop 27.432 %) — p(stop avant cible) 0.0448 [0.03 ; 0.07], R/R 0.732, perte reelle 27.787 % (gap inclus), EV 2.982 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.35 % > budget 12.00 %
   - 🟢 support a 4.62 ATR (stop 34.847 %) — p(stop avant cible) 0.0238 [0.01 ; 0.04], R/R 0.584, perte reelle 34.871 % (gap inclus), EV 2.9252 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.83 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.73 %) — p(stop avant cible) 0.8528 [0.81 ; 0.89], R/R 11.044, perte reelle 1.843 % (gap inclus), EV 0.8884 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 11.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.853, borne haute 0.887 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 8.651 %) — p(stop avant cible) 0.498 [0.45 ; 0.55], R/R 2.257, perte reelle 9.015 % (gap inclus), EV 1.4434 % — **REFUSE**
      - refuse : p_stop_first 0.498, borne haute 0.550 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.22 % > budget 12.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 12.111 %) — p(stop avant cible) 0.3686 [0.32 ; 0.42], R/R 1.629, perte reelle 12.491 % (gap inclus), EV 1.4823 % — **REFUSE**
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.91 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 13.841 %) — p(stop avant cible) 0.3156 [0.27 ; 0.37], R/R 1.433, perte reelle 14.201 % (gap inclus), EV 1.584 % — **REFUSE**
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.11 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 15.571 %) — p(stop avant cible) 0.2478 [0.20 ; 0.30], R/R 1.277, perte reelle 15.937 % (gap inclus), EV 1.9625 % — **REFUSE**
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.39 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 17.302 %) — p(stop avant cible) 0.2127 [0.17 ; 0.26], R/R 1.15, perte reelle 17.699 % (gap inclus), EV 2.1312 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.99 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 19.032 %) — p(stop avant cible) 0.172 [0.14 ; 0.21], R/R 1.047, perte reelle 19.443 % (gap inclus), EV 2.4613 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.45 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 20.762 %) — p(stop avant cible) 0.1055 [0.08 ; 0.14], R/R 0.954, perte reelle 21.325 % (gap inclus), EV 2.8075 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.95 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 38.063 %) — p(stop avant cible) 0.0101 [0.00 ; 0.03], R/R 0.534, perte reelle 38.143 % (gap inclus), EV 2.9547 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 41.524 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.49, perte reelle 41.524 % (gap inclus), EV 2.9883 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.53 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 44.984 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.452, perte reelle 44.984 % (gap inclus), EV 3.0033 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.23 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 48.444 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.42, perte reelle 48.444 % (gap inclus), EV 3.0033 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.23 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 51.905 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.392, perte reelle 51.905 % (gap inclus), EV 3.0033 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.23 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 55.365 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.368, perte reelle 55.365 % (gap inclus), EV 3.0033 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.23 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 155.075, ATR14 10.7321 (6.921 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 2.478 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.346 % | 154.5384 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.692 % | 154.0018 | 84.8 % | 89.79 % | 91.65 % | 94.29 % | 96.14 % | 97.4 % |
| 0.15 ATR | 1.038 % | 153.4652 | 77.84 % | 84.89 % | 87.52 % | 90.85 % | 93.67 % | 95.3 % |
| 0.2 ATR | 1.384 % | 152.9286 | 69.22 % | 79.69 % | 83.5 % | 87.8 % | 91.3 % | 93.31 % |
| 0.25 ATR | 1.73 % | 152.392 | 62.65 % | 75.86 % | 80.26 % | 86.12 % | 90.01 % | 92.71 % |
| 0.35 ATR | 2.422 % | 151.3187 | 50.78 % | 67.42 % | 73.18 % | 80.81 % | 85.66 % | 90.01 % |
| 0.5 ATR | 3.46 % | 149.7089 | 35.78 % | 55.25 % | 62.57 % | 72.83 % | 80.81 % | 87.21 % |
| 0.75 ATR | 5.19 % | 147.0259 | 16.96 % | 35.03 % | 46.56 % | 57.97 % | 72.5 % | 80.42 % |
| 1.0 ATR | 6.921 % | 144.3429 | 8.33 % | 23.85 % | 33.99 % | 47.15 % | 64.39 % | 74.93 % |
| 1.25 ATR | 8.651 % | 141.6598 | 4.12 % | 15.51 % | 24.95 % | 37.01 % | 56.18 % | 69.13 % |
| 1.5 ATR | 10.381 % | 138.9768 | 2.25 % | 10.4 % | 18.07 % | 29.43 % | 48.27 % | 62.84 % |
| 2.0 ATR | 13.841 % | 133.6107 | 0.59 % | 4.51 % | 8.84 % | 17.81 % | 34.62 % | 52.25 % |
| 2.5 ATR | 17.302 % | 128.2446 | 0.29 % | 2.45 % | 4.91 % | 11.61 % | 23.94 % | 44.36 % |
| 3.0 ATR | 20.762 % | 122.8786 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 16.42 % | 36.36 % |
| 4.0 ATR | 27.682 % | 112.1464 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.4 % | 23.18 % |
| 6.0 ATR | 41.524 % | 90.6822 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 11.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.56 ATR | 0.63 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.53 ATR | 1.96 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.78 ATR | 1.03 ATR | 1.25 ATR | 1.43 ATR | 1.94 ATR | 2.49 ATR |
| **5 s.** | 0.46 ATR | 0.93 ATR | 1.05 ATR | 1.38 ATR | 1.69 ATR | 1.91 ATR | 2.68 ATR | 3.59 ATR |
| **10 s.** | 0.68 ATR | 1.45 ATR | 1.62 ATR | 2.08 ATR | 2.45 ATR | 2.76 ATR | 3.92 ATR | 5.78 ATR |
| **20 s.** | 1.00 ATR | 2.14 ATR | 2.46 ATR | 3.25 ATR | 3.86 ATR | 4.57 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.408–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (60.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.627–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.781–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.921 %, prix 144.3423), p(touche) 33.99 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.053–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.62–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.459–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.026 | EV/share : €0.100 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 — | T3 —
- Kelly (position) : f* 0.068 | ¼-Kelly 0.017 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 15.5 | bear 5.0 | side 79.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 620.0 (= 4 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.015% → cible +2.024% / stop −2.5%, p_fill 80%, n_eff≈87.8) : P(cible|rempli) **48%** · **EV/risk -0.111** (×p_fill ; si rempli -0.34% du capital)
  - **swing** (entrée dip −2.242% → cible +18.736% / stop −9.368%, p_fill 68%, n_eff≈79.7) : P(cible|rempli) **23%** · **EV/risk -0.001** (×p_fill ; si rempli -0.02% du capital)
  - **deep** (entrée dip −3.469% → cible +10.896% / stop −10.754%, p_fill 76%, n_eff≈85.0) : P(cible|rempli) **44%** · **EV/risk -0.124** (×p_fill ; si rempli -1.76% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→66% · +3.0%→55% · +5.0%→38% · +8.0%→18%
- Range intraday médian 8.55% (p90 15.35%) · excursion haute méd. +3.44% / basse méd. −3.26%
- Profil de vol intra : ouverture 5.065% vs midi 1.637% vs clôture 2.274% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑0%/↓2% ; spike-down 71% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; mean-reverting — autocorr -0.065)_ ; drift intra méd. -0.356% ; recovery-V 38%
- **σ réalisé intraday** 4.387% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 56% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 128.644 (VA 127.828–129.324 ; dernier close 127.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 44% · rebond 82% · **stop −7.53%** sous le fill (sous le bruit) · cible +3.04% · R/R 0.4 (high win-rate)
- Gaps overnight (n=159) : méd. 0.59% · baisse 36% (gap-down >1% 25% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −1.1% (p90 −3.41%) · haut méd +0.9% · range méd 2.69%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −4.51%) · haut méd +1.25% · range méd 3.22%
- Excursion ouverture 30min (n=160) : bas méd −1.48% (p90 −5.08%) · haut méd +1.36% · range méd 3.53%
- Excursion ouverture 60min (n=160) : bas méd −1.54% (p90 −5.32%) · haut méd +1.59% · range méd 3.95%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 128.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 74% (123/159) · gap 32% · délai 0.2min · rebond 67% (84/123) (MFE +1.75%)
   - −1.0% : fill 30min 56% · séance 69% (112/159) · gap 25% · délai 0.2min · rebond 75% (83/112) (MFE +1.98%)
   - −1.5% : fill 30min 48% · séance 61% (104/159) · gap 20% · délai 0.4min · rebond 77% (79/104) (MFE +2.29%)
   - −2.0% : fill 30min 41% · séance 56% (94/159) · gap 17% · délai 0.6min · rebond 71% (72/94) (MFE +2.4%)
   - −3.0% : fill 30min 30% · séance 44% (76/159) · gap 9% · délai 1.5min · rebond 82% (65/76) (MFE +3.04%)
   - −4.0% : fill 30min 23% · séance 37% (63/159) · gap 5% · délai 10.8min · rebond 75% (51/63) (MFE +2.74%)
   - −5.0% : fill 30min 15% · séance 30% (48/159) · gap 1% · délai 33.1min · rebond 71% (38/48) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −3.46%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.41%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.87% (p90 −2.26%) → stop au-delà de −1.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1331 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 97% (52/54) · rebond 67% (35/52)
      · −2.0% : fill 93% (49/54) · rebond 67% (37/49)
      · −3.0% : fill 80% (43/54) · rebond 81% (37/43)
      · −4.0% : fill 66% (36/54) · rebond 88% (33/36)
      · −5.0% : fill 53% (29/54) · rebond 76% (24/29)
   - **flat** (14 séances) :
      · −1.0% : fill 93% (11/14) · rebond 78% (9/11)
      · −2.0% : fill 73% (10/14) · rebond 79% (9/10)
      · −3.0% : fill 70% (9/14) · rebond 78% (8/9)
      · −4.0% : fill 57% (8/14) · rebond 56% (5/8)
      · −5.0% : fill 55% (7/14) · rebond 73% (6/7)
   - **gap-up** (91 séances) :
      · −1.0% : fill 51% (49/91) · rebond 83% (39/49)
      · −2.0% : fill 35% (35/91) · rebond 74% (26/35)
      · −3.0% : fill 21% (24/91) · rebond 83% (20/24)
      · −4.0% : fill 18% (19/91) · rebond 56% (13/19)
      · −5.0% : fill 14% (12/91) · rebond 60% (8/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 62% si les 15 1res min sont vertes (77 cas) · 36% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 71% si début vert vs 26% si rouge (base 49% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **71%** · continue >prix actuel 49% ; creux résiduel méd -1.82% (q20 -4.93%) → **SL/trailing à −4.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.35% / q75 +4.36% → **scale +2.35% / runner +4.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **26%** (continue à baisser 64%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.65%** (au-delà de la MAE q10 -8.65%), cible rebond +2.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.6% .. +6.07%] · haut q95 +7.17% · bas q05 -5.93%
   - 60min (n=160) : retour [-5.38% .. +6.13%] · haut q95 +7.85% · bas q05 -6.55%
   - 2h (n=160) : retour [-6.02% .. +5.83%] · haut q95 +9.13% · bas q05 -7.42%
   - 4h (n=160) : retour [-6.79% .. +7.45%] · haut q95 +10.32% · bas q05 -8.11%
   - 6h (n=160) : retour [-7.62% .. +8.97%] · haut q95 +12.19% · bas q05 -9.36%
   - session (n=160) : retour [-11.07% .. +8.89%] · haut q95 +13.71% · bas q05 -12.62%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 5.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 8% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.06% (p75 1.5% / p90 2.89%) · ~5.06 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **89%** (reprise méd 20.0 min, n=60)
   - −1.0% → **82%** (reprise méd 34.26 min, n=34)
   - −1.5% → **69%** (reprise méd 46.21 min, n=18)
   - −2.0% → **87%** (reprise méd 49.49 min, n=15)
   - −3.0% → **100%** (reprise méd 61.93 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.89%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +7.26% (q75 +13.52% / q95 +17.07%), MFE méd +8.05% / q90 +18.11%
   - Échelle scale-out : +8.05% (33%) / +14.41% (33%) / +18.11% (34%)
- **DÉSARMER** : repli > **−2.89%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.11% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 95% du temps (retour médian dernière heure +1.89%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.49 · part idiosyncratique 0.51
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.1  _(momentum haussier)_
- **ADX** : 25.5  _(tendance etablie)_
- **MACD** : hist 0.465  _(pas de croisement recent)_
- **BB** : %B 0.84 · largeur 33.4%
- **ATR** : 10.73 (73.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.117  _(accumulation)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 53.8  _(transition)_
- **MA** : MA20 139.32 · MA50 123.98 · MA200 90.78  _(prix > MA20)_
- **Dist MA** : MA20 +11.3% · MA50 +25.1% · MA200 +70.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (845330 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
