# RHM

**Generated** : 2026-08-24T21:35:48.156594+00:00  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €1125.20  

> 🟡 **WAIT-FOR-DIP** — spot +4.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €1125.20 (+4.5% vs entrée) · entrée €1077.03 · stop €1055.48 · T1 €1091.08 · R/R 0.65  
> ↳ P(T1 av. stop) 64 % · EV/risk 0.323 · ¼-Kelly 0.031 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1074.21–€1079.84 (mid €1077.03)
- Spot actuel : €1125.20 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : €1055.48 (stop swing_plan-based (-13.71%))
- Targets : T1 €1091.08 · R/R 0.65 | T2 €1105.14 · R/R 1.3 | T3 €1119.20 · R/R 1.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1055.48


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (13.71 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **8.719 pt plus bas** dans le cas TYPIQUE (médiane), 8.719 au p90, **8.719 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 13.71 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0068 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0854** [0.0506 ; 0.1339] _(largeur 8.3 pt, n_eff 173.1)_
   - swing : **0.4052** [0.3544 ; 0.4576] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.5107** [0.4581 ; 0.5631] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (53.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.86 %** | CVaR **-6.85 %** | vol 3.06 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 2.06 % contre 3.37 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.6 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.846 ; < 1 = le √5 surestime)_
- **β de baisse : 0.496** (β de hausse 0.5891, asymétrie 0.842) vs GDAXI — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.164× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 1004.4499 sur atr_grid (2.5 ATR, 10.731 %) — p(stop avant cible) 0.2585 [0.21 ; 0.31], R/R 1.609, perte reelle 22.429 % (gap inclus), CVaR 10.74 %, EV -3.1774 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.3 ATR (stop 3.336 %) — p(stop avant cible) 0.7078 [0.66 ; 0.75], R/R 6.682, perte reelle 5.402 % (gap inclus), EV -1.2493 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.708, borne haute 0.754 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.1 % x 36.09 % + P(rien) 29.1 % x 8.74 % ne couvrent pas P(stop) 70.8 % x 5.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 6.439 %) — p(stop avant cible) 0.4785 [0.43 ; 0.53], R/R 2.384, perte reelle 15.141 % (gap inclus), EV -4.1054 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.11 %) : P(cible) 0.2 % x 36.09 % + P(rien) 52.0 % x 5.93 % ne couvrent pas P(stop) 47.9 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.07 ATR (stop 19.524 %) — p(stop avant cible) 0.0617 [0.04 ; 0.09], R/R 1.609, perte reelle 22.429 % (gap inclus), EV -0.5461 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 0.2 % x 36.09 % + P(rien) 93.7 % x 0.83 % ne couvrent pas P(stop) 6.2 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 4.293 %) — p(stop avant cible) 0.6271 [0.58 ; 0.68], R/R 4.867, perte reelle 7.416 % (gap inclus), EV -1.6703 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.627, borne haute 0.677 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.67 %) : P(cible) 0.1 % x 36.09 % + P(rien) 37.2 % x 7.94 % ne couvrent pas P(stop) 62.7 % x 7.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.585 %) — p(stop avant cible) 0.3733 [0.32 ; 0.43], R/R 1.609, perte reelle 22.429 % (gap inclus), EV -5.3098 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.31 %) : P(cible) 0.2 % x 36.09 % + P(rien) 62.5 % x 4.81 % ne couvrent pas P(stop) 37.3 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.731 %) — p(stop avant cible) 0.2585 [0.21 ; 0.31], R/R 1.609, perte reelle 22.429 % (gap inclus), EV -3.1774 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.18 %) : P(cible) 0.2 % x 36.09 % + P(rien) 74.0 % x 3.46 % ne couvrent pas P(stop) 25.9 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 12.878 %) — p(stop avant cible) 0.1888 [0.15 ; 0.23], R/R 1.609, perte reelle 22.429 % (gap inclus), EV -2.0893 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.09 %) : P(cible) 0.2 % x 36.09 % + P(rien) 81.0 % x 2.58 % ne couvrent pas P(stop) 18.9 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 15.024 %) — p(stop avant cible) 0.1365 [0.10 ; 0.18], R/R 1.609, perte reelle 22.429 % (gap inclus), EV -1.2981 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 0.2 % x 36.09 % + P(rien) 86.2 % x 1.98 % ne couvrent pas P(stop) 13.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 21.463 %) — p(stop avant cible) 0.038 [0.02 ; 0.06], R/R 1.609, perte reelle 22.429 % (gap inclus), EV -0.3313 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 21.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.2 % x 36.09 % + P(rien) 96.0 % x 0.48 % ne couvrent pas P(stop) 3.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 23.609 %) — p(stop avant cible) 0.0117 [0.00 ; 0.03], R/R 1.529, perte reelle 23.609 % (gap inclus), EV -0.1215 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.2 % x 36.09 % + P(rien) 98.7 % x 0.10 % ne couvrent pas P(stop) 1.2 % x 23.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 25.755 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 1.401, perte reelle 25.755 % (gap inclus), EV -0.1343 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.2 % x 36.09 % + P(rien) 99.1 % x -0.01 % ne couvrent pas P(stop) 0.7 % x 25.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 27.902 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 1.294, perte reelle 27.902 % (gap inclus), EV -0.0861 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.2 % x 36.09 % + P(rien) 99.3 % x 0.01 % ne couvrent pas P(stop) 0.5 % x 27.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 30.048 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 1.201, perte reelle 30.048 % (gap inclus), EV -0.0271 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.2 % x 36.09 % + P(rien) 99.5 % x 0.01 % ne couvrent pas P(stop) 0.3 % x 30.05 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 32.194 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.121, perte reelle 32.194 % (gap inclus), EV 0.0844 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.19 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 34.341 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.051, perte reelle 34.341 % (gap inclus), EV 0.0844 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.34 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.086 | EV/share : €1.854 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 60 % | T2 36 % | T3 19 %
- Kelly (position) : f* 0.123 | ¼-Kelly 0.031 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 44.4 | bear 47.9 | side 7.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.286% → cible +1.305% / stop −2.0%, p_fill 9%, n_eff≈8.4) : P(cible|rempli) **73%** · **EV/risk +0.017** (×p_fill ; si rempli +0.36% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→70% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.17% (p90 6.98%) · excursion haute méd. +2.05% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.674% vs midi 0.943% vs clôture 1.127% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.09 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. -0.194% ; recovery-V 23%
- **σ réalisé intraday** 2.742% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 60% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 1151.1575 (VA 1148.5825–1154.2475 ; dernier close 1152.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 17% · rebond 64% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 31% (gap-down >1% 10% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.74%) · haut méd +0.57% · range méd 1.39%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −2.0%) · haut méd +0.67% · range méd 1.8%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.19%) · haut méd +0.88% · range méd 2.07%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −2.62%) · haut méd +1.0% · range méd 2.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1152.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 71% (117/159) · gap 21% · délai 0.4min · rebond 53% (61/117) (MFE +1.1%)
   - −1.0% : fill 30min 40% · séance 65% (108/159) · gap 10% · délai 5.9min · rebond 59% (61/108) (MFE +1.27%)
   - −1.5% : fill 30min 28% · séance 54% (88/159) · gap 6% · délai 24.4min · rebond 62% (50/88) (MFE +1.36%)
   - −2.0% : fill 30min 18% · séance 40% (74/159) · gap 5% · délai 33.7min · rebond 66% (46/74) (MFE +1.58%)
   - −3.0% : fill 30min 8% · séance 24% (46/159) · gap 3% · délai 120.4min · rebond 58% (27/46) (MFE +1.31%)
   - −4.0% : fill 30min 3% · séance 17% (28/159) · gap 1% · délai 245.4min · rebond 64% (16/28) (MFE +1.5%)
   - −5.0% : fill 30min 1% · séance 9% (16/159) · gap 1% · délai 293.4min · rebond 56% (8/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.61%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.44% (p90 −1.76%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.77%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=533 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 94% (46/48) · rebond 65% (27/46)
      · −2.0% : fill 80% (38/48) · rebond 66% (25/38)
      · −3.0% : fill 53% (26/48) · rebond 63% (16/26)
      · −4.0% : fill 41% (16/48) · rebond 75% (11/16)
      · −5.0% : fill 22% (9/48) · rebond 83% (7/9)
   - **flat** (47 séances) :
      · −1.0% : fill 67% (34/47) · rebond 64% (21/34)
      · −2.0% : fill 24% (17/47) · rebond 72% (10/17)
      · −3.0% : fill 16% (10/47) · rebond 55% (5/10)
      · −4.0% : fill 14% (8/47) · rebond 36% (2/8)
      · −5.0% : fill 9% (6/47) · rebond 22% (1/6)
   - **gap-up** (64 séances) :
      · −1.0% : fill 48% (28/64) · rebond 48% (13/28)
      · −2.0% : fill 30% (19/64) · rebond 63% (11/19)
      · −3.0% : fill 14% (10/64) · rebond 49% (6/10)
      · −4.0% : fill 6% (4/64) · rebond 61% (3/4)
      · −5.0% : fill 2% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 62% si les 15 1res min sont vertes (77 cas) · 33% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:37** → P(séance verte=clôture>ouverture) 73% si début vert vs 19% si rouge (base 47% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 44% ; creux résiduel méd -1.21% (q20 -2.72%) → **SL/trailing à −2.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.76% / q75 +1.81% → **scale +0.76% / runner +1.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **19%** (continue à baisser 59%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.7%** (au-delà de la MAE q10 -3.7%), cible rebond +0.95% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +3.27%] · haut q95 +3.75% · bas q05 -3.11%
   - 60min (n=160) : retour [-2.78% .. +3.22%] · haut q95 +4.4% · bas q05 -3.85%
   - 2h (n=160) : retour [-3.2% .. +3.04%] · haut q95 +4.4% · bas q05 -4.48%
   - 4h (n=160) : retour [-3.4% .. +3.3%] · haut q95 +4.87% · bas q05 -4.63%
   - 6h (n=160) : retour [-4.15% .. +3.3%] · haut q95 +4.95% · bas q05 -5.04%
   - session (n=160) : retour [-5.21% .. +3.79%] · haut q95 +5.07% · bas q05 -5.93%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 33.3  _(momentum baissier)_
- **ADX** : 20.4  _(pas de tendance nette)_
- **MACD** : hist -5.345  _(bearish_recent)_
- **BB** : %B 0.2 · largeur 11.0%
- **ATR** : 48.3 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.147  _(distribution)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 64.3  _(marche en range (choppy))_
- **MA** : MA20 1163.51 · MA50 1093.52 · MA200 1414.88  _(prix < MA20)_
- **Dist MA** : MA20 -3.3% · MA50 +2.9% · MA200 -20.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (844706 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
