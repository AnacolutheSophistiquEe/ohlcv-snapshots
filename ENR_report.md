# ENR

**Generated** : 2026-08-27T21:40:38.157291+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €150.24  

> 🟡 **WAIT-FOR-DIP** — spot +9.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €150.24 (+9.1% vs entrée) · entrée €137.77 · stop €132.21 · T1 €141.01 · R/R 0.58  
> ↳ P(T1 av. stop) 86 % · EV/risk 0.433 · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €137.12–€138.42 (mid €137.77)
- Spot actuel : €150.24 (+9.1% au-dessus de la zone — repli à attendre)
- Stop : €132.21 (stop swing_plan-based (-12.0%))
- Targets : T1 €141.01 · R/R 0.58 | T2 €144.25 · R/R 1.17 | T3 €147.49 · R/R 1.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €132.21


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.0 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **4.17 pt plus bas** dans le cas TYPIQUE (médiane), 19.84 au p90, **23.757 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 12.0 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0232 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.307 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0101** [0.0019 ; 0.0342] _(largeur 3.2 pt, n_eff 173.1)_
   - swing : **0.387** [0.3368 ; 0.4391] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3287** [0.2808 ; 0.3795] _(largeur 9.9 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 11.5 observations effectives », dont la borne haute a 95 % vaut environ 26.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (51.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-4.63 %** | CVaR **-6.6 %** | vol 3.21 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 6.24 % contre 3.34 % aujourd'hui, rapport 1.87)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.74 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3631** (β de hausse 1.0908, asymétrie 1.2497) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.414× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 133.56 sur atr_grid (3.0 ATR, 11.102 %) — p(stop avant cible) 0.2011 [0.16 ; 0.25], R/R 1.138, perte reelle 21.854 % (gap inclus), CVaR 11.127 %, EV -1.3376 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 27 des 27 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 52.8 % de la queue et il ne reste que -406.12 EUR a partager. Prix du risque -0.191 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.95 ATR (stop 5.393 %) — p(stop avant cible) 0.5482 [0.50 ; 0.60], R/R 2.411, perte reelle 10.316 % (gap inclus), EV -2.4913 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.548, borne haute 0.600 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.49 %) : P(cible) 1.1 % x 24.88 % + P(rien) 44.0 % x 6.54 % ne couvrent pas P(stop) 54.8 % x 10.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 4.18 ATR (stop 17.347 %) — p(stop avant cible) 0.0343 [0.02 ; 0.06], R/R 0.696, perte reelle 35.757 % (gap inclus), EV 1.0253 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.36 % > budget 12.00 %
   - 🟢 support a 7.22 ATR (stop 28.614 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.696, perte reelle 35.757 % (gap inclus), EV 1.8215 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.62 % > budget 12.00 %
   - 🔴 support a 12.1 ATR (stop 46.661 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.533, perte reelle 46.661 % (gap inclus), EV 1.8644 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.66 % > budget 12.00 %
      - ⚠ support DETECTE a 10.43 ATR du spot — compartiment >=6, mesure a 46.0 % de casse (IC clusterise [0.340 ; 0.581] sur 50 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 0.925 %) — p(stop avant cible) 0.9217 [0.89 ; 0.95], R/R 10.939, perte reelle 2.274 % (gap inclus), EV -1.262 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 10.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.922, borne haute 0.947 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 0.3 % x 24.88 % + P(rien) 7.5 % x 10.04 % ne couvrent pas P(stop) 92.2 % x 2.27 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.85 %) — p(stop avant cible) 0.8405 [0.80 ; 0.88], R/R 6.453, perte reelle 3.855 % (gap inclus), EV -1.7143 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.841, borne haute 0.876 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.71 %) : P(cible) 0.5 % x 24.88 % + P(rien) 15.4 % x 9.03 % ne couvrent pas P(stop) 84.0 % x 3.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.95 ATR (stop 4.619 %) — p(stop avant cible) 0.5858 [0.53 ; 0.64], R/R 2.774, perte reelle 8.968 % (gap inclus), EV -2.2061 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.586, borne haute 0.637 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.21 %) : P(cible) 1.1 % x 24.88 % + P(rien) 40.4 % x 6.90 % ne couvrent pas P(stop) 58.6 % x 8.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.476 %) — p(stop avant cible) 0.4683 [0.42 ; 0.52], R/R 1.688, perte reelle 14.737 % (gap inclus), EV -3.6814 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.68 %) : P(cible) 1.1 % x 24.88 % + P(rien) 52.0 % x 5.64 % ne couvrent pas P(stop) 46.8 % x 14.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.401 %) — p(stop avant cible) 0.3978 [0.35 ; 0.45], R/R 1.339, perte reelle 18.578 % (gap inclus), EV -4.0944 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.09 %) : P(cible) 1.2 % x 24.88 % + P(rien) 59.0 % x 5.08 % ne couvrent pas P(stop) 39.8 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.327 %) — p(stop avant cible) 0.3462 [0.30 ; 0.40], R/R 1.339, perte reelle 18.578 % (gap inclus), EV -3.1258 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.13 %) : P(cible) 1.2 % x 24.88 % + P(rien) 64.2 % x 4.69 % ne couvrent pas P(stop) 34.6 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.252 %) — p(stop avant cible) 0.291 [0.24 ; 0.34], R/R 1.138, perte reelle 21.854 % (gap inclus), EV -3.0679 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.07 %) : P(cible) 1.2 % x 24.88 % + P(rien) 69.7 % x 4.30 % ne couvrent pas P(stop) 29.1 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.177 %) — p(stop avant cible) 0.2556 [0.21 ; 0.30], R/R 1.138, perte reelle 21.854 % (gap inclus), EV -2.3452 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.35 %) : P(cible) 1.2 % x 24.88 % + P(rien) 73.2 % x 4.02 % ne couvrent pas P(stop) 25.6 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 11.102 %) — p(stop avant cible) 0.2011 [0.16 ; 0.25], R/R 1.138, perte reelle 21.854 % (gap inclus), EV -1.3376 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.34 %) : P(cible) 1.2 % x 24.88 % + P(rien) 78.7 % x 3.51 % ne couvrent pas P(stop) 20.1 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.953 %) — p(stop avant cible) 0.1176 [0.09 ; 0.15], R/R 1.138, perte reelle 21.854 % (gap inclus), EV 0.2731 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.97 % > budget 12.00 %
   - ⚪ grid_snapped a 4.18 ATR (stop 16.573 %) — p(stop avant cible) 0.0373 [0.02 ; 0.06], R/R 0.696, perte reelle 35.757 % (gap inclus), EV 0.94 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.59 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.504 %) — p(stop avant cible) 0.0297 [0.02 ; 0.05], R/R 0.696, perte reelle 35.757 % (gap inclus), EV 1.1519 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.52 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.354 %) — p(stop avant cible) 0.0145 [0.01 ; 0.03], R/R 0.696, perte reelle 35.757 % (gap inclus), EV 1.5409 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.37 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.204 %) — p(stop avant cible) 0.0084 [0.00 ; 0.02], R/R 0.696, perte reelle 35.757 % (gap inclus), EV 1.648 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.21 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.055 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 0.696, perte reelle 35.757 % (gap inclus), EV 1.7511 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.06 % > budget 12.00 %
   - 🟢 grid_snapped a 7.22 ATR (stop 27.84 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.696, perte reelle 35.757 % (gap inclus), EV 1.8068 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.85 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.606 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.696, perte reelle 35.757 % (gap inclus), EV 1.8215 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.61 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 150.24, ATR14 5.56 (3.701 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.358 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.185 % | 149.962 | 91.32 % | 94.08 % | 95.55 % | 96.24 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.37 % | 149.684 | 83.73 % | 88.06 % | 90.61 % | 92.77 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.555 % | 149.406 | 76.33 % | 82.43 % | 86.07 % | 88.81 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.74 % | 149.128 | 70.22 % | 79.17 % | 83.2 % | 86.63 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.925 % | 148.85 | 63.91 % | 75.02 % | 79.74 % | 83.66 % | 87.36 % | 90.45 % |
| 0.35 ATR | 1.295 % | 148.294 | 51.78 % | 65.15 % | 70.95 % | 76.34 % | 81.99 % | 86.33 % |
| 0.5 ATR | 1.85 % | 147.46 | 36.39 % | 52.32 % | 60.08 % | 66.83 % | 74.43 % | 80.2 % |
| 0.75 ATR | 2.776 % | 146.07 | 20.02 % | 36.33 % | 45.65 % | 54.85 % | 65.37 % | 73.27 % |
| 1.0 ATR | 3.701 % | 144.68 | 11.24 % | 25.57 % | 34.58 % | 44.36 % | 56.72 % | 65.03 % |
| 1.25 ATR | 4.626 % | 143.29 | 6.21 % | 17.18 % | 25.1 % | 35.84 % | 48.16 % | 57.59 % |
| 1.5 ATR | 5.551 % | 141.9 | 2.86 % | 11.15 % | 17.89 % | 27.82 % | 41.09 % | 51.36 % |
| 2.0 ATR | 7.401 % | 139.12 | 0.79 % | 4.05 % | 8.5 % | 16.14 % | 28.26 % | 40.3 % |
| 2.5 ATR | 9.252 % | 136.34 | 0.3 % | 1.97 % | 4.15 % | 9.5 % | 19.8 % | 30.75 % |
| 3.0 ATR | 11.102 % | 133.56 | 0.1 % | 0.79 % | 1.88 % | 4.95 % | 12.94 % | 23.12 % |
| 4.0 ATR | 14.803 % | 128.0 | 0.1 % | 0.39 % | 1.09 % | 2.38 % | 6.77 % | 13.47 % |
| 6.0 ATR | 22.204 % | 116.88 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.29 % | 5.83 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.34 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.83 ATR | 1.02 ATR | 1.17 ATR | 1.58 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.77 ATR | 1.04 ATR | 1.25 ATR | 1.43 ATR | 1.92 ATR | 2.40 ATR |
| **5 s.** | 0.37 ATR | 0.87 ATR | 0.98 ATR | 1.34 ATR | 1.62 ATR | 1.83 ATR | 2.46 ATR | 3.00 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.19 ATR | 2.49 ATR | 3.48 ATR | 4.79 ATR |
| **20 s.** | 0.69 ATR | 1.56 ATR | 1.79 ATR | 2.38 ATR | 2.88 ATR | 3.32 ATR | 4.91 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.776 %, prix 146.0693), p(touche) 36.33 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.765–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.701 %, prix 144.6796), p(touche) 34.58 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (85.4 % des re-echantillons)
- **5 seance(s)** : plage utile 0.985–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.701 %, prix 144.6796), p(touche) 44.36 % (en stress 99.01 %)  ✅ optimum identifie (87.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.362–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.551 %, prix 141.9002), p(touche) 41.09 % (en stress 100.0 %)  ✅ optimum identifie (90.9 % des re-echantillons)
- **20 seance(s)** : plage utile 1.788–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.401 %, prix 139.1207), p(touche) 40.3 % (en stress 99.0 %)  ✅ optimum identifie (88.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.026 | EV/share : €0.143 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 62 % | T2 42 % | T3 32 %
- Kelly (position) : f* 0.011 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 6.9 | bear 7.4 | side 85.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 150.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.772% → cible +1.052% / stop −8.0%, p_fill 25%, n_eff≈11.5) : P(cible|rempli) **62%** · **EV/risk +0.004** (×p_fill ; si rempli +0.14% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→60% · +2.0%→40% · +3.0%→21% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.89% (p90 6.15%) · excursion haute méd. +1.33% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.118% vs midi 0.904% vs clôture 1.113% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 57% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr -0.013)_ ; drift intra méd. -0.513% ; recovery-V 12%
- **σ réalisé intraday** 2.549% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 70% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 154.3315 (VA 153.7155–154.7165 ; dernier close 153.12)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 59% · **stop −3.51%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 33% (gap-down >1% 18% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.56% (p90 −1.67%) · haut méd +0.45% · range méd 1.23%
- Excursion ouverture 15min (n=160) : bas méd −0.71% (p90 −2.21%) · haut méd +0.61% · range méd 1.56%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.28%) · haut méd +0.67% · range méd 1.98%
- Excursion ouverture 60min (n=160) : bas méd −0.95% (p90 −2.6%) · haut méd +0.78% · range méd 2.15%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 153.36 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 71% (114/159) · gap 26% · délai 0.6min · rebond 58% (63/114) (MFE +1.2%)
   - −1.0% : fill 30min 43% · séance 66% (105/159) · gap 18% · délai 8.3min · rebond 60% (59/105) (MFE +1.58%)
   - −1.5% : fill 30min 30% · séance 55% (89/159) · gap 15% · délai 13.2min · rebond 60% (51/89) (MFE +1.48%)
   - −2.0% : fill 30min 21% · séance 44% (75/159) · gap 10% · délai 52.3min · rebond 65% (52/75) (MFE +1.53%)
   - −3.0% : fill 30min 11% · séance 29% (51/159) · gap 4% · délai 208.7min · rebond 60% (34/51) (MFE +1.55%)
   - −4.0% : fill 30min 6% · séance 19% (37/159) · gap 2% · délai 131.9min · rebond 59% (26/37) (MFE +1.45%)
   - −5.0% : fill 30min 2% · séance 14% (24/159) · gap 0% · délai 389.0min · rebond 41% (13/24) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.54% (p90 −1.72%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.95%) → stop au-delà de −0.95% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.42% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=534 jambes) : jambe baissière méd −1.07% (p90 −2.63%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 97% (50/51) · rebond 55% (26/50)
      · −2.0% : fill 75% (39/51) · rebond 49% (24/39)
      · −3.0% : fill 58% (30/51) · rebond 50% (19/30)
      · −4.0% : fill 45% (25/51) · rebond 63% (19/25)
      · −5.0% : fill 36% (17/51) · rebond 47% (11/17)
   - **flat** (14 séances) :
      · −1.0% : fill 80% (12/14) · rebond 87% (10/12)
      · −2.0% : fill 51% (8/14) · rebond 84% (6/8)
      · −3.0% : fill 34% (5/14) · rebond 76% (3/5)
      · −4.0% : fill 20% (4/14) · rebond 52% (2/4)
      · −5.0% : fill 15% (3/14) · rebond 0% (0/3)
   - **gap-up** (94 séances) :
      · −1.0% : fill 49% (43/94) · rebond 56% (23/43)
      · −2.0% : fill 29% (28/94) · rebond 78% (22/28)
      · −3.0% : fill 14% (16/94) · rebond 74% (12/16)
      · −4.0% : fill 6% (8/94) · rebond 50% (5/8)
      · −5.0% : fill 3% (4/94) · rebond 40% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 76% si les 15 1res min sont vertes (76 cas) · 21% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 79% si début vert vs 24% si rouge (base 46% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 282min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **79%** · continue >prix actuel 52% ; creux résiduel méd -1.18% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.47% → **scale +1.55% / runner +2.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **24%** (continue à baisser 55%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.19%** (au-delà de la MAE q10 -4.19%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.12% .. +2.22%] · haut q95 +2.68% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.5% .. +2.34%] · haut q95 +2.72% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.85% .. +2.65%] · haut q95 +3.03% · bas q05 -3.76%
   - 4h (n=160) : retour [-3.36% .. +2.67%] · haut q95 +3.74% · bas q05 -4.27%
   - 6h (n=160) : retour [-3.79% .. +3.51%] · haut q95 +4.35% · bas q05 -4.77%
   - session (n=160) : retour [-5.04% .. +4.33%] · haut q95 +5.4% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **20 min** → P(reste trend-up à la clôture) **15%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


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

- **RSI** : 45.1  _(neutre)_
- **ADX** : 11.4  _(pas de tendance nette)_
- **MACD** : hist -0.555  _(bearish_recent)_
- **BB** : %B 0.3 · largeur 12.0%
- **ATR** : 5.56 (36.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.272  _(distribution)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 51.9  _(transition)_
- **MA** : MA20 154.02 · MA50 155.01 · MA200 149.33  _(prix < MA20)_
- **Dist MA** : MA20 -2.5% · MA50 -3.1% · MA200 +0.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (865396 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
