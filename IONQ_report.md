# IONQ

**Generated** : 2026-08-26T00:26:58.121569+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $42.05  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $42.05 (+1.9% vs entrée) · entrée $41.26 · stop $39.61 · T1 $44.56 · R/R 2.0  
> ↳ P(T1 av. stop) 2 % _(réel 5 s)_ · EV/risk -0.035 _(réel 5 s)_ (GBM -0.03) · ¼-Kelly 0.031 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.01% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $41.00–$41.52 (mid $41.26)
- Spot actuel : $42.05 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : $39.61 (stop swing_plan-based (-13.93%))
- Targets : T1 $44.56 · R/R 2.0 | T2 $44.86 · R/R 2.18 | T3 $45.15 · R/R 2.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $39.61


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.78 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.93 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **7.929 pt plus bas** dans le cas TYPIQUE (médiane), 7.929 au p90, **7.929 au pire**
   - perte réelle **21.859 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 13.93 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0063 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.035 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3985** [0.3277 ; 0.4726] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.3746** [0.3248 ; 0.4265] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.4594** [0.4074 ; 0.5121] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.8 pt), swing (37.6 pt), deep (36.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.47 %** | CVaR **-10.08 %** | vol 6.17 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 9.72 % contre 5.94 % aujourd'hui, rapport 1.64)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.23 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.227** (β de hausse 1.9822, asymétrie 1.1235) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 37.1341 sur grid_snapped (1.4 ATR, 11.691 %) — p(stop avant cible) 0.4954 [0.44 ; 0.55], R/R 1.582, perte reelle 16.903 % (gap inclus), CVaR 11.699 %, EV -1.5107 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.58 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 25 des 25 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 50.7 % de la queue et il ne reste que -199.12 EUR a partager. Prix du risque -0.086 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.8 ATR (stop 8.58 %) — p(stop avant cible) 0.6314 [0.58 ; 0.68], R/R 2.265, perte reelle 11.81 % (gap inclus), EV -1.0286 % — **REFUSE**
      - refuse : p_stop_first 0.631, borne haute 0.681 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 19.7 % x 26.75 % + P(rien) 17.1 % x 6.71 % ne couvrent pas P(stop) 63.1 % x 11.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.4 ATR (stop 12.748 %) — p(stop avant cible) 0.4525 [0.40 ; 0.51], R/R 1.224, perte reelle 21.859 % (gap inclus), EV -3.0235 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.02 %) : P(cible) 21.4 % x 26.75 % + P(rien) 33.4 % x 3.44 % ne couvrent pas P(stop) 45.2 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.73 ATR (stop 21.832 %) — p(stop avant cible) 0.1827 [0.14 ; 0.23], R/R 1.224, perte reelle 21.859 % (gap inclus), EV 1.3833 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.83 % > budget 12.00 %
   - 🟢 support a 4.18 ATR (stop 31.796 %) — p(stop avant cible) 0.0428 [0.03 ; 0.07], R/R 0.841, perte reelle 31.796 % (gap inclus), EV 1.3331 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.80 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.716 %) — p(stop avant cible) 0.9147 [0.88 ; 0.94], R/R 7.543, perte reelle 3.546 % (gap inclus), EV -1.3066 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 7.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.915, borne haute 0.941 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 6.3 % x 26.75 % + P(rien) 2.2 % x 11.06 % ne couvrent pas P(stop) 91.5 % x 3.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.432 %) — p(stop avant cible) 0.8335 [0.79 ; 0.87], R/R 4.989, perte reelle 5.361 % (gap inclus), EV -0.9431 % — **REFUSE**
      - refuse : cible atteinte seulement 11.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.834, borne haute 0.870 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 11.4 % x 26.75 % + P(rien) 5.2 % x 8.94 % ne couvrent pas P(stop) 83.4 % x 5.36 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.8 ATR (stop 7.523 %) — p(stop avant cible) 0.653 [0.60 ; 0.70], R/R 2.514, perte reelle 10.638 % (gap inclus), EV -0.8573 % — **REFUSE**
      - refuse : p_stop_first 0.653, borne haute 0.702 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 18.5 % x 26.75 % + P(rien) 16.2 % x 7.00 % ne couvrent pas P(stop) 65.3 % x 10.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.4 ATR (stop 11.691 %) — p(stop avant cible) 0.4954 [0.44 ; 0.55], R/R 1.582, perte reelle 16.903 % (gap inclus), EV -1.5107 % — **REFUSE**
      - refuse : R/R 1.58 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.51 %) : P(cible) 20.9 % x 26.75 % + P(rien) 29.6 % x 4.33 % ne couvrent pas P(stop) 49.5 % x 16.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 13.729 %) — p(stop avant cible) 0.4107 [0.36 ; 0.46], R/R 1.224, perte reelle 21.859 % (gap inclus), EV -2.3134 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.31 %) : P(cible) 21.4 % x 26.75 % + P(rien) 37.5 % x 2.51 % ne couvrent pas P(stop) 41.1 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 15.445 %) — p(stop avant cible) 0.3409 [0.29 ; 0.39], R/R 1.224, perte reelle 21.859 % (gap inclus), EV -1.2055 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 21.6 % x 26.75 % + P(rien) 44.3 % x 1.04 % ne couvrent pas P(stop) 34.1 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.73 ATR (stop 20.775 %) — p(stop avant cible) 0.1952 [0.16 ; 0.24], R/R 1.224, perte reelle 21.859 % (gap inclus), EV 1.1981 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.78 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 24.025 %) — p(stop avant cible) 0.1192 [0.09 ; 0.16], R/R 1.113, perte reelle 24.025 % (gap inclus), EV 1.5194 % — **REFUSE**
      - refuse : R/R 1.11 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.03 % > budget 12.00 %
   - 🟢 grid_snapped a 4.18 ATR (stop 30.739 %) — p(stop avant cible) 0.0502 [0.03 ; 0.08], R/R 0.87, perte reelle 30.739 % (gap inclus), EV 1.3507 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.74 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 34.321 %) — p(stop avant cible) 0.0268 [0.01 ; 0.05], R/R 0.779, perte reelle 34.321 % (gap inclus), EV 1.3522 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.32 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 37.754 %) — p(stop avant cible) 0.0122 [0.00 ; 0.03], R/R 0.708, perte reelle 37.754 % (gap inclus), EV 1.4102 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.75 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 41.186 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 0.649, perte reelle 41.186 % (gap inclus), EV 1.4139 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.19 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 44.618 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.599, perte reelle 44.618 % (gap inclus), EV 1.4417 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.62 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 48.05 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.557, perte reelle 48.05 % (gap inclus), EV 1.4664 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.05 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 51.482 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.52, perte reelle 51.482 % (gap inclus), EV 1.4838 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.48 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 54.914 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.487, perte reelle 54.914 % (gap inclus), EV 1.4838 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.91 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 42.05, ATR14 2.8864 (6.864 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.381 ATR = 2.615 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.343 % | 41.9057 | 93.55 % | 95.26 % | 95.96 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.686 % | 41.7614 | 86.0 % | 91.03 % | 92.03 % | 94.54 % | 96.04 % | 97.02 % |
| 0.15 ATR | 1.03 % | 41.617 | 79.15 % | 86.09 % | 88.19 % | 91.51 % | 93.8 % | 95.89 % |
| 0.2 ATR | 1.373 % | 41.4727 | 71.7 % | 80.34 % | 84.16 % | 88.37 % | 91.06 % | 93.84 % |
| 0.25 ATR | 1.716 % | 41.3284 | 65.66 % | 76.51 % | 80.63 % | 85.74 % | 88.82 % | 92.3 % |
| 0.35 ATR | 2.402 % | 41.0397 | 53.17 % | 67.44 % | 73.97 % | 79.17 % | 84.15 % | 88.71 % |
| 0.5 ATR | 3.432 % | 40.6068 | 38.07 % | 54.54 % | 62.16 % | 70.78 % | 78.46 % | 84.91 % |
| 0.75 ATR | 5.148 % | 39.8852 | 22.26 % | 38.81 % | 48.13 % | 58.54 % | 68.8 % | 77.1 % |
| 1.0 ATR | 6.864 % | 39.1636 | 9.87 % | 24.5 % | 34.71 % | 45.6 % | 57.72 % | 68.38 % |
| 1.25 ATR | 8.58 % | 38.442 | 3.63 % | 14.31 % | 24.12 % | 34.68 % | 49.8 % | 62.22 % |
| 1.5 ATR | 10.296 % | 37.7204 | 1.01 % | 7.06 % | 15.84 % | 25.58 % | 41.06 % | 56.26 % |
| 2.0 ATR | 13.729 % | 36.2771 | 0.1 % | 1.92 % | 4.94 % | 14.56 % | 28.56 % | 44.87 % |
| 2.5 ATR | 17.161 % | 34.8339 | 0.0 % | 0.2 % | 1.21 % | 5.76 % | 18.19 % | 33.78 % |
| 3.0 ATR | 20.593 % | 33.3907 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.38 % | 25.87 % |
| 4.0 ATR | 27.457 % | 30.5043 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 41.186 % | 24.7314 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.23 ATR | 1.37 ATR | 1.77 ATR | 2.00 ATR |
| **5 s.** | 0.42 ATR | 0.92 ATR | 1.01 ATR | 1.30 ATR | 1.53 ATR | 1.75 ATR | 2.26 ATR | 2.62 ATR |
| **10 s.** | 0.59 ATR | 1.24 ATR | 1.39 ATR | 1.82 ATR | 2.17 ATR | 2.41 ATR | 3.16 ATR | 3.76 ATR |
| **20 s.** | 0.81 ATR | 1.77 ATR | 1.99 ATR | 2.55 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.431–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.652–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.148 %, prix 39.8853), p(touche) 38.81 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.808–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.864 %, prix 39.1637), p(touche) 34.71 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.014–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.58 %, prix 38.4421), p(touche) 34.68 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.387–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.296 %, prix 37.7205), p(touche) 41.06 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.994–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.729 %, prix 36.277), p(touche) 44.87 % (en stress 98.98 %)  ✅ optimum identifie (68.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.03 | EV/share : $-0.050 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.124 | ¼-Kelly 0.031 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 69.1 | bear 23.6 | side 7.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 126.0 (= 3 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.88% → cible +8.012% / stop −4.006%, p_fill 61%, n_eff≈27.1) : P(cible|rempli) **2%** · **EV/risk -0.035** (×p_fill ; si rempli -0.23% du capital)
  - **swing** (entrée dip −4.145% → cible +20.417% / stop −10.208%, p_fill 47%, n_eff≈24.6) : P(cible|rempli) **13%** · **EV/risk +0.000** (×p_fill ; si rempli +0.01% du capital)
  - **deep** (entrée dip −6.404% → cible +9.942% / stop −11.001%, p_fill 48%, n_eff≈27.0) : P(cible|rempli) **42%** · **EV/risk -0.114** (×p_fill ; si rempli -2.64% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→68% · +3.0%→59% · +5.0%→32% · +8.0%→15%
- Range intraday médian 7.64% (p90 12.17%) · excursion haute méd. +3.66% / basse méd. −2.75%
- Profil de vol intra : ouverture 5.31% vs midi 1.497% vs clôture 1.685% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; neutre — autocorr 0.011)_ ; drift intra méd. 0.322% ; recovery-V 29%
- **σ réalisé intraday** 4.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 50% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 44.7594 (VA 44.1094–45.0844 ; dernier close 44.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 85% · **stop −5.07%** sous le fill (sous le bruit) · cible +2.77% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. -0.31% · baisse 53% (gap-down >1% 36% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.16% (p90 −2.83%) · haut méd +1.33% · range méd 2.79%
- Excursion ouverture 15min (n=160) : bas méd −1.59% (p90 −4.01%) · haut méd +1.52% · range méd 3.72%
- Excursion ouverture 30min (n=160) : bas méd −1.91% (p90 −5.15%) · haut méd +2.05% · range méd 4.53%
- Excursion ouverture 60min (n=160) : bas méd −2.25% (p90 −5.61%) · haut méd +2.32% · range méd 5.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 44.86 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 73% · séance 82% (133/159) · gap 46% · délai 0.0min · rebond 62% (86/133) (MFE +1.86%)
   - −1.0% : fill 30min 69% · séance 75% (125/159) · gap 36% · délai 0.0min · rebond 72% (91/125) (MFE +2.35%)
   - −1.5% : fill 30min 62% · séance 68% (117/159) · gap 31% · délai 0.0min · rebond 69% (81/117) (MFE +2.07%)
   - −2.0% : fill 30min 55% · séance 63% (108/159) · gap 18% · délai 0.1min · rebond 72% (76/108) (MFE +2.31%)
   - −3.0% : fill 30min 46% · séance 54% (93/159) · gap 8% · délai 6.3min · rebond 75% (69/93) (MFE +2.5%)
   - −4.0% : fill 30min 26% · séance 43% (76/159) · gap 6% · délai 21.5min · rebond 73% (59/76) (MFE +2.36%)
   - −5.0% : fill 30min 18% · séance 35% (64/159) · gap 3% · délai 24.8min · rebond 85% (55/64) (MFE +2.77%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.89%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.88% (p90 −3.23%) → stop au-delà de −2.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.82% (p90 −2.73%) → stop au-delà de −1.84% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1125 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 100% (78/78) · rebond 73% (58/78)
      · −2.0% : fill 90% (72/78) · rebond 77% (55/72)
      · −3.0% : fill 77% (62/78) · rebond 76% (47/62)
      · −4.0% : fill 60% (48/78) · rebond 74% (38/48)
      · −5.0% : fill 48% (40/78) · rebond 80% (33/40)
   - **flat** (15 séances) :
      · −1.0% : fill 78% (12/15) · rebond 65% (7/12)
      · −2.0% : fill 69% (11/15) · rebond 79% (6/11)
      · −3.0% : fill 62% (9/15) · rebond 62% (6/9)
      · −4.0% : fill 54% (8/15) · rebond 53% (4/8)
      · −5.0% : fill 39% (7/15) · rebond 95% (6/7)
   - **gap-up** (66 séances) :
      · −1.0% : fill 42% (35/66) · rebond 73% (26/35)
      · −2.0% : fill 26% (25/66) · rebond 49% (15/25)
      · −3.0% : fill 23% (22/66) · rebond 76% (16/22)
      · −4.0% : fill 20% (20/66) · rebond 80% (17/20)
      · −5.0% : fill 17% (17/66) · rebond 98% (16/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 58% si les 15 1res min sont vertes (80 cas) · 32% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 70% si début vert vs 22% si rouge (base 46% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 234min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **70%** · continue >prix actuel 43% ; creux résiduel méd -2.94% (q20 -4.58%) → **SL/trailing à −4.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.03% / q75 +4.69% → **scale +2.03% / runner +4.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **22%** (continue à baisser 54%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.74%** (au-delà de la MAE q10 -4.74%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.1% .. +6.84%] · haut q95 +7.86% · bas q05 -5.64%
   - 60min (n=160) : retour [-4.98% .. +6.12%] · haut q95 +8.41% · bas q05 -6.18%
   - 2h (n=160) : retour [-6.38% .. +7.84%] · haut q95 +9.04% · bas q05 -7.04%
   - 4h (n=160) : retour [-7.04% .. +7.21%] · haut q95 +10.16% · bas q05 -8.09%
   - 6h (n=160) : retour [-7.2% .. +8.45%] · haut q95 +10.89% · bas q05 -8.3%
   - session (n=160) : retour [-6.6% .. +8.94%] · haut q95 +11.03% · bas q05 -8.35%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.29% (p75 2.28% / p90 3.82%) · ~3.0 replis/séance, durée méd 69.04 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 24.37 min, n=47)
   - −1.0% → **78%** (reprise méd 68.85 min, n=30)
   - −1.5% → **68%** (reprise méd 81.24 min, n=16)
   - −2.0% → **67%** (reprise méd 84.17 min, n=12)
   - −3.0% → **75%** (reprise méd 175.72 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.82%** (p90, défaut prudent ; serré/agressif −2.28%) ; extension open→close méd +8.23% (q75 +10.03% / q95 +16.4%), MFE méd +10.28% / q90 +13.1%
   - Échelle scale-out : +10.28% (33%) / +11.83% (33%) / +13.1% (34%)
- **DÉSARMER** : repli > **−3.82%** depuis le plus-haut = décay → P(retournement) **30%** (préavis méd 235.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.1% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 54.2  _(neutre)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist 0.17  _(pas de croisement recent)_
- **BB** : %B 0.52 · largeur 36.3%
- **ATR** : 2.89 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.019  _(neutre)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 60.0  _(transition)_
- **MA** : MA20 41.75 · MA50 43.89 · MA200 44.73  _(prix > MA20)_
- **Dist MA** : MA20 +0.7% · MA50 -4.2% · MA200 -6.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (814695 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
