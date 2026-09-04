# SMCI

**Generated** : 2026-09-04T22:02:41.883473+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $39.59  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot $39.59 (+0.4% vs entrée) · entrée $39.42 · stop $38.75 · T1 $39.80 · R/R 0.57  
> ↳ P(T1 av. stop) 77 % _(réel 5 s)_ · EV/risk 0.168 _(réel 5 s)_ (GBM 0.038) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.7% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 692 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $39.34–$39.50 (mid $39.42)
- Spot actuel : $39.59 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : $38.75 (stop swing_plan-based (-6.41%))
- Targets : T1 $39.80 · R/R 0.57 | T2 $41.27 · R/R 2.76 | T3 $42.73 · R/R 4.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $38.75


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.41 %)** : le gap seul le franchit 1.834 % des séances (23 fois sur 1254).
   - exécution **4.857 pt plus bas** dans le cas TYPIQUE (médiane), 17.138 au p90, **22.641 au pire**
   - perte réelle **13.25 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 6.41 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.1255 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.763 % | p01 -10.29 % | pire -29.051 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4624** [0.3893 ; 0.5368] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5368** [0.4841 ; 0.5889] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4046** [0.3538 ; 0.457] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 37.2 observations effectives », dont la borne haute a 95 % vaut environ 8.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (26.5 pt), swing (30.9 pt), deep (31.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.77 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.26 % contre 7.20 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.68 % vs -16.02 % si l'on extrapolait par √5 _(rapport 1.042 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5394** (β de hausse 1.2371, asymétrie 1.2444) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.968× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 35.13 sur atr_grid (2.0 ATR, 11.265 %) — p(stop avant cible) 0.3716 [0.32 ; 0.42], R/R 1.074, perte reelle 17.348 % (gap inclus), CVaR 11.323 %, EV -0.5606 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 0.05 ATR (stop 3.018 %) — p(stop avant cible) 0.8051 [0.76 ; 0.84], R/R 2.947, perte reelle 6.324 % (gap inclus), EV -1.9969 % — **REFUSE**
      - refuse : p_stop_first 0.805, borne haute 0.844 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.00 %) : P(cible) 15.0 % x 18.64 % + P(rien) 4.5 % x 6.64 % ne couvrent pas P(stop) 80.5 % x 6.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 8.449 %) — p(stop avant cible) 0.4924 [0.44 ; 0.55], R/R 1.318, perte reelle 14.137 % (gap inclus), EV -1.371 % — **REFUSE**
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 26.3 % x 18.64 % + P(rien) 24.5 % x 2.83 % ne couvrent pas P(stop) 49.2 % x 14.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.67 ATR (stop 17.734 %) — p(stop avant cible) 0.1807 [0.14 ; 0.22], R/R 0.748, perte reelle 24.92 % (gap inclus), EV 0.8185 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.76 % > budget 12.00 %
   - 🟢 support a 5.33 ATR (stop 32.723 %) — p(stop avant cible) 0.0759 [0.05 ; 0.11], R/R 0.569, perte reelle 32.723 % (gap inclus), EV 1.2647 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.72 % > budget 12.00 %
   - 🟢 support a 6.36 ATR (stop 38.532 %) — p(stop avant cible) 0.0273 [0.01 ; 0.05], R/R 0.484, perte reelle 38.532 % (gap inclus), EV 1.3518 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.53 % > budget 12.00 %
   - 🟢 grid_snapped a 0.05 ATR (stop 1.993 %) — p(stop avant cible) 0.8802 [0.84 ; 0.91], R/R 3.747, perte reelle 4.973 % (gap inclus), EV -2.3712 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.880, borne haute 0.911 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.37 %) : P(cible) 10.0 % x 18.64 % + P(rien) 2.0 % x 7.08 % ne couvrent pas P(stop) 88.0 % x 4.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.225 %) — p(stop avant cible) 0.7224 [0.67 ; 0.77], R/R 2.121, perte reelle 8.786 % (gap inclus), EV -2.3726 % — **REFUSE**
      - refuse : p_stop_first 0.722, borne haute 0.768 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.37 %) : P(cible) 18.7 % x 18.64 % + P(rien) 9.0 % x 5.38 % ne couvrent pas P(stop) 72.2 % x 8.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.633 %) — p(stop avant cible) 0.661 [0.61 ; 0.71], R/R 1.606, perte reelle 11.6 % (gap inclus), EV -3.0854 % — **REFUSE**
      - refuse : p_stop_first 0.661, borne haute 0.709 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.09 %) : P(cible) 21.7 % x 18.64 % + P(rien) 12.2 % x 4.41 % ne couvrent pas P(stop) 66.1 % x 11.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.041 %) — p(stop avant cible) 0.5824 [0.53 ; 0.63], R/R 1.375, perte reelle 13.549 % (gap inclus), EV -2.7588 % — **REFUSE**
      - refuse : p_stop_first 0.582, borne haute 0.633 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.76 %) : P(cible) 24.0 % x 18.64 % + P(rien) 17.7 % x 3.69 % ne couvrent pas P(stop) 58.2 % x 13.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 9.857 %) — p(stop avant cible) 0.4456 [0.39 ; 0.50], R/R 1.104, perte reelle 16.875 % (gap inclus), EV -1.8182 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.82 %) : P(cible) 26.9 % x 18.64 % + P(rien) 28.5 % x 2.41 % ne couvrent pas P(stop) 44.6 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 11.265 %) — p(stop avant cible) 0.3716 [0.32 ; 0.42], R/R 1.074, perte reelle 17.348 % (gap inclus), EV -0.5606 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 27.6 % x 18.64 % + P(rien) 35.2 % x 2.09 % ne couvrent pas P(stop) 37.2 % x 17.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 12.674 %) — p(stop avant cible) 0.3114 [0.26 ; 0.36], R/R 0.97, perte reelle 19.221 % (gap inclus), EV -0.2007 % — **REFUSE**
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 28.7 % x 18.64 % + P(rien) 40.1 % x 1.08 % ne couvrent pas P(stop) 31.1 % x 19.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.67 ATR (stop 16.709 %) — p(stop avant cible) 0.2063 [0.17 ; 0.25], R/R 0.796, perte reelle 23.404 % (gap inclus), EV 0.6071 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.74 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 19.715 %) — p(stop avant cible) 0.1513 [0.12 ; 0.19], R/R 0.694, perte reelle 26.856 % (gap inclus), EV 1.0188 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.73 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.531 %) — p(stop avant cible) 0.1273 [0.10 ; 0.17], R/R 0.694, perte reelle 26.856 % (gap inclus), EV 1.3483 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.54 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 25.347 %) — p(stop avant cible) 0.1006 [0.07 ; 0.14], R/R 0.667, perte reelle 27.955 % (gap inclus), EV 1.5338 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.35 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 28.164 %) — p(stop avant cible) 0.0901 [0.06 ; 0.12], R/R 0.641, perte reelle 29.051 % (gap inclus), EV 1.4951 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.16 % > budget 12.00 %
   - 🟢 grid_snapped a 5.33 ATR (stop 31.697 %) — p(stop avant cible) 0.0805 [0.06 ; 0.11], R/R 0.588, perte reelle 31.697 % (gap inclus), EV 1.3184 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.70 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.796 %) — p(stop avant cible) 0.0704 [0.05 ; 0.10], R/R 0.551, perte reelle 33.796 % (gap inclus), EV 1.229 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.80 % > budget 12.00 %
   - 🟢 grid_snapped a 6.36 ATR (stop 37.507 %) — p(stop avant cible) 0.0492 [0.03 ; 0.08], R/R 0.497, perte reelle 37.507 % (gap inclus), EV 1.1928 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.51 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 39.429 %) — p(stop avant cible) 0.0171 [0.01 ; 0.04], R/R 0.473, perte reelle 39.429 % (gap inclus), EV 1.3661 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.43 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 42.246 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.441, perte reelle 42.246 % (gap inclus), EV 1.3928 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.25 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 45.062 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.414, perte reelle 45.062 % (gap inclus), EV 1.3891 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.06 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 39.59, ATR14 2.23 (5.633 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.943 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.282 % | 39.4785 | 90.44 % | 93.15 % | 94.56 % | 95.05 % | 96.35 % | 97.54 % |
| 0.1 ATR | 0.563 % | 39.367 | 82.19 % | 87.11 % | 89.11 % | 91.11 % | 92.99 % | 94.87 % |
| 0.15 ATR | 0.845 % | 39.2555 | 75.05 % | 81.97 % | 84.88 % | 88.08 % | 90.56 % | 93.54 % |
| 0.2 ATR | 1.127 % | 39.144 | 68.11 % | 77.24 % | 80.44 % | 85.56 % | 89.14 % | 92.21 % |
| 0.25 ATR | 1.408 % | 39.0325 | 62.07 % | 72.71 % | 76.31 % | 82.22 % | 87.11 % | 90.46 % |
| 0.35 ATR | 1.971 % | 38.8095 | 49.4 % | 63.54 % | 69.66 % | 77.27 % | 82.74 % | 87.9 % |
| 0.5 ATR | 2.816 % | 38.475 | 34.91 % | 50.05 % | 58.27 % | 68.79 % | 76.95 % | 83.79 % |
| 0.75 ATR | 4.225 % | 37.9175 | 17.3 % | 33.33 % | 42.94 % | 55.15 % | 66.5 % | 75.69 % |
| 1.0 ATR | 5.633 % | 37.36 | 8.05 % | 21.75 % | 30.75 % | 43.84 % | 57.46 % | 68.72 % |
| 1.25 ATR | 7.041 % | 36.8025 | 3.82 % | 15.01 % | 22.68 % | 33.43 % | 48.43 % | 61.74 % |
| 1.5 ATR | 8.449 % | 36.245 | 1.51 % | 9.67 % | 16.43 % | 26.36 % | 42.13 % | 55.28 % |
| 2.0 ATR | 11.265 % | 35.13 | 0.3 % | 3.52 % | 8.37 % | 16.06 % | 30.05 % | 44.0 % |
| 2.5 ATR | 14.082 % | 34.015 | 0.2 % | 1.51 % | 4.33 % | 9.8 % | 19.8 % | 32.0 % |
| 3.0 ATR | 16.898 % | 32.9 | 0.2 % | 1.21 % | 2.62 % | 5.66 % | 14.21 % | 24.1 % |
| 4.0 ATR | 22.531 % | 30.67 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.41 % | 14.15 % |
| 6.0 ATR | 33.796 % | 26.21 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.58 ATR | 0.76 ATR | 0.93 ATR | 1.06 ATR | 1.49 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.95 ATR | 1.18 ATR | 1.36 ATR | 1.90 ATR | 2.42 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.26 ATR | 1.57 ATR | 1.81 ATR | 2.48 ATR | 3.22 ATR |
| **10 s.** | 0.55 ATR | 1.21 ATR | 1.39 ATR | 1.88 ATR | 2.25 ATR | 2.49 ATR | 3.62 ATR | 4.90 ATR |
| **20 s.** | 0.78 ATR | 1.73 ATR | 1.96 ATR | 2.46 ATR | 2.94 ATR | 3.41 ATR | 4.96 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.576–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.225 %, prix 37.9173), p(touche) 33.33 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.716–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.225 %, prix 37.9173), p(touche) 42.94 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 15.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.974–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.041 %, prix 36.8025), p(touche) 33.43 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.386–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.449 %, prix 36.245), p(touche) 42.13 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.956–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (16.898 %, prix 32.9001), p(touche) 24.1 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.038 | EV/share : $0.025 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 64 % | T2 26 % | T3 23 %
- Kelly (position) : f* 0.03 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.2 | bear 6.4 | side 8.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 594.0 (= 15 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.43% → cible +0.976% / stop −1.697%, p_fill 91%, n_eff≈37.2) : P(cible|rempli) **77%** · **EV/risk +0.168** (×p_fill ; si rempli +0.32% du capital)
  - **swing** (entrée dip −0.777% → cible +10.112% / stop −5.677%, p_fill 86%, n_eff≈35.1) : P(cible|rempli) **31%** · **EV/risk -0.168** (×p_fill ; si rempli -1.12% du capital)
  - **deep** (entrée dip −1.04% → cible +21.584% / stop −10.792%, p_fill 89%, n_eff≈34.7) : P(cible|rempli) **35%** · **EV/risk +0.283** (×p_fill ; si rempli +3.44% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→76% · +2.0%→60% · +3.0%→45% · +5.0%→28% · +8.0%→12%
- Range intraday médian 6.14% (p90 10.79%) · excursion haute méd. +2.53% / basse méd. −2.38%
- Profil de vol intra : ouverture 4.146% vs midi 1.257% vs clôture 1.632% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. 0.072% ; recovery-V 34%
- **σ réalisé intraday** 3.89% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 68% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 36.4477 (VA 36.1638–36.8028 ; dernier close 36.71)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 81% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.59% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.16% · baisse 46% (gap-down >1% 36% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −0.88% (p90 −2.79%) · haut méd +1.02% · range méd 2.23%
- Excursion ouverture 15min (n=160) : bas méd −1.26% (p90 −3.28%) · haut méd +1.46% · range méd 2.94%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.82%) · haut méd +1.56% · range méd 3.7%
- Excursion ouverture 60min (n=160) : bas méd −1.68% (p90 −4.43%) · haut méd +1.84% · range méd 4.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 36.71 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 73% (120/159) · gap 42% · délai 0.0min · rebond 56% (72/120) (MFE +1.26%)
   - −1.0% : fill 30min 55% · séance 69% (111/159) · gap 36% · délai 0.0min · rebond 60% (65/111) (MFE +1.38%)
   - −1.5% : fill 30min 48% · séance 63% (101/159) · gap 24% · délai 0.0min · rebond 69% (64/101) (MFE +1.56%)
   - −2.0% : fill 30min 44% · séance 55% (88/159) · gap 18% · délai 0.2min · rebond 72% (58/88) (MFE +1.73%)
   - −3.0% : fill 30min 31% · séance 49% (76/159) · gap 10% · délai 8.8min · rebond 61% (47/76) (MFE +1.78%)
   - −4.0% : fill 30min 18% · séance 38% (57/159) · gap 6% · délai 36.7min · rebond 78% (38/57) (MFE +1.88%)
   - −5.0% : fill 30min 13% · séance 29% (46/159) · gap 4% · délai 42.5min · rebond 81% (34/46) (MFE +2.59%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.81%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −2.98%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.83%) → stop au-delà de −1.93% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=899 jambes) : jambe baissière méd −1.2% (p90 −2.86%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 97% (68/70) · rebond 48% (35/68)
      · −2.0% : fill 92% (64/70) · rebond 69% (39/64)
      · −3.0% : fill 85% (58/70) · rebond 57% (34/58)
      · −4.0% : fill 68% (45/70) · rebond 78% (30/45)
      · −5.0% : fill 51% (37/70) · rebond 80% (27/37)
   - **flat** (13 séances) :
      · −1.0% : fill 100% (13/13) · rebond 92% (11/13)
      · −2.0% : fill 41% (6/13) · rebond 89% (4/6)
      · −3.0% : fill 26% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 22% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 40% (30/76) · rebond 74% (19/30)
      · −2.0% : fill 22% (18/76) · rebond 81% (15/18)
      · −3.0% : fill 18% (15/76) · rebond 70% (10/15)
      · −4.0% : fill 13% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 12% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 65% si les 15 1res min sont vertes (77 cas) · 26% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 72% si début vert vs 20% si rouge (base 45% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **72%** · continue >prix actuel 45% ; creux résiduel méd -2.21% (q20 -3.74%) → **SL/trailing à −3.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.03% / q75 +3.98% → **scale +2.03% / runner +3.98%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **20%** (continue à baisser 50%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.68%** (au-delà de la MAE q10 -5.68%), cible rebond +1.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.24% .. +4.68%] · haut q95 +5.97% · bas q05 -4.53%
   - 60min (n=160) : retour [-4.5% .. +5.32%] · haut q95 +6.54% · bas q05 -5.34%
   - 2h (n=160) : retour [-4.71% .. +6.65%] · haut q95 +7.61% · bas q05 -5.85%
   - 4h (n=160) : retour [-5.21% .. +7.13%] · haut q95 +8.57% · bas q05 -6.74%
   - 6h (n=160) : retour [-5.68% .. +6.82%] · haut q95 +9.28% · bas q05 -6.91%
   - session (n=160) : retour [-6.84% .. +7.77%] · haut q95 +9.38% · bas q05 -7.43%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.61%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.4  _(neutre)_
- **ADX** : 25.1  _(tendance etablie)_
- **MACD** : hist -0.081  _(pas de croisement recent)_
- **BB** : %B 0.79 · largeur 23.6%
- **ATR** : 2.23 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.035  _(neutre)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 57.6  _(transition)_
- **MA** : MA20 37.03 · MA50 31.71 · MA200 31.37  _(prix > MA20)_
- **Dist MA** : MA20 +6.9% · MA50 +24.9% · MA200 +26.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (762900 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
