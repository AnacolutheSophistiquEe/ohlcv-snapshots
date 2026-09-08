# SRT3

**Generated** : 2026-09-08T00:04:58.971337+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €233.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €233.00 (+1.4% vs entrée) · entrée €229.85 · stop €221.87 · T1 €235.63 · R/R 0.72  
> ↳ P(T1 av. stop) 65 % _(réel 5 s)_ · EV/risk 0.06 _(réel 5 s)_ (GBM 0.051) · ¼-Kelly 0.011 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €228.69–€231.00 (mid €229.85)
- Spot actuel : €233.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : €221.87 (stop swing_plan-based (-4.78%))
- Targets : T1 €235.63 · R/R 0.72 | T2 €241.40 · R/R 1.45 | T3 €247.18 · R/R 2.17
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €221.87


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.78 %)** : le gap seul le franchit 0.863 % des séances (11 fois sur 1274).
   - exécution **2.598 pt plus bas** dans le cas TYPIQUE (médiane), 5.192 au p90, **9.425 au pire**
   - perte réelle **7.948 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 4.78 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0274 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3927** [0.3222 ; 0.4667] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.3969** [0.3464 ; 0.4492] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3666** [0.3171 ; 0.4183] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.2 pt), swing (34.7 pt), deep (29.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.11 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0622** (β de hausse 1.1837, asymétrie 0.8973) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.296× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 205.075 sur atr_grid (3.5 ATR, 11.985 %) — p(stop avant cible) 0.1107 [0.08 ; 0.15], R/R 0.428, perte reelle 14.205 % (gap inclus), CVaR 11.987 %, EV 0.3758 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.82 ATR (stop 5.029 %) — p(stop avant cible) 0.4547 [0.40 ; 0.51], R/R 0.737, perte reelle 8.26 % (gap inclus), EV -1.1872 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 42.0 % x 6.09 % + P(rien) 12.6 % x 0.11 % ne couvrent pas P(stop) 45.5 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 5.48 ATR (stop 21.004 %) — p(stop avant cible) 0.0098 [0.00 ; 0.02], R/R 0.29, perte reelle 21.004 % (gap inclus), EV 0.7748 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.00 % > budget 12.00 %
      - ⚠ support DETECTE a 0.72 ATR du spot — compartiment <1, mesure a 45.8 % de casse (IC clusterise [0.427 ; 0.489] sur 1234 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 0.856 %) — p(stop avant cible) 0.8639 [0.82 ; 0.90], R/R 3.402, perte reelle 1.789 % (gap inclus), EV -0.7501 % — **REFUSE**
      - refuse : cible atteinte seulement 12.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.864, borne haute 0.897 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 12.8 % x 6.09 % + P(rien) 0.8 % x 1.80 % ne couvrent pas P(stop) 86.4 % x 1.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.712 %) — p(stop avant cible) 0.7831 [0.74 ; 0.82], R/R 1.855, perte reelle 3.28 % (gap inclus), EV -1.3115 % — **REFUSE**
      - refuse : p_stop_first 0.783, borne haute 0.824 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 20.3 % x 6.09 % + P(rien) 1.4 % x 1.58 % ne couvrent pas P(stop) 78.3 % x 3.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.82 ATR (stop 3.83 %) — p(stop avant cible) 0.5495 [0.50 ; 0.60], R/R 0.794, perte reelle 7.669 % (gap inclus), EV -1.9456 % — **REFUSE**
      - refuse : p_stop_first 0.549, borne haute 0.601 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.95 %) : P(cible) 36.8 % x 6.09 % + P(rien) 8.3 % x 0.37 % ne couvrent pas P(stop) 54.9 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.28 %) — p(stop avant cible) 0.5192 [0.47 ; 0.57], R/R 0.794, perte reelle 7.669 % (gap inclus), EV -1.6065 % — **REFUSE**
      - refuse : p_stop_first 0.519, borne haute 0.572 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.61 %) : P(cible) 38.3 % x 6.09 % + P(rien) 9.7 % x 0.43 % ne couvrent pas P(stop) 51.9 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.992 %) — p(stop avant cible) 0.3624 [0.31 ; 0.41], R/R 0.656, perte reelle 9.276 % (gap inclus), EV -0.5879 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 46.1 % x 6.09 % + P(rien) 17.6 % x -0.19 % ne couvrent pas P(stop) 36.2 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.849 %) — p(stop avant cible) 0.3217 [0.27 ; 0.37], R/R 0.656, perte reelle 9.276 % (gap inclus), EV -0.2143 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 46.8 % x 6.09 % + P(rien) 21.0 % x -0.37 % ne couvrent pas P(stop) 32.2 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.705 %) — p(stop avant cible) 0.2642 [0.22 ; 0.31], R/R 0.603, perte reelle 10.096 % (gap inclus), EV -0.0551 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 47.5 % x 6.09 % + P(rien) 26.1 % x -1.06 % ne couvrent pas P(stop) 26.4 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.561 %) — p(stop avant cible) 0.2327 [0.19 ; 0.28], R/R 0.54, perte reelle 11.278 % (gap inclus), EV -0.1168 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 47.8 % x 6.09 % + P(rien) 29.0 % x -1.38 % ne couvrent pas P(stop) 23.3 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.417 %) — p(stop avant cible) 0.1945 [0.16 ; 0.24], R/R 0.54, perte reelle 11.278 % (gap inclus), EV 0.2174 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 10.273 %) — p(stop avant cible) 0.1715 [0.13 ; 0.21], R/R 0.428, perte reelle 14.205 % (gap inclus), EV -0.1306 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 48.4 % x 6.09 % + P(rien) 34.4 % x -1.86 % ne couvrent pas P(stop) 17.2 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 11.985 %) — p(stop avant cible) 0.1107 [0.08 ; 0.15], R/R 0.428, perte reelle 14.205 % (gap inclus), EV 0.3758 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 13.697 %) — p(stop avant cible) 0.071 [0.05 ; 0.10], R/R 0.428, perte reelle 14.205 % (gap inclus), EV 0.6173 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.70 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 15.409 %) — p(stop avant cible) 0.0441 [0.03 ; 0.07], R/R 0.395, perte reelle 15.409 % (gap inclus), EV 0.6566 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.41 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.121 %) — p(stop avant cible) 0.0145 [0.01 ; 0.03], R/R 0.355, perte reelle 17.121 % (gap inclus), EV 0.7953 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.12 % > budget 12.00 %
   - 🔴 grid_snapped a 5.48 ATR (stop 19.805 %) — p(stop avant cible) 0.0113 [0.00 ; 0.03], R/R 0.307, perte reelle 19.805 % (gap inclus), EV 0.7776 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.81 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 20.546 %) — p(stop avant cible) 0.01 [0.00 ; 0.03], R/R 0.296, perte reelle 20.546 % (gap inclus), EV 0.7781 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.55 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 22.258 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.273, perte reelle 22.258 % (gap inclus), EV 0.8077 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.26 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 23.97 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.254, perte reelle 23.97 % (gap inclus), EV 0.8202 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.97 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 25.682 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.237, perte reelle 25.682 % (gap inclus), EV 0.8217 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.68 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 27.394 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.222, perte reelle 27.394 % (gap inclus), EV 0.8196 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.39 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 233.0, ATR14 7.9786 (3.424 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.383 ATR = 1.311 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.171 % | 232.6011 | 89.05 % | 92.99 % | 94.37 % | 96.14 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.342 % | 232.2021 | 82.54 % | 88.45 % | 90.71 % | 93.47 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.514 % | 231.8032 | 75.15 % | 84.01 % | 86.96 % | 90.59 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.685 % | 231.4043 | 68.54 % | 79.07 % | 83.0 % | 87.43 % | 92.24 % | 94.37 % |
| 0.25 ATR | 0.856 % | 231.0054 | 63.31 % | 75.72 % | 79.74 % | 85.05 % | 90.45 % | 93.07 % |
| 0.35 ATR | 1.198 % | 230.2075 | 53.25 % | 69.4 % | 74.11 % | 80.89 % | 87.06 % | 90.95 % |
| 0.5 ATR | 1.712 % | 229.0107 | 38.36 % | 56.86 % | 64.53 % | 74.06 % | 82.59 % | 88.34 % |
| 0.75 ATR | 2.568 % | 227.0161 | 19.72 % | 37.02 % | 48.12 % | 59.31 % | 72.24 % | 81.81 % |
| 1.0 ATR | 3.424 % | 225.0214 | 10.26 % | 24.88 % | 34.98 % | 47.92 % | 62.89 % | 74.77 % |
| 1.25 ATR | 4.28 % | 223.0268 | 4.83 % | 15.1 % | 24.9 % | 38.51 % | 53.33 % | 67.84 % |
| 1.5 ATR | 5.136 % | 221.0321 | 2.37 % | 10.07 % | 18.08 % | 31.19 % | 46.07 % | 62.21 % |
| 2.0 ATR | 6.849 % | 217.0429 | 0.79 % | 4.74 % | 8.5 % | 17.72 % | 34.93 % | 52.36 % |
| 2.5 ATR | 8.561 % | 213.0536 | 0.3 % | 2.17 % | 5.04 % | 11.09 % | 24.78 % | 42.31 % |
| 3.0 ATR | 10.273 % | 209.0643 | 0.2 % | 1.68 % | 3.16 % | 6.83 % | 17.81 % | 34.77 % |
| 4.0 ATR | 13.697 % | 201.0857 | 0.0 % | 0.69 % | 1.88 % | 3.96 % | 9.45 % | 20.7 % |
| 6.0 ATR | 20.546 % | 185.1286 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.19 % | 7.34 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.75 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.59 ATR | 0.65 ATR | 0.83 ATR | 1.00 ATR | 1.12 ATR | 1.51 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.81 ATR | 1.05 ATR | 1.25 ATR | 1.43 ATR | 1.92 ATR | 2.51 ATR |
| **5 s.** | 0.48 ATR | 0.95 ATR | 1.08 ATR | 1.44 ATR | 1.73 ATR | 1.92 ATR | 2.63 ATR | 3.64 ATR |
| **10 s.** | 0.68 ATR | 1.36 ATR | 1.55 ATR | 2.10 ATR | 2.49 ATR | 2.84 ATR | 3.93 ATR | 5.23 ATR |
| **20 s.** | 0.99 ATR | 2.12 ATR | 2.37 ATR | 3.13 ATR | 3.69 ATR | 4.11 ATR | 5.60 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.433–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.712 %, prix 229.011), p(touche) 38.36 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.649–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.568 %, prix 227.0166), p(touche) 37.02 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.809–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.424 %, prix 225.0221), p(touche) 34.98 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.078–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.28 %, prix 223.0276), p(touche) 38.51 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.548–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.849 %, prix 217.0418), p(touche) 34.93 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.366–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.561 %, prix 213.0529), p(touche) 42.31 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.051 | EV/share : €0.405 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 60 % | T2 33 % | T3 18 %
- Kelly (position) : f* 0.046 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 24.2 | bear 68.0 | side 7.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 233.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.619% → cible +1.124% / stop −1.5%, p_fill 79%, n_eff≈32.1) : P(cible|rempli) **55%** · **EV/risk +0.051** (×p_fill ; si rempli +0.10% du capital)
  - **swing** (entrée dip −1.356% → cible +2.514% / stop −3.471%, p_fill 58%, n_eff≈26.7) : P(cible|rempli) **65%** · **EV/risk +0.060** (×p_fill ; si rempli +0.35% du capital)
  - **deep** (entrée dip −2.094% → cible +3.555% / stop −5.246%, p_fill 57%, n_eff≈22.2) : P(cible|rempli) **85%** · **EV/risk +0.229** (×p_fill ; si rempli +2.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→48% · +3.0%→24% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.22% (p90 5.97%) · excursion haute méd. +1.89% / basse méd. −1.26%
- Profil de vol intra : ouverture 1.96% vs midi 0.809% vs clôture 0.978% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.093 ; neutre — autocorr -0.023)_ ; drift intra méd. 0.176% ; recovery-V 26%
- **σ réalisé intraday** 2.303% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 71% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 242.1875 (VA 239.7375–242.8875 ; dernier close 238.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 35% · rebond 66% · **stop −2.22%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.68 (high win-rate)
- Gaps overnight (n=159) : méd. -0.11% · baisse 55% (gap-down >1% 7% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.33% (p90 −1.51%) · haut méd +0.61% · range méd 1.07%
- Excursion ouverture 15min (n=160) : bas méd −0.46% (p90 −1.75%) · haut méd +0.77% · range méd 1.38%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −1.92%) · haut méd +0.82% · range méd 1.56%
- Excursion ouverture 60min (n=160) : bas méd −0.72% (p90 −2.09%) · haut méd +0.87% · range méd 1.75%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 237.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 78% (121/159) · gap 27% · délai 0.4min · rebond 50% (65/121) (MFE +1.01%)
   - −1.0% : fill 30min 41% · séance 67% (105/159) · gap 7% · délai 8.9min · rebond 59% (61/105) (MFE +1.23%)
   - −1.5% : fill 30min 25% · séance 47% (84/159) · gap 4% · délai 23.6min · rebond 59% (48/84) (MFE +1.33%)
   - −2.0% : fill 30min 9% · séance 35% (65/159) · gap 1% · délai 133.4min · rebond 66% (38/65) (MFE +1.52%)
   - −3.0% : fill 30min 4% · séance 13% (33/159) · gap 1% · délai 99.5min · rebond 67% (20/33) (MFE +1.96%)
   - −4.0% : fill 30min 2% · séance 8% (18/159) · gap 0% · délai 55.3min · rebond 68% (13/18) (MFE +2.14%)
   - −5.0% : fill 30min 0% · séance 5% (10/159) · gap 0% · délai 122.6min · rebond 86% (9/10) (MFE +2.89%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.88%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.99%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −2.51%) → stop au-delà de −1.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=453 jambes) : jambe baissière méd −1.01% (p90 −2.24%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 84% (49/58) · rebond 66% (31/49)
      · −2.0% : fill 41% (29/58) · rebond 69% (18/29)
      · −3.0% : fill 14% (18/58) · rebond 62% (11/18)
      · −4.0% : fill 10% (12/58) · rebond 68% (10/12)
      · −5.0% : fill 5% (6/58) · rebond 100% (6/6)
   - **flat** (39 séances) :
      · −1.0% : fill 67% (25/39) · rebond 48% (12/25)
      · −2.0% : fill 36% (17/39) · rebond 55% (9/17)
      · −3.0% : fill 9% (6/39) · rebond 38% (2/6)
      · −4.0% : fill 3% (2/39) · rebond 0% (0/2)
      · −5.0% : fill 3% (1/39) · rebond 0% (0/1)
   - **gap-up** (62 séances) :
      · −1.0% : fill 47% (31/62) · rebond 58% (18/31)
      · −2.0% : fill 26% (19/62) · rebond 72% (11/19)
      · −3.0% : fill 14% (9/62) · rebond 90% (7/9)
      · −4.0% : fill 8% (4/62) · rebond 90% (3/4)
      · −5.0% : fill 7% (3/62) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 54% si les 15 1res min sont vertes (83 cas) · 41% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 63% si début vert vs 31% si rouge (base 48% · écart 32 pts) ; prédictivité sature ensuite (plafond brut 254min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **63%** · continue >prix actuel 47% ; creux résiduel méd -1.47% (q20 -2.17%) → **SL/trailing à −2.17%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.03% / q75 +1.9% → **scale +1.03% / runner +1.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **31%** (continue à baisser 43%) → **RÉDUIRE ~69%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.57%** (au-delà de la MAE q10 -2.57%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.31% .. +2.02%] · haut q95 +2.59% · bas q05 -2.9%
   - 60min (n=160) : retour [-2.31% .. +2.33%] · haut q95 +2.71% · bas q05 -3.26%
   - 2h (n=160) : retour [-2.18% .. +2.26%] · haut q95 +2.94% · bas q05 -3.71%
   - 4h (n=160) : retour [-2.26% .. +2.33%] · haut q95 +3.11% · bas q05 -3.65%
   - 6h (n=160) : retour [-2.48% .. +2.72%] · haut q95 +3.35% · bas q05 -3.82%
   - session (n=160) : retour [-3.37% .. +3.79%] · haut q95 +4.79% · bas q05 -4.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 53.4  _(neutre)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist -1.408  _(bearish_recent)_
- **BB** : %B 0.18 · largeur 11.5%
- **ATR** : 7.98 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.045  _(neutre)_
- **Vol ratio** : 0.32  _(volume atone)_
- **Choppiness** : 50.3  _(transition)_
- **MA** : MA20 241.77 · MA50 235.01 · MA200 232.98  _(prix < MA20)_
- **Dist MA** : MA20 -3.6% · MA50 -0.9% · MA200 +0.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (762398 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
