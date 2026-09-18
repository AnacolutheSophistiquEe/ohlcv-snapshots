# SOI

**Generated** : 2026-09-18T00:14:22.121209+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 10/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €141.95  

> 🟡 **WAIT-FOR-DIP** — spot +1.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €141.95 (+1.1% vs entrée) · entrée €140.40 · stop €136.22 · T1 €148.75 · R/R 2.0  
> ↳ P(T1 av. stop) 12 % _(réel 5 s)_ · EV/risk 0.01 _(réel 5 s)_ (GBM 0.094) · ¼-Kelly 0.026 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.97% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 371 % hors [0,100] (R² max 0.28). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 10/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €139.46–€141.34 (mid €140.40)
- Spot actuel : €141.95 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : €136.22 (stop swing_plan-based (-10.3%))
- Targets : T1 €148.75 · R/R 2.0 | T2 €151.61 · R/R 2.68 | T3 €154.47 · R/R 3.37
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €136.22


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.91 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.3 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1279).
   - exécution **8.419 pt plus bas** dans le cas TYPIQUE (médiane), 16.879 au p90, **18.994 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 10.3 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0262 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.677 % | p01 -5.133 % | pire -29.294 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.409** [0.3378 ; 0.4832] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.3294** [0.2814 ; 0.3802] _(largeur 9.9 pt, n_eff 345.8)_
   - deep : **0.3267** [0.2789 ; 0.3774] _(largeur 9.9 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.5 pt), swing (37.2 pt), deep (34.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-14.04 %** | vol 6.64 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.17 % contre 7.69 % aujourd'hui, rapport 0.41)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.31 % vs -11.44 % si l'on extrapolait par √5 _(rapport 1.075 ; < 1 = le √5 surestime)_
- **β de baisse : 1.121** (β de hausse 1.5766, asymétrie 0.711) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.058× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 124.3005 sur support (1.24 ATR, 12.434 %) — p(stop avant cible) 0.3566 [0.31 ; 0.41], R/R 0.908, perte reelle 21.456 % (gap inclus), CVaR 12.455 %, EV -1.7484 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0379 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.46 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.58 ATR (stop 7.22 %) — p(stop avant cible) 0.5548 [0.50 ; 0.61], R/R 1.271, perte reelle 15.318 % (gap inclus), EV -2.9472 % — **REFUSE**
      - refuse : p_stop_first 0.555, borne haute 0.607 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.55 ATR du spot — compartiment <1, mesure a 50.6 % de casse (IC clusterise [0.471 ; 0.543] sur 1124 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.95 %) : P(cible) 23.6 % x 19.47 % + P(rien) 21.0 % x 4.60 % ne couvrent pas P(stop) 55.5 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.24 ATR (stop 12.434 %) — p(stop avant cible) 0.3566 [0.31 ; 0.41], R/R 0.908, perte reelle 21.456 % (gap inclus), EV -1.7484 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.75 %) : P(cible) 29.1 % x 19.47 % + P(rien) 35.2 % x 0.67 % ne couvrent pas P(stop) 35.7 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.23 ATR (stop 20.183 %) — p(stop avant cible) 0.1414 [0.11 ; 0.18], R/R 0.665, perte reelle 29.294 % (gap inclus), EV 0.934 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.19 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.974 %) — p(stop avant cible) 0.8246 [0.78 ; 0.86], R/R 4.955, perte reelle 3.93 % (gap inclus), EV -0.3606 % — **REFUSE**
      - refuse : cible atteinte seulement 12.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.825, borne haute 0.862 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 12.7 % x 19.47 % + P(rien) 4.9 % x 8.46 % ne couvrent pas P(stop) 82.5 % x 3.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 13.821 %) — p(stop avant cible) 0.3146 [0.27 ; 0.36], R/R 0.908, perte reelle 21.456 % (gap inclus), EV -0.93 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 29.6 % x 19.47 % + P(rien) 39.0 % x 0.16 % ne couvrent pas P(stop) 31.5 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 21.719 %) — p(stop avant cible) 0.103 [0.07 ; 0.14], R/R 0.665, perte reelle 29.294 % (gap inclus), EV 1.5137 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.72 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 23.693 %) — p(stop avant cible) 0.0701 [0.05 ; 0.10], R/R 0.665, perte reelle 29.294 % (gap inclus), EV 2.1535 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.70 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 27.642 %) — p(stop avant cible) 0.0457 [0.03 ; 0.07], R/R 0.665, perte reelle 29.294 % (gap inclus), EV 2.3899 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.64 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 31.591 %) — p(stop avant cible) 0.0307 [0.02 ; 0.05], R/R 0.616, perte reelle 31.591 % (gap inclus), EV 2.4279 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.59 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 35.539 %) — p(stop avant cible) 0.0209 [0.01 ; 0.04], R/R 0.548, perte reelle 35.539 % (gap inclus), EV 2.4032 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.54 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 39.488 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 0.493, perte reelle 39.488 % (gap inclus), EV 2.4208 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.49 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 43.437 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.448, perte reelle 43.437 % (gap inclus), EV 2.473 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.44 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 47.386 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.411, perte reelle 47.386 % (gap inclus), EV 2.473 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.39 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 51.335 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.379, perte reelle 51.335 % (gap inclus), EV 2.473 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.33 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 55.284 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.352, perte reelle 55.284 % (gap inclus), EV 2.473 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.28 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 59.232 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.329, perte reelle 59.232 % (gap inclus), EV 2.473 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 59.23 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 63.181 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.308, perte reelle 63.181 % (gap inclus), EV 2.473 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 63.18 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 141.95, ATR14 11.2107 (7.898 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 2.827 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.395 % | 141.3895 | 91.17 % | 94.2 % | 95.58 % | 96.65 % | 97.72 % | 98.7 % |
| 0.1 ATR | 0.79 % | 140.8289 | 84.89 % | 89.98 % | 91.94 % | 94.48 % | 96.14 % | 97.4 % |
| 0.15 ATR | 1.185 % | 140.2684 | 77.92 % | 85.07 % | 87.81 % | 91.03 % | 93.66 % | 95.3 % |
| 0.2 ATR | 1.58 % | 139.7079 | 69.28 % | 79.86 % | 83.87 % | 88.08 % | 91.39 % | 93.4 % |
| 0.25 ATR | 1.974 % | 139.1473 | 62.81 % | 76.03 % | 80.63 % | 86.4 % | 90.1 % | 92.8 % |
| 0.35 ATR | 2.764 % | 138.0262 | 50.83 % | 67.68 % | 73.65 % | 81.28 % | 85.74 % | 90.2 % |
| 0.5 ATR | 3.949 % | 136.3446 | 36.02 % | 55.5 % | 62.93 % | 73.3 % | 80.99 % | 87.5 % |
| 0.75 ATR | 5.923 % | 133.542 | 17.17 % | 35.46 % | 47.0 % | 58.52 % | 72.77 % | 81.2 % |
| 1.0 ATR | 7.898 % | 130.7393 | 8.44 % | 24.17 % | 34.41 % | 47.68 % | 64.65 % | 75.8 % |
| 1.25 ATR | 9.872 % | 127.9366 | 4.12 % | 15.82 % | 25.47 % | 37.44 % | 56.44 % | 70.0 % |
| 1.5 ATR | 11.846 % | 125.1339 | 2.26 % | 10.61 % | 18.58 % | 29.95 % | 48.71 % | 63.7 % |
| 2.0 ATR | 15.795 % | 119.5286 | 0.59 % | 4.52 % | 8.95 % | 18.33 % | 34.95 % | 53.1 % |
| 2.5 ATR | 19.744 % | 113.9232 | 0.29 % | 2.46 % | 4.92 % | 11.82 % | 24.06 % | 45.0 % |
| 3.0 ATR | 23.693 % | 108.3179 | 0.2 % | 0.79 % | 2.56 % | 7.09 % | 16.63 % | 36.9 % |
| 4.0 ATR | 31.591 % | 97.1071 | 0.1 % | 0.59 % | 1.38 % | 3.55 % | 9.5 % | 23.4 % |
| 6.0 ATR | 47.386 % | 74.6857 | 0.0 % | 0.29 % | 0.79 % | 1.58 % | 4.46 % | 12.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.63 ATR | 0.80 ATR | 0.98 ATR | 1.12 ATR | 1.55 ATR | 1.96 ATR |
| **3 s.** | 0.33 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.27 ATR | 1.45 ATR | 1.95 ATR | 2.49 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.06 ATR | 1.40 ATR | 1.71 ATR | 1.93 ATR | 2.69 ATR | 3.59 ATR |
| **10 s.** | 0.68 ATR | 1.46 ATR | 1.64 ATR | 2.09 ATR | 2.46 ATR | 2.77 ATR | 3.93 ATR | 5.79 ATR |
| **20 s.** | 1.03 ATR | 2.19 ATR | 2.50 ATR | 3.29 ATR | 3.88 ATR | 4.60 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.631–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.79–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.065–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.635–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.5–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.094 | EV/share : €0.393 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 30 % | T3 30 %
- Kelly (position) : f* 0.105 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 27.5 | bear 16.8 | side 55.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 568.0 (= 4 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.089% → cible +5.947% / stop −2.974%, p_fill 71%, n_eff≈31.6) : P(cible|rempli) **12%** · **EV/risk +0.010** (×p_fill ; si rempli +0.04% du capital)
  - **swing** (entrée dip −2.402% → cible +7.471% / stop −8.092%, p_fill 60%, n_eff≈24.9) : P(cible|rempli) **56%** · **EV/risk +0.051** (×p_fill ; si rempli +0.69% du capital)
  - **deep** (entrée dip −3.714% → cible +10.565% / stop −12.303%, p_fill 72%, n_eff≈30.0) : P(cible|rempli) **41%** · **EV/risk -0.161** (×p_fill ; si rempli -2.76% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→64% · +3.0%→50% · +5.0%→31% · +8.0%→9%
- Range intraday médian 7.57% (p90 13.58%) · excursion haute méd. +3.14% / basse méd. −2.94%
- Profil de vol intra : ouverture 4.623% vs midi 1.318% vs clôture 1.973% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑0%/↓2% ; spike-down 71% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. -0.422% ; recovery-V 38%
- **σ réalisé intraday** 4.323% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 56% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 128.644 (VA 127.828–129.324 ; dernier close 127.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 44% · rebond 81% · **stop −7.63%** sous le fill (sous le bruit) · cible +3.11% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.59% · baisse 37% (gap-down >1% 26% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.11% (p90 −3.4%) · haut méd +0.9% · range méd 2.7%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −4.51%) · haut méd +1.25% · range méd 3.23%
- Excursion ouverture 30min (n=160) : bas méd −1.48% (p90 −5.08%) · haut méd +1.36% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.55% (p90 −5.31%) · haut méd +1.64% · range méd 3.96%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 128.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 74% (124/159) · gap 33% · délai 0.1min · rebond 68% (87/124) (MFE +1.75%)
   - −1.0% : fill 30min 56% · séance 69% (113/159) · gap 26% · délai 0.2min · rebond 76% (84/113) (MFE +1.99%)
   - −1.5% : fill 30min 48% · séance 61% (104/159) · gap 20% · délai 0.3min · rebond 76% (77/104) (MFE +2.3%)
   - −2.0% : fill 30min 41% · séance 56% (93/159) · gap 18% · délai 0.4min · rebond 70% (70/93) (MFE +2.4%)
   - −3.0% : fill 30min 31% · séance 44% (77/159) · gap 9% · délai 1.5min · rebond 81% (65/77) (MFE +3.11%)
   - −4.0% : fill 30min 24% · séance 37% (64/159) · gap 5% · délai 10.8min · rebond 76% (54/64) (MFE +3.3%)
   - −5.0% : fill 30min 15% · séance 30% (49/159) · gap 2% · délai 31.6min · rebond 72% (39/49) (MFE +2.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −3.45%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.4%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −2.25%) → stop au-delà de −1.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1344 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 97% (54/56) · rebond 67% (36/54)
      · −2.0% : fill 93% (51/56) · rebond 68% (38/51)
      · −3.0% : fill 81% (46/56) · rebond 81% (39/46)
      · −4.0% : fill 67% (39/56) · rebond 89% (36/39)
      · −5.0% : fill 54% (31/56) · rebond 77% (26/31)
   - **flat** (13 séances) :
      · −1.0% : fill 93% (10/13) · rebond 77% (8/10)
      · −2.0% : fill 73% (9/13) · rebond 78% (8/9)
      · −3.0% : fill 70% (8/13) · rebond 78% (7/8)
      · −4.0% : fill 56% (7/13) · rebond 58% (5/7)
      · −5.0% : fill 56% (7/13) · rebond 72% (6/7)
   - **gap-up** (90 séances) :
      · −1.0% : fill 51% (49/90) · rebond 84% (40/49)
      · −2.0% : fill 33% (33/90) · rebond 73% (24/33)
      · −3.0% : fill 21% (23/90) · rebond 82% (19/23)
      · −4.0% : fill 18% (18/90) · rebond 57% (13/18)
      · −5.0% : fill 14% (11/90) · rebond 59% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 62% si les 15 1res min sont vertes (77 cas) · 36% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 72% si début vert vs 25% si rouge (base 49% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **72%** · continue >prix actuel 49% ; creux résiduel méd -1.81% (q20 -4.92%) → **SL/trailing à −4.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.35% / q75 +4.48% → **scale +2.35% / runner +4.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **25%** (continue à baisser 65%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.65%** (au-delà de la MAE q10 -8.65%), cible rebond +2.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.59% .. +6.13%] · haut q95 +7.22% · bas q05 -5.93%
   - 60min (n=160) : retour [-5.37% .. +6.48%] · haut q95 +7.85% · bas q05 -6.55%
   - 2h (n=160) : retour [-6.01% .. +5.93%] · haut q95 +9.18% · bas q05 -7.41%
   - 4h (n=160) : retour [-6.77% .. +7.89%] · haut q95 +10.91% · bas q05 -8.1%
   - 6h (n=160) : retour [-7.61% .. +9.07%] · haut q95 +12.33% · bas q05 -9.35%
   - session (n=160) : retour [-11.05% .. +10.07%] · haut q95 +13.99% · bas q05 -12.6%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 8% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.06% (p75 1.5% / p90 2.89%) · ~5.05 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **89%** (reprise méd 20.0 min, n=60)
   - −1.0% → **82%** (reprise méd 34.22 min, n=34)
   - −1.5% → **69%** (reprise méd 46.1 min, n=18)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.89%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +7.26% (q75 +13.51% / q95 +17.04%), MFE méd +8.03% / q90 +18.1%
   - Échelle scale-out : +8.03% (33%) / +14.35% (33%) / +18.1% (34%)
- **DÉSARMER** : repli > **−2.89%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.1% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +1.92%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 65.6  _(momentum haussier)_
- **ADX** : 21.7  _(pas de tendance nette)_
- **MACD** : hist 1.439  _(pas de croisement recent)_
- **BB** : %B 0.84 · largeur 46.7%
- **ATR** : 11.21 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.119  _(distribution)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 50.7  _(transition)_
- **MA** : MA20 122.42 · MA50 114.64 · MA200 85.32  _(prix > MA20)_
- **Dist MA** : MA20 +16.0% · MA50 +23.8% · MA200 +66.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (756272 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
