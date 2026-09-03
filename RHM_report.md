# RHM

**Generated** : 2026-09-03T21:36:12.482420+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1070.20  

> 🟡 **WAIT-FOR-DIP** — spot +3.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €1070.20 (+3.3% vs entrée) · entrée €1035.78 · stop €1015.06 · T1 €1047.04 · R/R 0.54  
> ↳ P(T1 av. stop) 67 % · EV/risk 0.201 · ¼-Kelly 0.041 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1033.52–€1038.03 (mid €1035.78)
- Spot actuel : €1070.20 (+3.3% au-dessus de la zone — repli à attendre)
- Stop : €1015.06 (stop swing_plan-based (-10.41%))
- Targets : T1 €1047.04 · R/R 0.54 | T2 €1058.31 · R/R 1.09 | T3 €1069.58 · R/R 1.63
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1015.06


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (10.41 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **12.019 pt plus bas** dans le cas TYPIQUE (médiane), 12.019 au p90, **12.019 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 10.41 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0094 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3309** [0.2641 ; 0.4033] _(largeur 13.9 pt, n_eff 173.1)_
   - swing : **0.3867** [0.3365 ; 0.4388] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.4015** [0.3508 ; 0.4538] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (55.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-4.63 %** | CVaR **-6.46 %** | vol 2.84 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 1.55 % contre 3.26 % aujourd'hui, rapport 0.48)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.68 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.855 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5078** (β de hausse 0.5824, asymétrie 0.8719) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.308× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 945.3499 sur atr_grid (3.5 ATR, 11.666 %) — p(stop avant cible) 0.2363 [0.19 ; 0.28], R/R 1.937, perte reelle 22.429 % (gap inclus), CVaR 11.674 %, EV -3.006 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.4 % de la queue et il ne reste que -955.87 EUR a partager. Prix du risque -0.692 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.0 %) — p(stop avant cible) 0.5887 [0.54 ; 0.64], R/R 4.2, perte reelle 10.343 % (gap inclus), EV -3.1835 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.589, borne haute 0.640 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.18 %) : P(cible) 0.0 % x 43.44 % + P(rien) 41.1 % x 7.06 % ne couvrent pas P(stop) 58.9 % x 10.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.96 ATR (stop 15.219 %) — p(stop avant cible) 0.1303 [0.10 ; 0.17], R/R 1.937, perte reelle 22.429 % (gap inclus), EV -1.462 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.46 %) : P(cible) 0.1 % x 43.44 % + P(rien) 86.9 % x 1.64 % ne couvrent pas P(stop) 13.0 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.833 %) — p(stop avant cible) 0.9308 [0.90 ; 0.95], R/R 20.836, perte reelle 2.085 % (gap inclus), EV -1.1716 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 20.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.931, borne haute 0.954 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 0.0 % x 43.44 % + P(rien) 6.9 % x 11.11 % ne couvrent pas P(stop) 93.1 % x 2.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.667 %) — p(stop avant cible) 0.8612 [0.82 ; 0.89], R/R 13.517, perte reelle 3.214 % (gap inclus), EV -1.1861 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 13.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.861, borne haute 0.895 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.0 % x 43.44 % + P(rien) 13.9 % x 11.40 % ne couvrent pas P(stop) 86.1 % x 3.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.5 %) — p(stop avant cible) 0.8005 [0.76 ; 0.84], R/R 10.012, perte reelle 4.339 % (gap inclus), EV -1.3539 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.800, borne haute 0.840 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 0.0 % x 43.44 % + P(rien) 20.0 % x 10.62 % ne couvrent pas P(stop) 80.0 % x 4.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.333 %) — p(stop avant cible) 0.7099 [0.66 ; 0.76], R/R 8.042, perte reelle 5.402 % (gap inclus), EV -1.3981 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.710, borne haute 0.756 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.40 %) : P(cible) 0.0 % x 43.44 % + P(rien) 29.0 % x 8.40 % ne couvrent pas P(stop) 71.0 % x 5.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.166 %) — p(stop avant cible) 0.643 [0.59 ; 0.69], R/R 6.4, perte reelle 6.788 % (gap inclus), EV -1.5956 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.643, borne haute 0.692 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 0.0 % x 43.44 % + P(rien) 35.7 % x 7.76 % ne couvrent pas P(stop) 64.3 % x 6.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.833 %) — p(stop avant cible) 0.5294 [0.48 ; 0.58], R/R 3.586, perte reelle 12.114 % (gap inclus), EV -3.4188 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.529, borne haute 0.582 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.42 %) : P(cible) 0.1 % x 43.44 % + P(rien) 47.0 % x 6.30 % ne couvrent pas P(stop) 52.9 % x 12.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.666 %) — p(stop avant cible) 0.4674 [0.42 ; 0.52], R/R 2.869, perte reelle 15.141 % (gap inclus), EV -4.079 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.08 %) : P(cible) 0.1 % x 43.44 % + P(rien) 53.2 % x 5.57 % ne couvrent pas P(stop) 46.7 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.5 %) — p(stop avant cible) 0.4088 [0.36 ; 0.46], R/R 2.869, perte reelle 15.141 % (gap inclus), EV -3.2818 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.28 %) : P(cible) 0.1 % x 43.44 % + P(rien) 59.0 % x 4.87 % ne couvrent pas P(stop) 40.9 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.333 %) — p(stop avant cible) 0.3889 [0.34 ; 0.44], R/R 1.937, perte reelle 22.429 % (gap inclus), EV -5.8479 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.85 %) : P(cible) 0.1 % x 43.44 % + P(rien) 61.0 % x 4.65 % ne couvrent pas P(stop) 38.9 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.166 %) — p(stop avant cible) 0.3408 [0.29 ; 0.39], R/R 1.937, perte reelle 22.429 % (gap inclus), EV -4.8957 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.90 %) : P(cible) 0.1 % x 43.44 % + P(rien) 65.8 % x 4.12 % ne couvrent pas P(stop) 34.1 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 9.999 %) — p(stop avant cible) 0.291 [0.24 ; 0.34], R/R 1.937, perte reelle 22.429 % (gap inclus), EV -4.0246 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.02 %) : P(cible) 0.1 % x 43.44 % + P(rien) 70.8 % x 3.48 % ne couvrent pas P(stop) 29.1 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 11.666 %) — p(stop avant cible) 0.2363 [0.19 ; 0.28], R/R 1.937, perte reelle 22.429 % (gap inclus), EV -3.006 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.01 %) : P(cible) 0.1 % x 43.44 % + P(rien) 76.3 % x 2.96 % ne couvrent pas P(stop) 23.6 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.96 ATR (stop 14.212 %) — p(stop avant cible) 0.1366 [0.10 ; 0.18], R/R 1.937, perte reelle 22.429 % (gap inclus), EV -1.5607 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.56 %) : P(cible) 0.1 % x 43.44 % + P(rien) 86.2 % x 1.70 % ne couvrent pas P(stop) 13.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 16.666 %) — p(stop avant cible) 0.1045 [0.08 ; 0.14], R/R 1.937, perte reelle 22.429 % (gap inclus), EV -1.1826 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 0.1 % x 43.44 % + P(rien) 89.5 % x 1.26 % ne couvrent pas P(stop) 10.4 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 18.332 %) — p(stop avant cible) 0.069 [0.05 ; 0.10], R/R 1.937, perte reelle 22.429 % (gap inclus), EV -0.8217 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 0.1 % x 43.44 % + P(rien) 93.0 % x 0.74 % ne couvrent pas P(stop) 6.9 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 19.999 %) — p(stop avant cible) 0.0526 [0.03 ; 0.08], R/R 1.937, perte reelle 22.429 % (gap inclus), EV -0.7095 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 0.1 % x 43.44 % + P(rien) 94.7 % x 0.46 % ne couvrent pas P(stop) 5.3 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 21.666 %) — p(stop avant cible) 0.0363 [0.02 ; 0.06], R/R 1.937, perte reelle 22.429 % (gap inclus), EV -0.5399 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.1 % x 43.44 % + P(rien) 96.3 % x 0.25 % ne couvrent pas P(stop) 3.6 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 23.332 %) — p(stop avant cible) 0.0111 [0.00 ; 0.03], R/R 1.862, perte reelle 23.332 % (gap inclus), EV -0.3345 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.1 % x 43.44 % + P(rien) 98.8 % x -0.11 % ne couvrent pas P(stop) 1.1 % x 23.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 24.999 %) — p(stop avant cible) 0.0068 [0.00 ; 0.02], R/R 1.738, perte reelle 24.999 % (gap inclus), EV -0.3469 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 0.1 % x 43.44 % + P(rien) 99.2 % x -0.21 % ne couvrent pas P(stop) 0.7 % x 25.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 26.665 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 1.629, perte reelle 26.665 % (gap inclus), EV -0.324 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.1 % x 43.44 % + P(rien) 99.3 % x -0.20 % ne couvrent pas P(stop) 0.6 % x 26.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1070.2, ATR14 35.6714 (3.333 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.392 ATR = 1.307 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.167 % | 1068.4164 | 89.25 % | 92.1 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.333 % | 1066.6328 | 83.23 % | 87.76 % | 89.72 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.5 % | 1064.8492 | 76.23 % | 82.92 % | 85.67 % | 88.32 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.667 % | 1063.0657 | 69.63 % | 78.48 % | 81.62 % | 85.25 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.833 % | 1061.2821 | 62.13 % | 72.66 % | 76.58 % | 81.09 % | 88.36 % | 91.36 % |
| 0.35 ATR | 1.167 % | 1057.715 | 53.75 % | 65.75 % | 71.05 % | 76.63 % | 85.77 % | 89.25 % |
| 0.5 ATR | 1.667 % | 1052.3642 | 40.34 % | 54.69 % | 61.46 % | 69.01 % | 80.1 % | 83.62 % |
| 0.75 ATR | 2.5 % | 1043.4464 | 23.67 % | 39.09 % | 47.13 % | 57.52 % | 70.25 % | 76.88 % |
| 1.0 ATR | 3.333 % | 1034.5285 | 13.02 % | 26.65 % | 36.17 % | 48.32 % | 62.09 % | 70.35 % |
| 1.25 ATR | 4.166 % | 1025.6107 | 7.4 % | 18.07 % | 26.38 % | 38.81 % | 53.93 % | 63.82 % |
| 1.5 ATR | 5.0 % | 1016.6928 | 3.94 % | 13.13 % | 20.65 % | 31.39 % | 45.67 % | 56.58 % |
| 2.0 ATR | 6.666 % | 998.8571 | 1.78 % | 7.01 % | 12.15 % | 20.69 % | 33.93 % | 46.63 % |
| 2.5 ATR | 8.333 % | 981.0214 | 0.49 % | 3.36 % | 6.32 % | 12.48 % | 24.58 % | 37.39 % |
| 3.0 ATR | 9.999 % | 963.1857 | 0.1 % | 1.38 % | 3.85 % | 7.52 % | 16.92 % | 30.85 % |
| 4.0 ATR | 13.333 % | 927.5142 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.46 % | 19.8 % |
| 6.0 ATR | 19.999 % | 856.1714 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.84 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.57 ATR | 0.66 ATR | 0.87 ATR | 1.05 ATR | 1.19 ATR | 1.76 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.31 ATR | 1.54 ATR | 2.18 ATR | 2.77 ATR |
| **5 s.** | 0.38 ATR | 0.95 ATR | 1.09 ATR | 1.45 ATR | 1.80 ATR | 2.04 ATR | 2.75 ATR | 3.59 ATR |
| **10 s.** | 0.63 ATR | 1.37 ATR | 1.53 ATR | 2.05 ATR | 2.48 ATR | 2.80 ATR | 3.82 ATR | 4.90 ATR |
| **20 s.** | 0.82 ATR | 1.83 ATR | 2.09 ATR | 2.84 ATR | 3.53 ATR | 3.98 ATR | 5.20 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.448–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.655–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.5 %, prix 1043.445), p(touche) 39.09 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.799–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.333 %, prix 1034.5302), p(touche) 36.17 % (en stress 95.1 %)  ✅ optimum identifie (67.1 % des re-echantillons)
- **5 seance(s)** : plage utile 1.087–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.166 %, prix 1025.6154), p(touche) 38.81 % (en stress 98.02 %)  ✅ optimum identifie (88.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.529–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.666 %, prix 998.8604), p(touche) 33.93 % (en stress 96.04 %)  ✅ optimum identifie (99.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.088–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.333 %, prix 981.0202), p(touche) 37.39 % (en stress 98.0 %)  ✅ optimum identifie (99.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.086 | EV/share : €1.772 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 65 % | T2 44 % | T3 28 %
- Kelly (position) : f* 0.165 | ¼-Kelly 0.041 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 82.4 | bear 6.6 | side 10.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.214% → cible +1.088% / stop −2.0%, p_fill 27%, n_eff≈9.8) : P(cible|rempli) **45%** · **EV/risk +0.035** (×p_fill ; si rempli +0.25% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→70% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.03% (p90 6.55%) · excursion haute méd. +2.05% / basse méd. −1.62%
- Profil de vol intra : ouverture 2.584% vs midi 0.93% vs clôture 1.052% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -0.438% ; recovery-V 22%
- **σ réalisé intraday** 2.549% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 1077.4625 (VA 1075.4125–1087.7125 ; dernier close 1079.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 42% · rebond 62% · **stop −2.78%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.53% · baisse 28% (gap-down >1% 9% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.75% (p90 −1.76%) · haut méd +0.49% · range méd 1.34%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −2.04%) · haut méd +0.58% · range méd 1.72%
- Excursion ouverture 30min (n=160) : bas méd −0.99% (p90 −2.24%) · haut méd +0.77% · range méd 1.98%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −2.64%) · haut méd +0.88% · range méd 2.17%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1079.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 69% (105/159) · gap 19% · délai 1.0min · rebond 52% (55/105) (MFE +1.05%)
   - −1.0% : fill 30min 40% · séance 63% (93/159) · gap 9% · délai 6.3min · rebond 61% (56/93) (MFE +1.19%)
   - −1.5% : fill 30min 25% · séance 50% (77/159) · gap 6% · délai 28.2min · rebond 57% (44/77) (MFE +1.19%)
   - −2.0% : fill 30min 18% · séance 42% (65/159) · gap 4% · délai 53.3min · rebond 62% (40/65) (MFE +1.3%)
   - −3.0% : fill 30min 6% · séance 24% (34/159) · gap 3% · délai 225.8min · rebond 46% (17/34) (MFE +0.93%)
   - −4.0% : fill 30min 4% · séance 13% (23/159) · gap 2% · délai 174.9min · rebond 69% (14/23) (MFE +1.69%)
   - −5.0% : fill 30min 1% · séance 7% (12/159) · gap 1% · délai 301.9min · rebond 92% (11/12) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −1.47%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.7%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.74%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=542 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (34 séances) :
      · −1.0% : fill 96% (33/34) · rebond 80% (25/33)
      · −2.0% : fill 76% (28/34) · rebond 66% (19/28)
      · −3.0% : fill 40% (13/34) · rebond 60% (8/13)
      · −4.0% : fill 34% (11/34) · rebond 72% (8/11)
      · −5.0% : fill 23% (7/34) · rebond 100% (7/7)
   - **flat** (20 séances) :
      · −1.0% : fill 84% (14/20) · rebond 60% (10/14)
      · −2.0% : fill 52% (8/20) · rebond 71% (6/8)
      · −3.0% : fill 29% (4/20) · rebond 37% (1/4)
      · −4.0% : fill 9% (2/20) · rebond 62% (1/2)
      · −5.0% : fill 9% (2/20) · rebond 62% (1/2)
   - **gap-up** (105 séances) :
      · −1.0% : fill 47% (46/105) · rebond 48% (21/46)
      · −2.0% : fill 28% (29/105) · rebond 54% (15/29)
      · −3.0% : fill 17% (17/105) · rebond 41% (8/17)
      · −4.0% : fill 7% (10/105) · rebond 67% (5/10)
      · −5.0% : fill 2% (3/105) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 60% si les 15 1res min sont vertes (74 cas) · 33% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 66% si début vert vs 25% si rouge (base 44% · écart 40 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **66%** · continue >prix actuel 40% ; creux résiduel méd -1.25% (q20 -2.93%) → **SL/trailing à −2.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.28% / q75 +1.88% → **scale +1.28% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **25%** (continue à baisser 52%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.11%** (au-delà de la MAE q10 -4.11%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.6% .. +3.18%] · haut q95 +3.56% · bas q05 -3.0%
   - 60min (n=160) : retour [-2.72% .. +3.16%] · haut q95 +4.28% · bas q05 -3.69%
   - 2h (n=160) : retour [-3.14% .. +2.91%] · haut q95 +4.35% · bas q05 -4.21%
   - 4h (n=160) : retour [-3.27% .. +3.05%] · haut q95 +4.82% · bas q05 -4.57%
   - 6h (n=160) : retour [-4.0% .. +3.22%] · haut q95 +4.87% · bas q05 -4.89%
   - session (n=160) : retour [-4.46% .. +3.65%] · haut q95 +4.99% · bas q05 -5.62%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.0  _(survente)_
- **ADX** : 16.6  _(pas de tendance nette)_
- **MACD** : hist -13.595  _(pas de croisement recent)_
- **BB** : %B 0.02 · largeur 14.1%
- **ATR** : 35.67 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.21  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 39.0  _(transition)_
- **MA** : MA20 1147.55 · MA50 1093.22 · MA200 1390.64  _(prix < MA20)_
- **Dist MA** : MA20 -6.7% · MA50 -2.1% · MA200 -23.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (770866 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
