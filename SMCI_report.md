# SMCI

**Generated** : 2026-08-28T00:25:32.367628+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $38.46  

> 🟡 **WAIT-FOR-DIP** — spot +10.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $38.46 (+10.8% vs entrée) · entrée $34.71 · stop $32.04 · T1 $37.10 · R/R 0.9  
> ↳ P(T1 av. stop) 55 % · EV/risk 0.03 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $34.23–$35.19 (mid $34.71)
- Spot actuel : $38.46 (+10.8% au-dessus de la zone — repli à attendre)
- Stop : $32.04 (stop swing_plan-based (-16.69%))
- Targets : T1 $37.10 · R/R 0.9 | T2 $39.49 · R/R 1.79 | T3 $41.89 · R/R 2.69
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $32.04


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (16.69 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **7.967 pt plus bas** dans le cas TYPIQUE (médiane), 11.485 au p90, **12.361 au pire**
   - perte réelle **23.404 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 16.69 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0268 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.765 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2739** [0.2116 ; 0.3437] _(largeur 13.2 pt, n_eff 173.1)_
   - swing : **0.3834** [0.3333 ; 0.4355] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3043** [0.2576 ; 0.3543] _(largeur 9.7 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.0 observations effectives », dont la borne haute a 95 % vaut environ 21.4 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.77 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.29 % contre 7.19 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.05 % si l'on extrapolait par √5 _(rapport 1.04 ; < 1 = le √5 surestime)_
- **β de baisse : 1.536** (β de hausse 1.2402, asymétrie 1.2385) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.916× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 35.1287 sur atr_grid (1.25 ATR, 8.662 %) — p(stop avant cible) 0.4958 [0.44 ; 0.55], R/R 1.541, perte reelle 14.137 % (gap inclus), CVaR 8.749 %, EV -0.8225 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 27 des 27 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 52.8 % de la queue et il ne reste que -406.12 EUR a partager. Prix du risque -0.191 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.394 %) — p(stop avant cible) 0.4286 [0.38 ; 0.48], R/R 1.291, perte reelle 16.875 % (gap inclus), EV -0.9868 % — **REFUSE**
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.99 %) : P(cible) 23.4 % x 21.78 % + P(rien) 33.7 % x 3.38 % ne couvrent pas P(stop) 42.9 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.84 ATR (stop 15.153 %) — p(stop avant cible) 0.2493 [0.21 ; 0.30], R/R 0.931, perte reelle 23.404 % (gap inclus), EV -0.018 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 24.7 % x 21.78 % + P(rien) 50.4 % x 0.86 % ne couvrent pas P(stop) 24.9 % x 23.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.66 ATR (stop 20.837 %) — p(stop avant cible) 0.1489 [0.11 ; 0.19], R/R 0.811, perte reelle 26.856 % (gap inclus), EV 1.4164 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.85 % > budget 12.00 %
   - 🟢 support a 4.03 ATR (stop 30.356 %) — p(stop avant cible) 0.0874 [0.06 ; 0.12], R/R 0.718, perte reelle 30.356 % (gap inclus), EV 1.7171 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.36 % > budget 12.00 %
   - 🟢 support a 4.9 ATR (stop 36.336 %) — p(stop avant cible) 0.0618 [0.04 ; 0.09], R/R 0.599, perte reelle 36.336 % (gap inclus), EV 1.4324 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.34 % > budget 12.00 %
   - 🟢 support a 5.66 ATR (stop 41.614 %) — p(stop avant cible) 0.0089 [0.00 ; 0.02], R/R 0.523, perte reelle 41.614 % (gap inclus), EV 1.6956 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.61 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.732 %) — p(stop avant cible) 0.8959 [0.86 ; 0.92], R/R 5.003, perte reelle 4.354 % (gap inclus), EV -1.8807 % — **REFUSE**
      - refuse : cible atteinte seulement 8.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.896, borne haute 0.925 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.88 %) : P(cible) 8.4 % x 21.78 % + P(rien) 2.0 % x 9.17 % ne couvrent pas P(stop) 89.6 % x 4.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.465 %) — p(stop avant cible) 0.7693 [0.72 ; 0.81], R/R 3.07, perte reelle 7.094 % (gap inclus), EV -1.6078 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.769, borne haute 0.811 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.61 %) : P(cible) 14.9 % x 21.78 % + P(rien) 8.2 % x 7.42 % ne couvrent pas P(stop) 76.9 % x 7.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.197 %) — p(stop avant cible) 0.6807 [0.63 ; 0.73], R/R 1.942, perte reelle 11.218 % (gap inclus), EV -2.8409 % — **REFUSE**
      - refuse : p_stop_first 0.681, borne haute 0.728 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.84 %) : P(cible) 18.1 % x 21.78 % + P(rien) 13.8 % x 6.12 % ne couvrent pas P(stop) 68.1 % x 11.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.929 %) — p(stop avant cible) 0.5761 [0.52 ; 0.63], R/R 1.608, perte reelle 13.549 % (gap inclus), EV -2.0778 % — **REFUSE**
      - refuse : p_stop_first 0.576, borne haute 0.627 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 21.4 % x 21.78 % + P(rien) 21.0 % x 5.05 % ne couvrent pas P(stop) 57.6 % x 13.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 8.662 %) — p(stop avant cible) 0.4958 [0.44 ; 0.55], R/R 1.541, perte reelle 14.137 % (gap inclus), EV -0.8225 % — **REFUSE**
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 23.2 % x 21.78 % + P(rien) 27.3 % x 4.18 % ne couvrent pas P(stop) 49.6 % x 14.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 24.252 %) — p(stop avant cible) 0.1103 [0.08 ; 0.15], R/R 0.811, perte reelle 26.856 % (gap inclus), EV 1.9101 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.26 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 45.04 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.484, perte reelle 45.04 % (gap inclus), EV 1.6932 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.04 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 48.505 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.449, perte reelle 48.505 % (gap inclus), EV 1.6862 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.51 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 51.97 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.419, perte reelle 51.97 % (gap inclus), EV 1.6849 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.97 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 55.434 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.393, perte reelle 55.434 % (gap inclus), EV 1.6791 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.43 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 38.46, ATR14 2.665 (6.929 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 2.398 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.346 % | 38.3267 | 90.43 % | 93.15 % | 94.65 % | 95.15 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.693 % | 38.1935 | 82.18 % | 87.1 % | 89.2 % | 91.2 % | 92.99 % | 94.87 % |
| 0.15 ATR | 1.039 % | 38.0602 | 75.03 % | 81.96 % | 84.96 % | 88.17 % | 90.55 % | 93.63 % |
| 0.2 ATR | 1.386 % | 37.927 | 68.08 % | 77.22 % | 80.52 % | 85.64 % | 89.13 % | 92.3 % |
| 0.25 ATR | 1.732 % | 37.7937 | 62.03 % | 72.68 % | 76.39 % | 82.31 % | 87.09 % | 90.76 % |
| 0.35 ATR | 2.425 % | 37.5272 | 49.45 % | 63.71 % | 69.93 % | 77.35 % | 82.72 % | 88.3 % |
| 0.5 ATR | 3.465 % | 37.1275 | 35.05 % | 50.1 % | 58.53 % | 68.86 % | 76.93 % | 84.19 % |
| 0.75 ATR | 5.197 % | 36.4612 | 17.32 % | 33.57 % | 43.19 % | 55.21 % | 66.46 % | 76.18 % |
| 1.0 ATR | 6.929 % | 35.795 | 8.16 % | 22.08 % | 31.08 % | 44.19 % | 57.42 % | 69.3 % |
| 1.25 ATR | 8.662 % | 35.1287 | 3.93 % | 15.12 % | 23.01 % | 33.97 % | 48.78 % | 62.32 % |
| 1.5 ATR | 10.394 % | 34.4625 | 1.51 % | 9.78 % | 16.65 % | 26.9 % | 42.48 % | 55.85 % |
| 2.0 ATR | 13.859 % | 33.13 | 0.3 % | 3.63 % | 8.58 % | 16.48 % | 30.49 % | 44.56 % |
| 2.5 ATR | 17.323 % | 31.7975 | 0.2 % | 1.61 % | 4.44 % | 10.01 % | 20.33 % | 32.55 % |
| 3.0 ATR | 20.788 % | 30.465 | 0.2 % | 1.21 % | 2.62 % | 5.76 % | 14.74 % | 24.64 % |
| 4.0 ATR | 27.717 % | 27.8 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.52 % | 14.37 % |
| 6.0 ATR | 41.576 % | 22.47 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.19 ATR |
| **2 s.** | 0.22 ATR | 0.50 ATR | 0.58 ATR | 0.76 ATR | 0.94 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.96 ATR | 1.19 ATR | 1.37 ATR | 1.91 ATR | 2.43 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.98 ATR | 1.28 ATR | 1.59 ATR | 1.83 ATR | 2.50 ATR | 3.24 ATR |
| **10 s.** | 0.55 ATR | 1.22 ATR | 1.40 ATR | 1.90 ATR | 2.27 ATR | 2.53 ATR | 3.66 ATR | 4.92 ATR |
| **20 s.** | 0.79 ATR | 1.76 ATR | 1.98 ATR | 2.48 ATR | 2.98 ATR | 3.45 ATR | 4.99 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.577–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.197 %, prix 36.4612), p(touche) 33.57 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.721–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.197 %, prix 36.4612), p(touche) 43.19 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.982–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.662 %, prix 35.1286), p(touche) 33.97 % (en stress 89.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.4–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.394 %, prix 34.4625), p(touche) 42.48 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.981–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.323 %, prix 31.7976), p(touche) 32.55 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.028 | EV/share : $0.075 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 24 % | T3 16 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 83.3 | bear 5.4 | side 11.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 500.0 (= 13 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.434% → cible +8.006% / stop −4.003%, p_fill 22%, n_eff≈14.0) : P(cible|rempli) **0%** · **EV/risk +0.009** (×p_fill ; si rempli +0.18% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=13, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→61% · +3.0%→50% · +5.0%→29% · +8.0%→14%
- Range intraday médian 6.69% (p90 11.21%) · excursion haute méd. +3.0% / basse méd. −2.68%
- Profil de vol intra : ouverture 4.16% vs midi 1.286% vs clôture 1.677% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.061)_ ; drift intra méd. 0.054% ; recovery-V 32%
- **σ réalisé intraday** 4.115% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 67% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 36.8811 (VA 36.8514–37.2084 ; dernier close 37.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 79% · **stop −4.24%** sous le fill (sous le bruit) · cible +2.72% · R/R 0.64 (high win-rate)
- Gaps overnight (n=159) : méd. 0.39% · baisse 42% (gap-down >1% 31% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.83%) · haut méd +1.04% · range méd 2.22%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −3.23%) · haut méd +1.47% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.42% (p90 −3.75%) · haut méd +1.52% · range méd 3.73%
- Excursion ouverture 60min (n=160) : bas méd −1.7% (p90 −4.4%) · haut méd +1.79% · range méd 4.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 37.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 73% (120/159) · gap 39% · délai 0.0min · rebond 58% (73/120) (MFE +1.31%)
   - −1.0% : fill 30min 52% · séance 69% (111/159) · gap 31% · délai 0.0min · rebond 62% (66/111) (MFE +1.5%)
   - −1.5% : fill 30min 45% · séance 62% (100/159) · gap 23% · délai 0.1min · rebond 67% (62/100) (MFE +1.59%)
   - −2.0% : fill 30min 42% · séance 52% (87/159) · gap 17% · délai 0.7min · rebond 70% (56/87) (MFE +1.77%)
   - −3.0% : fill 30min 32% · séance 48% (75/159) · gap 12% · délai 8.5min · rebond 63% (46/75) (MFE +1.97%)
   - −4.0% : fill 30min 19% · séance 38% (57/159) · gap 6% · délai 26.3min · rebond 74% (37/57) (MFE +1.95%)
   - −5.0% : fill 30min 14% · séance 31% (48/159) · gap 4% · délai 48.0min · rebond 79% (35/48) (MFE +2.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.86%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −3.01%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.7% (p90 −2.87%) → stop au-delà de −1.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=901 jambes) : jambe baissière méd −1.21% (p90 −2.88%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 96% (67/69) · rebond 50% (35/67)
      · −2.0% : fill 90% (63/69) · rebond 65% (37/63)
      · −3.0% : fill 86% (57/69) · rebond 59% (33/57)
      · −4.0% : fill 70% (45/69) · rebond 73% (29/45)
      · −5.0% : fill 59% (39/69) · rebond 78% (28/39)
   - **flat** (13 séances) :
      · −1.0% : fill 100% (13/13) · rebond 92% (11/13)
      · −2.0% : fill 41% (6/13) · rebond 89% (4/6)
      · −3.0% : fill 26% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 22% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (77 séances) :
      · −1.0% : fill 42% (31/77) · rebond 75% (20/31)
      · −2.0% : fill 24% (18/77) · rebond 81% (15/18)
      · −3.0% : fill 19% (15/77) · rebond 70% (10/15)
      · −4.0% : fill 14% (10/77) · rebond 71% (6/10)
      · −5.0% : fill 13% (9/77) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 69% si les 15 1res min sont vertes (78 cas) · 22% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 72% si début vert vs 16% si rouge (base 46% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **72%** · continue >prix actuel 44% ; creux résiduel méd -2.66% (q20 -3.77%) → **SL/trailing à −3.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.13% / q75 +3.85% → **scale +2.13% / runner +3.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **16%** (continue à baisser 59%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.34%** (au-delà de la MAE q10 -5.34%), cible rebond +1.65% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.05% .. +4.41%] · haut q95 +6.19% · bas q05 -4.32%
   - 60min (n=160) : retour [-4.23% .. +5.66%] · haut q95 +6.83% · bas q05 -5.29%
   - 2h (n=160) : retour [-4.78% .. +6.84%] · haut q95 +8.56% · bas q05 -5.81%
   - 4h (n=160) : retour [-5.25% .. +7.37%] · haut q95 +9.01% · bas q05 -6.9%
   - 6h (n=160) : retour [-5.77% .. +6.98%] · haut q95 +10.21% · bas q05 -6.92%
   - session (n=160) : retour [-7.11% .. +7.84%] · haut q95 +10.21% · bas q05 -7.83%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **13%**. Lecture précoce 30 min : signature présente → 7% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.84% / p90 2.17%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 14.9 min, n=37)
   - −1.0% → **72%** (reprise méd 30.0 min, n=17)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.17%** (p90, défaut prudent ; serré/agressif −1.84%) ; extension open→close méd +7.84% (q75 +8.68% / q95 +9.89%), MFE méd +8.72% / q90 +10.39%
   - Échelle scale-out : +8.72% (33%) / +9.19% (33%) / +10.39% (34%)
- **DÉSARMER** : repli > **−2.17%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.39% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 68.1  _(momentum haussier)_
- **ADX** : 25.6  _(tendance etablie)_
- **MACD** : hist 0.16  _(pas de croisement recent)_
- **BB** : %B 0.74 · largeur 45.0%
- **ATR** : 2.66 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.031  _(neutre)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 45.0  _(transition)_
- **MA** : MA20 34.74 · MA50 31.02 · MA200 31.35  _(prix > MA20)_
- **Dist MA** : MA20 +10.7% · MA50 +24.0% · MA200 +22.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (836935 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
