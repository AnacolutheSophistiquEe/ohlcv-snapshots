# AL2SI

**Generated** : 2026-09-08T00:17:29.248726+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €28.94  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €28.94 (+0.7% vs entrée) · entrée €28.75 · stop €28.31 · T1 €29.28 · R/R 1.2  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk -0.045 _(réel 5 s)_ (GBM 0.042) · ¼-Kelly 0.007 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.54% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -27 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €28.64–€28.86 (mid €28.75)
- Spot actuel : €28.94 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €28.31 (stop swing_plan-based (-6.53%))
- Targets : T1 €29.28 · R/R 1.2 | T2 €29.81 · R/R 2.41 | T3 €30.34 · R/R 3.61
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €28.31


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.53 %)** : le gap seul le franchit 1.094 % des séances (14 fois sur 1280).
   - exécution **3.163 pt plus bas** dans le cas TYPIQUE (médiane), 19.929 au p90, **31.587 au pire**
   - perte réelle **14.446 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 6.53 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0866 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 14 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5224** [0.4481 ; 0.5959] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4346** [0.3831 ; 0.4872] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3957** [0.3452 ; 0.4479] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.6 pt), swing (32.6 pt), deep (33.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.27 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.25 % contre 7.26 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.22** (β de hausse 0.9486, asymétrie 1.2861) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.951× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 25.9971 sur atr_grid (2.0 ATR, 10.169 %) — p(stop avant cible) 0.3494 [0.30 ; 0.40], R/R 0.477, perte reelle 22.515 % (gap inclus), CVaR 10.227 %, EV -2.5629 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.52 ATR (stop 5.041 %) — p(stop avant cible) 0.613 [0.56 ; 0.66], R/R 0.856, perte reelle 12.539 % (gap inclus), EV -3.8266 % — **REFUSE**
      - refuse : p_stop_first 0.613, borne haute 0.663 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.52 ATR du spot — compartiment <1, mesure a 45.8 % de casse (IC clusterise [0.427 ; 0.489] sur 1234 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.83 %) : P(cible) 34.7 % x 10.74 % + P(rien) 4.0 % x 3.42 % ne couvrent pas P(stop) 61.3 % x 12.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 7.626 %) — p(stop avant cible) 0.4907 [0.44 ; 0.54], R/R 0.654, perte reelle 16.422 % (gap inclus), EV -3.4377 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.44 %) : P(cible) 41.6 % x 10.74 % + P(rien) 9.3 % x 1.62 % ne couvrent pas P(stop) 49.1 % x 16.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.46 ATR (stop 14.924 %) — p(stop avant cible) 0.2439 [0.20 ; 0.29], R/R 0.435, perte reelle 24.668 % (gap inclus), EV -0.7416 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 51.8 % x 10.74 % + P(rien) 23.8 % x -1.20 % ne couvrent pas P(stop) 24.4 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.88 ATR (stop 17.046 %) — p(stop avant cible) 0.2031 [0.16 ; 0.25], R/R 0.398, perte reelle 27.014 % (gap inclus), EV -0.4907 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 51.8 % x 10.74 % + P(rien) 27.9 % x -2.03 % ne couvrent pas P(stop) 20.3 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.31 ATR (stop 24.322 %) — p(stop avant cible) 0.1121 [0.08 ; 0.15], R/R 0.358, perte reelle 30.031 % (gap inclus), EV 0.633 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.34 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.271 %) — p(stop avant cible) 0.8595 [0.82 ; 0.89], R/R 3.113, perte reelle 3.45 % (gap inclus), EV -1.5229 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.860, borne haute 0.893 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.52 %) : P(cible) 13.4 % x 10.74 % + P(rien) 0.7 % x 0.83 % ne couvrent pas P(stop) 86.0 % x 3.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 0.52 ATR (stop 4.151 %) — p(stop avant cible) 0.6587 [0.61 ; 0.71], R/R 1.113, perte reelle 9.649 % (gap inclus), EV -2.9355 % — **REFUSE**
      - refuse : p_stop_first 0.659, borne haute 0.707 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.94 %) : P(cible) 31.0 % x 10.74 % + P(rien) 3.1 % x 2.89 % ne couvrent pas P(stop) 65.9 % x 9.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 6.356 %) — p(stop avant cible) 0.5442 [0.49 ; 0.60], R/R 0.743, perte reelle 14.446 % (gap inclus), EV -3.5116 % — **REFUSE**
      - refuse : p_stop_first 0.544, borne haute 0.596 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.51 %) : P(cible) 39.3 % x 10.74 % + P(rien) 6.3 % x 2.12 % ne couvrent pas P(stop) 54.4 % x 14.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.898 %) — p(stop avant cible) 0.423 [0.37 ; 0.48], R/R 0.59, perte reelle 18.187 % (gap inclus), EV -2.7291 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.73 %) : P(cible) 45.0 % x 10.74 % + P(rien) 12.7 % x 1.00 % ne couvrent pas P(stop) 42.3 % x 18.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 10.169 %) — p(stop avant cible) 0.3494 [0.30 ; 0.40], R/R 0.477, perte reelle 22.515 % (gap inclus), EV -2.5629 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.56 %) : P(cible) 49.4 % x 10.74 % + P(rien) 15.7 % x 0.01 % ne couvrent pas P(stop) 34.9 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.46 ATR (stop 14.034 %) — p(stop avant cible) 0.2503 [0.21 ; 0.30], R/R 0.435, perte reelle 24.668 % (gap inclus), EV -0.8698 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 51.6 % x 10.74 % + P(rien) 23.3 % x -1.04 % ne couvrent pas P(stop) 25.0 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.88 ATR (stop 16.157 %) — p(stop avant cible) 0.2169 [0.18 ; 0.26], R/R 0.398, perte reelle 27.014 % (gap inclus), EV -0.7271 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 51.8 % x 10.74 % + P(rien) 26.5 % x -1.62 % ne couvrent pas P(stop) 21.7 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 17.795 %) — p(stop avant cible) 0.1991 [0.16 ; 0.24], R/R 0.398, perte reelle 27.014 % (gap inclus), EV -0.4304 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 51.8 % x 10.74 % + P(rien) 28.3 % x -2.17 % ne couvrent pas P(stop) 19.9 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 20.338 %) — p(stop avant cible) 0.1497 [0.12 ; 0.19], R/R 0.358, perte reelle 30.031 % (gap inclus), EV 0.002 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.36 % > budget 12.00 %
   - 🟢 grid_snapped a 4.31 ATR (stop 23.433 %) — p(stop avant cible) 0.1122 [0.08 ; 0.15], R/R 0.358, perte reelle 30.031 % (gap inclus), EV 0.6318 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.45 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 25.422 %) — p(stop avant cible) 0.1028 [0.07 ; 0.14], R/R 0.329, perte reelle 32.641 % (gap inclus), EV 0.4833 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.43 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.964 %) — p(stop avant cible) 0.0903 [0.06 ; 0.12], R/R 0.282, perte reelle 38.117 % (gap inclus), EV 0.1534 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.97 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 30.506 %) — p(stop avant cible) 0.085 [0.06 ; 0.12], R/R 0.282, perte reelle 38.117 % (gap inclus), EV 0.2472 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.51 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 33.049 %) — p(stop avant cible) 0.0762 [0.05 ; 0.11], R/R 0.282, perte reelle 38.117 % (gap inclus), EV 0.3895 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.05 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 35.591 %) — p(stop avant cible) 0.055 [0.03 ; 0.08], R/R 0.282, perte reelle 38.117 % (gap inclus), EV 0.8879 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.59 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 38.133 %) — p(stop avant cible) 0.0483 [0.03 ; 0.07], R/R 0.282, perte reelle 38.133 % (gap inclus), EV 1.0126 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.13 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 40.675 %) — p(stop avant cible) 0.039 [0.02 ; 0.06], R/R 0.264, perte reelle 40.675 % (gap inclus), EV 1.1441 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.68 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 28.94, ATR14 1.4714 (5.084 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.399 ATR = 2.029 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.254 % | 28.8664 | 86.86 % | 90.48 % | 92.83 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.508 % | 28.7929 | 82.35 % | 86.95 % | 90.08 % | 91.93 % | 93.77 % | 95.9 % |
| 0.15 ATR | 0.763 % | 28.7193 | 78.33 % | 83.32 % | 87.03 % | 88.88 % | 91.79 % | 94.71 % |
| 0.2 ATR | 1.017 % | 28.6457 | 72.45 % | 79.2 % | 83.2 % | 85.73 % | 89.42 % | 92.51 % |
| 0.25 ATR | 1.271 % | 28.5721 | 66.37 % | 74.58 % | 79.08 % | 82.38 % | 87.14 % | 90.91 % |
| 0.35 ATR | 1.78 % | 28.425 | 54.41 % | 65.65 % | 70.83 % | 75.69 % | 82.29 % | 87.61 % |
| 0.5 ATR | 2.542 % | 28.2043 | 40.78 % | 54.07 % | 61.79 % | 68.8 % | 77.74 % | 85.11 % |
| 0.75 ATR | 3.813 % | 27.8364 | 22.75 % | 37.78 % | 47.74 % | 55.81 % | 66.86 % | 76.42 % |
| 1.0 ATR | 5.084 % | 27.4686 | 13.04 % | 25.32 % | 34.28 % | 44.88 % | 57.27 % | 68.23 % |
| 1.25 ATR | 6.356 % | 27.1007 | 7.75 % | 17.76 % | 24.95 % | 36.52 % | 50.25 % | 61.94 % |
| 1.5 ATR | 7.627 % | 26.7329 | 3.82 % | 11.48 % | 17.68 % | 28.84 % | 43.22 % | 55.84 % |
| 2.0 ATR | 10.169 % | 25.9971 | 0.88 % | 5.3 % | 9.82 % | 17.22 % | 31.85 % | 44.26 % |
| 2.5 ATR | 12.711 % | 25.2614 | 0.1 % | 2.36 % | 4.91 % | 10.43 % | 22.06 % | 34.47 % |
| 3.0 ATR | 15.253 % | 24.5257 | 0.1 % | 0.98 % | 2.55 % | 7.09 % | 16.02 % | 27.17 % |
| 4.0 ATR | 20.338 % | 23.0543 | 0.0 % | 0.59 % | 1.28 % | 3.05 % | 9.5 % | 18.48 % |
| 6.0 ATR | 30.506 % | 20.1114 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.47 % | 8.79 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.14 ATR | 1.43 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.85 ATR | 1.01 ATR | 1.18 ATR | 1.62 ATR | 2.05 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.99 ATR | 2.49 ATR |
| **5 s.** | 0.36 ATR | 0.88 ATR | 1.00 ATR | 1.36 ATR | 1.67 ATR | 1.88 ATR | 2.56 ATR | 3.52 ATR |
| **10 s.** | 0.56 ATR | 1.26 ATR | 1.44 ATR | 1.95 ATR | 2.35 ATR | 2.67 ATR | 3.92 ATR | 5.28 ATR |
| **20 s.** | 0.79 ATR | 1.75 ATR | 1.97 ATR | 2.60 ATR | 3.25 ATR | 3.83 ATR | 5.75 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.454–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.542 %, prix 28.2043), p(touche) 40.78 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (91.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.639–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.813 %, prix 27.8365), p(touche) 37.78 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.801–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.084 %, prix 27.4687), p(touche) 34.28 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.997–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.084 %, prix 27.4687), p(touche) 44.88 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.437–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.627 %, prix 26.7327), p(touche) 43.22 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.968–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.169 %, prix 25.9971), p(touche) 44.26 % (en stress 97.03 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.042 | EV/share : €0.018 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 31 % | T3 25 %
- Kelly (position) : f* 0.029 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.6 | bear 6.3 | side 8.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 376.0 (= 13 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.655% → cible +1.843% / stop −1.535%, p_fill 84%, n_eff≈36.0) : P(cible|rempli) **44%** · **EV/risk -0.045** (×p_fill ; si rempli -0.08% du capital)
  - **swing** (entrée dip −1.446% → cible +4.121% / stop −5.159%, p_fill 81%, n_eff≈33.6) : P(cible|rempli) **43%** · **EV/risk -0.186** (×p_fill ; si rempli -1.19% du capital)
  - **deep** (entrée dip −2.234% → cible +5.828% / stop −7.801%, p_fill 68%, n_eff≈32.5) : P(cible|rempli) **45%** · **EV/risk -0.078** (×p_fill ; si rempli -0.89% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 64.7  _(momentum haussier)_
- **ADX** : 11.9  _(pas de tendance nette)_
- **MACD** : hist 0.388  _(pas de croisement recent)_
- **BB** : %B 0.96 · largeur 14.3%
- **ATR** : 1.47 (48.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.09  _(distribution)_
- **Vol ratio** : 0.94  _(volume normal)_
- **Choppiness** : 58.3  _(transition)_
- **MA** : MA20 27.17 · MA50 28.34 · MA200 26.59  _(prix > MA20)_
- **Dist MA** : MA20 +6.5% · MA50 +2.1% · MA200 +8.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (769510 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
