# SRT3

**Generated** : 2026-09-04T21:37:27.963499+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €237.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot €237.20 (+2.4% vs entrée) · entrée €231.74 · stop €223.87 · T1 €237.72 · R/R 0.76  
> ↳ P(T1 av. stop) 86 % _(réel 5 s)_ · EV/risk 0.169 _(réel 5 s)_ (GBM 0.021) · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €230.54–€232.93 (mid €231.74)
- Spot actuel : €237.20 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : €223.87 (stop swing_plan-based (-5.62%))
- Targets : T1 €237.72 · R/R 0.76 | T2 €243.69 · R/R 1.52 | T3 €249.67 · R/R 2.28
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €223.87


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.62 %)** : le gap seul le franchit 0.785 % des séances (10 fois sur 1274).
   - exécution **2.19 pt plus bas** dans le cas TYPIQUE (médiane), 4.775 au p90, **8.585 au pire**
   - perte réelle **8.26 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 5.62 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0207 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3876** [0.3174 ; 0.4616] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.4058** [0.355 ; 0.4582] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3912** [0.3408 ; 0.4434] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (38.3 pt), swing (30.8 pt), deep (43.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.12 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0632** (β de hausse 1.1837, asymétrie 0.8982) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.295× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 209.675 sur atr_grid (3.5 ATR, 11.604 %) — p(stop avant cible) 0.1293 [0.10 ; 0.17], R/R 0.37, perte reelle 14.205 % (gap inclus), CVaR 11.606 %, EV 0.0387 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.973 %) — p(stop avant cible) 0.4539 [0.40 ; 0.51], R/R 0.637, perte reelle 8.26 % (gap inclus), EV -1.3899 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.39 %) : P(cible) 45.0 % x 5.26 % + P(rien) 9.6 % x -0.06 % ne couvrent pas P(stop) 45.4 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.36 ATR (stop 6.462 %) — p(stop avant cible) 0.3291 [0.28 ; 0.38], R/R 0.567, perte reelle 9.276 % (gap inclus), EV -0.4887 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 50.7 % x 5.26 % + P(rien) 16.4 % x -0.63 % ne couvrent pas P(stop) 32.9 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 6.1 ATR (stop 22.159 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 0.237, perte reelle 22.159 % (gap inclus), EV 0.6289 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.16 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.829 %) — p(stop avant cible) 0.8507 [0.81 ; 0.89], R/R 3.007, perte reelle 1.749 % (gap inclus), EV -0.7027 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.851, borne haute 0.885 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 14.9 % x 5.26 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 85.1 % x 1.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.658 %) — p(stop avant cible) 0.7776 [0.73 ; 0.82], R/R 1.616, perte reelle 3.255 % (gap inclus), EV -1.3732 % — **REFUSE**
      - refuse : p_stop_first 0.778, borne haute 0.819 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 22.0 % x 5.26 % + P(rien) 0.2 % x 0.40 % ne couvrent pas P(stop) 77.8 % x 3.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.487 %) — p(stop avant cible) 0.6874 [0.64 ; 0.73], R/R 1.004, perte reelle 5.237 % (gap inclus), EV -2.0039 % — **REFUSE**
      - refuse : p_stop_first 0.687, borne haute 0.735 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.00 %) : P(cible) 30.1 % x 5.26 % + P(rien) 1.1 % x 0.94 % ne couvrent pas P(stop) 68.7 % x 5.24 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.315 %) — p(stop avant cible) 0.5744 [0.52 ; 0.63], R/R 0.686, perte reelle 7.669 % (gap inclus), EV -2.3765 % — **REFUSE**
      - refuse : p_stop_first 0.574, borne haute 0.626 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.38 %) : P(cible) 38.2 % x 5.26 % + P(rien) 4.3 % x 0.41 % ne couvrent pas P(stop) 57.4 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.36 ATR (stop 5.514 %) — p(stop avant cible) 0.3946 [0.34 ; 0.45], R/R 0.637, perte reelle 8.26 % (gap inclus), EV -0.7239 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 48.8 % x 5.26 % + P(rien) 11.8 % x -0.26 % ne couvrent pas P(stop) 39.5 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.46 %) — p(stop avant cible) 0.2841 [0.24 ; 0.33], R/R 0.521, perte reelle 10.096 % (gap inclus), EV -0.3515 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 52.1 % x 5.26 % + P(rien) 19.5 % x -1.14 % ne couvrent pas P(stop) 28.4 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.289 %) — p(stop avant cible) 0.2482 [0.20 ; 0.30], R/R 0.498, perte reelle 10.559 % (gap inclus), EV -0.2146 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 52.5 % x 5.26 % + P(rien) 22.7 % x -1.56 % ne couvrent pas P(stop) 24.8 % x 10.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.118 %) — p(stop avant cible) 0.2134 [0.17 ; 0.26], R/R 0.466, perte reelle 11.278 % (gap inclus), EV -0.1403 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 52.8 % x 5.26 % + P(rien) 25.9 % x -1.97 % ne couvrent pas P(stop) 21.3 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 9.946 %) — p(stop avant cible) 0.1826 [0.14 ; 0.23], R/R 0.435, perte reelle 12.088 % (gap inclus), EV -0.0022 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 53.2 % x 5.26 % + P(rien) 28.6 % x -2.07 % ne couvrent pas P(stop) 18.3 % x 12.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 11.604 %) — p(stop avant cible) 0.1293 [0.10 ; 0.17], R/R 0.37, perte reelle 14.205 % (gap inclus), EV 0.0387 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 13.262 %) — p(stop avant cible) 0.088 [0.06 ; 0.12], R/R 0.37, perte reelle 14.205 % (gap inclus), EV 0.3255 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.26 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 14.92 %) — p(stop avant cible) 0.0499 [0.03 ; 0.08], R/R 0.352, perte reelle 14.92 % (gap inclus), EV 0.4666 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.92 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.577 %) — p(stop avant cible) 0.0164 [0.01 ; 0.03], R/R 0.317, perte reelle 16.577 % (gap inclus), EV 0.6017 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.58 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 18.235 %) — p(stop avant cible) 0.014 [0.01 ; 0.03], R/R 0.288, perte reelle 18.235 % (gap inclus), EV 0.6029 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.23 % > budget 12.00 %
   - 🟢 grid_snapped a 6.1 ATR (stop 21.211 %) — p(stop avant cible) 0.0096 [0.00 ; 0.02], R/R 0.248, perte reelle 21.211 % (gap inclus), EV 0.5963 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.21 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 23.208 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.227, perte reelle 23.208 % (gap inclus), EV 0.6361 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.21 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.866 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.211, perte reelle 24.866 % (gap inclus), EV 0.644 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.87 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 26.524 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.198, perte reelle 26.524 % (gap inclus), EV 0.6426 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.52 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 237.2, ATR14 7.8643 (3.315 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 1.267 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.166 % | 236.8068 | 89.05 % | 92.99 % | 94.37 % | 96.14 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.332 % | 236.4136 | 82.54 % | 88.45 % | 90.71 % | 93.47 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.497 % | 236.0204 | 75.05 % | 83.91 % | 86.96 % | 90.59 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.663 % | 235.6271 | 68.44 % | 78.97 % | 83.0 % | 87.43 % | 92.24 % | 94.37 % |
| 0.25 ATR | 0.829 % | 235.2339 | 63.21 % | 75.62 % | 79.74 % | 85.05 % | 90.45 % | 93.07 % |
| 0.35 ATR | 1.16 % | 234.4475 | 53.16 % | 69.3 % | 74.11 % | 80.89 % | 87.06 % | 90.95 % |
| 0.5 ATR | 1.658 % | 233.2679 | 38.26 % | 56.76 % | 64.43 % | 74.06 % | 82.59 % | 88.34 % |
| 0.75 ATR | 2.487 % | 231.3018 | 19.63 % | 36.92 % | 48.02 % | 59.31 % | 72.24 % | 81.91 % |
| 1.0 ATR | 3.315 % | 229.3357 | 10.26 % | 24.78 % | 34.88 % | 47.82 % | 62.89 % | 74.87 % |
| 1.25 ATR | 4.144 % | 227.3696 | 4.83 % | 15.1 % | 24.9 % | 38.42 % | 53.43 % | 67.94 % |
| 1.5 ATR | 4.973 % | 225.4036 | 2.37 % | 10.07 % | 18.08 % | 31.09 % | 46.17 % | 62.31 % |
| 2.0 ATR | 6.631 % | 221.4714 | 0.79 % | 4.74 % | 8.5 % | 17.62 % | 35.02 % | 52.46 % |
| 2.5 ATR | 8.289 % | 217.5393 | 0.3 % | 2.17 % | 5.04 % | 11.09 % | 24.88 % | 42.41 % |
| 3.0 ATR | 9.946 % | 213.6071 | 0.2 % | 1.68 % | 3.16 % | 6.83 % | 17.91 % | 34.87 % |
| 4.0 ATR | 13.262 % | 205.7428 | 0.0 % | 0.69 % | 1.88 % | 3.96 % | 9.55 % | 20.8 % |
| 6.0 ATR | 19.893 % | 190.0143 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.19 % | 7.34 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.51 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.81 ATR | 1.05 ATR | 1.25 ATR | 1.43 ATR | 1.92 ATR | 2.51 ATR |
| **5 s.** | 0.48 ATR | 0.95 ATR | 1.07 ATR | 1.44 ATR | 1.73 ATR | 1.91 ATR | 2.63 ATR | 3.64 ATR |
| **10 s.** | 0.68 ATR | 1.37 ATR | 1.55 ATR | 2.10 ATR | 2.49 ATR | 2.85 ATR | 3.95 ATR | 5.24 ATR |
| **20 s.** | 0.99 ATR | 2.12 ATR | 2.37 ATR | 3.13 ATR | 3.70 ATR | 4.12 ATR | 5.61 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.658 %, prix 233.2672), p(touche) 38.26 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.648–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.487 %, prix 231.3008), p(touche) 36.92 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.807–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.315 %, prix 229.3368), p(touche) 34.88 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.075–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.144 %, prix 227.3704), p(touche) 38.42 % (en stress 92.08 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.552–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.631 %, prix 221.4713), p(touche) 35.02 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.371–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.289 %, prix 217.5385), p(touche) 42.41 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.021 | EV/share : €0.162 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 31 % | T3 16 %
- Kelly (position) : f* 0.017 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 21.8 | bear 8.6 | side 69.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 237.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.046% → cible +1.154% / stop −1.5%, p_fill 55%, n_eff≈23.5) : P(cible|rempli) **34%** · **EV/risk +0.007** (×p_fill ; si rempli +0.02% du capital)
  - **swing** (entrée dip −2.305% → cible +2.58% / stop −3.394%, p_fill 34%, n_eff≈18.1) : P(cible|rempli) **86%** · **EV/risk +0.169** (×p_fill ; si rempli +1.69% du capital)
  - **deep** (entrée dip −3.557% → cible +3.649% / stop −5.157%, p_fill 33%, n_eff≈15.6) : P(cible|rempli) **68%** · **EV/risk +0.048** (×p_fill ; si rempli +0.74% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→75% · +2.0%→46% · +3.0%→24% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.23% (p90 5.97%) · excursion haute méd. +1.84% / basse méd. −1.33%
- Profil de vol intra : ouverture 1.989% vs midi 0.806% vs clôture 0.981% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.095 ; neutre — autocorr -0.029)_ ; drift intra méd. 0.27% ; recovery-V 21%
- **σ réalisé intraday** 2.325% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 67% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 251.1125 (VA 249.6425–254.0525 ; dernier close 247.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 33% · rebond 68% · **stop −2.45%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. -0.08% · baisse 52% (gap-down >1% 7% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.43% (p90 −1.55%) · haut méd +0.57% · range méd 1.15%
- Excursion ouverture 15min (n=160) : bas méd −0.53% (p90 −1.85%) · haut méd +0.66% · range méd 1.46%
- Excursion ouverture 30min (n=160) : bas méd −0.58% (p90 −1.95%) · haut méd +0.83% · range méd 1.66%
- Excursion ouverture 60min (n=160) : bas méd −0.73% (p90 −2.23%) · haut méd +0.92% · range méd 1.78%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 247.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 76% (120/159) · gap 25% · délai 0.4min · rebond 49% (64/120) (MFE +0.97%)
   - −1.0% : fill 30min 42% · séance 65% (104/159) · gap 7% · délai 4.5min · rebond 59% (60/104) (MFE +1.21%)
   - −1.5% : fill 30min 26% · séance 46% (83/159) · gap 4% · délai 19.3min · rebond 60% (48/83) (MFE +1.32%)
   - −2.0% : fill 30min 9% · séance 33% (63/159) · gap 1% · délai 98.0min · rebond 68% (37/63) (MFE +1.52%)
   - −3.0% : fill 30min 4% · séance 13% (33/159) · gap 1% · délai 99.5min · rebond 67% (20/33) (MFE +1.96%)
   - −4.0% : fill 30min 3% · séance 8% (18/159) · gap 0% · délai 55.3min · rebond 68% (13/18) (MFE +2.14%)
   - −5.0% : fill 30min 0% · séance 5% (10/159) · gap 0% · délai 122.6min · rebond 86% (9/10) (MFE +2.89%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.4% (p90 −1.95%) → stop au-delà de −1.09% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.1% (p90 −2.04%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −2.51%) → stop au-delà de −1.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=452 jambes) : jambe baissière méd −1.02% (p90 −2.27%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 81% (47/56) · rebond 66% (30/47)
      · −2.0% : fill 37% (27/56) · rebond 74% (17/27)
      · −3.0% : fill 17% (18/56) · rebond 62% (11/18)
      · −4.0% : fill 12% (12/56) · rebond 68% (10/12)
      · −5.0% : fill 6% (6/56) · rebond 100% (6/6)
   - **flat** (40 séances) :
      · −1.0% : fill 67% (26/40) · rebond 48% (12/26)
      · −2.0% : fill 36% (17/40) · rebond 55% (9/17)
      · −3.0% : fill 9% (6/40) · rebond 38% (2/6)
      · −4.0% : fill 3% (2/40) · rebond 0% (0/2)
      · −5.0% : fill 3% (1/40) · rebond 0% (0/1)
   - **gap-up** (63 séances) :
      · −1.0% : fill 47% (31/63) · rebond 58% (18/31)
      · −2.0% : fill 26% (19/63) · rebond 72% (11/19)
      · −3.0% : fill 14% (9/63) · rebond 90% (7/9)
      · −4.0% : fill 8% (4/63) · rebond 90% (3/4)
      · −5.0% : fill 7% (3/63) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 56% si les 15 1res min sont vertes (84 cas) · 40% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 62% si début vert vs 34% si rouge (base 49% · écart 28 pts) ; prédictivité sature ensuite (plafond brut 254min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **62%** · continue >prix actuel 45% ; creux résiduel méd -1.45% (q20 -2.33%) → **SL/trailing à −2.33%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.0% / q75 +1.73% → **scale +1.0% / runner +1.73%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **34%** (continue à baisser 42%) → **RÉDUIRE ~66%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.59% .. +2.06%] · haut q95 +2.61% · bas q05 -2.99%
   - 60min (n=160) : retour [-2.37% .. +2.33%] · haut q95 +2.73% · bas q05 -3.34%
   - 2h (n=160) : retour [-2.18% .. +2.28%] · haut q95 +2.94% · bas q05 -3.76%
   - 4h (n=160) : retour [-2.28% .. +2.4%] · haut q95 +3.17% · bas q05 -3.76%
   - 6h (n=160) : retour [-2.5% .. +2.81%] · haut q95 +3.43% · bas q05 -3.83%
   - session (n=160) : retour [-3.41% .. +3.85%] · haut q95 +4.96% · bas q05 -4.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.7  _(neutre)_
- **ADX** : 18.1  _(pas de tendance nette)_
- **MACD** : hist -0.641  _(bearish_recent)_
- **BB** : %B 0.32 · largeur 11.0%
- **ATR** : 7.86 (30.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.015  _(neutre)_
- **Vol ratio** : 1.17  _(volume normal)_
- **Choppiness** : 49.8  _(transition)_
- **MA** : MA20 242.05 · MA50 234.82 · MA200 232.93  _(prix < MA20)_
- **Dist MA** : MA20 -2.0% · MA50 +1.0% · MA200 +1.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (760996 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
