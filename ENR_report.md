# ENR

**Generated** : 2026-09-09T00:09:07.379155+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €148.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €148.80 (+3.7% vs entrée) · entrée €143.49 · stop €132.01 · T1 €145.18 · R/R 0.15  
> ↳ P(T1 av. stop) 96 % · EV/risk 0.158 · ¼-Kelly 0.101 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €143.15–€143.83 (mid €143.49)
- Spot actuel : €148.80 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : €132.01 (stop swing_plan-based (-11.07%))
- Targets : T1 €145.18 · R/R 0.15 | T2 €146.87 · R/R 0.29 | T3 €148.56 · R/R 0.44
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €132.01


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (11.07 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **5.1 pt plus bas** dans le cas TYPIQUE (médiane), 20.77 au p90, **24.687 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 11.07 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0254 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.307 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0092** [0.0016 ; 0.0327] _(largeur 3.1 pt, n_eff 173.1)_
   - swing : **0.4521** [0.4002 ; 0.5048] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4048** [0.354 ; 0.4572] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 11.0 observations effectives », dont la borne haute a 95 % vaut environ 27.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (51.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.63 %** | CVaR **-6.59 %** | vol 3.23 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.54 % contre 3.25 % aujourd'hui, rapport 1.71)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.68 % vs -9.74 % si l'on extrapolait par √5 _(rapport 0.891 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3526** (β de hausse 1.0928, asymétrie 1.2377) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.421× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 132.03 sur atr_grid (3.5 ATR, 11.27 %) — p(stop avant cible) 0.1975 [0.16 ; 0.24], R/R 1.201, perte reelle 21.854 % (gap inclus), CVaR 11.295 %, EV -1.631 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.83 %) — p(stop avant cible) 0.5982 [0.55 ; 0.65], R/R 2.739, perte reelle 9.581 % (gap inclus), EV -2.7869 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.598, borne haute 0.649 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.79 %) : P(cible) 0.9 % x 26.24 % + P(rien) 39.3 % x 6.90 % ne couvrent pas P(stop) 59.8 % x 9.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.21 ATR (stop 9.177 %) — p(stop avant cible) 0.3083 [0.26 ; 0.36], R/R 1.201, perte reelle 21.854 % (gap inclus), EV -3.6567 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.66 %) : P(cible) 1.0 % x 26.24 % + P(rien) 68.2 % x 4.14 % ne couvrent pas P(stop) 30.8 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 4.53 ATR (stop 16.648 %) — p(stop avant cible) 0.0356 [0.02 ; 0.06], R/R 0.734, perte reelle 35.757 % (gap inclus), EV 0.6007 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.66 % > budget 12.00 %
   - 🟢 support a 8.08 ATR (stop 28.075 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.734, perte reelle 35.757 % (gap inclus), EV 1.4234 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.08 % > budget 12.00 %
   - 🔴 support a 12.29 ATR (stop 41.627 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.63, perte reelle 41.627 % (gap inclus), EV 1.4737 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.63 % > budget 12.00 %
      - ⚠ support DETECTE a 11.21 ATR du spot — compartiment >=6, mesure a 46.2 % de casse (IC clusterise [0.333 ; 0.612] sur 52 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 0.805 %) — p(stop avant cible) 0.9372 [0.91 ; 0.96], R/R 12.572, perte reelle 2.087 % (gap inclus), EV -1.2744 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 12.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.937, borne haute 0.959 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 0.2 % x 26.24 % + P(rien) 6.1 % x 10.36 % ne couvrent pas P(stop) 93.7 % x 2.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.61 %) — p(stop avant cible) 0.8688 [0.83 ; 0.90], R/R 7.52, perte reelle 3.489 % (gap inclus), EV -1.7118 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 7.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.869, borne haute 0.901 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.71 %) : P(cible) 0.5 % x 26.24 % + P(rien) 12.7 % x 9.47 % ne couvrent pas P(stop) 86.9 % x 3.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.415 %) — p(stop avant cible) 0.8007 [0.76 ; 0.84], R/R 5.598, perte reelle 4.687 % (gap inclus), EV -1.9127 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.801, borne haute 0.840 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 0.8 % x 26.24 % + P(rien) 19.2 % x 8.57 % ne couvrent pas P(stop) 80.1 % x 4.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.22 %) — p(stop avant cible) 0.7175 [0.67 ; 0.76], R/R 3.907, perte reelle 6.716 % (gap inclus), EV -2.4037 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.718, borne haute 0.763 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.40 %) : P(cible) 0.8 % x 26.24 % + P(rien) 27.5 % x 8.06 % ne couvrent pas P(stop) 71.8 % x 6.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.025 %) — p(stop avant cible) 0.6457 [0.59 ; 0.69], R/R 3.471, perte reelle 7.559 % (gap inclus), EV -2.1399 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.646, borne haute 0.695 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 0.8 % x 26.24 % + P(rien) 34.6 % x 7.31 % ne couvrent pas P(stop) 64.6 % x 7.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.635 %) — p(stop avant cible) 0.5471 [0.49 ; 0.60], R/R 2.44, perte reelle 10.753 % (gap inclus), EV -2.8146 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.547, borne haute 0.599 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.81 %) : P(cible) 1.0 % x 26.24 % + P(rien) 44.3 % x 6.35 % ne couvrent pas P(stop) 54.7 % x 10.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.21 ATR (stop 8.089 %) — p(stop avant cible) 0.3809 [0.33 ; 0.43], R/R 1.412, perte reelle 18.578 % (gap inclus), EV -3.9157 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.92 %) : P(cible) 1.0 % x 26.24 % + P(rien) 60.9 % x 4.76 % ne couvrent pas P(stop) 38.1 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 9.66 %) — p(stop avant cible) 0.2835 [0.24 ; 0.33], R/R 1.201, perte reelle 21.854 % (gap inclus), EV -3.2269 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.23 %) : P(cible) 1.0 % x 26.24 % + P(rien) 70.7 % x 3.83 % ne couvrent pas P(stop) 28.3 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 11.27 %) — p(stop avant cible) 0.1975 [0.16 ; 0.24], R/R 1.201, perte reelle 21.854 % (gap inclus), EV -1.631 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.63 %) : P(cible) 1.0 % x 26.24 % + P(rien) 79.3 % x 3.06 % ne couvrent pas P(stop) 19.8 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 12.88 %) — p(stop avant cible) 0.1172 [0.09 ; 0.15], R/R 1.201, perte reelle 21.854 % (gap inclus), EV -0.084 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 1.0 % x 26.24 % + P(rien) 87.3 % x 2.54 % ne couvrent pas P(stop) 11.7 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 4.53 ATR (stop 15.559 %) — p(stop avant cible) 0.0536 [0.03 ; 0.08], R/R 1.011, perte reelle 25.963 % (gap inclus), EV 0.6351 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.58 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.1 %) — p(stop avant cible) 0.0385 [0.02 ; 0.06], R/R 1.011, perte reelle 25.963 % (gap inclus), EV 0.9067 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.12 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.71 %) — p(stop avant cible) 0.0318 [0.02 ; 0.05], R/R 0.734, perte reelle 35.757 % (gap inclus), EV 0.7068 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.72 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 19.32 %) — p(stop avant cible) 0.0221 [0.01 ; 0.04], R/R 0.734, perte reelle 35.757 % (gap inclus), EV 0.9703 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.33 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 20.93 %) — p(stop avant cible) 0.0087 [0.00 ; 0.02], R/R 0.734, perte reelle 35.757 % (gap inclus), EV 1.2589 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.94 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 22.54 %) — p(stop avant cible) 0.0073 [0.00 ; 0.02], R/R 0.734, perte reelle 35.757 % (gap inclus), EV 1.3054 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.55 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.15 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 0.734, perte reelle 35.757 % (gap inclus), EV 1.3714 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.16 % > budget 12.00 %
   - 🟢 grid_snapped a 8.08 ATR (stop 26.987 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.734, perte reelle 35.757 % (gap inclus), EV 1.4234 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.99 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 148.8, ATR14 4.7914 (3.22 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.182 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.161 % | 148.5604 | 91.32 % | 93.98 % | 95.45 % | 96.24 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.322 % | 148.3209 | 83.73 % | 87.96 % | 90.51 % | 92.77 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.483 % | 148.0813 | 76.33 % | 82.33 % | 85.97 % | 88.81 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.644 % | 147.8417 | 70.32 % | 79.07 % | 83.1 % | 86.63 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.805 % | 147.6021 | 63.91 % | 74.83 % | 79.55 % | 83.66 % | 87.36 % | 90.45 % |
| 0.35 ATR | 1.127 % | 147.123 | 51.78 % | 64.96 % | 70.65 % | 76.24 % | 81.99 % | 86.33 % |
| 0.5 ATR | 1.61 % | 146.4043 | 36.29 % | 52.02 % | 59.78 % | 66.73 % | 74.43 % | 80.2 % |
| 0.75 ATR | 2.415 % | 145.2064 | 19.92 % | 36.13 % | 45.36 % | 54.75 % | 65.37 % | 73.27 % |
| 1.0 ATR | 3.22 % | 144.0086 | 11.14 % | 25.57 % | 34.39 % | 44.26 % | 56.72 % | 64.92 % |
| 1.25 ATR | 4.025 % | 142.8107 | 6.11 % | 17.28 % | 25.1 % | 35.84 % | 48.16 % | 57.29 % |
| 1.5 ATR | 4.83 % | 141.6129 | 2.86 % | 11.06 % | 17.79 % | 27.72 % | 41.09 % | 50.95 % |
| 2.0 ATR | 6.44 % | 139.2171 | 0.79 % | 4.05 % | 8.7 % | 16.14 % | 28.06 % | 39.7 % |
| 2.5 ATR | 8.05 % | 136.8214 | 0.3 % | 1.97 % | 4.15 % | 9.41 % | 19.3 % | 29.95 % |
| 3.0 ATR | 9.66 % | 134.4257 | 0.1 % | 0.79 % | 1.88 % | 4.85 % | 12.34 % | 22.31 % |
| 4.0 ATR | 12.88 % | 129.6343 | 0.1 % | 0.39 % | 1.09 % | 2.38 % | 6.47 % | 12.66 % |
| 6.0 ATR | 19.32 % | 120.0514 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.29 % | 5.43 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.02 ATR | 1.17 ATR | 1.58 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.04 ATR | 1.25 ATR | 1.42 ATR | 1.93 ATR | 2.41 ATR |
| **5 s.** | 0.37 ATR | 0.86 ATR | 0.98 ATR | 1.34 ATR | 1.62 ATR | 1.83 ATR | 2.46 ATR | 2.98 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.17 ATR | 2.46 ATR | 3.40 ATR | 4.70 ATR |
| **20 s.** | 0.69 ATR | 1.54 ATR | 1.76 ATR | 2.34 ATR | 2.82 ATR | 3.24 ATR | 4.74 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.61–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.415 %, prix 145.2065), p(touche) 36.13 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.758–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.22 %, prix 144.0086), p(touche) 34.39 % (en stress 91.18 %)  ✅ optimum identifie (85.5 % des re-echantillons)
- **5 seance(s)** : plage utile 0.982–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.22 %, prix 144.0086), p(touche) 44.26 % (en stress 99.01 %)  ✅ optimum identifie (89.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.362–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.83 %, prix 141.613), p(touche) 41.09 % (en stress 100.0 %)  ✅ optimum identifie (92.2 % des re-echantillons)
- **20 seance(s)** : plage utile 1.764–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.44 %, prix 139.2173), p(touche) 39.7 % (en stress 99.0 %)  ✅ optimum identifie (88.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.06 | EV/share : €-0.691 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 32 % | T3 16 %
- Kelly (position) : f* 0.405 | ¼-Kelly 0.101 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 82.0 | bear 6.6 | side 11.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.565% → cible +1.178% / stop −8.0%, p_fill 15%, n_eff≈11.0) : P(cible|rempli) **63%** · **EV/risk +0.003** (×p_fill ; si rempli +0.15% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=2))
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.9  _(momentum baissier)_
- **ADX** : 10.9  _(pas de tendance nette)_
- **MACD** : hist -0.2  _(pas de croisement recent)_
- **BB** : %B 0.4 · largeur 17.1%
- **ATR** : 4.79 (27.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.236  _(distribution)_
- **Vol ratio** : 0.34  _(volume atone)_
- **Choppiness** : 50.7  _(transition)_
- **MA** : MA20 151.39 · MA50 152.28 · MA200 150.83  _(prix < MA20)_
- **Dist MA** : MA20 -1.7% · MA50 -2.3% · MA200 -1.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (773397 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
