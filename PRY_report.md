# PRY

**Generated** : 2026-08-26T21:48:52.644176+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €121.65  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €121.65 (+2.7% vs entrée) · entrée €118.49 · stop €116.13 · T1 €123.20 · R/R 2.0  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk -0.166 _(réel 5 s)_ (GBM -0.058) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.99% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €118.16–€118.82 (mid €118.49)
- Spot actuel : €121.65 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : €116.13 (stop swing_plan-based (-9.49%))
- Targets : T1 €123.20 · R/R 2.0 | T2 €123.31 · R/R 2.04 | T3 €123.42 · R/R 2.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €116.13


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.50 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.49 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1270).
   - exécution **0.508 pt plus bas** dans le cas TYPIQUE (médiane), 0.508 au p90, **0.508 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 9.49 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0004 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.846 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3845** [0.3144 ; 0.4584] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.3939** [0.3435 ; 0.4461] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3191** [0.2716 ; 0.3696] _(largeur 9.8 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.9 pt), swing (51.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.27 %** | CVaR **-5.76 %** | vol 2.64 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 1.76 % contre 2.94 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.48 % vs -7.48 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0292** (β de hausse 1.2232, asymétrie 0.8414) vs FTSEMIB — 561 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.43× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 108.0072 sur grid_snapped (2.68 ATR, 11.215 %) — p(stop avant cible) 0.1264 [0.09 ; 0.16], R/R 2.421, perte reelle 11.215 % (gap inclus), CVaR 11.215 %, EV 1.5005 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 24 des 24 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 55.6 % de la queue et il ne reste que -172.39 EUR a partager. Prix du risque -0.087 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.654 %) — p(stop avant cible) 0.419 [0.37 ; 0.47], R/R 3.434, perte reelle 7.909 % (gap inclus), EV -0.0407 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 1.1 % x 27.16 % + P(rien) 57.0 % x 5.24 % ne couvrent pas P(stop) 41.9 % x 7.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.68 ATR (stop 12.21 %) — p(stop avant cible) 0.0847 [0.06 ; 0.12], R/R 2.224, perte reelle 12.21 % (gap inclus), EV 1.6646 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.21 % > budget 12.00 %
   - 🟢 support a 3.85 ATR (stop 16.655 %) — p(stop avant cible) 0.0205 [0.01 ; 0.04], R/R 1.631, perte reelle 16.655 % (gap inclus), EV 1.8297 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.66 % > budget 12.00 %
   - 🔴 support a 10.7 ATR (stop 42.464 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.64, perte reelle 42.464 % (gap inclus), EV 1.8282 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.46 % > budget 12.00 %
      - ⚠ support DETECTE a 7.79 ATR du spot — compartiment >=6, mesure a 46.3 % de casse (IC clusterise [0.346 ; 0.571] sur 54 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 0.942 %) — p(stop avant cible) 0.8858 [0.85 ; 0.92], R/R 14.166, perte reelle 1.917 % (gap inclus), EV -0.6446 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 14.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.886, borne haute 0.916 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 0.7 % x 27.16 % + P(rien) 10.7 % x 8.04 % ne couvrent pas P(stop) 88.6 % x 1.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.885 %) — p(stop avant cible) 0.7754 [0.73 ; 0.82], R/R 8.91, perte reelle 3.048 % (gap inclus), EV -0.5628 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 8.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.775, borne haute 0.817 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 1.1 % x 27.16 % + P(rien) 21.4 % x 7.08 % ne couvrent pas P(stop) 77.5 % x 3.05 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.827 %) — p(stop avant cible) 0.6576 [0.61 ; 0.71], R/R 6.193, perte reelle 4.385 % (gap inclus), EV -0.3455 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.658, borne haute 0.706 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 1.1 % x 27.16 % + P(rien) 33.2 % x 6.79 % ne couvrent pas P(stop) 65.8 % x 4.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.77 %) — p(stop avant cible) 0.5763 [0.52 ; 0.63], R/R 4.849, perte reelle 5.601 % (gap inclus), EV -0.4118 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.576, borne haute 0.628 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 1.1 % x 27.16 % + P(rien) 41.3 % x 6.13 % ne couvrent pas P(stop) 57.6 % x 5.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.712 %) — p(stop avant cible) 0.5133 [0.46 ; 0.57], R/R 4.342, perte reelle 6.254 % (gap inclus), EV -0.2204 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.513, borne haute 0.566 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 1.1 % x 27.16 % + P(rien) 47.6 % x 5.68 % ne couvrent pas P(stop) 51.3 % x 6.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.597 %) — p(stop avant cible) 0.3676 [0.32 ; 0.42], R/R 3.163, perte reelle 8.587 % (gap inclus), EV 0.2868 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 7.539 %) — p(stop avant cible) 0.2809 [0.24 ; 0.33], R/R 2.716, perte reelle 9.998 % (gap inclus), EV 0.6421 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 8.482 %) — p(stop avant cible) 0.2467 [0.20 ; 0.29], R/R 2.716, perte reelle 9.998 % (gap inclus), EV 0.8602 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.68 ATR (stop 11.215 %) — p(stop avant cible) 0.1264 [0.09 ; 0.16], R/R 2.421, perte reelle 11.215 % (gap inclus), EV 1.5005 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 13.194 %) — p(stop avant cible) 0.0765 [0.05 ; 0.11], R/R 2.058, perte reelle 13.194 % (gap inclus), EV 1.6013 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.19 % > budget 12.00 %
   - 🟢 grid_snapped a 3.85 ATR (stop 15.66 %) — p(stop avant cible) 0.0211 [0.01 ; 0.04], R/R 1.734, perte reelle 15.66 % (gap inclus), EV 1.8454 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.66 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.848 %) — p(stop avant cible) 0.0124 [0.00 ; 0.03], R/R 1.441, perte reelle 18.848 % (gap inclus), EV 1.8286 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.85 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.733 %) — p(stop avant cible) 0.0104 [0.00 ; 0.03], R/R 1.31, perte reelle 20.733 % (gap inclus), EV 1.8117 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.73 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.618 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 1.201, perte reelle 22.618 % (gap inclus), EV 1.809 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.62 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.502 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 1.108, perte reelle 24.502 % (gap inclus), EV 1.8227 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.50 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.387 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 1.029, perte reelle 26.387 % (gap inclus), EV 1.8205 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.39 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.272 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.961, perte reelle 28.272 % (gap inclus), EV 1.8208 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.27 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.157 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.901, perte reelle 30.157 % (gap inclus), EV 1.8259 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.16 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 121.65, ATR14 4.5857 (3.77 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.343 ATR = 1.293 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.188 % | 121.4207 | 91.98 % | 94.05 % | 94.84 % | 95.63 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.377 % | 121.1914 | 85.45 % | 89.1 % | 91.37 % | 93.04 % | 95.2 % | 96.27 % |
| 0.15 ATR | 0.565 % | 120.9621 | 77.82 % | 84.34 % | 87.7 % | 90.56 % | 93.01 % | 94.25 % |
| 0.2 ATR | 0.754 % | 120.7329 | 69.6 % | 78.99 % | 82.84 % | 86.88 % | 90.71 % | 92.23 % |
| 0.25 ATR | 0.942 % | 120.5036 | 61.88 % | 74.23 % | 78.77 % | 83.1 % | 87.91 % | 90.31 % |
| 0.35 ATR | 1.319 % | 120.045 | 49.11 % | 63.83 % | 71.03 % | 76.74 % | 83.52 % | 87.49 % |
| 0.5 ATR | 1.885 % | 119.3571 | 34.95 % | 52.13 % | 60.12 % | 67.99 % | 76.12 % | 81.94 % |
| 0.75 ATR | 2.827 % | 118.2107 | 19.11 % | 34.29 % | 43.25 % | 54.37 % | 64.44 % | 73.36 % |
| 1.0 ATR | 3.77 % | 117.0643 | 10.0 % | 23.19 % | 31.55 % | 44.14 % | 55.24 % | 65.29 % |
| 1.25 ATR | 4.712 % | 115.9179 | 5.74 % | 15.86 % | 23.91 % | 34.29 % | 46.95 % | 57.52 % |
| 1.5 ATR | 5.654 % | 114.7714 | 2.48 % | 9.71 % | 15.97 % | 24.25 % | 36.56 % | 49.14 % |
| 2.0 ATR | 7.539 % | 112.4786 | 0.4 % | 3.96 % | 7.44 % | 13.82 % | 24.58 % | 38.24 % |
| 2.5 ATR | 9.424 % | 110.1857 | 0.0 % | 1.59 % | 3.37 % | 7.75 % | 16.08 % | 27.85 % |
| 3.0 ATR | 11.309 % | 107.8929 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 10.19 % | 20.08 % |
| 4.0 ATR | 15.078 % | 103.3071 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.9 % | 11.5 % |
| 6.0 ATR | 22.618 % | 94.1357 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.31 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.49 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 0.97 ATR | 1.21 ATR | 1.37 ATR | 1.85 ATR | 2.30 ATR |
| **5 s.** | 0.38 ATR | 0.86 ATR | 0.98 ATR | 1.28 ATR | 1.48 ATR | 1.70 ATR | 2.31 ATR | 2.88 ATR |
| **10 s.** | 0.52 ATR | 1.16 ATR | 1.30 ATR | 1.65 ATR | 1.98 ATR | 2.27 ATR | 3.04 ATR | 3.98 ATR |
| **20 s.** | 0.70 ATR | 1.47 ATR | 1.69 ATR | 2.25 ATR | 2.68 ATR | 3.01 ATR | 4.38 ATR | 5.65 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.6–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.827 %, prix 118.211), p(touche) 34.29 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.724–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.827 %, prix 118.211), p(touche) 43.25 % (en stress 94.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.979–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.77 %, prix 117.0638), p(touche) 44.14 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.297–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.654 %, prix 114.7719), p(touche) 36.56 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.69–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.539 %, prix 112.4788), p(touche) 38.24 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.058 | EV/share : €-0.137 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 14 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 35.6 | bear 11.1 | side 53.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.603% → cible +3.978% / stop −1.989%, p_fill 40%, n_eff≈18.4) : P(cible|rempli) **0%** · **EV/risk -0.166** (×p_fill ; si rempli -0.83% du capital)
  - **swing** (entrée dip −5.72% → cible +3.104% / stop −3.998%, p_fill 23%, n_eff≈10.4) : P(cible|rempli) **68%** · **EV/risk +0.056** (×p_fill ; si rempli +0.98% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=13, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→68% · +2.0%→41% · +3.0%→28% · +5.0%→8% · +8.0%→1%
- Range intraday médian 4.25% (p90 6.33%) · excursion haute méd. +1.5% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.383% vs midi 0.821% vs clôture 1.183% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; neutre — autocorr -0.001)_ ; drift intra méd. -0.683% ; recovery-V 23%
- **σ réalisé intraday** 2.619% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 59% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 125.1795 (VA 124.6845–125.8725 ; dernier close 123.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 29% · rebond 71% · **stop −2.82%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. 0.31% · baisse 37% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.04%) · haut méd +0.35% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −2.49%) · haut méd +0.56% · range méd 1.74%
- Excursion ouverture 30min (n=160) : bas méd −1.04% (p90 −2.92%) · haut méd +0.66% · range méd 1.99%
- Excursion ouverture 60min (n=160) : bas méd −1.21% (p90 −3.14%) · haut méd +0.86% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 124.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 71% (109/159) · gap 22% · délai 0.3min · rebond 55% (65/109) (MFE +1.43%)
   - −1.0% : fill 30min 47% · séance 60% (91/159) · gap 16% · délai 0.9min · rebond 60% (57/91) (MFE +1.26%)
   - −1.5% : fill 30min 33% · séance 49% (71/159) · gap 11% · délai 4.6min · rebond 56% (43/71) (MFE +1.15%)
   - −2.0% : fill 30min 22% · séance 42% (60/159) · gap 7% · délai 21.9min · rebond 61% (40/60) (MFE +1.18%)
   - −3.0% : fill 30min 8% · séance 29% (41/159) · gap 3% · délai 89.5min · rebond 71% (30/41) (MFE +1.69%)
   - −4.0% : fill 30min 2% · séance 19% (25/159) · gap 1% · délai 281.2min · rebond 59% (16/25) (MFE +1.57%)
   - −5.0% : fill 30min 1% · séance 12% (16/159) · gap 1% · délai 394.7min · rebond 56% (11/16) (MFE +1.26%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −1.75%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −2.02%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.85%) → stop au-delà de −1.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=495 jambes) : jambe baissière méd −1.07% (p90 −2.48%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 90% (39/43) · rebond 46% (21/39)
      · −2.0% : fill 80% (33/43) · rebond 61% (22/33)
      · −3.0% : fill 60% (26/43) · rebond 71% (19/26)
      · −4.0% : fill 40% (15/43) · rebond 50% (9/15)
      · −5.0% : fill 33% (12/43) · rebond 48% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 59% (16/27) · rebond 70% (12/16)
      · −2.0% : fill 29% (7/27) · rebond 100% (7/7)
      · −3.0% : fill 14% (4/27) · rebond 68% (3/4)
      · −4.0% : fill 8% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 45% (36/89) · rebond 70% (24/36)
      · −2.0% : fill 29% (20/89) · rebond 45% (11/20)
      · −3.0% : fill 19% (11/89) · rebond 72% (8/11)
      · −4.0% : fill 13% (8/89) · rebond 70% (6/8)
      · −5.0% : fill 4% (3/89) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 69% si les 15 1res min sont vertes (74 cas) · 30% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 80% si début vert vs 22% si rouge (base 47% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **80%** · continue >prix actuel 57% ; creux résiduel méd -0.93% (q20 -1.85%) → **SL/trailing à −1.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.42% / q75 +2.63% → **scale +1.42% / runner +2.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **22%** (continue à baisser 63%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.1%** (au-delà de la MAE q10 -4.1%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.83% .. +2.92%] · haut q95 +3.42% · bas q05 -3.39%
   - 60min (n=160) : retour [-3.29% .. +2.43%] · haut q95 +3.88% · bas q05 -3.54%
   - 2h (n=160) : retour [-3.57% .. +2.64%] · haut q95 +3.98% · bas q05 -4.41%
   - 4h (n=160) : retour [-3.5% .. +3.29%] · haut q95 +4.1% · bas q05 -4.59%
   - 6h (n=160) : retour [-3.71% .. +3.75%] · haut q95 +4.55% · bas q05 -4.85%
   - session (n=160) : retour [-4.33% .. +4.0%] · haut q95 +5.34% · bas q05 -6.25%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 45.8  _(neutre)_
- **ADX** : 27.4  _(tendance etablie)_
- **MACD** : hist -0.135  _(bearish_recent)_
- **BB** : %B 0.34 · largeur 12.7%
- **ATR** : 4.59 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.179  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 48.6  _(transition)_
- **MA** : MA20 124.26 · MA50 131.7 · MA200 113.74  _(prix < MA20)_
- **Dist MA** : MA20 -2.1% · MA50 -7.6% · MA200 +7.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (815129 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
