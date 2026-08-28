# SRT3

**Generated** : 2026-08-28T21:37:24.088138+00:00  
**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €253.50  

> 🟡 **WAIT-FOR-DIP** — spot +2.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €253.50 (+2.8% vs entrée) · entrée €246.60 · stop €242.90 · T1 €249.24 · R/R 0.71  
> ↳ P(T1 av. stop) 64 % · EV/risk 0.241 · ¼-Kelly 0.038 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 0.97 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €246.08–€247.13 (mid €246.60)
- Spot actuel : €253.50 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : €242.90 (stop swing_plan-based (-8.8%))
- Targets : T1 €249.24 · R/R 0.71 | T2 €251.88 · R/R 1.43 | T3 €254.52 · R/R 2.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €242.90


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.8 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **1.172 pt plus bas** dans le cas TYPIQUE (médiane), 4.559 au p90, **5.405 au pire**
   - perte réelle **11.278 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 8.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0058 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3739** [0.3044 ; 0.4476] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.4301** [0.3787 ; 0.4827] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4426** [0.3909 ; 0.4952] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (52.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.12 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0673** (β de hausse 1.1747, asymétrie 0.9086) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.319× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 228.5 sur atr_grid (3.5 ATR, 9.862 %) — p(stop avant cible) 0.058 [0.04 ; 0.09], R/R 0.063, perte reelle 12.088 % (gap inclus), CVaR 9.865 %, EV -0.1265 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.227 %) — p(stop avant cible) 0.1594 [0.12 ; 0.20], R/R 0.1, perte reelle 7.669 % (gap inclus), EV -0.5785 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 84.1 % x 0.77 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 15.9 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.99 ATR (stop 7.399 %) — p(stop avant cible) 0.0989 [0.07 ; 0.13], R/R 0.076, perte reelle 10.096 % (gap inclus), EV -0.3255 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 89.6 % x 0.77 % + P(rien) 0.5 % x -2.68 % ne couvrent pas P(stop) 9.9 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.96 ATR (stop 12.95 %) — p(stop avant cible) 0.0374 [0.02 ; 0.06], R/R 0.054, perte reelle 14.205 % (gap inclus), EV -0.0642 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 92.4 % x 0.77 % + P(rien) 3.9 % x -6.17 % ne couvrent pas P(stop) 3.7 % x 14.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 9.36 ATR (stop 28.155 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.027, perte reelle 28.155 % (gap inclus), EV 0.0291 % — **REFUSE**
      - refuse : R/R 0.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.16 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.704 %) — p(stop avant cible) 0.5029 [0.45 ; 0.56], R/R 0.477, perte reelle 1.606 % (gap inclus), EV -0.4269 % — **REFUSE**
      - refuse : p_stop_first 0.503, borne haute 0.555 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 49.7 % x 0.77 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 50.3 % x 1.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.409 %) — p(stop avant cible) 0.3943 [0.34 ; 0.45], R/R 0.285, perte reelle 2.686 % (gap inclus), EV -0.5951 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 60.6 % x 0.77 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 39.4 % x 2.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.113 %) — p(stop avant cible) 0.3101 [0.26 ; 0.36], R/R 0.173, perte reelle 4.426 % (gap inclus), EV -0.844 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.84 %) : P(cible) 69.0 % x 0.77 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 31.0 % x 4.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.818 %) — p(stop avant cible) 0.2322 [0.19 ; 0.28], R/R 0.117, perte reelle 6.529 % (gap inclus), EV -0.9279 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 76.8 % x 0.77 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 23.2 % x 6.53 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.522 %) — p(stop avant cible) 0.1904 [0.15 ; 0.23], R/R 0.1, perte reelle 7.669 % (gap inclus), EV -0.84 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.84 %) : P(cible) 81.0 % x 0.77 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 19.0 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.99 ATR (stop 6.458 %) — p(stop avant cible) 0.1112 [0.08 ; 0.15], R/R 0.083, perte reelle 9.276 % (gap inclus), EV -0.3572 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 88.7 % x 0.77 % + P(rien) 0.2 % x -2.67 % ne couvrent pas P(stop) 11.1 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.044 %) — p(stop avant cible) 0.1061 [0.08 ; 0.14], R/R 0.083, perte reelle 9.276 % (gap inclus), EV -0.3085 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 89.1 % x 0.77 % + P(rien) 0.3 % x -2.75 % ne couvrent pas P(stop) 10.6 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 8.453 %) — p(stop avant cible) 0.0767 [0.05 ; 0.11], R/R 0.068, perte reelle 11.278 % (gap inclus), EV -0.25 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 90.5 % x 0.77 % + P(rien) 1.9 % x -4.20 % ne couvrent pas P(stop) 7.7 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 9.862 %) — p(stop avant cible) 0.058 [0.04 ; 0.09], R/R 0.063, perte reelle 12.088 % (gap inclus), EV -0.1265 % — **REFUSE**
      - refuse : R/R 0.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 91.5 % x 0.77 % + P(rien) 2.7 % x -4.74 % ne couvrent pas P(stop) 5.8 % x 12.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.96 ATR (stop 12.009 %) — p(stop avant cible) 0.0452 [0.03 ; 0.07], R/R 0.054, perte reelle 14.205 % (gap inclus), EV -0.0958 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 92.4 % x 0.77 % + P(rien) 3.1 % x -5.17 % ne couvrent pas P(stop) 4.5 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 14.088 %) — p(stop avant cible) 0.0255 [0.01 ; 0.05], R/R 0.054, perte reelle 14.205 % (gap inclus), EV -0.0055 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 92.4 % x 0.77 % + P(rien) 5.1 % x -6.91 % ne couvrent pas P(stop) 2.5 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 15.497 %) — p(stop avant cible) 0.015 [0.01 ; 0.03], R/R 0.049, perte reelle 15.497 % (gap inclus), EV -0.0034 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 92.4 % x 0.77 % + P(rien) 6.1 % x -7.81 % ne couvrent pas P(stop) 1.5 % x 15.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 16.906 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 0.045, perte reelle 16.906 % (gap inclus), EV 0.0424 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.91 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 18.315 %) — p(stop avant cible) 0.0042 [0.00 ; 0.02], R/R 0.042, perte reelle 18.315 % (gap inclus), EV 0.0375 % — **REFUSE**
      - refuse : R/R 0.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.32 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 19.724 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.039, perte reelle 19.724 % (gap inclus), EV 0.0333 % — **REFUSE**
      - refuse : R/R 0.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.72 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 21.133 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.036, perte reelle 21.133 % (gap inclus), EV 0.0267 % — **REFUSE**
      - refuse : R/R 0.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.13 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 22.542 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.034, perte reelle 22.542 % (gap inclus), EV 0.0309 % — **REFUSE**
      - refuse : R/R 0.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.54 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 253.5, ATR14 7.1429 (2.818 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.381 ATR = 1.074 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.141 % | 253.1429 | 88.95 % | 92.99 % | 94.37 % | 96.04 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.282 % | 252.7857 | 82.45 % | 88.45 % | 90.71 % | 93.37 % | 95.72 % | 97.09 % |
| 0.15 ATR | 0.423 % | 252.4286 | 74.85 % | 83.91 % | 86.96 % | 90.5 % | 93.63 % | 95.08 % |
| 0.2 ATR | 0.564 % | 252.0714 | 68.34 % | 78.97 % | 83.0 % | 87.33 % | 92.24 % | 94.47 % |
| 0.25 ATR | 0.704 % | 251.7143 | 63.21 % | 75.62 % | 79.74 % | 84.95 % | 90.55 % | 93.17 % |
| 0.35 ATR | 0.986 % | 251.0 | 53.06 % | 69.1 % | 74.11 % | 80.89 % | 87.06 % | 91.26 % |
| 0.5 ATR | 1.409 % | 249.9286 | 38.07 % | 56.56 % | 64.43 % | 74.16 % | 82.69 % | 88.74 % |
| 0.75 ATR | 2.113 % | 248.1429 | 19.63 % | 36.82 % | 47.92 % | 59.31 % | 72.34 % | 82.41 % |
| 1.0 ATR | 2.818 % | 246.3571 | 10.26 % | 24.68 % | 34.68 % | 47.72 % | 63.08 % | 75.38 % |
| 1.25 ATR | 3.522 % | 244.5714 | 4.83 % | 15.0 % | 24.7 % | 38.32 % | 53.73 % | 68.44 % |
| 1.5 ATR | 4.227 % | 242.7857 | 2.37 % | 10.07 % | 18.08 % | 31.09 % | 46.47 % | 62.81 % |
| 2.0 ATR | 5.635 % | 239.2143 | 0.79 % | 4.74 % | 8.5 % | 17.62 % | 35.32 % | 52.96 % |
| 2.5 ATR | 7.044 % | 235.6429 | 0.3 % | 2.17 % | 5.04 % | 11.09 % | 25.17 % | 42.91 % |
| 3.0 ATR | 8.453 % | 232.0714 | 0.2 % | 1.68 % | 3.16 % | 6.83 % | 18.21 % | 35.38 % |
| 4.0 ATR | 11.271 % | 224.9286 | 0.0 % | 0.69 % | 1.88 % | 3.96 % | 9.55 % | 21.31 % |
| 6.0 ATR | 16.906 % | 210.6429 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.19 % | 7.34 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.51 ATR | 1.98 ATR |
| **3 s.** | 0.33 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.24 ATR | 1.43 ATR | 1.92 ATR | 2.51 ATR |
| **5 s.** | 0.48 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.73 ATR | 1.91 ATR | 2.63 ATR | 3.64 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.57 ATR | 2.11 ATR | 2.51 ATR | 2.87 ATR | 3.95 ATR | 5.24 ATR |
| **20 s.** | 1.01 ATR | 2.15 ATR | 2.40 ATR | 3.17 ATR | 3.74 ATR | 4.19 ATR | 5.62 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.431–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.409 %, prix 249.9282), p(touche) 38.07 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.113 %, prix 248.1435), p(touche) 36.82 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.818 %, prix 246.3564), p(touche) 34.68 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.072–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.522 %, prix 244.5717), p(touche) 38.32 % (en stress 92.08 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.566–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.635 %, prix 239.2153), p(touche) 35.32 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.396–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.044 %, prix 235.6435), p(touche) 42.91 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.054 | EV/share : €0.201 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 66 % | T2 37 % | T3 18 %
- Kelly (position) : f* 0.153 | ¼-Kelly 0.038 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.3 | bear 7.2 | side 80.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 507.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.721% → cible +1.071% / stop −1.5%, p_fill 14%, n_eff≈11.1) : P(cible|rempli) **46%** · **EV/risk -0.012** (×p_fill ; si rempli -0.13% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→45% · +3.0%→24% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.23% (p90 6.3%) · excursion haute méd. +1.79% / basse méd. −1.33%
- Profil de vol intra : ouverture 1.999% vs midi 0.826% vs clôture 0.975% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.098 ; mean-reverting — autocorr -0.03)_ ; drift intra méd. 0.303% ; recovery-V 26%
- **σ réalisé intraday** 2.396% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 62% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 249.5637 (VA 248.0238–250.3337 ; dernier close 249.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 33% · rebond 66% · **stop −2.49%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 51% (gap-down >1% 8% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.44% (p90 −1.69%) · haut méd +0.54% · range méd 1.2%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −1.87%) · haut méd +0.64% · range méd 1.46%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −1.99%) · haut méd +0.82% · range méd 1.68%
- Excursion ouverture 60min (n=160) : bas méd −0.75% (p90 −2.27%) · haut méd +0.82% · range méd 1.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 250.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 77% (121/159) · gap 25% · délai 0.4min · rebond 51% (66/121) (MFE +1.05%)
   - −1.0% : fill 30min 42% · séance 65% (105/159) · gap 8% · délai 4.4min · rebond 62% (62/105) (MFE +1.33%)
   - −1.5% : fill 30min 26% · séance 47% (85/159) · gap 4% · délai 14.3min · rebond 59% (49/85) (MFE +1.43%)
   - −2.0% : fill 30min 10% · séance 33% (65/159) · gap 1% · délai 105.3min · rebond 66% (38/65) (MFE +1.39%)
   - −3.0% : fill 30min 4% · séance 14% (34/159) · gap 1% · délai 106.5min · rebond 68% (21/34) (MFE +1.93%)
   - −4.0% : fill 30min 3% · séance 8% (18/159) · gap 0% · délai 55.3min · rebond 68% (13/18) (MFE +2.14%)
   - −5.0% : fill 30min 0% · séance 6% (10/159) · gap 0% · délai 122.6min · rebond 86% (9/10) (MFE +2.89%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.97%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −2.15%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −2.51%) → stop au-delà de −1.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=448 jambes) : jambe baissière méd −1.02% (p90 −2.28%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 80% (49/58) · rebond 70% (32/49)
      · −2.0% : fill 35% (29/58) · rebond 70% (18/29)
      · −3.0% : fill 18% (19/58) · rebond 63% (12/19)
      · −4.0% : fill 13% (12/58) · rebond 68% (10/12)
      · −5.0% : fill 6% (6/58) · rebond 100% (6/6)
   - **flat** (38 séances) :
      · −1.0% : fill 69% (25/38) · rebond 53% (12/25)
      · −2.0% : fill 41% (17/38) · rebond 55% (9/17)
      · −3.0% : fill 10% (6/38) · rebond 38% (2/6)
      · −4.0% : fill 4% (2/38) · rebond 0% (0/2)
      · −5.0% : fill 3% (1/38) · rebond 0% (0/1)
   - **gap-up** (63 séances) :
      · −1.0% : fill 47% (31/63) · rebond 58% (18/31)
      · −2.0% : fill 26% (19/63) · rebond 72% (11/19)
      · −3.0% : fill 14% (9/63) · rebond 90% (7/9)
      · −4.0% : fill 8% (4/63) · rebond 90% (3/4)
      · −5.0% : fill 7% (3/63) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 57% si les 15 1res min sont vertes (85 cas) · 42% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 63% si début vert vs 35% si rouge (base 50% · écart 28 pts) ; prédictivité sature ensuite (plafond brut 254min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **63%** · continue >prix actuel 44% ; creux résiduel méd -1.45% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.0% / q75 +1.83% → **scale +1.0% / runner +1.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **35%** (continue à baisser 44%) → **RÉDUIRE ~65%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +1.42% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.7% .. +2.1%] · haut q95 +2.63% · bas q05 -3.08%
   - 60min (n=160) : retour [-2.49% .. +2.34%] · haut q95 +2.77% · bas q05 -3.54%
   - 2h (n=160) : retour [-2.18% .. +2.38%] · haut q95 +2.94% · bas q05 -3.81%
   - 4h (n=160) : retour [-2.35% .. +2.45%] · haut q95 +3.23% · bas q05 -3.82%
   - 6h (n=160) : retour [-2.54% .. +2.86%] · haut q95 +3.51% · bas q05 -3.84%
   - session (n=160) : retour [-3.51% .. +3.98%] · haut q95 +5.34% · bas q05 -4.42%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_up
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

- **RSI** : 63.6  _(momentum haussier)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist 1.673  _(pas de croisement recent)_
- **BB** : %B 0.97 · largeur 14.0%
- **ATR** : 7.14 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.102  _(accumulation)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 47.7  _(transition)_
- **MA** : MA20 238.0 · MA50 232.32 · MA200 232.51  _(prix > MA20)_
- **Dist MA** : MA20 +6.5% · MA50 +9.1% · MA200 +9.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (916030 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
