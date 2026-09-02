# SRT3

**Generated** : 2026-09-02T00:03:37.812964+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €246.90  

> 🟡 **WAIT-FOR-DIP** — spot +4.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €246.90 (+4.6% vs entrée) · entrée €236.10 · stop €228.57 · T1 €241.76 · R/R 0.75  
> ↳ P(T1 av. stop) 67 % · EV/risk 0.071 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €234.97–€237.23 (mid €236.10)
- Spot actuel : €246.90 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : €228.57 (stop swing_plan-based (-7.42%))
- Targets : T1 €241.76 · R/R 0.75 | T2 €247.42 · R/R 1.5 | T3 €253.08 · R/R 2.25
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €228.57


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.42 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **2.237 pt plus bas** dans le cas TYPIQUE (médiane), 5.092 au p90, **6.785 au pire**
   - perte réelle **10.096 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 7.42 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0105 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3768** [0.3071 ; 0.4505] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.4088** [0.3579 ; 0.4612] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.4163** [0.3652 ; 0.4688] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (45.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.12 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0637** (β de hausse 1.1747, asymétrie 0.9055) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.327× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 224.2558 sur grid_snapped (2.71 ATR, 9.171 %) — p(stop avant cible) 0.1646 [0.13 ; 0.21], R/R 0.222, perte reelle 11.278 % (gap inclus), CVaR 9.176 %, EV -0.352 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.02 ATR (stop 5.042 %) — p(stop avant cible) 0.3474 [0.30 ; 0.40], R/R 0.303, perte reelle 8.26 % (gap inclus), EV -1.2697 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 64.2 % x 2.50 % + P(rien) 1.1 % x -0.61 % ne couvrent pas P(stop) 34.7 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.71 ATR (stop 10.178 %) — p(stop avant cible) 0.1402 [0.11 ; 0.18], R/R 0.176, perte reelle 14.205 % (gap inclus), EV -0.5475 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 74.8 % x 2.50 % + P(rien) 11.2 % x -3.81 % ne couvrent pas P(stop) 14.0 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 7.66 ATR (stop 25.271 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.099, perte reelle 25.271 % (gap inclus), EV 0.1934 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.27 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.762 %) — p(stop avant cible) 0.7143 [0.67 ; 0.76], R/R 1.483, perte reelle 1.687 % (gap inclus), EV -0.4902 % — **REFUSE**
      - refuse : p_stop_first 0.714, borne haute 0.760 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 28.6 % x 2.50 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 71.4 % x 1.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.525 %) — p(stop avant cible) 0.6302 [0.58 ; 0.68], R/R 0.871, perte reelle 2.873 % (gap inclus), EV -0.8853 % — **REFUSE**
      - refuse : p_stop_first 0.630, borne haute 0.680 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 37.0 % x 2.50 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 63.0 % x 2.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.287 %) — p(stop avant cible) 0.5286 [0.48 ; 0.58], R/R 0.509, perte reelle 4.92 % (gap inclus), EV -1.4213 % — **REFUSE**
      - refuse : p_stop_first 0.529, borne haute 0.581 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.42 %) : P(cible) 47.1 % x 2.50 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 52.9 % x 4.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.02 ATR (stop 4.036 %) — p(stop avant cible) 0.3943 [0.34 ; 0.45], R/R 0.326, perte reelle 7.669 % (gap inclus), EV -1.5328 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.53 %) : P(cible) 59.9 % x 2.50 % + P(rien) 0.7 % x -0.98 % ne couvrent pas P(stop) 39.4 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 4.574 %) — p(stop avant cible) 0.3813 [0.33 ; 0.43], R/R 0.326, perte reelle 7.669 % (gap inclus), EV -1.4048 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.40 %) : P(cible) 61.1 % x 2.50 % + P(rien) 0.8 % x -1.07 % ne couvrent pas P(stop) 38.1 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.098 %) — p(stop avant cible) 0.2739 [0.23 ; 0.32], R/R 0.27, perte reelle 9.276 % (gap inclus), EV -0.8166 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 70.1 % x 2.50 % + P(rien) 2.5 % x -1.14 % ne couvrent pas P(stop) 27.4 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.861 %) — p(stop avant cible) 0.2455 [0.20 ; 0.29], R/R 0.27, perte reelle 9.276 % (gap inclus), EV -0.532 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 72.0 % x 2.50 % + P(rien) 3.4 % x -1.68 % ne couvrent pas P(stop) 24.6 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.71 ATR (stop 9.171 %) — p(stop avant cible) 0.1646 [0.13 ; 0.21], R/R 0.222, perte reelle 11.278 % (gap inclus), EV -0.352 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 74.4 % x 2.50 % + P(rien) 9.2 % x -3.89 % ne couvrent pas P(stop) 16.5 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 10.672 %) — p(stop avant cible) 0.1303 [0.10 ; 0.17], R/R 0.176, perte reelle 14.205 % (gap inclus), EV -0.4613 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 74.8 % x 2.50 % + P(rien) 12.2 % x -3.97 % ne couvrent pas P(stop) 13.0 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 12.197 %) — p(stop avant cible) 0.0889 [0.06 ; 0.12], R/R 0.176, perte reelle 14.205 % (gap inclus), EV -0.1374 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 75.1 % x 2.50 % + P(rien) 16.0 % x -4.70 % ne couvrent pas P(stop) 8.9 % x 14.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.722 %) — p(stop avant cible) 0.0656 [0.04 ; 0.10], R/R 0.176, perte reelle 14.205 % (gap inclus), EV 0.0164 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.72 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 15.246 %) — p(stop avant cible) 0.0391 [0.02 ; 0.06], R/R 0.164, perte reelle 15.246 % (gap inclus), EV 0.0601 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.25 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.771 %) — p(stop avant cible) 0.0117 [0.00 ; 0.03], R/R 0.149, perte reelle 16.771 % (gap inclus), EV 0.1713 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.77 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.295 %) — p(stop avant cible) 0.0113 [0.00 ; 0.03], R/R 0.137, perte reelle 18.295 % (gap inclus), EV 0.1534 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.30 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.82 %) — p(stop avant cible) 0.0089 [0.00 ; 0.02], R/R 0.126, perte reelle 19.82 % (gap inclus), EV 0.1536 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.82 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.345 %) — p(stop avant cible) 0.0066 [0.00 ; 0.02], R/R 0.117, perte reelle 21.345 % (gap inclus), EV 0.1525 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.34 % > budget 12.00 %
   - 🟢 grid_snapped a 7.66 ATR (stop 24.265 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.103, perte reelle 24.265 % (gap inclus), EV 0.1937 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.27 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 246.9, ATR14 7.5286 (3.049 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 1.165 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.152 % | 246.5236 | 89.05 % | 92.99 % | 94.37 % | 96.14 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.305 % | 246.1471 | 82.54 % | 88.45 % | 90.71 % | 93.47 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.457 % | 245.7707 | 75.05 % | 83.91 % | 86.96 % | 90.59 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.61 % | 245.3943 | 68.44 % | 78.97 % | 83.0 % | 87.43 % | 92.24 % | 94.37 % |
| 0.25 ATR | 0.762 % | 245.0179 | 63.31 % | 75.62 % | 79.74 % | 85.05 % | 90.55 % | 93.07 % |
| 0.35 ATR | 1.067 % | 244.265 | 53.16 % | 69.2 % | 74.11 % | 80.99 % | 87.16 % | 91.16 % |
| 0.5 ATR | 1.525 % | 243.1357 | 38.17 % | 56.66 % | 64.43 % | 74.26 % | 82.79 % | 88.54 % |
| 0.75 ATR | 2.287 % | 241.2536 | 19.63 % | 36.82 % | 47.92 % | 59.31 % | 72.44 % | 82.21 % |
| 1.0 ATR | 3.049 % | 239.3714 | 10.26 % | 24.68 % | 34.68 % | 47.72 % | 63.08 % | 75.18 % |
| 1.25 ATR | 3.812 % | 237.4893 | 4.83 % | 15.0 % | 24.7 % | 38.32 % | 53.73 % | 68.24 % |
| 1.5 ATR | 4.574 % | 235.6071 | 2.37 % | 10.07 % | 18.08 % | 31.09 % | 46.47 % | 62.61 % |
| 2.0 ATR | 6.098 % | 231.8429 | 0.79 % | 4.74 % | 8.5 % | 17.62 % | 35.32 % | 52.76 % |
| 2.5 ATR | 7.623 % | 228.0786 | 0.3 % | 2.17 % | 5.04 % | 11.09 % | 25.17 % | 42.71 % |
| 3.0 ATR | 9.148 % | 224.3143 | 0.2 % | 1.68 % | 3.16 % | 6.83 % | 18.21 % | 35.18 % |
| 4.0 ATR | 12.197 % | 216.7857 | 0.0 % | 0.69 % | 1.88 % | 3.96 % | 9.55 % | 21.11 % |
| 6.0 ATR | 18.295 % | 201.7286 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.19 % | 7.34 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.51 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.24 ATR | 1.43 ATR | 1.92 ATR | 2.51 ATR |
| **5 s.** | 0.48 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.73 ATR | 1.91 ATR | 2.63 ATR | 3.64 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.57 ATR | 2.11 ATR | 2.51 ATR | 2.87 ATR | 3.95 ATR | 5.24 ATR |
| **20 s.** | 1.01 ATR | 2.14 ATR | 2.39 ATR | 3.15 ATR | 3.72 ATR | 4.16 ATR | 5.61 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.525 %, prix 243.1348), p(touche) 38.17 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.647–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.287 %, prix 241.2534), p(touche) 36.82 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.049 %, prix 239.372), p(touche) 34.68 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.072–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.812 %, prix 237.4882), p(touche) 38.32 % (en stress 92.08 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.566–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.098 %, prix 231.844), p(touche) 35.32 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.386–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.623 %, prix 228.0788), p(touche) 42.71 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : €-0.059 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 34 % | T3 20 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 20.7 | bear 8.5 | side 70.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 494.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.99% → cible +1.072% / stop −1.5%, p_fill 31%, n_eff≈14.1) : P(cible|rempli) **67%** · **EV/risk +0.099** (×p_fill ; si rempli +0.48% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→75% · +2.0%→45% · +3.0%→24% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.23% (p90 6.3%) · excursion haute méd. +1.79% / basse méd. −1.33%
- Profil de vol intra : ouverture 1.983% vs midi 0.826% vs clôture 0.981% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.097 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. 0.332% ; recovery-V 23%
- **σ réalisé intraday** 2.338% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 65% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 250.4338 (VA 248.4388–251.8587 ; dernier close 251.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 34% · rebond 68% · **stop −2.44%** sous le fill (sous le bruit) · cible +1.53% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. -0.09% · baisse 53% (gap-down >1% 8% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.44% (p90 −1.64%) · haut méd +0.54% · range méd 1.17%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −1.85%) · haut méd +0.64% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −1.95%) · haut méd +0.82% · range méd 1.63%
- Excursion ouverture 60min (n=160) : bas méd −0.75% (p90 −2.24%) · haut méd +0.82% · range méd 1.78%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 249.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 76% (120/159) · gap 26% · délai 0.4min · rebond 50% (65/120) (MFE +1.01%)
   - −1.0% : fill 30min 42% · séance 65% (104/159) · gap 8% · délai 2.6min · rebond 60% (61/104) (MFE +1.23%)
   - −1.5% : fill 30min 26% · séance 47% (84/159) · gap 4% · délai 19.5min · rebond 60% (49/84) (MFE +1.33%)
   - −2.0% : fill 30min 9% · séance 34% (64/159) · gap 1% · délai 98.2min · rebond 68% (38/64) (MFE +1.53%)
   - −3.0% : fill 30min 4% · séance 14% (33/159) · gap 1% · délai 99.5min · rebond 67% (20/33) (MFE +1.96%)
   - −4.0% : fill 30min 3% · séance 8% (18/159) · gap 0% · délai 55.3min · rebond 68% (13/18) (MFE +2.14%)
   - −5.0% : fill 30min 0% · séance 5% (10/159) · gap 0% · délai 122.6min · rebond 86% (9/10) (MFE +2.89%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.97%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −2.15%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −2.51%) → stop au-delà de −1.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=451 jambes) : jambe baissière méd −1.01% (p90 −2.27%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 81% (48/57) · rebond 66% (31/48)
      · −2.0% : fill 37% (28/57) · rebond 75% (18/28)
      · −3.0% : fill 17% (18/57) · rebond 62% (11/18)
      · −4.0% : fill 12% (12/57) · rebond 68% (10/12)
      · −5.0% : fill 6% (6/57) · rebond 100% (6/6)
   - **flat** (39 séances) :
      · −1.0% : fill 65% (25/39) · rebond 53% (12/25)
      · −2.0% : fill 38% (17/39) · rebond 55% (9/17)
      · −3.0% : fill 9% (6/39) · rebond 38% (2/6)
      · −4.0% : fill 3% (2/39) · rebond 0% (0/2)
      · −5.0% : fill 3% (1/39) · rebond 0% (0/1)
   - **gap-up** (63 séances) :
      · −1.0% : fill 47% (31/63) · rebond 58% (18/31)
      · −2.0% : fill 26% (19/63) · rebond 72% (11/19)
      · −3.0% : fill 14% (9/63) · rebond 90% (7/9)
      · −4.0% : fill 8% (4/63) · rebond 90% (3/4)
      · −5.0% : fill 7% (3/63) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 58% si les 15 1res min sont vertes (84 cas) · 40% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 64% si début vert vs 34% si rouge (base 50% · écart 30 pts) ; prédictivité sature ensuite (plafond brut 254min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **64%** · continue >prix actuel 46% ; creux résiduel méd -1.43% (q20 -2.13%) → **SL/trailing à −2.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.03% / q75 +1.78% → **scale +1.03% / runner +1.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **34%** (continue à baisser 42%) → **RÉDUIRE ~66%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.68% .. +2.07%] · haut q95 +2.62% · bas q05 -3.01%
   - 60min (n=160) : retour [-2.42% .. +2.33%] · haut q95 +2.74% · bas q05 -3.4%
   - 2h (n=160) : retour [-2.18% .. +2.29%] · haut q95 +2.94% · bas q05 -3.78%
   - 4h (n=160) : retour [-2.28% .. +2.42%] · haut q95 +3.19% · bas q05 -3.79%
   - 6h (n=160) : retour [-2.51% .. +2.83%] · haut q95 +3.46% · bas q05 -3.83%
   - session (n=160) : retour [-3.44% .. +3.89%] · haut q95 +5.04% · bas q05 -4.28%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 59.3  _(momentum haussier)_
- **ADX** : 19.3  _(pas de tendance nette)_
- **MACD** : hist 0.965  _(pas de croisement recent)_
- **BB** : %B 0.72 · largeur 13.0%
- **ATR** : 7.53 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.077  _(accumulation)_
- **Vol ratio** : 0.35  _(volume atone)_
- **Choppiness** : 48.1  _(transition)_
- **MA** : MA20 240.16 · MA50 233.73 · MA200 232.69  _(prix > MA20)_
- **Dist MA** : MA20 +2.8% · MA50 +5.6% · MA200 +6.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (775867 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
