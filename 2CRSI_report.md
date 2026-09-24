# AL2SI

**Generated** : 2026-09-24T00:16:01.917313+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €30.86  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €30.86 (+2.2% vs entrée) · entrée €30.19 · stop €29.61 · T1 €31.19 · R/R 1.72  
> ↳ P(T1 av. stop) 8 % _(réel 5 s)_ · EV/risk -0.26 _(réel 5 s)_ (GBM 0.131) · ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.9% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -3074 % hors [0,100] (R² max 0.92). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : %B 1.01 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €30.05–€30.33 (mid €30.19)
- Spot actuel : €30.86 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : €29.61 (stop swing_plan-based (-10.99%))
- Targets : T1 €31.19 · R/R 1.72 | T2 €31.74 · R/R 2.67 | T3 €32.29 · R/R 3.62
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €29.61


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.99 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **10.396 pt plus bas** dans le cas TYPIQUE (médiane), 21.651 au p90, **27.127 au pire**
   - perte réelle **22.515 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 10.99 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.054 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5743** [0.4999 ; 0.6462] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.3795** [0.3295 ; 0.4315] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3111** [0.264 ; 0.3613] _(largeur 9.7 pt, n_eff 345.8)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 24.6 observations effectives », dont la borne haute a 95 % vaut environ 12.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.5 pt), swing (40.6 pt), deep (35.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.3 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.29 % contre 7.18 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2034** (β de hausse 0.9592, asymétrie 1.2546) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.872× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 27.2387 sur support (1.4 ATR, 11.735 %) — p(stop avant cible) 0.2728 [0.23 ; 0.32], R/R 0.447, perte reelle 22.515 % (gap inclus), CVaR 11.786 %, EV -0.9879 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 46.9 % de la queue et il ne reste que -384.52 EUR a partager. Prix du risque -0.123 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.319 %) — p(stop avant cible) 0.3739 [0.32 ; 0.43], R/R 0.521, perte reelle 19.309 % (gap inclus), EV -2.2749 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.27 %) : P(cible) 48.6 % x 10.06 % + P(rien) 14.0 % x 0.37 % ne couvrent pas P(stop) 37.4 % x 19.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.4 ATR (stop 11.735 %) — p(stop avant cible) 0.2728 [0.23 ; 0.32], R/R 0.447, perte reelle 22.515 % (gap inclus), EV -0.9879 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.99 %) : P(cible) 52.7 % x 10.06 % + P(rien) 20.0 % x -0.75 % ne couvrent pas P(stop) 27.3 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.54 ATR (stop 18.81 %) — p(stop avant cible) 0.1724 [0.14 ; 0.21], R/R 0.335, perte reelle 30.031 % (gap inclus), EV -0.4377 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 54.5 % x 10.06 % + P(rien) 28.3 % x -2.61 % ne couvrent pas P(stop) 17.2 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.06 ATR (stop 22.039 %) — p(stop avant cible) 0.1297 [0.10 ; 0.17], R/R 0.335, perte reelle 30.031 % (gap inclus), EV 0.4316 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.06 % > budget 12.00 %
   - 🟢 support a 4.31 ATR (stop 29.816 %) — p(stop avant cible) 0.0799 [0.05 ; 0.11], R/R 0.264, perte reelle 38.117 % (gap inclus), EV 0.4896 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.82 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.553 %) — p(stop avant cible) 0.8323 [0.79 ; 0.87], R/R 2.496, perte reelle 4.03 % (gap inclus), EV -1.6832 % — **REFUSE**
      - refuse : p_stop_first 0.832, borne haute 0.869 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.68 %) : P(cible) 16.6 % x 10.06 % + P(rien) 0.2 % x 2.81 % ne couvrent pas P(stop) 83.2 % x 4.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.106 %) — p(stop avant cible) 0.7159 [0.67 ; 0.76], R/R 1.353, perte reelle 7.433 % (gap inclus), EV -2.5292 % — **REFUSE**
      - refuse : p_stop_first 0.716, borne haute 0.761 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.53 %) : P(cible) 27.4 % x 10.06 % + P(rien) 1.0 % x 3.39 % ne couvrent pas P(stop) 71.6 % x 7.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.659 %) — p(stop avant cible) 0.6221 [0.57 ; 0.67], R/R 0.855, perte reelle 11.766 % (gap inclus), EV -3.704 % — **REFUSE**
      - refuse : p_stop_first 0.622, borne haute 0.672 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.70 %) : P(cible) 34.8 % x 10.06 % + P(rien) 3.0 % x 3.85 % ne couvrent pas P(stop) 62.2 % x 11.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.212 %) — p(stop avant cible) 0.5445 [0.49 ; 0.60], R/R 0.724, perte reelle 13.9 % (gap inclus), EV -3.3749 % — **REFUSE**
      - refuse : p_stop_first 0.544, borne haute 0.596 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.37 %) : P(cible) 40.6 % x 10.06 % + P(rien) 5.0 % x 2.26 % ne couvrent pas P(stop) 54.4 % x 13.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.4 ATR (stop 10.548 %) — p(stop avant cible) 0.3108 [0.26 ; 0.36], R/R 0.447, perte reelle 22.515 % (gap inclus), EV -1.808 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.81 %) : P(cible) 52.0 % x 10.06 % + P(rien) 16.9 % x -0.26 % ne couvrent pas P(stop) 31.1 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 13.978 %) — p(stop avant cible) 0.2334 [0.19 ; 0.28], R/R 0.408, perte reelle 24.668 % (gap inclus), EV -0.5362 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 54.3 % x 10.06 % + P(rien) 22.3 % x -1.09 % ne couvrent pas P(stop) 23.3 % x 24.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.54 ATR (stop 17.623 %) — p(stop avant cible) 0.1861 [0.15 ; 0.23], R/R 0.372, perte reelle 27.014 % (gap inclus), EV -0.1369 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 54.5 % x 10.06 % + P(rien) 26.9 % x -2.18 % ne couvrent pas P(stop) 18.6 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.06 ATR (stop 20.853 %) — p(stop avant cible) 0.1364 [0.10 ; 0.18], R/R 0.335, perte reelle 30.031 % (gap inclus), EV 0.3192 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.87 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 24.85 %) — p(stop avant cible) 0.0963 [0.07 ; 0.13], R/R 0.308, perte reelle 32.641 % (gap inclus), EV 0.7137 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.86 % > budget 12.00 %
   - 🟢 grid_snapped a 4.31 ATR (stop 28.63 %) — p(stop avant cible) 0.0804 [0.06 ; 0.11], R/R 0.264, perte reelle 38.117 % (gap inclus), EV 0.4797 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.64 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 31.062 %) — p(stop avant cible) 0.0792 [0.05 ; 0.11], R/R 0.264, perte reelle 38.117 % (gap inclus), EV 0.5031 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.07 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 34.168 %) — p(stop avant cible) 0.0609 [0.04 ; 0.09], R/R 0.264, perte reelle 38.117 % (gap inclus), EV 0.7774 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.17 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 37.274 %) — p(stop avant cible) 0.0496 [0.03 ; 0.08], R/R 0.264, perte reelle 38.117 % (gap inclus), EV 1.1387 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.27 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 40.381 %) — p(stop avant cible) 0.0363 [0.02 ; 0.06], R/R 0.249, perte reelle 40.381 % (gap inclus), EV 1.3464 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.38 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 43.487 %) — p(stop avant cible) 0.0319 [0.02 ; 0.05], R/R 0.231, perte reelle 43.487 % (gap inclus), EV 1.2766 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.49 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 46.593 %) — p(stop avant cible) 0.0319 [0.02 ; 0.05], R/R 0.216, perte reelle 46.593 % (gap inclus), EV 1.1775 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.59 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 49.699 %) — p(stop avant cible) 0.0319 [0.02 ; 0.05], R/R 0.202, perte reelle 49.699 % (gap inclus), EV 1.0785 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.70 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 30.86, ATR14 1.9171 (6.212 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 2.485 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.311 % | 30.7641 | 86.67 % | 90.38 % | 92.83 % | 94.09 % | 95.25 % | 96.8 % |
| 0.1 ATR | 0.621 % | 30.6683 | 82.16 % | 86.85 % | 90.08 % | 91.93 % | 93.77 % | 95.9 % |
| 0.15 ATR | 0.932 % | 30.5724 | 78.14 % | 83.12 % | 86.94 % | 88.78 % | 91.79 % | 94.71 % |
| 0.2 ATR | 1.242 % | 30.4766 | 72.35 % | 79.0 % | 83.1 % | 85.63 % | 89.42 % | 92.51 % |
| 0.25 ATR | 1.553 % | 30.3807 | 66.37 % | 74.39 % | 78.98 % | 82.28 % | 87.14 % | 90.91 % |
| 0.35 ATR | 2.174 % | 30.189 | 54.61 % | 65.46 % | 70.83 % | 75.49 % | 82.2 % | 87.51 % |
| 0.5 ATR | 3.106 % | 29.9014 | 40.69 % | 53.78 % | 61.69 % | 68.5 % | 77.65 % | 85.01 % |
| 0.75 ATR | 4.659 % | 29.4221 | 22.65 % | 37.39 % | 47.25 % | 55.51 % | 66.77 % | 76.22 % |
| 1.0 ATR | 6.212 % | 28.9429 | 12.94 % | 24.93 % | 33.69 % | 44.19 % | 56.97 % | 67.83 % |
| 1.25 ATR | 7.765 % | 28.4636 | 7.65 % | 17.66 % | 24.66 % | 36.12 % | 49.85 % | 61.34 % |
| 1.5 ATR | 9.319 % | 27.9843 | 3.82 % | 11.48 % | 17.39 % | 28.54 % | 42.73 % | 54.85 % |
| 2.0 ATR | 12.425 % | 27.0257 | 0.88 % | 5.3 % | 9.72 % | 16.83 % | 31.06 % | 43.16 % |
| 2.5 ATR | 15.531 % | 26.0671 | 0.1 % | 2.26 % | 4.72 % | 9.94 % | 21.07 % | 33.27 % |
| 3.0 ATR | 18.637 % | 25.1086 | 0.1 % | 0.98 % | 2.46 % | 6.69 % | 15.03 % | 25.97 % |
| 4.0 ATR | 24.85 % | 23.1914 | 0.0 % | 0.59 % | 1.28 % | 2.85 % | 8.61 % | 17.28 % |
| 6.0 ATR | 37.274 % | 19.3571 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.14 ATR | 1.42 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.63 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.62 ATR | 2.05 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.24 ATR | 1.41 ATR | 1.98 ATR | 2.47 ATR |
| **5 s.** | 0.36 ATR | 0.87 ATR | 0.98 ATR | 1.35 ATR | 1.65 ATR | 1.86 ATR | 2.50 ATR | 3.44 ATR |
| **10 s.** | 0.56 ATR | 1.25 ATR | 1.42 ATR | 1.92 ATR | 2.30 ATR | 2.59 ATR | 3.78 ATR | 5.12 ATR |
| **20 s.** | 0.79 ATR | 1.71 ATR | 1.92 ATR | 2.52 ATR | 3.11 ATR | 3.69 ATR | 5.57 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.454–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.106 %, prix 29.9015), p(touche) 40.69 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (90.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.634–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.659 %, prix 29.4222), p(touche) 37.39 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.791–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.212 %, prix 28.943), p(touche) 33.69 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.982–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.212 %, prix 28.943), p(touche) 44.19 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.42–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.319 %, prix 27.9842), p(touche) 42.73 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.921–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.425 %, prix 27.0256), p(touche) 43.16 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.131 | EV/share : €0.075 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 29 % | T3 29 %
- Kelly (position) : f* 0.07 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.8 | bear 11.2 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 494.0 (= 16 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.166% → cible +3.306% / stop −1.905%, p_fill 56%, n_eff≈26.4) : P(cible|rempli) **8%** · **EV/risk -0.260** (×p_fill ; si rempli -0.89% du capital)
  - **swing** (entrée dip −4.778% → cible +5.193% / stop −6.524%, p_fill 37%, n_eff≈20.6) : P(cible|rempli) **54%** · **EV/risk -0.010** (×p_fill ; si rempli -0.17% du capital)
  - **deep** (entrée dip −7.381% → cible +7.344% / stop −10.061%, p_fill 46%, n_eff≈24.6) : P(cible|rempli) **69%** · **EV/risk +0.018** (×p_fill ; si rempli +0.39% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 62.4  _(momentum haussier)_
- **ADX** : 19.8  _(pas de tendance nette)_
- **MACD** : hist 0.24  _(pas de croisement recent)_
- **BB** : %B 1.01 · largeur 18.1%
- **ATR** : 1.92 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.014  _(neutre)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 62.5  _(marche en range (choppy))_
- **MA** : MA20 28.26 · MA50 27.31 · MA200 27.64  _(prix > MA20)_
- **Dist MA** : MA20 +9.2% · MA50 +13.0% · MA200 +11.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (853144 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
