# SMCI

**Generated** : 2026-08-31T00:25:07.508741+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $37.08  

> 🟡 **WAIT-FOR-DIP** — spot +8.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $37.08 (+8.8% vs entrée) · entrée $34.09 · stop $31.43 · T1 $36.49 · R/R 0.9  
> ↳ P(T1 av. stop) 57 % · EV/risk 0.127 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $33.61–$34.57 (mid $34.09)
- Spot actuel : $37.08 (+8.8% au-dessus de la zone — repli à attendre)
- Stop : $31.43 (stop swing_plan-based (-15.23%))
- Targets : T1 $36.49 · R/R 0.9 | T2 $38.89 · R/R 1.8 | T3 $41.29 · R/R 2.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $31.43


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.23 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1254).
   - exécution **9.427 pt plus bas** dans le cas TYPIQUE (médiane), 12.945 au p90, **13.821 au pire**
   - perte réelle **23.404 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 15.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0326 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.763 % | p01 -10.29 % | pire -29.051 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.512** [0.4379 ; 0.5857] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3896** [0.3393 ; 0.4418] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3066** [0.2598 ; 0.3567] _(largeur 9.7 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.9 pt), swing (56.8 pt), deep (53.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.76 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.30 % contre 7.19 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.68 % vs -16.02 % si l'on extrapolait par √5 _(rapport 1.042 ; < 1 = le √5 surestime)_
- **β de baisse : 1.537** (β de hausse 1.2402, asymétrie 1.2393) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.943× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 32.6836 sur swing_based (1.33 ATR, 11.857 %) — p(stop avant cible) 0.3534 [0.30 ; 0.40], R/R 1.42, perte reelle 18.539 % (gap inclus), CVaR 11.91 %, EV 0.2667 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.33 ATR (stop 11.857 %) — p(stop avant cible) 0.3534 [0.30 ; 0.40], R/R 1.42, perte reelle 18.539 % (gap inclus), EV 0.2667 % — **REFUSE**
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 2.15 ATR (stop 17.756 %) — p(stop avant cible) 0.1865 [0.15 ; 0.23], R/R 1.056, perte reelle 24.92 % (gap inclus), EV 1.5034 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.78 % > budget 12.00 %
   - 🟢 support a 3.53 ATR (stop 27.631 %) — p(stop avant cible) 0.093 [0.07 ; 0.13], R/R 0.906, perte reelle 29.051 % (gap inclus), EV 2.2164 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.63 % > budget 12.00 %
   - 🟢 support a 4.4 ATR (stop 33.834 %) — p(stop avant cible) 0.0725 [0.05 ; 0.10], R/R 0.778, perte reelle 33.834 % (gap inclus), EV 1.939 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.83 % > budget 12.00 %
   - 🟢 support a 5.16 ATR (stop 39.309 %) — p(stop avant cible) 0.0176 [0.01 ; 0.04], R/R 0.67, perte reelle 39.309 % (gap inclus), EV 2.086 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.31 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.789 %) — p(stop avant cible) 0.8976 [0.86 ; 0.93], R/R 5.865, perte reelle 4.488 % (gap inclus), EV -1.7568 % — **REFUSE**
      - refuse : cible atteinte seulement 7.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.898, borne haute 0.926 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 7.5 % x 26.32 % + P(rien) 2.7 % x 10.74 % ne couvrent pas P(stop) 89.8 % x 4.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.578 %) — p(stop avant cible) 0.7652 [0.72 ; 0.81], R/R 3.61, perte reelle 7.292 % (gap inclus), EV -1.2326 % — **REFUSE**
      - refuse : cible atteinte seulement 13.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.765, borne haute 0.807 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.23 %) : P(cible) 13.6 % x 26.32 % + P(rien) 9.9 % x 7.75 % ne couvrent pas P(stop) 76.5 % x 7.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.367 %) — p(stop avant cible) 0.6745 [0.62 ; 0.72], R/R 2.346, perte reelle 11.218 % (gap inclus), EV -2.1968 % — **REFUSE**
      - refuse : p_stop_first 0.674, borne haute 0.722 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 16.1 % x 26.32 % + P(rien) 16.5 % x 6.92 % ne couvrent pas P(stop) 67.5 % x 11.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 7.156 %) — p(stop avant cible) 0.5746 [0.52 ; 0.63], R/R 1.943, perte reelle 13.549 % (gap inclus), EV -1.5995 % — **REFUSE**
      - refuse : p_stop_first 0.575, borne haute 0.626 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 17.9 % x 26.32 % + P(rien) 24.7 % x 6.00 % ne couvrent pas P(stop) 57.5 % x 13.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 19.68 %) — p(stop avant cible) 0.1563 [0.12 ; 0.20], R/R 0.98, perte reelle 26.856 % (gap inclus), EV 1.7129 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.70 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 21.469 %) — p(stop avant cible) 0.144 [0.11 ; 0.18], R/R 0.98, perte reelle 26.856 % (gap inclus), EV 1.8758 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.48 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 28.625 %) — p(stop avant cible) 0.0914 [0.06 ; 0.13], R/R 0.906, perte reelle 29.051 % (gap inclus), EV 2.2233 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.63 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 42.938 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.613, perte reelle 42.938 % (gap inclus), EV 2.1092 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.94 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 46.516 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.566, perte reelle 46.516 % (gap inclus), EV 2.1025 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.52 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 50.094 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.525, perte reelle 50.094 % (gap inclus), EV 2.1023 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.09 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 53.673 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.49, perte reelle 53.673 % (gap inclus), EV 2.0962 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.67 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 57.251 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.46, perte reelle 57.251 % (gap inclus), EV 2.0953 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.25 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 37.08, ATR14 2.6536 (7.156 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 2.476 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.358 % | 36.9473 | 90.44 % | 93.15 % | 94.56 % | 95.15 % | 96.35 % | 97.54 % |
| 0.1 ATR | 0.716 % | 36.8146 | 82.19 % | 87.11 % | 89.11 % | 91.21 % | 92.99 % | 94.87 % |
| 0.15 ATR | 1.073 % | 36.682 | 75.05 % | 81.97 % | 84.88 % | 88.18 % | 90.56 % | 93.64 % |
| 0.2 ATR | 1.431 % | 36.5493 | 68.11 % | 77.24 % | 80.44 % | 85.66 % | 89.14 % | 92.31 % |
| 0.25 ATR | 1.789 % | 36.4166 | 62.07 % | 72.71 % | 76.31 % | 82.32 % | 87.11 % | 90.77 % |
| 0.35 ATR | 2.505 % | 36.1513 | 49.5 % | 63.65 % | 69.86 % | 77.37 % | 82.74 % | 88.31 % |
| 0.5 ATR | 3.578 % | 35.7532 | 35.01 % | 50.05 % | 58.47 % | 68.89 % | 76.95 % | 84.21 % |
| 0.75 ATR | 5.367 % | 35.0898 | 17.3 % | 33.53 % | 43.15 % | 55.25 % | 66.5 % | 76.1 % |
| 1.0 ATR | 7.156 % | 34.4264 | 8.15 % | 22.05 % | 31.05 % | 44.24 % | 57.46 % | 69.23 % |
| 1.25 ATR | 8.945 % | 33.763 | 3.92 % | 15.11 % | 22.98 % | 33.94 % | 48.83 % | 62.26 % |
| 1.5 ATR | 10.735 % | 33.0996 | 1.51 % | 9.77 % | 16.63 % | 26.87 % | 42.54 % | 55.79 % |
| 2.0 ATR | 14.313 % | 31.7729 | 0.3 % | 3.63 % | 8.57 % | 16.46 % | 30.46 % | 44.51 % |
| 2.5 ATR | 17.891 % | 30.4461 | 0.2 % | 1.61 % | 4.44 % | 10.0 % | 20.3 % | 32.51 % |
| 3.0 ATR | 21.469 % | 29.1193 | 0.2 % | 1.21 % | 2.62 % | 5.76 % | 14.72 % | 24.62 % |
| 4.0 ATR | 28.625 % | 26.4657 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.51 % | 14.36 % |
| 6.0 ATR | 42.938 % | 21.1586 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.19 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.58 ATR | 0.76 ATR | 0.94 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.96 ATR | 1.19 ATR | 1.37 ATR | 1.91 ATR | 2.43 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.98 ATR | 1.28 ATR | 1.59 ATR | 1.83 ATR | 2.50 ATR | 3.24 ATR |
| **10 s.** | 0.55 ATR | 1.22 ATR | 1.40 ATR | 1.90 ATR | 2.27 ATR | 2.53 ATR | 3.65 ATR | 4.92 ATR |
| **20 s.** | 0.79 ATR | 1.76 ATR | 1.98 ATR | 2.48 ATR | 2.98 ATR | 3.45 ATR | 4.99 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.397–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.576–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.367 %, prix 35.0899), p(touche) 33.53 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.72–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.367 %, prix 35.0899), p(touche) 43.15 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.983–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.945 %, prix 33.7632), p(touche) 33.94 % (en stress 89.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.402–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.735 %, prix 33.0995), p(touche) 42.54 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.978–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.891 %, prix 30.446), p(touche) 32.51 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.022 | EV/share : $0.058 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 23 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 83.7 | bear 5.6 | side 10.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 593.0 (= 16 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.673% → cible +3.149% / stop −2.229%, p_fill 31%, n_eff≈15.9) : P(cible|rempli) **37%** · **EV/risk +0.038** (×p_fill ; si rempli +0.27% du capital)
  - **swing** (entrée dip −8.074% → cible +7.041% / stop −7.785%, p_fill 18%, n_eff≈8.9) : P(cible|rempli) **60%** · **EV/risk +0.037** (×p_fill ; si rempli +1.58% du capital)
  - **deep** (entrée dip −12.475% → cible +9.957% / stop −12.265%, p_fill 14%, n_eff≈10.1) : P(cible|rempli) **63%** · **EV/risk +0.014** (×p_fill ; si rempli +1.23% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→76% · +2.0%→60% · +3.0%→46% · +5.0%→28% · +8.0%→12%
- Range intraday médian 6.47% (p90 10.79%) · excursion haute méd. +2.53% / basse méd. −2.68%
- Profil de vol intra : ouverture 4.165% vs midi 1.268% vs clôture 1.642% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓1% ; spike-down 72% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.03)_ ; drift intra méd. -0.066% ; recovery-V 25%
- **σ réalisé intraday** 3.99% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 70% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 37.2164 (VA 36.9059–37.8891 ; dernier close 37.08)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 81% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.59% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.33% · baisse 43% (gap-down >1% 34% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −2.79%) · haut méd +1.02% · range méd 2.24%
- Excursion ouverture 15min (n=160) : bas méd −1.26% (p90 −3.4%) · haut méd +1.46% · range méd 2.95%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.86%) · haut méd +1.56% · range méd 3.74%
- Excursion ouverture 60min (n=160) : bas méd −1.68% (p90 −4.55%) · haut méd +1.84% · range méd 4.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 37.08 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 72% (120/159) · gap 40% · délai 0.0min · rebond 56% (72/120) (MFE +1.26%)
   - −1.0% : fill 30min 53% · séance 68% (111/159) · gap 34% · délai 0.0min · rebond 60% (65/111) (MFE +1.38%)
   - −1.5% : fill 30min 46% · séance 62% (100/159) · gap 23% · délai 0.1min · rebond 67% (62/100) (MFE +1.55%)
   - −2.0% : fill 30min 41% · séance 53% (87/159) · gap 17% · délai 0.9min · rebond 70% (56/87) (MFE +1.73%)
   - −3.0% : fill 30min 30% · séance 49% (76/159) · gap 11% · délai 10.4min · rebond 60% (46/76) (MFE +1.7%)
   - −4.0% : fill 30min 19% · séance 38% (57/159) · gap 6% · délai 29.1min · rebond 76% (38/57) (MFE +1.74%)
   - −5.0% : fill 30min 14% · séance 30% (47/159) · gap 4% · délai 42.3min · rebond 81% (35/47) (MFE +2.59%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.85%) → stop au-delà de −1.66% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.99%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.83%) → stop au-delà de −1.93% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=905 jambes) : jambe baissière méd −1.2% (p90 −2.87%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 96% (67/69) · rebond 48% (34/67)
      · −2.0% : fill 91% (63/69) · rebond 65% (37/63)
      · −3.0% : fill 88% (58/69) · rebond 55% (33/58)
      · −4.0% : fill 70% (45/69) · rebond 76% (30/45)
      · −5.0% : fill 56% (38/69) · rebond 80% (28/38)
   - **flat** (13 séances) :
      · −1.0% : fill 100% (13/13) · rebond 92% (11/13)
      · −2.0% : fill 41% (6/13) · rebond 89% (4/6)
      · −3.0% : fill 26% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 22% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (77 séances) :
      · −1.0% : fill 40% (31/77) · rebond 75% (20/31)
      · −2.0% : fill 22% (18/77) · rebond 81% (15/18)
      · −3.0% : fill 18% (15/77) · rebond 70% (10/15)
      · −4.0% : fill 13% (10/77) · rebond 71% (6/10)
      · −5.0% : fill 12% (9/77) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 65% si les 15 1res min sont vertes (78 cas) · 20% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 71% si début vert vs 17% si rouge (base 43% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **71%** · continue >prix actuel 46% ; creux résiduel méd -2.28% (q20 -3.75%) → **SL/trailing à −3.75%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.16% / q75 +3.98% → **scale +2.16% / runner +3.98%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **17%** (continue à baisser 52%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.75%** (au-delà de la MAE q10 -5.75%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.28% .. +4.71%] · haut q95 +6.07% · bas q05 -4.54%
   - 60min (n=160) : retour [-4.57% .. +5.48%] · haut q95 +6.59% · bas q05 -5.38%
   - 2h (n=160) : retour [-4.73% .. +6.66%] · haut q95 +8.35% · bas q05 -5.86%
   - 4h (n=160) : retour [-5.23% .. +7.21%] · haut q95 +8.7% · bas q05 -6.79%
   - 6h (n=160) : retour [-5.71% .. +6.87%] · haut q95 +9.41% · bas q05 -6.91%
   - session (n=160) : retour [-6.9% .. +7.79%] · haut q95 +9.45% · bas q05 -7.56%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.64%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 63.2  _(momentum haussier)_
- **ADX** : 25.6  _(tendance etablie)_
- **MACD** : hist 0.038  _(pas de croisement recent)_
- **BB** : %B 0.63 · largeur 41.4%
- **ATR** : 2.65 (75.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.006  _(neutre)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 44.8  _(transition)_
- **MA** : MA20 35.17 · MA50 31.21 · MA200 31.34  _(prix > MA20)_
- **Dist MA** : MA20 +5.4% · MA50 +18.8% · MA200 +18.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (884746 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
