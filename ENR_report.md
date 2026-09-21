# ENR

**Generated** : 2026-09-21T00:08:16.625000+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €140.20  

> 🟡 **WAIT-FOR-DIP** — spot +2.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €140.20 (+2.1% vs entrée) · entrée €137.27 · stop €126.29 · T1 €139.43 · R/R 0.2  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk 0.007 _(réel 5 s)_ (GBM -0.06) · ¼-Kelly 0.079 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.290 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €136.84–€137.70 (mid €137.27)
- Spot actuel : €140.20 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : €126.29 (stop swing_plan-based (-8.43%))
- Targets : T1 €139.43 · R/R 0.2 | T2 €141.58 · R/R 0.39 | T3 €143.74 · R/R 0.59
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.29


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.59 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.43 %)** : le gap seul le franchit 0.314 % des séances (4 fois sur 1273).
   - exécution **6.473 pt plus bas** dans le cas TYPIQUE (médiane), 21.451 au p90, **27.327 au pire**
   - perte réelle **18.578 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 8.43 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0319 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.333 % | p01 -5.092 % | pire -35.757 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0085** [0.0014 ; 0.0315] _(largeur 3.0 pt, n_eff 173.1)_
   - swing : **0.472** [0.4198 ; 0.5247] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4276** [0.3762 ; 0.4802] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 20.5 observations effectives », dont la borne haute a 95 % vaut environ 14.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (40.9 pt), swing (46.4 pt), deep (41.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.65 %** | CVaR **-6.68 %** | vol 3.23 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.68 % contre 3.24 % aujourd'hui, rapport 1.75)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3547** (β de hausse 1.0891, asymétrie 1.2439) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.376× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 124.4454 sur sr_based (2.28 ATR, 11.237 %) — p(stop avant cible) 0.1896 [0.15 ; 0.23], R/R 1.549, perte reelle 21.854 % (gap inclus), CVaR 11.262 %, EV -1.7245 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 22 des 22 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 42.1 % de la queue et il ne reste que -112.43 EUR a partager. Prix du risque -0.036 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.39 ATR (stop 4.006 %) — p(stop avant cible) 0.6622 [0.61 ; 0.71], R/R 4.479, perte reelle 7.559 % (gap inclus), EV -2.377 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.662, borne haute 0.711 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.38 %) : P(cible) 0.2 % x 33.86 % + P(rien) 33.6 % x 7.61 % ne couvrent pas P(stop) 66.2 % x 7.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.747 %) — p(stop avant cible) 0.5469 [0.49 ; 0.60], R/R 3.007, perte reelle 11.258 % (gap inclus), EV -3.2151 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.547, borne haute 0.599 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.22 %) : P(cible) 0.2 % x 33.86 % + P(rien) 45.1 % x 6.35 % ne couvrent pas P(stop) 54.7 % x 11.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.28 ATR (stop 11.237 %) — p(stop avant cible) 0.1896 [0.15 ; 0.23], R/R 1.549, perte reelle 21.854 % (gap inclus), EV -1.7245 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.72 %) : P(cible) 0.2 % x 33.86 % + P(rien) 80.8 % x 2.90 % ne couvrent pas P(stop) 19.0 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.61 ATR (stop 23.981 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 0.947, perte reelle 35.757 % (gap inclus), EV 1.1301 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.99 % > budget 12.00 %
   - 🟢 support a 8.6 ATR (stop 35.451 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.947, perte reelle 35.757 % (gap inclus), EV 1.2542 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.45 % > budget 12.00 %
   - ⚪ grid_snapped a 0.39 ATR (stop 2.657 %) — p(stop avant cible) 0.7866 [0.74 ; 0.83], R/R 6.298, perte reelle 5.376 % (gap inclus), EV -2.2907 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.787, borne haute 0.827 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.29 %) : P(cible) 0.2 % x 33.86 % + P(rien) 21.1 % x 8.83 % ne couvrent pas P(stop) 78.7 % x 5.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.789 %) — p(stop avant cible) 0.6166 [0.56 ; 0.67], R/R 3.534, perte reelle 9.581 % (gap inclus), EV -3.074 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.617, borne haute 0.667 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.07 %) : P(cible) 0.2 % x 33.86 % + P(rien) 38.1 % x 7.24 % ne couvrent pas P(stop) 61.7 % x 9.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.705 %) — p(stop avant cible) 0.4845 [0.43 ; 0.54], R/R 2.297, perte reelle 14.737 % (gap inclus), EV -4.1925 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.19 %) : P(cible) 0.2 % x 33.86 % + P(rien) 51.3 % x 5.59 % ne couvrent pas P(stop) 48.4 % x 14.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.663 %) — p(stop avant cible) 0.4086 [0.36 ; 0.46], R/R 1.822, perte reelle 18.578 % (gap inclus), EV -4.5994 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.60 %) : P(cible) 0.2 % x 33.86 % + P(rien) 58.9 % x 4.95 % ne couvrent pas P(stop) 40.9 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.28 ATR (stop 9.889 %) — p(stop avant cible) 0.2689 [0.22 ; 0.32], R/R 1.549, perte reelle 21.854 % (gap inclus), EV -3.106 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.11 %) : P(cible) 0.2 % x 33.86 % + P(rien) 72.9 % x 3.69 % ne couvrent pas P(stop) 26.9 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.536 %) — p(stop avant cible) 0.23 [0.19 ; 0.28], R/R 1.549, perte reelle 21.854 % (gap inclus), EV -2.4306 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.43 %) : P(cible) 0.2 % x 33.86 % + P(rien) 76.8 % x 3.28 % ne couvrent pas P(stop) 23.0 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 13.409 %) — p(stop avant cible) 0.0955 [0.07 ; 0.13], R/R 1.549, perte reelle 21.854 % (gap inclus), EV -0.0328 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.2 % x 33.86 % + P(rien) 90.2 % x 2.19 % ne couvrent pas P(stop) 9.6 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 15.325 %) — p(stop avant cible) 0.0523 [0.03 ; 0.08], R/R 1.304, perte reelle 25.963 % (gap inclus), EV 0.4316 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.34 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 17.241 %) — p(stop avant cible) 0.0342 [0.02 ; 0.06], R/R 0.947, perte reelle 35.757 % (gap inclus), EV 0.4168 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.26 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 19.156 %) — p(stop avant cible) 0.0239 [0.01 ; 0.04], R/R 0.947, perte reelle 35.757 % (gap inclus), EV 0.6934 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.17 % > budget 12.00 %
   - 🟢 grid_snapped a 5.61 ATR (stop 22.633 %) — p(stop avant cible) 0.007 [0.00 ; 0.02], R/R 0.947, perte reelle 35.757 % (gap inclus), EV 1.0946 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.64 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.903 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.947, perte reelle 35.757 % (gap inclus), EV 1.1894 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.91 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.819 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.947, perte reelle 35.757 % (gap inclus), EV 1.2096 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.83 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.734 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.947, perte reelle 35.757 % (gap inclus), EV 1.2253 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.74 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.65 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.947, perte reelle 35.757 % (gap inclus), EV 1.2371 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.65 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 140.2, ATR14 5.3714 (3.831 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.406 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.192 % | 139.9314 | 91.41 % | 93.97 % | 95.45 % | 96.13 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.383 % | 139.6629 | 83.71 % | 88.04 % | 90.5 % | 92.67 % | 94.62 % | 95.67 % |
| 0.15 ATR | 0.575 % | 139.3943 | 76.21 % | 82.41 % | 85.95 % | 88.7 % | 91.24 % | 93.26 % |
| 0.2 ATR | 0.766 % | 139.1257 | 70.29 % | 79.15 % | 83.09 % | 86.52 % | 89.44 % | 91.85 % |
| 0.25 ATR | 0.958 % | 138.8571 | 63.87 % | 74.9 % | 79.53 % | 83.45 % | 87.35 % | 90.44 % |
| 0.35 ATR | 1.341 % | 138.32 | 51.73 % | 65.02 % | 70.52 % | 76.02 % | 81.97 % | 86.32 % |
| 0.5 ATR | 1.916 % | 137.5143 | 36.23 % | 51.88 % | 59.64 % | 66.5 % | 74.4 % | 80.18 % |
| 0.75 ATR | 2.873 % | 136.1714 | 19.84 % | 36.07 % | 45.4 % | 54.51 % | 65.34 % | 73.24 % |
| 1.0 ATR | 3.831 % | 134.8286 | 11.15 % | 25.49 % | 34.42 % | 44.0 % | 56.67 % | 64.89 % |
| 1.25 ATR | 4.789 % | 133.4857 | 6.12 % | 17.39 % | 25.12 % | 35.68 % | 48.11 % | 57.24 % |
| 1.5 ATR | 5.747 % | 132.1429 | 2.76 % | 11.07 % | 17.8 % | 27.75 % | 40.94 % | 50.91 % |
| 2.0 ATR | 7.663 % | 129.4571 | 0.79 % | 3.95 % | 8.61 % | 16.15 % | 27.89 % | 39.64 % |
| 2.5 ATR | 9.578 % | 126.7714 | 0.3 % | 1.98 % | 3.96 % | 9.42 % | 19.02 % | 29.88 % |
| 3.0 ATR | 11.494 % | 124.0857 | 0.1 % | 0.79 % | 1.88 % | 4.86 % | 12.05 % | 22.03 % |
| 4.0 ATR | 15.325 % | 118.7143 | 0.1 % | 0.4 % | 1.09 % | 2.28 % | 6.27 % | 12.37 % |
| 6.0 ATR | 22.988 % | 107.9714 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.01 ATR | 1.17 ATR | 1.57 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.04 ATR | 1.25 ATR | 1.43 ATR | 1.92 ATR | 2.39 ATR |
| **5 s.** | 0.37 ATR | 0.86 ATR | 0.98 ATR | 1.33 ATR | 1.62 ATR | 1.83 ATR | 2.46 ATR | 2.98 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.80 ATR | 2.16 ATR | 2.44 ATR | 3.35 ATR | 4.62 ATR |
| **20 s.** | 0.69 ATR | 1.54 ATR | 1.76 ATR | 2.34 ATR | 2.81 ATR | 3.21 ATR | 4.67 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.415–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.609–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.873 %, prix 136.1721), p(touche) 36.07 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.759–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.831 %, prix 134.8289), p(touche) 34.42 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (87.5 % des re-echantillons)
- **5 seance(s)** : plage utile 0.976–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.831 %, prix 134.8289), p(touche) 44.0 % (en stress 99.01 %)  ✅ optimum identifie (91.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.358–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.747 %, prix 132.1427), p(touche) 40.94 % (en stress 100.0 %)  ✅ optimum identifie (94.0 % des re-echantillons)
- **20 seance(s)** : plage utile 1.762–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.663 %, prix 129.4565), p(touche) 39.64 % (en stress 99.0 %)  ✅ optimum identifie (88.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.06 | EV/share : €-0.659 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 19 % | T3 8 %
- Kelly (position) : f* 0.315 | ¼-Kelly 0.079 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 80.4 | side 14.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.087% → cible +1.57% / stop −8.0%, p_fill 47%, n_eff≈20.5) : P(cible|rempli) **48%** · **EV/risk +0.007** (×p_fill ; si rempli +0.11% du capital)
  - **swing** (entrée dip −4.599% → cible +3.511% / stop −4.016%, p_fill 38%, n_eff≈15.1) : P(cible|rempli) **56%** · **EV/risk +0.076** (×p_fill ; si rempli +0.81% du capital)
  - **deep** (entrée dip −7.103% → cible +4.966% / stop −6.186%, p_fill 21%, n_eff≈15.5) : P(cible|rempli) **73%** · **EV/risk +0.076** (×p_fill ; si rempli +2.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→59% · +2.0%→39% · +3.0%→20% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.81% (p90 6.15%) · excursion haute méd. +1.47% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.113% vs midi 0.87% vs clôture 1.056% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑1%/↓0% ; spike-down 58% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; neutre — autocorr -0.022)_ ; drift intra méd. -0.48% ; recovery-V 14%
- **σ réalisé intraday** 2.425% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 69% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 147.6975 (VA 146.6265–147.9355 ; dernier close 146.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 66% · **stop −3.12%** sous le fill (sous le bruit) · cible +1.27% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 33% (gap-down >1% 18% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.63% (p90 −1.67%) · haut méd +0.43% · range méd 1.16%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.21%) · haut méd +0.58% · range méd 1.56%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.28%) · haut méd +0.63% · range méd 1.92%
- Excursion ouverture 60min (n=160) : bas méd −1.0% (p90 −2.6%) · haut méd +0.74% · range méd 2.02%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 146.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 73% (116/159) · gap 25% · délai 0.4min · rebond 59% (65/116) (MFE +1.2%)
   - −1.0% : fill 30min 46% · séance 67% (107/159) · gap 18% · délai 6.9min · rebond 62% (62/107) (MFE +1.53%)
   - −1.5% : fill 30min 30% · séance 53% (89/159) · gap 14% · délai 10.1min · rebond 62% (53/89) (MFE +1.52%)
   - −2.0% : fill 30min 21% · séance 42% (74/159) · gap 10% · délai 33.3min · rebond 65% (50/74) (MFE +1.49%)
   - −3.0% : fill 30min 11% · séance 28% (52/159) · gap 4% · délai 208.4min · rebond 53% (33/52) (MFE +1.05%)
   - −4.0% : fill 30min 7% · séance 19% (38/159) · gap 2% · délai 129.6min · rebond 66% (27/38) (MFE +1.27%)
   - −5.0% : fill 30min 2% · séance 14% (25/159) · gap 0% · délai 398.5min · rebond 36% (13/25) (MFE +0.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.58%) → stop au-delà de −1.06% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.68%) → stop au-delà de −0.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.43% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=543 jambes) : jambe baissière méd −1.09% (p90 −2.59%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 98% (51/52) · rebond 58% (28/51)
      · −2.0% : fill 73% (39/52) · rebond 49% (23/39)
      · −3.0% : fill 60% (31/52) · rebond 40% (18/31)
      · −4.0% : fill 48% (26/52) · rebond 71% (20/26)
      · −5.0% : fill 36% (18/52) · rebond 39% (11/18)
   - **flat** (14 séances) :
      · −1.0% : fill 85% (12/14) · rebond 91% (10/12)
      · −2.0% : fill 51% (8/14) · rebond 88% (6/8)
      · −3.0% : fill 25% (5/14) · rebond 76% (3/5)
      · −4.0% : fill 14% (4/14) · rebond 52% (2/4)
      · −5.0% : fill 11% (3/14) · rebond 0% (0/3)
   - **gap-up** (93 séances) :
      · −1.0% : fill 48% (44/93) · rebond 56% (24/44)
      · −2.0% : fill 25% (27/93) · rebond 78% (21/27)
      · −3.0% : fill 12% (16/93) · rebond 74% (12/16)
      · −4.0% : fill 5% (8/93) · rebond 50% (5/8)
      · −5.0% : fill 3% (4/93) · rebond 40% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 75% si les 15 1res min sont vertes (75 cas) · 20% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:26** → P(séance verte=clôture>ouverture) 76% si début vert vs 21% si rouge (base 45% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **76%** · continue >prix actuel 56% ; creux résiduel méd -1.11% (q20 -2.16%) → **SL/trailing à −2.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.28% → **scale +1.46% / runner +2.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **21%** (continue à baisser 56%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.96%** (au-delà de la MAE q10 -3.96%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.05% .. +1.95%] · haut q95 +2.65% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.48% .. +2.32%] · haut q95 +2.69% · bas q05 -2.94%
   - 2h (n=160) : retour [-2.79% .. +2.64%] · haut q95 +2.9% · bas q05 -3.6%
   - 4h (n=160) : retour [-3.15% .. +2.61%] · haut q95 +3.68% · bas q05 -3.96%
   - 6h (n=160) : retour [-3.7% .. +3.22%] · haut q95 +4.1% · bas q05 -4.58%
   - session (n=160) : retour [-4.9% .. +3.93%] · haut q95 +5.13% · bas q05 -6.19%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **13%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


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

- **RSI** : 39.9  _(momentum baissier)_
- **ADX** : 14.9  _(pas de tendance nette)_
- **MACD** : hist -0.762  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 16.6%
- **ATR** : 5.37 (33.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.294  _(distribution)_
- **Vol ratio** : 2.53  _(volume au-dessus de la moyenne)_
- **Choppiness** : 51.5  _(transition)_
- **MA** : MA20 144.69 · MA50 149.12 · MA200 151.87  _(prix < MA20)_
- **Dist MA** : MA20 -3.1% · MA50 -6.0% · MA200 -7.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (823126 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
