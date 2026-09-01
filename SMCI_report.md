# SMCI

**Generated** : 2026-09-01T00:25:00.873783+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $37.28  

> 🟡 **WAIT-FOR-DIP** — spot +8.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $37.28 (+8.8% vs entrée) · entrée $34.25 · stop $31.59 · T1 $36.66 · R/R 0.91  
> ↳ P(T1 av. stop) 55 % · EV/risk 0.123 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $33.77–$34.73 (mid $34.25)
- Spot actuel : $37.28 (+8.8% au-dessus de la zone — repli à attendre)
- Stop : $31.59 (stop swing_plan-based (-15.25%))
- Targets : T1 $36.66 · R/R 0.91 | T2 $39.07 · R/R 1.81 | T3 $41.49 · R/R 2.72
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $31.59


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.25 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **9.407 pt plus bas** dans le cas TYPIQUE (médiane), 12.925 au p90, **13.801 au pire**
   - perte réelle **23.404 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 15.25 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0325 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.765 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5246** [0.4503 ; 0.5981] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3874** [0.3372 ; 0.4395] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3123** [0.2652 ; 0.3626] _(largeur 9.7 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.9 pt), swing (57.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.76 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.30 % contre 7.19 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.05 % si l'on extrapolait par √5 _(rapport 1.04 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5382** (β de hausse 1.2446, asymétrie 1.2358) vs IWM — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.953× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 33.2964 sur atr_based (1.5 ATR, 10.686 %) — p(stop avant cible) 0.4172 [0.37 ; 0.47], R/R 1.52, perte reelle 16.875 % (gap inclus), CVaR 10.75 %, EV -0.3976 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 19 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 61.4 % de la queue et il ne reste que 29.65 EUR a partager. Prix du risque 0.019 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.686 %) — p(stop avant cible) 0.4172 [0.37 ; 0.47], R/R 1.52, perte reelle 16.875 % (gap inclus), EV -0.3976 % — **REFUSE**
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 20.2 % x 25.64 % + P(rien) 38.1 % x 3.84 % ne couvrent pas P(stop) 41.7 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.4 ATR (stop 12.831 %) — p(stop avant cible) 0.3179 [0.27 ; 0.37], R/R 1.334, perte reelle 19.221 % (gap inclus), EV 0.3347 % — **REFUSE**
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.88 % > budget 12.00 %
   - ⚪ sr_based a 2.18 ATR (stop 18.345 %) — p(stop avant cible) 0.1691 [0.13 ; 0.21], R/R 1.029, perte reelle 24.92 % (gap inclus), EV 1.5973 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.37 % > budget 12.00 %
   - 🟢 support a 3.6 ATR (stop 28.52 %) — p(stop avant cible) 0.0909 [0.06 ; 0.12], R/R 0.883, perte reelle 29.051 % (gap inclus), EV 2.0677 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.52 % > budget 12.00 %
   - 🟢 support a 4.47 ATR (stop 34.69 %) — p(stop avant cible) 0.0721 [0.05 ; 0.10], R/R 0.739, perte reelle 34.69 % (gap inclus), EV 1.7232 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.69 % > budget 12.00 %
   - 🟢 support a 5.23 ATR (stop 40.135 %) — p(stop avant cible) 0.0137 [0.01 ; 0.03], R/R 0.639, perte reelle 40.135 % (gap inclus), EV 1.9513 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.13 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.781 %) — p(stop avant cible) 0.8974 [0.86 ; 0.93], R/R 5.733, perte reelle 4.473 % (gap inclus), EV -1.7834 % — **REFUSE**
      - refuse : cible atteinte seulement 7.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.897, borne haute 0.926 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.78 %) : P(cible) 7.6 % x 25.64 % + P(rien) 2.7 % x 10.65 % ne couvrent pas P(stop) 89.7 % x 4.47 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.562 %) — p(stop avant cible) 0.7655 [0.72 ; 0.81], R/R 3.517, perte reelle 7.292 % (gap inclus), EV -1.3197 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.765, borne haute 0.808 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.32 %) : P(cible) 13.7 % x 25.64 % + P(rien) 9.8 % x 7.70 % ne couvrent pas P(stop) 76.5 % x 7.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.343 %) — p(stop avant cible) 0.6761 [0.63 ; 0.72], R/R 2.286, perte reelle 11.218 % (gap inclus), EV -2.3249 % — **REFUSE**
      - refuse : p_stop_first 0.676, borne haute 0.724 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.32 %) : P(cible) 16.2 % x 25.64 % + P(rien) 16.2 % x 6.88 % ne couvrent pas P(stop) 67.6 % x 11.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 7.124 %) — p(stop avant cible) 0.5782 [0.53 ; 0.63], R/R 1.893, perte reelle 13.549 % (gap inclus), EV -1.7639 % — **REFUSE**
      - refuse : p_stop_first 0.578, borne haute 0.629 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 18.3 % x 25.64 % + P(rien) 23.9 % x 5.78 % ne couvrent pas P(stop) 57.8 % x 13.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 19.59 %) — p(stop avant cible) 0.1561 [0.12 ; 0.20], R/R 0.955, perte reelle 26.856 % (gap inclus), EV 1.5536 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.61 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 21.371 %) — p(stop avant cible) 0.1432 [0.11 ; 0.18], R/R 0.955, perte reelle 26.856 % (gap inclus), EV 1.7202 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.38 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 39.18 %) — p(stop avant cible) 0.0174 [0.01 ; 0.04], R/R 0.655, perte reelle 39.18 % (gap inclus), EV 1.9377 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.18 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 42.742 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.6, perte reelle 42.742 % (gap inclus), EV 1.9544 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.74 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 46.304 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.554, perte reelle 46.304 % (gap inclus), EV 1.9525 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.30 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 49.866 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.514, perte reelle 49.866 % (gap inclus), EV 1.9471 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.87 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 53.428 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.48, perte reelle 53.428 % (gap inclus), EV 1.942 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.43 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 56.99 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.45, perte reelle 56.99 % (gap inclus), EV 1.9407 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.99 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 37.28, ATR14 2.6557 (7.124 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 2.465 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.356 % | 37.1472 | 90.43 % | 93.15 % | 94.55 % | 95.15 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.712 % | 37.0144 | 82.18 % | 87.1 % | 89.1 % | 91.2 % | 92.99 % | 94.87 % |
| 0.15 ATR | 1.069 % | 36.8816 | 75.03 % | 81.96 % | 84.86 % | 88.17 % | 90.55 % | 93.63 % |
| 0.2 ATR | 1.425 % | 36.7489 | 68.08 % | 77.22 % | 80.42 % | 85.64 % | 89.13 % | 92.3 % |
| 0.25 ATR | 1.781 % | 36.6161 | 62.03 % | 72.68 % | 76.29 % | 82.31 % | 87.09 % | 90.66 % |
| 0.35 ATR | 2.493 % | 36.3505 | 49.45 % | 63.61 % | 69.83 % | 77.35 % | 82.72 % | 88.19 % |
| 0.5 ATR | 3.562 % | 35.9521 | 34.94 % | 50.1 % | 58.43 % | 68.86 % | 76.93 % | 84.09 % |
| 0.75 ATR | 5.343 % | 35.2882 | 17.32 % | 33.47 % | 43.09 % | 55.21 % | 66.46 % | 75.98 % |
| 1.0 ATR | 7.124 % | 34.6243 | 8.16 % | 21.98 % | 30.98 % | 44.08 % | 57.42 % | 69.1 % |
| 1.25 ATR | 8.905 % | 33.9604 | 3.93 % | 15.12 % | 22.91 % | 33.77 % | 48.78 % | 62.11 % |
| 1.5 ATR | 10.686 % | 33.2964 | 1.51 % | 9.78 % | 16.65 % | 26.69 % | 42.48 % | 55.65 % |
| 2.0 ATR | 14.247 % | 31.9686 | 0.3 % | 3.63 % | 8.58 % | 16.38 % | 30.39 % | 44.35 % |
| 2.5 ATR | 17.809 % | 30.6407 | 0.2 % | 1.61 % | 4.44 % | 10.01 % | 20.12 % | 32.34 % |
| 3.0 ATR | 21.371 % | 29.3129 | 0.2 % | 1.21 % | 2.62 % | 5.76 % | 14.53 % | 24.44 % |
| 4.0 ATR | 28.495 % | 26.6571 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.27 % |
| 6.0 ATR | 42.742 % | 21.3457 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.19 ATR |
| **2 s.** | 0.22 ATR | 0.50 ATR | 0.58 ATR | 0.76 ATR | 0.93 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.96 ATR | 1.19 ATR | 1.37 ATR | 1.91 ATR | 2.43 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.98 ATR | 1.28 ATR | 1.58 ATR | 1.82 ATR | 2.50 ATR | 3.24 ATR |
| **10 s.** | 0.55 ATR | 1.22 ATR | 1.40 ATR | 1.89 ATR | 2.26 ATR | 2.51 ATR | 3.64 ATR | 4.90 ATR |
| **20 s.** | 0.79 ATR | 1.75 ATR | 1.97 ATR | 2.47 ATR | 2.96 ATR | 3.44 ATR | 4.98 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.577–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.343 %, prix 35.2881), p(touche) 33.47 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.719–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.343 %, prix 35.2881), p(touche) 43.09 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.979–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.905 %, prix 33.9602), p(touche) 33.77 % (en stress 89.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.4–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.686 %, prix 33.2963), p(touche) 42.48 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.971–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.809 %, prix 30.6408), p(touche) 32.34 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.031 | EV/share : $0.082 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 23 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.1 | bear 6.6 | side 8.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 485.0 (= 13 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.693% → cible +3.15% / stop −2.219%, p_fill 31%, n_eff≈15.9) : P(cible|rempli) **37%** · **EV/risk +0.039** (×p_fill ; si rempli +0.28% du capital)
  - **swing** (entrée dip −8.126% → cible +7.043% / stop −7.754%, p_fill 18%, n_eff≈8.5) : P(cible|rempli) **61%** · **EV/risk +0.034** (×p_fill ; si rempli +1.50% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=9))
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
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 63.3  _(momentum haussier)_
- **ADX** : 25.2  _(tendance etablie)_
- **MACD** : hist -0.046  _(bearish_recent)_
- **BB** : %B 0.63 · largeur 37.3%
- **ATR** : 2.66 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.005  _(neutre)_
- **Vol ratio** : 0.41  _(volume atone)_
- **Choppiness** : 56.5  _(transition)_
- **MA** : MA20 35.6 · MA50 31.34 · MA200 31.33  _(prix > MA20)_
- **Dist MA** : MA20 +4.7% · MA50 +18.9% · MA200 +19.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (774915 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
