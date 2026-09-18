# SAF

**Generated** : 2026-09-18T21:45:59.357957+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €323.00  

> 🟡 **WAIT-FOR-DIP** — spot +2.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €323.00 (+2.2% vs entrée) · entrée €316.19 · stop €309.87 · T1 €318.84 · R/R 0.42  
> ↳ P(T1 av. stop) 81 % · EV/risk 0.082 · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €315.67–€316.72 (mid €316.19)
- Spot actuel : €323.00 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : €309.87 (stop swing_plan-based (-6.87%))
- Targets : T1 €318.84 · R/R 0.42 | T2 €321.49 · R/R 0.84 | T3 €324.14 · R/R 1.26
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €309.87


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (6.87 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1279).
   - exécution **3.116 pt plus bas** dans le cas TYPIQUE (médiane), 3.116 au p90, **3.116 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 6.87 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0024 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.396 % | p01 -2.356 % | pire -9.986 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1909** [0.1377 ; 0.2543] _(largeur 11.7 pt, n_eff 173.1)_
   - swing : **0.4099** [0.359 ; 0.4623] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3596** [0.3104 ; 0.4112] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (50.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.21 %** | CVaR **-4.01 %** | vol 2.07 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.35 % contre 2.42 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.933 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3896** (β de hausse 1.3421, asymétrie 1.0354) vs FCHI — 618 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 289.884 sur sr_based (3.88 ATR, 10.253 %) — p(stop avant cible) 0.0708 [0.05 ; 0.10], R/R 1.162, perte reelle 10.253 % (gap inclus), CVaR 10.253 %, EV 0.9176 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.77 ATR (stop 3.318 %) — p(stop avant cible) 0.4751 [0.42 ; 0.53], R/R 2.244, perte reelle 5.309 % (gap inclus), EV -0.0591 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 8.3 % x 11.92 % + P(rien) 44.2 % x 3.33 % ne couvrent pas P(stop) 47.5 % x 5.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.88 ATR (stop 10.253 %) — p(stop avant cible) 0.0708 [0.05 ; 0.10], R/R 1.162, perte reelle 10.253 % (gap inclus), EV 0.9176 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 8.79 ATR (stop 21.205 %) — p(stop avant cible) 0.0042 [0.00 ; 0.02], R/R 0.562, perte reelle 21.205 % (gap inclus), EV 0.8725 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.20 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.558 %) — p(stop avant cible) 0.8991 [0.86 ; 0.93], R/R 9.223, perte reelle 1.292 % (gap inclus), EV -0.4377 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 9.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.899, borne haute 0.927 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 3.4 % x 11.92 % + P(rien) 6.7 % x 4.74 % ne couvrent pas P(stop) 89.9 % x 1.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.116 %) — p(stop avant cible) 0.7916 [0.75 ; 0.83], R/R 6.139, perte reelle 1.941 % (gap inclus), EV -0.2609 % — **REFUSE**
      - refuse : cible atteinte seulement 4.8 % du temps (< 15 %) meme a 10 seances : le R/R de 6.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.792, borne haute 0.832 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 4.8 % x 11.92 % + P(rien) 16.0 % x 4.39 % ne couvrent pas P(stop) 79.2 % x 1.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.77 ATR (stop 2.385 %) — p(stop avant cible) 0.6053 [0.55 ; 0.66], R/R 2.99, perte reelle 3.985 % (gap inclus), EV -0.2439 % — **REFUSE**
      - refuse : cible atteinte seulement 7.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.605, borne haute 0.656 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 7.5 % x 11.92 % + P(rien) 31.9 % x 3.98 % ne couvrent pas P(stop) 60.5 % x 3.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 2.789 %) — p(stop avant cible) 0.543 [0.49 ; 0.59], R/R 2.693, perte reelle 4.424 % (gap inclus), EV -0.0682 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.543, borne haute 0.595 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 7.9 % x 11.92 % + P(rien) 37.8 % x 3.68 % ne couvrent pas P(stop) 54.3 % x 4.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 3.905 %) — p(stop avant cible) 0.394 [0.34 ; 0.45], R/R 1.933, perte reelle 6.163 % (gap inclus), EV 0.1432 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 4.463 %) — p(stop avant cible) 0.3516 [0.30 ; 0.40], R/R 1.753, perte reelle 6.799 % (gap inclus), EV 0.1854 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 5.02 %) — p(stop avant cible) 0.2994 [0.25 ; 0.35], R/R 1.753, perte reelle 6.799 % (gap inclus), EV 0.595 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.578 %) — p(stop avant cible) 0.2584 [0.21 ; 0.31], R/R 1.193, perte reelle 9.986 % (gap inclus), EV -0.0011 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 9.0 % x 11.92 % + P(rien) 65.2 % x 2.32 % ne couvrent pas P(stop) 25.8 % x 9.99 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 6.136 %) — p(stop avant cible) 0.2346 [0.19 ; 0.28], R/R 1.193, perte reelle 9.986 % (gap inclus), EV 0.2094 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 6.694 %) — p(stop avant cible) 0.1994 [0.16 ; 0.24], R/R 1.193, perte reelle 9.986 % (gap inclus), EV 0.3845 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.81 %) — p(stop avant cible) 0.1422 [0.11 ; 0.18], R/R 1.193, perte reelle 9.986 % (gap inclus), EV 0.706 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.88 ATR (stop 9.32 %) — p(stop avant cible) 0.0899 [0.06 ; 0.12], R/R 1.193, perte reelle 9.986 % (gap inclus), EV 0.8798 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 11.157 %) — p(stop avant cible) 0.0585 [0.04 ; 0.09], R/R 1.068, perte reelle 11.157 % (gap inclus), EV 0.8942 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.5 ATR (stop 12.272 %) — p(stop avant cible) 0.0409 [0.02 ; 0.07], R/R 0.971, perte reelle 12.272 % (gap inclus), EV 0.9044 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.27 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 13.388 %) — p(stop avant cible) 0.0318 [0.02 ; 0.05], R/R 0.89, perte reelle 13.388 % (gap inclus), EV 0.8684 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.39 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 14.504 %) — p(stop avant cible) 0.0186 [0.01 ; 0.04], R/R 0.822, perte reelle 14.504 % (gap inclus), EV 0.8678 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.50 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 15.619 %) — p(stop avant cible) 0.0092 [0.00 ; 0.02], R/R 0.763, perte reelle 15.619 % (gap inclus), EV 0.8733 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.62 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 16.735 %) — p(stop avant cible) 0.0064 [0.00 ; 0.02], R/R 0.712, perte reelle 16.735 % (gap inclus), EV 0.8778 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.74 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 17.851 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 0.668, perte reelle 17.851 % (gap inclus), EV 0.8788 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.85 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 323.0, ATR14 7.2071 (2.231 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 0.768 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.112 % | 322.6396 | 89.21 % | 92.53 % | 93.71 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.223 % | 322.2793 | 81.45 % | 87.23 % | 89.18 % | 91.43 % | 93.47 % | 94.8 % |
| 0.15 ATR | 0.335 % | 321.9189 | 75.07 % | 83.3 % | 86.23 % | 88.67 % | 91.29 % | 92.7 % |
| 0.2 ATR | 0.446 % | 321.5586 | 68.11 % | 78.0 % | 82.6 % | 85.32 % | 88.91 % | 90.9 % |
| 0.25 ATR | 0.558 % | 321.1982 | 61.04 % | 73.28 % | 78.96 % | 83.25 % | 87.62 % | 90.0 % |
| 0.35 ATR | 0.781 % | 320.4775 | 49.26 % | 63.26 % | 69.81 % | 76.95 % | 82.67 % | 87.0 % |
| 0.5 ATR | 1.116 % | 319.3964 | 35.23 % | 51.67 % | 59.1 % | 68.47 % | 75.84 % | 81.3 % |
| 0.75 ATR | 1.673 % | 317.5946 | 20.51 % | 35.46 % | 42.87 % | 53.2 % | 63.17 % | 70.7 % |
| 1.0 ATR | 2.231 % | 315.7929 | 9.81 % | 23.67 % | 32.45 % | 41.97 % | 53.47 % | 61.2 % |
| 1.25 ATR | 2.789 % | 313.9911 | 4.32 % | 15.42 % | 23.99 % | 33.2 % | 46.14 % | 54.4 % |
| 1.5 ATR | 3.347 % | 312.1893 | 2.26 % | 10.02 % | 16.62 % | 25.02 % | 37.92 % | 46.4 % |
| 2.0 ATR | 4.463 % | 308.5857 | 0.98 % | 4.42 % | 7.47 % | 15.37 % | 26.83 % | 36.7 % |
| 2.5 ATR | 5.578 % | 304.9821 | 0.2 % | 1.47 % | 3.64 % | 8.67 % | 18.32 % | 27.9 % |
| 3.0 ATR | 6.694 % | 301.3786 | 0.0 % | 0.88 % | 2.06 % | 5.71 % | 12.08 % | 21.6 % |
| 4.0 ATR | 8.925 % | 294.1714 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 4.55 % | 10.8 % |
| 6.0 ATR | 13.388 % | 279.7571 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.67 ATR | 0.76 ATR | 1.00 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.50 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.72 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.86 ATR | 2.32 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.26 ATR | 1.50 ATR | 1.76 ATR | 2.40 ATR | 3.15 ATR |
| **10 s.** | 0.52 ATR | 1.12 ATR | 1.28 ATR | 1.72 ATR | 2.11 ATR | 2.40 ATR | 3.28 ATR | 3.94 ATR |
| **20 s.** | 0.65 ATR | 1.39 ATR | 1.57 ATR | 2.21 ATR | 2.73 ATR | 3.15 ATR | 4.21 ATR | 5.49 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.673 %, prix 317.5962), p(touche) 35.46 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.717–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.673 %, prix 317.5962), p(touche) 42.87 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.933–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.231 %, prix 315.7939), p(touche) 41.97 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.285–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.347 %, prix 312.1892), p(touche) 37.92 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.572–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.463 %, prix 308.5845), p(touche) 36.7 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.004 | EV/share : €0.022 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 36 % | T3 17 %
- Kelly (position) : f* 0.083 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 41.6 | bear 52.9 | side 5.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.102% → cible +0.838% / stop −2.0%, p_fill 23%, n_eff≈8.9) : P(cible|rempli) **18%** · **EV/risk -0.006** (×p_fill ; si rempli -0.05% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→52% · +2.0%→28% · +3.0%→9% · +5.0%→0% · +8.0%→0%
- Range intraday médian 2.45% (p90 3.72%) · excursion haute méd. +1.09% / basse méd. −0.77%
- Profil de vol intra : ouverture 1.461% vs midi 0.5% vs clôture 0.665% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.3% ; recovery-V 12%
- **σ réalisé intraday** 1.544% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 61% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 331.8075 (VA 331.3325–332.7575 ; dernier close 333.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 23% · rebond 36% · **stop −1.2%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 31% (gap-down >1% 1% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.56%) · haut méd +0.18% · range méd 0.85%
- Excursion ouverture 15min (n=160) : bas méd −0.48% (p90 −1.76%) · haut méd +0.31% · range méd 1.02%
- Excursion ouverture 30min (n=160) : bas méd −0.49% (p90 −1.78%) · haut méd +0.44% · range méd 1.22%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.84%) · haut méd +0.53% · range méd 1.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 333.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 60% (86/159) · gap 10% · délai 0.4min · rebond 38% (34/86) (MFE +0.84%)
   - −1.0% : fill 30min 25% · séance 48% (71/159) · gap 1% · délai 25.1min · rebond 42% (33/71) (MFE +0.79%)
   - −1.5% : fill 30min 11% · séance 29% (45/159) · gap 1% · délai 67.5min · rebond 31% (19/45) (MFE +0.52%)
   - −2.0% : fill 30min 4% · séance 23% (37/159) · gap 0% · délai 240.5min · rebond 36% (16/37) (MFE +0.74%)
   - −3.0% : fill 30min 1% · séance 7% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −0.77%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.77%) → stop au-delà de −0.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=205 jambes) : jambe baissière méd −1.05% (p90 −2.26%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 76% (18/22) · rebond 29% (7/18)
      · −2.0% : fill 48% (12/22) · rebond 42% (6/12)
      · −3.0% : fill 16% (5/22) · rebond 31% (2/5)
      · −4.0% : fill 7% (2/22) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/22) · rebond 0% (0/0)
   - **flat** (38 séances) :
      · −1.0% : fill 49% (20/38) · rebond 40% (10/20)
      · −2.0% : fill 26% (9/38) · rebond 12% (1/9)
      · −3.0% : fill 5% (3/38) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/38) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/38) · rebond 0% (0/0)
   - **gap-up** (99 séances) :
      · −1.0% : fill 39% (33/99) · rebond 53% (16/33)
      · −2.0% : fill 13% (16/99) · rebond 59% (9/16)
      · −3.0% : fill 5% (6/99) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/99) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/99) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 70% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 77% si début vert vs 22% si rouge (base 48% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **77%** · continue >prix actuel 50% ; creux résiduel méd -0.71% (q20 -1.34%) → **SL/trailing à −1.34%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.96% / q75 +1.45% → **scale +0.96% / runner +1.45%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **22%** (continue à baisser 60%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.29%** (au-delà de la MAE q10 -2.29%), cible rebond +0.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.49% .. +1.54%] · haut q95 +1.94% · bas q05 -2.06%
   - 60min (n=160) : retour [-1.63% .. +1.81%] · haut q95 +1.99% · bas q05 -2.34%
   - 2h (n=160) : retour [-2.32% .. +2.06%] · haut q95 +2.49% · bas q05 -2.92%
   - 4h (n=160) : retour [-1.87% .. +2.1%] · haut q95 +2.7% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.06% .. +2.31%] · haut q95 +2.78% · bas q05 -2.98%
   - session (n=160) : retour [-2.7% .. +2.39%] · haut q95 +3.33% · bas q05 -3.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 31.6  _(momentum baissier)_
- **ADX** : 20.1  _(pas de tendance nette)_
- **MACD** : hist -1.06  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 10.6%
- **ATR** : 7.21 (38.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.268  _(distribution)_
- **Vol ratio** : 2.59  _(volume au-dessus de la moyenne)_
- **Choppiness** : 53.3  _(transition)_
- **MA** : MA20 333.12 · MA50 339.18 · MA200 313.0  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 -4.8% · MA200 +3.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (843449 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
