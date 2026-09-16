# AL2SI

**Generated** : 2026-09-16T00:15:09.938640+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.02  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot €27.02 (+1.8% vs entrée) · entrée €26.55 · stop €25.74 · T1 €28.18 · R/R 2.01  
> ↳ P(T1 av. stop) 13 % _(réel 5 s)_ · EV/risk -0.121 _(réel 5 s)_ (GBM 0.057) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.06% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €26.44–€26.67 (mid €26.55)
- Spot actuel : €27.02 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : €25.74 (stop swing_plan-based (-10.42%))
- Targets : T1 €28.18 · R/R 2.01 | T2 €28.22 · R/R 2.06 | T3 €28.26 · R/R 2.11
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €25.74


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.42 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1279).
   - exécution **10.966 pt plus bas** dans le cas TYPIQUE (médiane), 22.221 au p90, **27.697 au pire**
   - perte réelle **22.515 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 10.42 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0567 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.815 % | pire -38.117 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4812** [0.4076 ; 0.5554] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3615** [0.3122 ; 0.4131] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.2874** [0.2416 ; 0.3367] _(largeur 9.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.8 pt), swing (37.8 pt), deep (36.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.28 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.40 % contre 7.28 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.77 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2147** (β de hausse 0.949, asymétrie 1.28) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.909× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 23.9691 sur support (1.13 ATR, 11.291 %) — p(stop avant cible) 0.3058 [0.26 ; 0.36], R/R 0.477, perte reelle 22.515 % (gap inclus), CVaR 11.344 %, EV -1.5002 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.13 ATR (stop 11.291 %) — p(stop avant cible) 0.3058 [0.26 ; 0.36], R/R 0.477, perte reelle 22.515 % (gap inclus), EV -1.5002 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.50 %) : P(cible) 50.5 % x 10.74 % + P(rien) 19.0 % x -0.18 % ne couvrent pas P(stop) 30.6 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.47 ATR (stop 20.174 %) — p(stop avant cible) 0.1556 [0.12 ; 0.20], R/R 0.358, perte reelle 30.031 % (gap inclus), EV 0.0854 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.20 % > budget 12.00 %
   - 🟢 support a 3.86 ATR (stop 29.426 %) — p(stop avant cible) 0.0834 [0.06 ; 0.12], R/R 0.282, perte reelle 38.117 % (gap inclus), EV 0.4835 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.43 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.659 %) — p(stop avant cible) 0.8285 [0.79 ; 0.87], R/R 2.556, perte reelle 4.202 % (gap inclus), EV -1.7172 % — **REFUSE**
      - refuse : p_stop_first 0.829, borne haute 0.865 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.72 %) : P(cible) 16.3 % x 10.74 % + P(rien) 0.9 % x 1.56 % ne couvrent pas P(stop) 82.8 % x 4.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.318 %) — p(stop avant cible) 0.7129 [0.66 ; 0.76], R/R 1.326, perte reelle 8.101 % (gap inclus), EV -2.8323 % — **REFUSE**
      - refuse : p_stop_first 0.713, borne haute 0.759 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.83 %) : P(cible) 27.0 % x 10.74 % + P(rien) 1.8 % x 2.72 % ne couvrent pas P(stop) 71.3 % x 8.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.976 %) — p(stop avant cible) 0.6241 [0.57 ; 0.67], R/R 0.857, perte reelle 12.539 % (gap inclus), EV -4.0754 % — **REFUSE**
      - refuse : p_stop_first 0.624, borne haute 0.674 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.08 %) : P(cible) 33.7 % x 10.74 % + P(rien) 3.9 % x 3.42 % ne couvrent pas P(stop) 62.4 % x 12.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.13 ATR (stop 9.467 %) — p(stop avant cible) 0.3853 [0.34 ; 0.44], R/R 0.556, perte reelle 19.309 % (gap inclus), EV -2.247 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 47.7 % x 10.74 % + P(rien) 13.8 % x 0.49 % ne couvrent pas P(stop) 38.5 % x 19.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 13.271 %) — p(stop avant cible) 0.2558 [0.21 ; 0.30], R/R 0.435, perte reelle 24.668 % (gap inclus), EV -0.9226 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 51.8 % x 10.74 % + P(rien) 22.6 % x -0.80 % ne couvrent pas P(stop) 25.6 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.47 ATR (stop 18.349 %) — p(stop avant cible) 0.1849 [0.15 ; 0.23], R/R 0.358, perte reelle 30.031 % (gap inclus), EV -0.5712 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 52.6 % x 10.74 % + P(rien) 28.9 % x -2.32 % ne couvrent pas P(stop) 18.5 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 23.224 %) — p(stop avant cible) 0.1103 [0.08 ; 0.15], R/R 0.358, perte reelle 30.031 % (gap inclus), EV 0.8555 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.24 % > budget 12.00 %
   - 🟢 grid_snapped a 3.86 ATR (stop 27.601 %) — p(stop avant cible) 0.0928 [0.07 ; 0.13], R/R 0.282, perte reelle 38.117 % (gap inclus), EV 0.2936 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.61 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 33.176 %) — p(stop avant cible) 0.074 [0.05 ; 0.11], R/R 0.282, perte reelle 38.117 % (gap inclus), EV 0.6379 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.18 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 36.494 %) — p(stop avant cible) 0.0516 [0.03 ; 0.08], R/R 0.282, perte reelle 38.117 % (gap inclus), EV 1.1666 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.50 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.812 %) — p(stop avant cible) 0.0378 [0.02 ; 0.06], R/R 0.27, perte reelle 39.812 % (gap inclus), EV 1.4056 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.81 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 43.129 %) — p(stop avant cible) 0.0332 [0.02 ; 0.06], R/R 0.249, perte reelle 43.129 % (gap inclus), EV 1.3247 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.13 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 46.447 %) — p(stop avant cible) 0.0332 [0.02 ; 0.06], R/R 0.231, perte reelle 46.447 % (gap inclus), EV 1.2146 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.45 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 49.765 %) — p(stop avant cible) 0.0332 [0.02 ; 0.06], R/R 0.216, perte reelle 49.765 % (gap inclus), EV 1.1044 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.76 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 53.082 %) — p(stop avant cible) 0.0332 [0.02 ; 0.06], R/R 0.202, perte reelle 53.082 % (gap inclus), EV 0.9943 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.08 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 27.02, ATR14 1.7929 (6.635 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 2.654 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.332 % | 26.9304 | 86.85 % | 90.47 % | 92.82 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.664 % | 26.8407 | 82.34 % | 86.84 % | 89.97 % | 91.82 % | 93.76 % | 95.9 % |
| 0.15 ATR | 0.995 % | 26.7511 | 78.31 % | 83.2 % | 86.92 % | 88.77 % | 91.78 % | 94.7 % |
| 0.2 ATR | 1.327 % | 26.6614 | 72.42 % | 79.08 % | 83.09 % | 85.62 % | 89.41 % | 92.5 % |
| 0.25 ATR | 1.659 % | 26.5718 | 66.34 % | 74.46 % | 78.96 % | 82.27 % | 87.13 % | 90.9 % |
| 0.35 ATR | 2.322 % | 26.3925 | 54.56 % | 65.52 % | 70.8 % | 75.47 % | 82.28 % | 87.6 % |
| 0.5 ATR | 3.318 % | 26.1236 | 40.82 % | 53.93 % | 61.75 % | 68.57 % | 77.72 % | 85.1 % |
| 0.75 ATR | 4.976 % | 25.6754 | 22.77 % | 37.72 % | 47.59 % | 55.67 % | 66.83 % | 76.4 % |
| 1.0 ATR | 6.635 % | 25.2271 | 13.15 % | 25.25 % | 34.12 % | 44.53 % | 57.23 % | 68.2 % |
| 1.25 ATR | 8.294 % | 24.7789 | 7.75 % | 17.88 % | 25.07 % | 36.45 % | 50.2 % | 61.9 % |
| 1.5 ATR | 9.953 % | 24.3307 | 3.83 % | 11.59 % | 17.7 % | 28.97 % | 43.17 % | 55.4 % |
| 2.0 ATR | 13.271 % | 23.4343 | 0.88 % | 5.4 % | 9.83 % | 17.24 % | 31.68 % | 43.7 % |
| 2.5 ATR | 16.588 % | 22.5379 | 0.1 % | 2.36 % | 4.92 % | 10.44 % | 21.68 % | 33.9 % |
| 3.0 ATR | 19.906 % | 21.6414 | 0.1 % | 0.98 % | 2.56 % | 7.09 % | 15.64 % | 26.6 % |
| 4.0 ATR | 26.541 % | 19.8486 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.21 % | 17.9 % |
| 6.0 ATR | 39.812 % | 16.2629 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.38 % | 8.2 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.15 ATR | 1.43 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.01 ATR | 1.18 ATR | 1.63 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.99 ATR | 2.49 ATR |
| **5 s.** | 0.36 ATR | 0.88 ATR | 0.99 ATR | 1.36 ATR | 1.67 ATR | 1.88 ATR | 2.57 ATR | 3.52 ATR |
| **10 s.** | 0.56 ATR | 1.26 ATR | 1.44 ATR | 1.94 ATR | 2.33 ATR | 2.64 ATR | 3.88 ATR | 5.23 ATR |
| **20 s.** | 0.79 ATR | 1.73 ATR | 1.94 ATR | 2.56 ATR | 3.18 ATR | 3.76 ATR | 5.63 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.454–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.318 %, prix 26.1235), p(touche) 40.82 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (89.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.638–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.976 %, prix 25.6755), p(touche) 37.72 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.798–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.635 %, prix 25.2272), p(touche) 34.12 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.989–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.635 %, prix 25.2272), p(touche) 44.53 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.435–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.953 %, prix 24.3307), p(touche) 43.17 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.944–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.271 %, prix 23.4342), p(touche) 43.7 % (en stress 97.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.057 | EV/share : €0.047 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 33 % | T3 33 %
- Kelly (position) : f* 0.082 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.9 | bear 5.8 | side 8.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 270.0 (= 10 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.723% → cible +6.119% / stop −3.06%, p_fill 61%, n_eff≈28.3) : P(cible|rempli) **13%** · **EV/risk -0.121** (×p_fill ; si rempli -0.60% du capital)
  - **swing** (entrée dip −3.784% → cible +4.797% / stop −6.897%, p_fill 49%, n_eff≈24.1) : P(cible|rempli) **55%** · **EV/risk -0.022** (×p_fill ; si rempli -0.31% du capital)
  - **deep** (entrée dip −5.847% → cible +6.784% / stop −10.572%, p_fill 49%, n_eff≈25.3) : P(cible|rempli) **61%** · **EV/risk -0.025** (×p_fill ; si rempli -0.53% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→76% · +2.0%→68% · +3.0%→54% · +5.0%→41% · +8.0%→21%
- Range intraday médian 7.92% (p90 22.19%) · excursion haute méd. +4.07% / basse méd. −3.9%
- Profil de vol intra : ouverture 5.308% vs midi 1.708% vs clôture 1.799% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 7% · trend ↑2%/↓1% ; spike-down 71% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.082)_ ; drift intra méd. 0.153% ; recovery-V 24%
- **σ réalisé intraday** 4.977% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 67% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 28.2728 (VA 28.0733–28.5862 ; dernier close 28.62)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 89% · **stop −5.18%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.23% · baisse 42% (gap-down >1% 14% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.91% (p90 −4.33%) · haut méd +0.81% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −4.9%) · haut méd +1.34% · range méd 3.08%
- Excursion ouverture 30min (n=160) : bas méd −1.41% (p90 −5.48%) · haut méd +1.96% · range méd 4.04%
- Excursion ouverture 60min (n=160) : bas méd −1.53% (p90 −6.01%) · haut méd +2.1% · range méd 4.57%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.76 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 78% (123/159) · gap 22% · délai 0.3min · rebond 64% (85/123) (MFE +2.38%)
   - −1.0% : fill 30min 51% · séance 75% (117/159) · gap 14% · délai 1.2min · rebond 64% (80/117) (MFE +2.0%)
   - −1.5% : fill 30min 43% · séance 68% (104/159) · gap 9% · délai 6.7min · rebond 63% (66/104) (MFE +1.52%)
   - −2.0% : fill 30min 36% · séance 62% (96/159) · gap 5% · délai 13.5min · rebond 62% (61/96) (MFE +1.57%)
   - −3.0% : fill 30min 22% · séance 51% (81/159) · gap 4% · délai 42.5min · rebond 59% (57/81) (MFE +1.47%)
   - −4.0% : fill 30min 18% · séance 42% (70/159) · gap 2% · délai 88.6min · rebond 77% (57/70) (MFE +1.84%)
   - −5.0% : fill 30min 12% · séance 30% (57/159) · gap 2% · délai 85.2min · rebond 89% (52/57) (MFE +2.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −4.03%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.0% (p90 −4.32%) → stop au-delà de −2.56% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.98% (p90 −4.76%) → stop au-delà de −2.89% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1523 jambes) : jambe baissière méd −1.24% (p90 −3.1%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 95% (48/51) · rebond 59% (29/48)
      · −2.0% : fill 87% (44/51) · rebond 54% (25/44)
      · −3.0% : fill 76% (41/51) · rebond 60% (30/41)
      · −4.0% : fill 66% (37/51) · rebond 70% (29/37)
      · −5.0% : fill 45% (31/51) · rebond 79% (27/31)
   - **flat** (30 séances) :
      · −1.0% : fill 72% (23/30) · rebond 65% (16/23)
      · −2.0% : fill 49% (18/30) · rebond 57% (12/18)
      · −3.0% : fill 41% (13/30) · rebond 53% (8/13)
      · −4.0% : fill 36% (12/30) · rebond 85% (10/12)
      · −5.0% : fill 22% (9/30) · rebond 100% (9/9)
   - **gap-up** (78 séances) :
      · −1.0% : fill 62% (46/78) · rebond 67% (35/46)
      · −2.0% : fill 52% (34/78) · rebond 74% (24/34)
      · −3.0% : fill 39% (27/78) · rebond 60% (19/27)
      · −4.0% : fill 28% (21/78) · rebond 84% (18/21)
      · −5.0% : fill 22% (17/78) · rebond 99% (16/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 56% si les 15 1res min sont vertes (74 cas) · 32% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 69% si début vert vs 22% si rouge (base 44% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **69%** · continue >prix actuel 56% ; creux résiduel méd -2.58% (q20 -5.56%) → **SL/trailing à −5.56%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.47% / q75 +5.87% → **scale +3.47% / runner +5.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **22%** (continue à baisser 61%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.72%** (au-delà de la MAE q10 -7.72%), cible rebond +2.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.93% .. +6.13%] · haut q95 +7.67% · bas q05 -7.05%
   - 60min (n=160) : retour [-5.72% .. +6.19%] · haut q95 +8.22% · bas q05 -7.63%
   - 2h (n=160) : retour [-5.75% .. +8.33%] · haut q95 +9.95% · bas q05 -7.79%
   - 4h (n=160) : retour [-6.16% .. +8.77%] · haut q95 +11.4% · bas q05 -9.41%
   - 6h (n=160) : retour [-6.69% .. +9.25%] · haut q95 +12.36% · bas q05 -9.9%
   - session (n=160) : retour [-7.46% .. +11.07%] · haut q95 +13.23% · bas q05 -10.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.0  _(neutre)_
- **ADX** : 14.5  _(pas de tendance nette)_
- **MACD** : hist 0.132  _(pas de croisement recent)_
- **BB** : %B 0.44 · largeur 17.8%
- **ATR** : 1.79 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.068  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 51.0  _(transition)_
- **MA** : MA20 27.33 · MA50 27.55 · MA200 27.02  _(prix < MA20)_
- **Dist MA** : MA20 -1.1% · MA50 -1.9% · MA200 +0.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (756913 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
