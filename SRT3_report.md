# SRT3

**Generated** : 2026-09-18T21:38:50.516991+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €247.30  

> 🟡 **WAIT-FOR-DIP** — spot +1.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €247.30 (+1.9% vs entrée) · entrée €242.66 · stop €235.38 · T1 €249.11 · R/R 0.89  
> ↳ P(T1 av. stop) 14 % _(réel 5 s)_ · EV/risk 0.062 _(réel 5 s)_ (GBM 0.047) · ¼-Kelly 0.037 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €242.14–€243.18 (mid €242.66)
- Spot actuel : €247.30 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : €235.38 (stop swing_plan-based (-7.19%))
- Targets : T1 €249.11 · R/R 0.89 | T2 €249.78 · R/R 0.98 | T3 €250.45 · R/R 1.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €235.38


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.19 %)** : le gap seul le franchit 0.471 % des séances (6 fois sur 1273).
   - exécution **1.839 pt plus bas** dans le cas TYPIQUE (médiane), 4.898 au p90, **7.015 au pire**
   - perte réelle **9.643 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 7.19 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0116 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.241 % | pire -14.205 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1271** [0.0838 ; 0.1828] _(largeur 9.9 pt, n_eff 173.1)_
   - swing : **0.4254** [0.3741 ; 0.478] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4169** [0.3658 ; 0.4694] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.09 %** | CVaR **-6.57 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.2 % si l'on extrapolait par √5 _(rapport 1.087 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0744** (β de hausse 1.1782, asymétrie 0.9119) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.301× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 219.2364 sur swing_based (2.98 ATR, 11.348 %) — p(stop avant cible) 0.112 [0.08 ; 0.15], R/R 0.194, perte reelle 14.205 % (gap inclus), CVaR 11.35 %, EV -0.3638 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.601 %) — p(stop avant cible) 0.4027 [0.35 ; 0.46], R/R 0.36, perte reelle 7.669 % (gap inclus), EV -1.4971 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.50 %) : P(cible) 58.2 % x 2.76 % + P(rien) 1.5 % x -1.01 % ne couvrent pas P(stop) 40.3 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.55 ATR (stop 10.011 %) — p(stop avant cible) 0.1509 [0.12 ; 0.19], R/R 0.194, perte reelle 14.205 % (gap inclus), EV -0.686 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 71.2 % x 2.76 % + P(rien) 13.7 % x -3.68 % ne couvrent pas P(stop) 15.1 % x 14.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.98 ATR (stop 11.348 %) — p(stop avant cible) 0.112 [0.08 ; 0.15], R/R 0.194, perte reelle 14.205 % (gap inclus), EV -0.3638 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 71.7 % x 2.76 % + P(rien) 17.2 % x -4.37 % ne couvrent pas P(stop) 11.2 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 7.65 ATR (stop 25.677 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.107, perte reelle 25.677 % (gap inclus), EV 0.1623 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.68 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.767 %) — p(stop avant cible) 0.7367 [0.69 ; 0.78], R/R 1.636, perte reelle 1.686 % (gap inclus), EV -0.5159 % — **REFUSE**
      - refuse : p_stop_first 0.737, borne haute 0.781 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 26.3 % x 2.76 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 73.7 % x 1.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.534 %) — p(stop avant cible) 0.6519 [0.60 ; 0.70], R/R 0.943, perte reelle 2.926 % (gap inclus), EV -0.9474 % — **REFUSE**
      - refuse : p_stop_first 0.652, borne haute 0.701 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 34.8 % x 2.76 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 65.2 % x 2.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.301 %) — p(stop avant cible) 0.5448 [0.49 ; 0.60], R/R 0.561, perte reelle 4.92 % (gap inclus), EV -1.425 % — **REFUSE**
      - refuse : p_stop_first 0.545, borne haute 0.597 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.42 %) : P(cible) 45.5 % x 2.76 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 54.5 % x 4.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.067 %) — p(stop avant cible) 0.4801 [0.43 ; 0.53], R/R 0.407, perte reelle 6.774 % (gap inclus), EV -1.8266 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 51.7 % x 2.76 % + P(rien) 0.2 % x -0.67 % ne couvrent pas P(stop) 48.0 % x 6.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.834 %) — p(stop avant cible) 0.4255 [0.37 ; 0.48], R/R 0.36, perte reelle 7.669 % (gap inclus), EV -1.7238 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.72 %) : P(cible) 56.2 % x 2.76 % + P(rien) 1.2 % x -1.00 % ne couvrent pas P(stop) 42.5 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.368 %) — p(stop avant cible) 0.3285 [0.28 ; 0.38], R/R 0.334, perte reelle 8.26 % (gap inclus), EV -0.9562 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 64.5 % x 2.76 % + P(rien) 2.6 % x -0.85 % ne couvrent pas P(stop) 32.9 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.135 %) — p(stop avant cible) 0.2929 [0.25 ; 0.34], R/R 0.297, perte reelle 9.276 % (gap inclus), EV -0.921 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 67.0 % x 2.76 % + P(rien) 3.8 % x -1.34 % ne couvrent pas P(stop) 29.3 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.902 %) — p(stop avant cible) 0.2652 [0.22 ; 0.31], R/R 0.297, perte reelle 9.276 % (gap inclus), EV -0.6268 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 69.1 % x 2.76 % + P(rien) 4.4 % x -1.62 % ne couvrent pas P(stop) 26.5 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.55 ATR (stop 8.729 %) — p(stop avant cible) 0.1771 [0.14 ; 0.22], R/R 0.245, perte reelle 11.278 % (gap inclus), EV -0.4681 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 70.7 % x 2.76 % + P(rien) 11.7 % x -3.60 % ne couvrent pas P(stop) 17.7 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 10.736 %) — p(stop avant cible) 0.1286 [0.10 ; 0.17], R/R 0.194, perte reelle 14.205 % (gap inclus), EV -0.5091 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 71.4 % x 2.76 % + P(rien) 15.8 % x -4.13 % ne couvrent pas P(stop) 12.9 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 12.27 %) — p(stop avant cible) 0.0832 [0.06 ; 0.12], R/R 0.194, perte reelle 14.205 % (gap inclus), EV -0.144 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 71.7 % x 2.76 % + P(rien) 20.0 % x -4.68 % ne couvrent pas P(stop) 8.3 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.803 %) — p(stop avant cible) 0.0592 [0.04 ; 0.09], R/R 0.194, perte reelle 14.205 % (gap inclus), EV 0.0055 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.80 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 15.337 %) — p(stop avant cible) 0.0368 [0.02 ; 0.06], R/R 0.18, perte reelle 15.337 % (gap inclus), EV 0.0347 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.34 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.871 %) — p(stop avant cible) 0.011 [0.00 ; 0.03], R/R 0.163, perte reelle 16.871 % (gap inclus), EV 0.1413 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.87 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.404 %) — p(stop avant cible) 0.0105 [0.00 ; 0.03], R/R 0.15, perte reelle 18.404 % (gap inclus), EV 0.1265 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.40 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.938 %) — p(stop avant cible) 0.0083 [0.00 ; 0.02], R/R 0.138, perte reelle 19.938 % (gap inclus), EV 0.1264 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.94 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.472 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.128, perte reelle 21.472 % (gap inclus), EV 0.1421 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.47 % > budget 12.00 %
   - 🟢 grid_snapped a 7.65 ATR (stop 24.395 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.113, perte reelle 24.395 % (gap inclus), EV 0.1653 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.40 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 247.3, ATR14 7.5857 (3.067 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.38 ATR = 1.166 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.153 % | 246.9207 | 89.24 % | 92.98 % | 94.36 % | 96.13 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.307 % | 246.5414 | 82.53 % | 88.44 % | 90.7 % | 93.46 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.46 % | 246.1621 | 74.93 % | 83.79 % | 86.94 % | 90.58 % | 93.63 % | 94.97 % |
| 0.2 ATR | 0.613 % | 245.7829 | 68.31 % | 78.85 % | 82.99 % | 87.41 % | 92.23 % | 94.37 % |
| 0.25 ATR | 0.767 % | 245.4036 | 63.08 % | 75.49 % | 79.72 % | 85.03 % | 90.44 % | 93.06 % |
| 0.35 ATR | 1.074 % | 244.645 | 53.01 % | 69.17 % | 73.99 % | 80.87 % | 87.05 % | 90.95 % |
| 0.5 ATR | 1.534 % | 243.5071 | 38.2 % | 56.62 % | 64.39 % | 74.03 % | 82.57 % | 88.23 % |
| 0.75 ATR | 2.301 % | 241.6107 | 19.15 % | 36.66 % | 47.77 % | 59.27 % | 72.21 % | 81.69 % |
| 1.0 ATR | 3.067 % | 239.7143 | 9.77 % | 24.41 % | 34.62 % | 47.77 % | 62.95 % | 74.65 % |
| 1.25 ATR | 3.834 % | 237.8179 | 4.74 % | 14.92 % | 24.63 % | 38.45 % | 53.39 % | 67.51 % |
| 1.5 ATR | 4.601 % | 235.9214 | 2.27 % | 9.88 % | 17.71 % | 30.92 % | 46.22 % | 61.67 % |
| 2.0 ATR | 6.135 % | 232.1286 | 0.69 % | 4.55 % | 8.21 % | 17.24 % | 34.76 % | 51.71 % |
| 2.5 ATR | 7.669 % | 228.3357 | 0.3 % | 1.98 % | 4.75 % | 10.7 % | 24.5 % | 41.65 % |
| 3.0 ATR | 9.202 % | 224.5429 | 0.2 % | 1.48 % | 2.97 % | 6.34 % | 17.53 % | 34.21 % |
| 4.0 ATR | 12.27 % | 216.9571 | 0.0 % | 0.69 % | 1.78 % | 3.57 % | 8.96 % | 20.22 % |
| 6.0 ATR | 18.404 % | 201.7857 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 0.99 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.82 ATR | 0.99 ATR | 1.12 ATR | 1.49 ATR | 1.96 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.80 ATR | 1.04 ATR | 1.24 ATR | 1.42 ATR | 1.91 ATR | 2.46 ATR |
| **5 s.** | 0.48 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.72 ATR | 1.90 ATR | 2.58 ATR | 3.48 ATR |
| **10 s.** | 0.68 ATR | 1.37 ATR | 1.55 ATR | 2.09 ATR | 2.48 ATR | 2.82 ATR | 3.88 ATR | 5.15 ATR |
| **20 s.** | 0.99 ATR | 2.08 ATR | 2.33 ATR | 3.09 ATR | 3.66 ATR | 4.03 ATR | 5.55 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.431–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.534 %, prix 243.5064), p(touche) 38.2 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.301 %, prix 241.6096), p(touche) 36.66 % (en stress 89.22 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.067 %, prix 239.7153), p(touche) 34.62 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.074–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.834 %, prix 237.8185), p(touche) 38.45 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.553–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.135 %, prix 232.1281), p(touche) 34.76 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.333–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.669 %, prix 228.3346), p(touche) 41.65 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.047 | EV/share : €0.342 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 26 % | T3 22 %
- Kelly (position) : f* 0.147 | ¼-Kelly 0.037 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.1 | bear 7.0 | side 80.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 495.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.876% → cible +2.656% / stop −3.0%, p_fill 33%, n_eff≈15.0) : P(cible|rempli) **14%** · **EV/risk +0.062** (×p_fill ; si rempli +0.56% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=7))
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
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 44.6  _(momentum baissier)_
- **ADX** : 13.6  _(pas de tendance nette)_
- **MACD** : hist -0.155  _(pas de croisement recent)_
- **BB** : %B 0.69 · largeur 11.6%
- **ATR** : 7.59 (27.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.015  _(neutre)_
- **Vol ratio** : 1.46  _(volume normal)_
- **Choppiness** : 48.8  _(transition)_
- **MA** : MA20 241.88 · MA50 236.27 · MA200 232.94  _(prix > MA20)_
- **Dist MA** : MA20 +2.2% · MA50 +4.7% · MA200 +6.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (843732 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
