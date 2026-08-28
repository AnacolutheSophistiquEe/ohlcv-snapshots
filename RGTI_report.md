# RGTI

**Generated** : 2026-08-28T00:29:56.542298+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $16.44  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $16.44 (+1.7% vs entrée) · entrée $16.16 · stop $15.84 · T1 $16.64 · R/R 1.5  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk -0.085 _(réel 5 s)_ (GBM 0.228) · ¼-Kelly 0.034 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.07–$16.26 (mid $16.16)
- Spot actuel : $16.44 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : $15.84 (stop swing_plan-based (-10.23%))
- Targets : T1 $16.64 · R/R 1.5 | T2 $17.12 · R/R 3.0 | T3 $17.59 · R/R 4.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.84


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.30 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.23 %)** : le gap seul le franchit 0.798 % des séances (10 fois sur 1253).
   - exécution **3.405 pt plus bas** dans le cas TYPIQUE (médiane), 9.017 au p90, **20.983 au pire**
   - perte réelle **15.002 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 10.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0381 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.085 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5406** [0.4662 ; 0.6137] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4779** [0.4256 ; 0.5306] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5267** [0.474 ; 0.5789] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (37.5 pt), swing (39.0 pt), deep (34.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.77 %** | CVaR **-10.77 %** | vol 6.86 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 14.98 % contre 6.50 % aujourd'hui, rapport 2.30)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8181** (β de hausse 1.9954, asymétrie 0.9112) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.619× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 14.1486 sur grid_snapped (1.84 ATR, 13.938 %) — p(stop avant cible) 0.4524 [0.40 ; 0.51], R/R 1.455, perte reelle 19.597 % (gap inclus), CVaR 13.956 %, EV -2.4277 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.163 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 13.96 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 27 des 27 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 52.8 % de la queue et il ne reste que -406.12 EUR a partager. Prix du risque -0.191 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.92 ATR (stop 9.518 %) — p(stop avant cible) 0.6452 [0.59 ; 0.69], R/R 1.962, perte reelle 14.538 % (gap inclus), EV -3.4873 % — **REFUSE**
      - refuse : p_stop_first 0.645, borne haute 0.694 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.49 %) : P(cible) 15.5 % x 28.52 % + P(rien) 20.0 % x 7.40 % ne couvrent pas P(stop) 64.5 % x 14.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.84 ATR (stop 15.483 %) — p(stop avant cible) 0.3828 [0.33 ; 0.43], R/R 1.161, perte reelle 24.565 % (gap inclus), EV -3.1017 % — **REFUSE**
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.10 %) : P(cible) 17.9 % x 28.52 % + P(rien) 43.8 % x 2.74 % ne couvrent pas P(stop) 38.3 % x 24.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.65 ATR (stop 27.283 %) — p(stop avant cible) 0.0861 [0.06 ; 0.12], R/R 0.914, perte reelle 31.213 % (gap inclus), EV 0.7845 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.29 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.629 %) — p(stop avant cible) 0.9192 [0.89 ; 0.94], R/R 7.444, perte reelle 3.831 % (gap inclus), EV -1.6628 % — **REFUSE**
      - refuse : cible atteinte seulement 5.8 % du temps (< 15 %) meme a 10 seances : le R/R de 7.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.919, borne haute 0.945 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 5.8 % x 28.52 % + P(rien) 2.3 % x 9.43 % ne couvrent pas P(stop) 91.9 % x 3.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.259 %) — p(stop avant cible) 0.8455 [0.80 ; 0.88], R/R 4.635, perte reelle 6.153 % (gap inclus), EV -2.0126 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.846, borne haute 0.881 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.01 %) : P(cible) 9.0 % x 28.52 % + P(rien) 6.5 % x 9.64 % ne couvrent pas P(stop) 84.5 % x 6.15 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.92 ATR (stop 7.973 %) — p(stop avant cible) 0.689 [0.64 ; 0.74], R/R 2.241, perte reelle 12.728 % (gap inclus), EV -3.2948 % — **REFUSE**
      - refuse : cible atteinte seulement 14.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.689, borne haute 0.736 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.29 %) : P(cible) 14.6 % x 28.52 % + P(rien) 16.5 % x 7.91 % ne couvrent pas P(stop) 68.9 % x 12.73 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.84 ATR (stop 13.938 %) — p(stop avant cible) 0.4524 [0.40 ; 0.51], R/R 1.455, perte reelle 19.597 % (gap inclus), EV -2.4277 % — **REFUSE**
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.43 %) : P(cible) 17.2 % x 28.52 % + P(rien) 37.5 % x 4.06 % ne couvrent pas P(stop) 45.2 % x 19.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 17.922 %) — p(stop avant cible) 0.2939 [0.25 ; 0.34], R/R 0.914, perte reelle 31.213 % (gap inclus), EV -3.2302 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.23 %) : P(cible) 18.8 % x 28.52 % + P(rien) 51.8 % x 1.12 % ne couvrent pas P(stop) 29.4 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 19.552 %) — p(stop avant cible) 0.2565 [0.21 ; 0.30], R/R 0.914, perte reelle 31.213 % (gap inclus), EV -2.2578 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.26 %) : P(cible) 19.3 % x 28.52 % + P(rien) 55.0 % x 0.42 % ne couvrent pas P(stop) 25.7 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.65 ATR (stop 25.739 %) — p(stop avant cible) 0.1023 [0.07 ; 0.14], R/R 0.914, perte reelle 31.213 % (gap inclus), EV 0.6193 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.74 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.327 %) — p(stop avant cible) 0.0716 [0.05 ; 0.10], R/R 0.914, perte reelle 31.213 % (gap inclus), EV 1.0319 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.33 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 32.586 %) — p(stop avant cible) 0.0445 [0.03 ; 0.07], R/R 0.875, perte reelle 32.586 % (gap inclus), EV 1.2063 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.59 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 35.845 %) — p(stop avant cible) 0.0277 [0.01 ; 0.05], R/R 0.796, perte reelle 35.845 % (gap inclus), EV 1.2634 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.85 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.103 %) — p(stop avant cible) 0.015 [0.01 ; 0.03], R/R 0.729, perte reelle 39.103 % (gap inclus), EV 1.3033 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.10 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 42.362 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 0.673, perte reelle 42.362 % (gap inclus), EV 1.3711 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.36 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 45.62 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 0.625, perte reelle 45.62 % (gap inclus), EV 1.3597 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.62 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 48.879 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.583, perte reelle 48.879 % (gap inclus), EV 1.356 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.88 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 52.138 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 0.547, perte reelle 52.138 % (gap inclus), EV 1.347 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 52.14 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 16.44, ATR14 1.0714 (6.517 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.411 ATR = 2.679 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.326 % | 16.3864 | 92.25 % | 94.56 % | 95.66 % | 97.07 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.652 % | 16.3329 | 86.51 % | 91.23 % | 92.43 % | 94.94 % | 95.83 % | 97.43 % |
| 0.15 ATR | 0.978 % | 16.2793 | 81.07 % | 87.5 % | 89.1 % | 92.01 % | 93.9 % | 96.1 % |
| 0.2 ATR | 1.303 % | 16.2257 | 74.62 % | 82.96 % | 85.67 % | 88.88 % | 91.46 % | 94.56 % |
| 0.25 ATR | 1.629 % | 16.1721 | 68.58 % | 78.73 % | 81.84 % | 85.84 % | 88.82 % | 92.61 % |
| 0.35 ATR | 2.281 % | 16.065 | 56.09 % | 68.55 % | 74.07 % | 79.78 % | 84.45 % | 89.73 % |
| 0.5 ATR | 3.259 % | 15.9043 | 41.09 % | 56.75 % | 64.78 % | 71.99 % | 79.27 % | 85.73 % |
| 0.75 ATR | 4.888 % | 15.6364 | 21.75 % | 38.91 % | 49.34 % | 59.25 % | 70.93 % | 79.47 % |
| 1.0 ATR | 6.517 % | 15.3686 | 9.57 % | 23.79 % | 33.5 % | 46.31 % | 61.89 % | 73.31 % |
| 1.25 ATR | 8.147 % | 15.1007 | 4.03 % | 14.52 % | 23.51 % | 36.8 % | 52.85 % | 65.4 % |
| 1.5 ATR | 9.776 % | 14.8329 | 1.71 % | 7.16 % | 13.72 % | 25.38 % | 43.09 % | 57.19 % |
| 2.0 ATR | 13.034 % | 14.2971 | 0.4 % | 1.71 % | 3.94 % | 10.72 % | 25.3 % | 40.86 % |
| 2.5 ATR | 16.293 % | 13.7614 | 0.1 % | 0.4 % | 1.21 % | 4.45 % | 14.33 % | 28.44 % |
| 3.0 ATR | 19.552 % | 13.2257 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.15 % |
| 4.0 ATR | 26.069 % | 12.1543 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.93 % |
| 6.0 ATR | 39.103 % | 10.0114 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.29 ATR | 0.59 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.21 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.03 ATR | 1.33 ATR | 1.51 ATR | 1.68 ATR | 2.06 ATR | 2.46 ATR |
| **10 s.** | 0.63 ATR | 1.32 ATR | 1.45 ATR | 1.78 ATR | 2.01 ATR | 2.24 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.93 ATR | 1.72 ATR | 1.87 ATR | 2.32 ATR | 2.65 ATR | 2.87 ATR | 3.58 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.461–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.259 %, prix 15.9042), p(touche) 41.09 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (68.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.665–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.888 %, prix 15.6364), p(touche) 38.91 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.818–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.517 %, prix 15.3686), p(touche) 33.5 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.034–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.147 %, prix 15.1006), p(touche) 36.8 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.451–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.776 %, prix 14.8328), p(touche) 43.09 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.873–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.034 %, prix 14.2972), p(touche) 40.86 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.228 | EV/share : $0.074 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.134 | ¼-Kelly 0.034 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 19.9 | side 75.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.684% → cible +2.949% / stop −2.0%, p_fill 57%, n_eff≈24.4) : P(cible|rempli) **29%** · **EV/risk -0.085** (×p_fill ; si rempli -0.30% du capital)
  - **swing** (entrée dip −3.713% → cible +6.594% / stop −6.768%, p_fill 48%, n_eff≈22.7) : P(cible|rempli) **45%** · **EV/risk -0.066** (×p_fill ; si rempli -0.94% du capital)
  - **deep** (entrée dip −5.734% → cible +9.326% / stop −10.371%, p_fill 56%, n_eff≈28.8) : P(cible|rempli) **56%** · **EV/risk +0.033** (×p_fill ; si rempli +0.61% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→79% · +2.0%→72% · +3.0%→57% · +5.0%→42% · +8.0%→14%
- Range intraday médian 7.89% (p90 13.36%) · excursion haute méd. +4.06% / basse méd. −2.61%
- Profil de vol intra : ouverture 5.522% vs midi 1.598% vs clôture 1.838% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.026)_ ; drift intra méd. 0.515% ; recovery-V 31%
- **σ réalisé intraday** 4.56% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 45% / whipsaw 5%
- POC intraday (dernière séance, temps-au-prix) : 17.6928 (VA 17.3518–17.9911 ; dernier close 17.895)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 44% · rebond 74% · **stop −6.31%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. -0.46% · baisse 59% (gap-down >1% 40% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −1.19% (p90 −2.84%) · haut méd +1.28% · range méd 2.63%
- Excursion ouverture 15min (n=160) : bas méd −1.44% (p90 −3.96%) · haut méd +1.88% · range méd 3.78%
- Excursion ouverture 30min (n=160) : bas méd −1.83% (p90 −4.65%) · haut méd +2.1% · range méd 4.66%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −5.98%) · haut méd +2.53% · range méd 5.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.91 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 84% (135/159) · gap 48% · délai 0.0min · rebond 67% (88/135) (MFE +2.43%)
   - −1.0% : fill 30min 67% · séance 75% (126/159) · gap 40% · délai 0.0min · rebond 67% (82/126) (MFE +1.87%)
   - −1.5% : fill 30min 61% · séance 70% (120/159) · gap 35% · délai 0.0min · rebond 65% (78/120) (MFE +2.22%)
   - −2.0% : fill 30min 56% · séance 62% (111/159) · gap 27% · délai 0.0min · rebond 71% (76/111) (MFE +2.39%)
   - −3.0% : fill 30min 48% · séance 56% (99/159) · gap 11% · délai 1.2min · rebond 74% (73/99) (MFE +2.53%)
   - −4.0% : fill 30min 36% · séance 44% (78/159) · gap 5% · délai 6.3min · rebond 74% (57/78) (MFE +2.37%)
   - −5.0% : fill 30min 18% · séance 35% (65/159) · gap 3% · délai 27.2min · rebond 64% (46/65) (MFE +1.85%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −2.2%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −2.65%) → stop au-delà de −1.98% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.94% (p90 −2.91%) → stop au-delà de −2.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1171 jambes) : jambe baissière méd −1.29% (p90 −3.14%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 96% (82/84) · rebond 61% (49/82)
      · −2.0% : fill 85% (77/84) · rebond 70% (52/77)
      · −3.0% : fill 81% (72/84) · rebond 68% (51/72)
      · −4.0% : fill 67% (58/84) · rebond 71% (41/58)
      · −5.0% : fill 55% (50/84) · rebond 62% (35/50)
   - **flat** (15 séances) :
      · −1.0% : fill 96% (14/15) · rebond 94% (12/14)
      · −2.0% : fill 74% (12/15) · rebond 85% (10/12)
      · −3.0% : fill 50% (7/15) · rebond 90% (5/7)
      · −4.0% : fill 34% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 21% (5/15) · rebond 87% (3/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 41% (30/60) · rebond 68% (21/30)
      · −2.0% : fill 28% (22/60) · rebond 63% (14/22)
      · −3.0% : fill 23% (20/60) · rebond 89% (17/20)
      · −4.0% : fill 15% (14/60) · rebond 84% (12/14)
      · −5.0% : fill 12% (10/60) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 71% si les 15 1res min sont vertes (80 cas) · 29% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **51min** → P(séance verte=clôture>ouverture) 89% si début vert vs 15% si rouge (base 52% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **89%** · continue >prix actuel 52% ; creux résiduel méd -2.13% (q20 -3.51%) → **SL/trailing à −3.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.53% / q75 +5.77% → **scale +2.53% / runner +5.77%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **15%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.35%** (au-delà de la MAE q10 -5.35%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.17% .. +4.96%] · haut q95 +6.49% · bas q05 -6.26%
   - 60min (n=160) : retour [-5.56% .. +6.35%] · haut q95 +6.68% · bas q05 -6.83%
   - 2h (n=160) : retour [-6.39% .. +6.97%] · haut q95 +9.12% · bas q05 -7.59%
   - 4h (n=160) : retour [-7.13% .. +8.07%] · haut q95 +9.21% · bas q05 -7.87%
   - 6h (n=160) : retour [-7.45% .. +8.87%] · haut q95 +10.37% · bas q05 -8.62%
   - session (n=160) : retour [-7.26% .. +9.29%] · haut q95 +10.63% · bas q05 -8.63%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 14% vs absente 6% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.66% / p90 2.45%) · ~4.39 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 15.0 min, n=47)
   - −1.0% → **83%** (reprise méd 35.0 min, n=29)
   - −1.5% → **84%** (reprise méd 94.96 min, n=17)
   - −2.0% → **86%** (reprise méd 54.27 min, n=9)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.45%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.3% (q75 +9.62% / q95 +9.99%), MFE méd +9.65% / q90 +11.14%
   - Échelle scale-out : +9.65% (33%) / +10.43% (33%) / +11.14% (34%)
- **DÉSARMER** : repli > **−2.45%** depuis le plus-haut = décay → P(retournement) **23%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.14% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.16%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 42.2  _(momentum baissier)_
- **ADX** : 13.5  _(pas de tendance nette)_
- **MACD** : hist -0.134  _(bearish_recent)_
- **BB** : %B 0.32 · largeur 25.0%
- **ATR** : 1.07 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.003  _(neutre)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 53.0  _(transition)_
- **MA** : MA20 17.22 · MA50 17.04 · MA200 19.67  _(prix < MA20)_
- **Dist MA** : MA20 -4.5% · MA50 -3.5% · MA200 -16.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (840436 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
