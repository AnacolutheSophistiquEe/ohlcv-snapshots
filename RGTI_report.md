# RGTI

**Generated** : 2026-08-31T00:29:26.130308+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.59  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $15.59 (+0.5% vs entrée) · entrée $15.52 · stop $15.19 · T1 $15.99 · R/R 1.42  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.149 _(réel 5 s)_ (GBM 0.17) · ¼-Kelly 0.027 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.1% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.45–$15.59 (mid $15.52)
- Spot actuel : $15.59 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $15.19 (stop swing_plan-based (-7.8%))
- Targets : T1 $15.99 · R/R 1.42 | T2 $16.46 · R/R 2.85 | T3 $16.93 · R/R 4.27
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.19


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.29 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.8 %)** : le gap seul le franchit 1.276 % des séances (16 fois sur 1254).
   - exécution **3.084 pt plus bas** dans le cas TYPIQUE (médiane), 8.486 au p90, **23.413 au pire**
   - perte réelle **12.728 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 7.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0629 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.083 % | p01 -8.97 % | pire -31.213 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5314** [0.4571 ; 0.6047] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4637** [0.4116 ; 0.5164] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5284** [0.4757 ; 0.5806] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 37.9 observations effectives », dont la borne haute a 95 % vaut environ 7.9 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.6 pt), swing (31.6 pt), deep (30.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.77 %** | CVaR **-10.77 %** | vol 6.85 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 14.86 % contre 6.51 % aujourd'hui, rapport 2.28)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.75 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8195** (β de hausse 1.9954, asymétrie 0.9119) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.622× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 13.69 sur atr_grid (1.75 ATR, 12.187 %) — p(stop avant cible) 0.5433 [0.49 ; 0.60], R/R 2.016, perte reelle 17.61 % (gap inclus), CVaR 12.213 %, EV -3.0412 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1001 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.543, borne haute 0.595 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.21 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.13 ATR (stop 3.21 %) — p(stop avant cible) 0.8488 [0.81 ; 0.88], R/R 5.83, perte reelle 6.089 % (gap inclus), EV -1.6601 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.849, borne haute 0.884 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 7.1 % x 35.50 % + P(rien) 8.0 % x 12.35 % ne couvrent pas P(stop) 84.9 % x 6.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 0.74 ATR (stop 7.462 %) — p(stop avant cible) 0.7015 [0.65 ; 0.75], R/R 2.977, perte reelle 11.924 % (gap inclus), EV -2.6767 % — **REFUSE**
      - refuse : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.702, borne haute 0.748 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.08 ATR du spot — compartiment <1, mesure a 45.9 % de casse (IC clusterise [0.428 ; 0.490] sur 1144 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 10.4 % x 35.50 % + P(rien) 19.4 % x 10.20 % ne couvrent pas P(stop) 70.2 % x 11.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.446 %) — p(stop avant cible) 0.6314 [0.58 ; 0.68], R/R 2.366, perte reelle 15.002 % (gap inclus), EV -3.2322 % — **REFUSE**
      - refuse : cible atteinte seulement 11.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.631, borne haute 0.681 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.23 %) : P(cible) 11.2 % x 35.50 % + P(rien) 25.7 % x 8.81 % ne couvrent pas P(stop) 63.1 % x 15.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.82 ATR (stop 21.926 %) — p(stop avant cible) 0.1803 [0.14 ; 0.22], R/R 1.137, perte reelle 31.213 % (gap inclus), EV -0.3667 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 14.5 % x 35.50 % + P(rien) 67.5 % x 0.18 % ne couvrent pas P(stop) 18.0 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 8.705 %) — p(stop avant cible) 0.6646 [0.61 ; 0.71], R/R 2.654, perte reelle 13.376 % (gap inclus), EV -2.8528 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.665, borne haute 0.713 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.85 %) : P(cible) 10.7 % x 35.50 % + P(rien) 22.9 % x 9.83 % ne couvrent pas P(stop) 66.5 % x 13.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 12.187 %) — p(stop avant cible) 0.5433 [0.49 ; 0.60], R/R 2.016, perte reelle 17.61 % (gap inclus), EV -3.0412 % — **REFUSE**
      - refuse : cible atteinte seulement 11.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.543, borne haute 0.595 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.04 %) : P(cible) 11.7 % x 35.50 % + P(rien) 34.0 % x 7.01 % ne couvrent pas P(stop) 54.3 % x 17.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 13.928 %) — p(stop avant cible) 0.4584 [0.41 ; 0.51], R/R 1.811, perte reelle 19.597 % (gap inclus), EV -2.2459 % — **REFUSE**
      - refuse : cible atteinte seulement 12.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 12.3 % x 35.50 % + P(rien) 41.8 % x 5.64 % ne couvrent pas P(stop) 45.8 % x 19.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 15.669 %) — p(stop avant cible) 0.3716 [0.32 ; 0.42], R/R 1.445, perte reelle 24.565 % (gap inclus), EV -2.6783 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 12.9 % x 35.50 % + P(rien) 49.9 % x 3.72 % ne couvrent pas P(stop) 37.2 % x 24.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 17.41 %) — p(stop avant cible) 0.3157 [0.27 ; 0.37], R/R 1.445, perte reelle 24.565 % (gap inclus), EV -1.4111 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.41 %) : P(cible) 13.8 % x 35.50 % + P(rien) 54.7 % x 2.66 % ne couvrent pas P(stop) 31.6 % x 24.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 24.375 %) — p(stop avant cible) 0.1339 [0.10 ; 0.17], R/R 1.137, perte reelle 31.213 % (gap inclus), EV 0.4089 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.38 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 27.857 %) — p(stop avant cible) 0.0811 [0.06 ; 0.11], R/R 1.137, perte reelle 31.213 % (gap inclus), EV 1.2946 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.86 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 31.339 %) — p(stop avant cible) 0.0499 [0.03 ; 0.08], R/R 1.133, perte reelle 31.339 % (gap inclus), EV 1.5817 % — **REFUSE**
      - refuse : cible atteinte seulement 15.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.34 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 34.821 %) — p(stop avant cible) 0.0302 [0.02 ; 0.05], R/R 1.019, perte reelle 34.821 % (gap inclus), EV 1.6694 % — **REFUSE**
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.82 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 38.303 %) — p(stop avant cible) 0.0175 [0.01 ; 0.04], R/R 0.927, perte reelle 38.303 % (gap inclus), EV 1.6862 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.30 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 41.785 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 0.85, perte reelle 41.785 % (gap inclus), EV 1.7619 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.78 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 45.267 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 0.784, perte reelle 45.267 % (gap inclus), EV 1.7553 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.27 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 48.749 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.728, perte reelle 48.749 % (gap inclus), EV 1.7483 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.75 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 52.231 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.68, perte reelle 52.231 % (gap inclus), EV 1.732 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 52.23 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 55.713 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.637, perte reelle 55.713 % (gap inclus), EV 1.7538 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.71 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.59, ATR14 1.0857 (6.964 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.41 ATR = 2.855 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.348 % | 15.5357 | 92.25 % | 94.56 % | 95.67 % | 97.07 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.696 % | 15.4814 | 86.52 % | 91.24 % | 92.44 % | 94.95 % | 95.84 % | 97.44 % |
| 0.15 ATR | 1.045 % | 15.4271 | 81.09 % | 87.51 % | 89.11 % | 92.02 % | 93.91 % | 96.1 % |
| 0.2 ATR | 1.393 % | 15.3729 | 74.65 % | 82.98 % | 85.69 % | 88.89 % | 91.47 % | 94.56 % |
| 0.25 ATR | 1.741 % | 15.3186 | 68.61 % | 78.75 % | 81.85 % | 85.86 % | 88.83 % | 92.62 % |
| 0.35 ATR | 2.437 % | 15.21 | 56.04 % | 68.58 % | 74.09 % | 79.7 % | 84.47 % | 89.74 % |
| 0.5 ATR | 3.482 % | 15.0471 | 41.05 % | 56.8 % | 64.82 % | 71.92 % | 79.29 % | 85.64 % |
| 0.75 ATR | 5.223 % | 14.7757 | 21.73 % | 38.87 % | 49.4 % | 59.19 % | 70.96 % | 79.38 % |
| 1.0 ATR | 6.964 % | 14.5043 | 9.56 % | 23.77 % | 33.47 % | 46.26 % | 61.93 % | 73.23 % |
| 1.25 ATR | 8.705 % | 14.2329 | 4.02 % | 14.5 % | 23.49 % | 36.77 % | 52.89 % | 65.33 % |
| 1.5 ATR | 10.446 % | 13.9614 | 1.71 % | 7.15 % | 13.71 % | 25.35 % | 43.15 % | 57.13 % |
| 2.0 ATR | 13.928 % | 13.4186 | 0.4 % | 1.71 % | 3.93 % | 10.71 % | 25.38 % | 40.82 % |
| 2.5 ATR | 17.41 % | 12.8757 | 0.1 % | 0.4 % | 1.21 % | 4.44 % | 14.31 % | 28.41 % |
| 3.0 ATR | 20.893 % | 12.3329 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.13 % |
| 4.0 ATR | 27.857 % | 11.2471 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.92 % |
| 6.0 ATR | 41.785 % | 9.0757 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.29 ATR | 0.59 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.21 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.03 ATR | 1.33 ATR | 1.51 ATR | 1.68 ATR | 2.06 ATR | 2.46 ATR |
| **10 s.** | 0.63 ATR | 1.32 ATR | 1.45 ATR | 1.79 ATR | 2.02 ATR | 2.24 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.93 ATR | 1.72 ATR | 1.87 ATR | 2.31 ATR | 2.65 ATR | 2.87 ATR | 3.58 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.46–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.482 %, prix 15.0472), p(touche) 41.05 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (68.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.665–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.223 %, prix 14.7757), p(touche) 38.87 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.819–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.964 %, prix 14.5043), p(touche) 33.47 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.033–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.705 %, prix 14.2329), p(touche) 36.77 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.453–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.446 %, prix 13.9615), p(touche) 43.15 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.872–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.928 %, prix 13.4186), p(touche) 40.82 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.17 | EV/share : $0.055 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.107 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 19.9 | side 75.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.451% → cible +3.034% / stop −2.099%, p_fill 85%, n_eff≈35.2) : P(cible|rempli) **28%** · **EV/risk -0.149** (×p_fill ; si rempli -0.37% du capital)
  - **swing** (entrée dip −0.836% → cible +6.784% / stop −7.023%, p_fill 84%, n_eff≈35.8) : P(cible|rempli) **47%** · **EV/risk -0.073** (×p_fill ; si rempli -0.61% du capital)
  - **deep** (entrée dip −1.193% → cible +9.594% / stop −10.573%, p_fill 93%, n_eff≈37.9) : P(cible|rempli) **40%** · **EV/risk -0.274** (×p_fill ; si rempli -3.10% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→71% · +3.0%→54% · +5.0%→40% · +8.0%→14%
- Range intraday médian 7.62% (p90 13.36%) · excursion haute méd. +3.52% / basse méd. −2.8%
- Profil de vol intra : ouverture 5.444% vs midi 1.581% vs clôture 1.79% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 74% · range 26% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.142 ; mean-reverting — autocorr -0.035)_ ; drift intra méd. -0.147% ; recovery-V 33%
- **σ réalisé intraday** 4.285% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 48% / whipsaw 4%
- POC intraday (dernière séance, temps-au-prix) : 15.5205 (VA 15.4515–15.8195 ; dernier close 15.605)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 45% · rebond 73% · **stop −6.0%** sous le fill (sous le bruit) · cible +2.19% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.49% · baisse 59% (gap-down >1% 42% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.21% (p90 −2.88%) · haut méd +1.16% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.47% (p90 −3.82%) · haut méd +1.7% · range méd 3.63%
- Excursion ouverture 30min (n=160) : bas méd −1.78% (p90 −4.54%) · haut méd +2.09% · range méd 4.51%
- Excursion ouverture 60min (n=160) : bas méd −2.35% (p90 −5.72%) · haut méd +2.24% · range méd 5.3%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.59 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (133/159) · gap 49% · délai 0.0min · rebond 62% (84/133) (MFE +2.11%)
   - −1.0% : fill 30min 67% · séance 74% (125/159) · gap 42% · délai 0.0min · rebond 64% (79/125) (MFE +1.68%)
   - −1.5% : fill 30min 61% · séance 69% (119/159) · gap 34% · délai 0.0min · rebond 65% (77/119) (MFE +2.08%)
   - −2.0% : fill 30min 54% · séance 62% (110/159) · gap 26% · délai 0.0min · rebond 65% (73/110) (MFE +1.85%)
   - −3.0% : fill 30min 46% · séance 57% (99/159) · gap 10% · délai 1.2min · rebond 67% (71/99) (MFE +2.09%)
   - −4.0% : fill 30min 35% · séance 45% (78/159) · gap 5% · délai 6.5min · rebond 73% (56/78) (MFE +2.19%)
   - −5.0% : fill 30min 18% · séance 38% (68/159) · gap 2% · délai 31.4min · rebond 55% (46/68) (MFE +1.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −2.4%) → stop au-delà de −1.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −2.81%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −2.92%) → stop au-delà de −2.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1155 jambes) : jambe baissière méd −1.28% (p90 −3.1%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 96% (83/85) · rebond 58% (48/83)
      · −2.0% : fill 86% (78/85) · rebond 62% (50/78)
      · −3.0% : fill 83% (74/85) · rebond 60% (50/74)
      · −4.0% : fill 70% (60/85) · rebond 71% (42/60)
      · −5.0% : fill 60% (53/85) · rebond 51% (35/53)
   - **flat** (15 séances) :
      · −1.0% : fill 96% (14/15) · rebond 94% (12/14)
      · −2.0% : fill 74% (12/15) · rebond 85% (10/12)
      · −3.0% : fill 50% (7/15) · rebond 90% (5/7)
      · −4.0% : fill 34% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 21% (5/15) · rebond 87% (3/5)
   - **gap-up** (59 séances) :
      · −1.0% : fill 37% (28/59) · rebond 67% (19/28)
      · −2.0% : fill 25% (20/59) · rebond 64% (13/20)
      · −3.0% : fill 21% (18/59) · rebond 90% (16/18)
      · −4.0% : fill 13% (12/59) · rebond 84% (10/12)
      · −5.0% : fill 11% (10/59) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 72% si les 15 1res min sont vertes (80 cas) · 28% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 94% si début vert vs 9% si rouge (base 51% · écart 85 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **94%** · continue >prix actuel 54% ; creux résiduel méd -1.86% (q20 -2.9%) → **SL/trailing à −2.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.26% / q75 +4.34% → **scale +2.26% / runner +4.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **9%** (continue à baisser 70%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.62%** (au-delà de la MAE q10 -5.62%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.02% .. +4.88%] · haut q95 +6.44% · bas q05 -6.02%
   - 60min (n=160) : retour [-5.42% .. +6.2%] · haut q95 +6.62% · bas q05 -6.69%
   - 2h (n=160) : retour [-6.34% .. +6.73%] · haut q95 +9.07% · bas q05 -7.4%
   - 4h (n=160) : retour [-6.67% .. +7.89%] · haut q95 +9.19% · bas q05 -7.81%
   - 6h (n=160) : retour [-7.31% .. +8.64%] · haut q95 +10.13% · bas q05 -8.51%
   - session (n=160) : retour [-7.13% .. +9.11%] · haut q95 +10.34% · bas q05 -8.62%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 14% vs absente 5% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.66% / p90 2.45%) · ~4.39 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 15.0 min, n=47)
   - −1.0% → **83%** (reprise méd 35.0 min, n=29)
   - −1.5% → **84%** (reprise méd 94.96 min, n=17)
   - −2.0% → **86%** (reprise méd 54.27 min, n=9)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.45%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.3% (q75 +9.62% / q95 +9.99%), MFE méd +9.65% / q90 +11.14%
   - Échelle scale-out : +9.65% (33%) / +10.43% (33%) / +11.14% (34%)
- **DÉSARMER** : repli > **−2.45%** depuis le plus-haut = décay → P(retournement) **23%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.14% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.16%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 39.9  _(momentum baissier)_
- **ADX** : 13.5  _(pas de tendance nette)_
- **MACD** : hist -0.189  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 23.5%
- **ATR** : 1.09 (6.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.002  _(neutre)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 51.3  _(transition)_
- **MA** : MA20 17.25 · MA50 16.95 · MA200 19.59  _(prix < MA20)_
- **Dist MA** : MA20 -9.6% · MA50 -8.0% · MA200 -20.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (900173 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
