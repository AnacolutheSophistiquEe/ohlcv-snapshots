# ENR

**Generated** : 2026-09-01T21:40:47.077417+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €141.08  

> 🟡 **WAIT-FOR-DIP** — spot +2.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €141.08 (+2.5% vs entrée) · entrée €137.70 · stop €126.69 · T1 €139.34 · R/R 0.15  
> ↳ P(T1 av. stop) 55 % _(réel 5 s)_ · EV/risk 0.014 _(réel 5 s)_ (GBM -0.072) · ¼-Kelly 0.099 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €137.37–€138.03 (mid €137.70)
- Spot actuel : €141.08 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : €126.69 (stop swing_plan-based (-9.07%))
- Targets : T1 €139.34 · R/R 0.15 | T2 €140.98 · R/R 0.3 | T3 €142.62 · R/R 0.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.69


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.07 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **7.1 pt plus bas** dans le cas TYPIQUE (médiane), 22.77 au p90, **26.687 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 9.07 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0301 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.307 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0097** [0.0017 ; 0.0335] _(largeur 3.2 pt, n_eff 173.1)_
   - swing : **0.406** [0.3552 ; 0.4584] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3637** [0.3143 ; 0.4154] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 18.3 observations effectives », dont la borne haute a 95 % vaut environ 16.4 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.7 pt), swing (46.6 pt), deep (44.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 900 séances)** : VaR **-4.37 %** | CVaR **-7.71 %** | vol 3.55 %/j
   - _fenêtre arrêtée : rupture de regime a 960 seances en arriere (volatilite 2.06 % contre 3.32 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3616** (β de hausse 1.0924, asymétrie 1.2464) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.394× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 125.4199 sur grid_snapped (2.62 ATR, 11.1 %) — p(stop avant cible) 0.2091 [0.17 ; 0.25], R/R 1.511, perte reelle 21.854 % (gap inclus), CVaR 11.125 %, EV -1.5727 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 18 des 18 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 60.2 % de la queue et il ne reste que -755.68 EUR a partager. Prix du risque -0.422 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.7 %) — p(stop avant cible) 0.5244 [0.47 ; 0.58], R/R 3.071, perte reelle 10.753 % (gap inclus), EV -2.4812 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.524, borne haute 0.577 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.48 %) : P(cible) 0.4 % x 33.02 % + P(rien) 47.2 % x 6.44 % ne couvrent pas P(stop) 52.4 % x 10.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.62 ATR (stop 12.366 %) — p(stop avant cible) 0.1465 [0.11 ; 0.19], R/R 1.511, perte reelle 21.854 % (gap inclus), EV -0.4794 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 0.4 % x 33.02 % + P(rien) 85.0 % x 3.06 % ne couvrent pas P(stop) 14.6 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.78 ATR (stop 24.379 %) — p(stop avant cible) 0.0052 [0.00 ; 0.02], R/R 0.924, perte reelle 35.757 % (gap inclus), EV 1.5944 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.39 % > budget 12.00 %
   - 🟢 support a 9.54 ATR (stop 38.671 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.854, perte reelle 38.671 % (gap inclus), EV 1.692 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.67 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.95 %) — p(stop avant cible) 0.918 [0.89 ; 0.94], R/R 14.217, perte reelle 2.323 % (gap inclus), EV -1.2779 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 14.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.918, borne haute 0.944 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 0.1 % x 33.02 % + P(rien) 8.1 % x 10.10 % ne couvrent pas P(stop) 91.8 % x 2.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.9 %) — p(stop avant cible) 0.835 [0.79 ; 0.87], R/R 8.565, perte reelle 3.856 % (gap inclus), EV -1.7093 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 8.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.835, borne haute 0.871 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.71 %) : P(cible) 0.2 % x 33.02 % + P(rien) 16.3 % x 8.90 % ne couvrent pas P(stop) 83.5 % x 3.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.85 %) — p(stop avant cible) 0.7638 [0.72 ; 0.81], R/R 5.575, perte reelle 5.924 % (gap inclus), EV -2.3389 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.764, borne haute 0.806 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.34 %) : P(cible) 0.4 % x 33.02 % + P(rien) 23.3 % x 8.90 % ne couvrent pas P(stop) 76.4 % x 5.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.8 %) — p(stop avant cible) 0.6573 [0.61 ; 0.71], R/R 4.459, perte reelle 7.407 % (gap inclus), EV -2.1173 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.657, borne haute 0.706 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 0.4 % x 33.02 % + P(rien) 33.9 % x 7.77 % ne couvrent pas P(stop) 65.7 % x 7.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.75 %) — p(stop avant cible) 0.5899 [0.54 ; 0.64], R/R 3.447, perte reelle 9.581 % (gap inclus), EV -2.6213 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.590, borne haute 0.641 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.62 %) : P(cible) 0.4 % x 33.02 % + P(rien) 40.7 % x 7.17 % ne couvrent pas P(stop) 59.0 % x 9.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.65 %) — p(stop avant cible) 0.4602 [0.41 ; 0.51], R/R 2.241, perte reelle 14.737 % (gap inclus), EV -3.5834 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.58 %) : P(cible) 0.4 % x 33.02 % + P(rien) 53.6 % x 5.74 % ne couvrent pas P(stop) 46.0 % x 14.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.601 %) — p(stop avant cible) 0.4001 [0.35 ; 0.45], R/R 1.778, perte reelle 18.578 % (gap inclus), EV -4.1358 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.14 %) : P(cible) 0.4 % x 33.02 % + P(rien) 59.6 % x 5.33 % ne couvrent pas P(stop) 40.0 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.551 %) — p(stop avant cible) 0.3373 [0.29 ; 0.39], R/R 1.778, perte reelle 18.578 % (gap inclus), EV -3.0423 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.04 %) : P(cible) 0.4 % x 33.02 % + P(rien) 65.9 % x 4.71 % ne couvrent pas P(stop) 33.7 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.62 ATR (stop 11.1 %) — p(stop avant cible) 0.2091 [0.17 ; 0.25], R/R 1.511, perte reelle 21.854 % (gap inclus), EV -1.5727 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 0.4 % x 33.02 % + P(rien) 78.7 % x 3.66 % ne couvrent pas P(stop) 20.9 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 13.301 %) — p(stop avant cible) 0.1045 [0.08 ; 0.14], R/R 1.511, perte reelle 21.854 % (gap inclus), EV 0.2892 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.32 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 15.201 %) — p(stop avant cible) 0.0599 [0.04 ; 0.09], R/R 1.272, perte reelle 25.963 % (gap inclus), EV 0.7452 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.22 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 17.101 %) — p(stop avant cible) 0.0366 [0.02 ; 0.06], R/R 0.924, perte reelle 35.757 % (gap inclus), EV 0.8007 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.12 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 19.001 %) — p(stop avant cible) 0.0262 [0.01 ; 0.05], R/R 0.924, perte reelle 35.757 % (gap inclus), EV 1.0818 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.01 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.902 %) — p(stop avant cible) 0.0089 [0.00 ; 0.02], R/R 0.924, perte reelle 35.757 % (gap inclus), EV 1.479 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.91 % > budget 12.00 %
   - 🟢 grid_snapped a 5.78 ATR (stop 23.113 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.924, perte reelle 35.757 % (gap inclus), EV 1.5632 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.12 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.602 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.924, perte reelle 35.757 % (gap inclus), EV 1.6465 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.61 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.502 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.924, perte reelle 35.757 % (gap inclus), EV 1.6465 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.51 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.402 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.924, perte reelle 35.757 % (gap inclus), EV 1.6759 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.41 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 141.08, ATR14 5.3614 (3.8 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.368 ATR = 1.399 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.19 % | 140.8119 | 91.32 % | 94.08 % | 95.55 % | 96.24 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.38 % | 140.5439 | 83.73 % | 88.06 % | 90.61 % | 92.77 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.57 % | 140.2758 | 76.33 % | 82.43 % | 86.07 % | 88.81 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.76 % | 140.0077 | 70.22 % | 79.17 % | 83.2 % | 86.63 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.95 % | 139.7396 | 63.91 % | 75.02 % | 79.74 % | 83.66 % | 87.36 % | 90.45 % |
| 0.35 ATR | 1.33 % | 139.2035 | 51.87 % | 65.25 % | 70.95 % | 76.34 % | 81.99 % | 86.33 % |
| 0.5 ATR | 1.9 % | 138.3993 | 36.49 % | 52.32 % | 59.98 % | 66.83 % | 74.43 % | 80.2 % |
| 0.75 ATR | 2.85 % | 137.0589 | 20.02 % | 36.33 % | 45.45 % | 54.75 % | 65.37 % | 73.27 % |
| 1.0 ATR | 3.8 % | 135.7186 | 11.14 % | 25.57 % | 34.39 % | 44.26 % | 56.72 % | 64.92 % |
| 1.25 ATR | 4.75 % | 134.3782 | 6.11 % | 17.28 % | 25.1 % | 35.74 % | 48.16 % | 57.29 % |
| 1.5 ATR | 5.7 % | 133.0379 | 2.86 % | 11.15 % | 17.89 % | 27.72 % | 41.09 % | 51.06 % |
| 2.0 ATR | 7.601 % | 130.3571 | 0.79 % | 4.05 % | 8.6 % | 15.94 % | 28.16 % | 40.0 % |
| 2.5 ATR | 9.501 % | 127.6764 | 0.3 % | 1.97 % | 4.15 % | 9.41 % | 19.7 % | 30.45 % |
| 3.0 ATR | 11.401 % | 124.9957 | 0.1 % | 0.79 % | 1.88 % | 4.95 % | 12.84 % | 22.81 % |
| 4.0 ATR | 15.201 % | 119.6343 | 0.1 % | 0.39 % | 1.09 % | 2.38 % | 6.77 % | 13.17 % |
| 6.0 ATR | 22.802 % | 108.9114 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.29 % | 5.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.83 ATR | 1.02 ATR | 1.17 ATR | 1.58 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.04 ATR | 1.25 ATR | 1.43 ATR | 1.93 ATR | 2.40 ATR |
| **5 s.** | 0.37 ATR | 0.86 ATR | 0.98 ATR | 1.33 ATR | 1.61 ATR | 1.83 ATR | 2.46 ATR | 2.99 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.19 ATR | 2.48 ATR | 3.47 ATR | 4.79 ATR |
| **20 s.** | 0.69 ATR | 1.55 ATR | 1.77 ATR | 2.37 ATR | 2.86 ATR | 3.29 ATR | 4.84 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.417–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.85 %, prix 137.0592), p(touche) 36.33 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.76–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.8 %, prix 135.719), p(touche) 34.39 % (en stress 91.18 %)  ✅ optimum identifie (84.6 % des re-echantillons)
- **5 seance(s)** : plage utile 0.982–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.8 %, prix 135.719), p(touche) 44.26 % (en stress 99.01 %)  ✅ optimum identifie (88.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.362–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.7 %, prix 133.0384), p(touche) 41.09 % (en stress 100.0 %)  ✅ optimum identifie (92.4 % des re-echantillons)
- **20 seance(s)** : plage utile 1.774–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.601 %, prix 130.3565), p(touche) 40.0 % (en stress 99.0 %)  ✅ optimum identifie (88.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.072 | EV/share : €-0.798 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 32 % | T3 15 %
- Kelly (position) : f* 0.394 | ¼-Kelly 0.099 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 13.9 | side 81.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.391% → cible +1.191% / stop −8.0%, p_fill 44%, n_eff≈18.3) : P(cible|rempli) **55%** · **EV/risk +0.014** (×p_fill ; si rempli +0.26% du capital)
  - **swing** (entrée dip −5.27% → cible +2.664% / stop −4.012%, p_fill 25%, n_eff≈12.3) : P(cible|rempli) **71%** · **EV/risk +0.072** (×p_fill ; si rempli +1.17% du capital)
  - **deep** (entrée dip −8.139% → cible +3.767% / stop −6.206%, p_fill 17%, n_eff≈9.1) : P(cible|rempli) **84%** · **EV/risk +0.058** (×p_fill ; si rempli +2.10% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→57% · +2.0%→38% · +3.0%→20% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.86% (p90 6.15%) · excursion haute méd. +1.29% / basse méd. −2.18%
- Profil de vol intra : ouverture 2.139% vs midi 0.885% vs clôture 1.066% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑1%/↓0% ; spike-down 60% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; neutre — autocorr -0.005)_ ; drift intra méd. -0.726% ; recovery-V 8%
- **σ réalisé intraday** 2.456% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 74% / whipsaw 44%
- POC intraday (dernière séance, temps-au-prix) : 144.3727 (VA 143.2277–144.9452 ; dernier close 142.16)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 20% · rebond 66% · **stop −3.12%** sous le fill (sous le bruit) · cible +1.27% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 33% (gap-down >1% 19% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.58% (p90 −1.67%) · haut méd +0.44% · range méd 1.2%
- Excursion ouverture 15min (n=160) : bas méd −0.77% (p90 −2.23%) · haut méd +0.59% · range méd 1.56%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.29%) · haut méd +0.63% · range méd 1.92%
- Excursion ouverture 60min (n=160) : bas méd −1.0% (p90 −2.7%) · haut méd +0.73% · range méd 2.08%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 142.18 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 73% (115/159) · gap 27% · délai 0.5min · rebond 56% (64/115) (MFE +1.19%)
   - −1.0% : fill 30min 45% · séance 68% (107/159) · gap 19% · délai 7.9min · rebond 60% (62/107) (MFE +1.41%)
   - −1.5% : fill 30min 31% · séance 55% (89/159) · gap 16% · délai 11.9min · rebond 61% (53/89) (MFE +1.52%)
   - −2.0% : fill 30min 22% · séance 43% (74/159) · gap 11% · délai 15.4min · rebond 63% (50/74) (MFE +1.53%)
   - −3.0% : fill 30min 12% · séance 30% (52/159) · gap 4% · délai 208.4min · rebond 53% (33/52) (MFE +1.05%)
   - −4.0% : fill 30min 7% · séance 20% (38/159) · gap 2% · délai 129.6min · rebond 66% (27/38) (MFE +1.27%)
   - −5.0% : fill 30min 2% · séance 14% (25/159) · gap 0% · délai 398.5min · rebond 36% (13/25) (MFE +0.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −1.63%) → stop au-delà de −1.1% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.84%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.43% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=542 jambes) : jambe baissière méd −1.07% (p90 −2.64%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 98% (50/51) · rebond 55% (27/50)
      · −2.0% : fill 78% (39/51) · rebond 49% (23/39)
      · −3.0% : fill 63% (31/51) · rebond 40% (18/31)
      · −4.0% : fill 51% (26/51) · rebond 71% (20/26)
      · −5.0% : fill 38% (18/51) · rebond 39% (11/18)
   - **flat** (15 séances) :
      · −1.0% : fill 83% (13/15) · rebond 90% (11/13)
      · −2.0% : fill 43% (8/15) · rebond 84% (6/8)
      · −3.0% : fill 29% (5/15) · rebond 76% (3/5)
      · −4.0% : fill 16% (4/15) · rebond 52% (2/4)
      · −5.0% : fill 13% (3/15) · rebond 0% (0/3)
   - **gap-up** (93 séances) :
      · −1.0% : fill 51% (44/93) · rebond 56% (24/44)
      · −2.0% : fill 26% (27/93) · rebond 78% (21/27)
      · −3.0% : fill 13% (16/93) · rebond 74% (12/16)
      · −4.0% : fill 5% (8/93) · rebond 50% (5/8)
      · −5.0% : fill 3% (4/93) · rebond 40% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 73% si les 15 1res min sont vertes (74 cas) · 18% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **14min** → P(séance verte=clôture>ouverture) 66% si début vert vs 22% si rouge (base 43% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **66%** · continue >prix actuel 42% ; creux résiduel méd -1.32% (q20 -3.18%) → **SL/trailing à −3.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +2.48% → **scale +1.5% / runner +2.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **22%** (continue à baisser 60%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.36%** (au-delà de la MAE q10 -4.36%), cible rebond +1.09% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.08% .. +2.02%] · haut q95 +2.67% · bas q05 -2.72%
   - 60min (n=160) : retour [-2.49% .. +2.33%] · haut q95 +2.71% · bas q05 -3.05%
   - 2h (n=160) : retour [-2.84% .. +2.65%] · haut q95 +2.92% · bas q05 -3.69%
   - 4h (n=160) : retour [-3.18% .. +2.65%] · haut q95 +3.7% · bas q05 -4.1%
   - 6h (n=160) : retour [-3.74% .. +3.36%] · haut q95 +4.15% · bas q05 -4.61%
   - session (n=160) : retour [-4.9% .. +3.97%] · haut q95 +5.23% · bas q05 -6.2%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **20 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
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

- **RSI** : 20.1  _(survente)_
- **ADX** : 12.1  _(pas de tendance nette)_
- **MACD** : hist -1.424  _(pas de croisement recent)_
- **BB** : %B -0.03 · largeur 15.0%
- **ATR** : 5.36 (34.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.279  _(distribution)_
- **Vol ratio** : 1.14  _(volume normal)_
- **Choppiness** : 40.3  _(transition)_
- **MA** : MA20 153.38 · MA50 153.65 · MA200 149.93  _(prix < MA20)_
- **Dist MA** : MA20 -8.0% · MA50 -8.2% · MA200 -5.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (798863 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
