# ENR

**Generated** : 2026-08-26T00:05:20.075364+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €153.22  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €153.22 (+0.3% vs entrée) · entrée €152.76 · stop €140.54 · T1 €154.95 · R/R 0.18  
> ↳ P(T1 av. stop) 42 % _(réel 5 s)_ · EV/risk -0.07 _(réel 5 s)_ (GBM -0.066) · ¼-Kelly 0.085 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €152.32–€153.20 (mid €152.76)
- Spot actuel : €153.22 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €140.54 (stop swing_plan-based (-4.36%))
- Targets : T1 €154.95 · R/R 0.18 | T2 €157.14 · R/R 0.36 | T3 €159.33 · R/R 0.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €140.54


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.36 %)** : le gap seul le franchit 1.57 % des séances (20 fois sur 1274).
   - exécution **1.369 pt plus bas** dans le cas TYPIQUE (médiane), 9.53 au p90, **31.397 au pire**
   - perte réelle **8.071 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 4.36 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0583 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
- Chocs d'ouverture : p05 -2.307 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0103** [0.0019 ; 0.0345] _(largeur 3.3 pt, n_eff 173.1)_
   - swing : **0.4491** [0.3973 ; 0.5018] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4033** [0.3526 ; 0.4556] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 37.7 observations effectives », dont la borne haute a 95 % vaut environ 8.0 %.
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 33.2 observations effectives », dont la borne haute a 95 % vaut environ 9.0 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 37.6 observations effectives », dont la borne haute a 95 % vaut environ 8.0 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.5 pt), swing (30.6 pt), deep (31.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-4.63 %** | CVaR **-6.6 %** | vol 3.21 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 6.23 % contre 3.34 % aujourd'hui, rapport 1.86)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.74 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3638** (β de hausse 1.0874, asymétrie 1.2542) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.426× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 135.8843 sur atr_grid (3.0 ATR, 11.314 %) — p(stop avant cible) 0.2002 [0.16 ; 0.24], R/R 1.025, perte reelle 21.854 % (gap inclus), CVaR 11.339 %, EV -1.1864 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.03 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 25 des 25 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 50.7 % de la queue et il ne reste que -199.12 EUR a partager. Prix du risque -0.086 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.26 ATR (stop 3.308 %) — p(stop avant cible) 0.6917 [0.64 ; 0.74], R/R 3.214, perte reelle 6.97 % (gap inclus), EV -2.2051 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.692, borne haute 0.739 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.26 ATR du spot — compartiment <1, mesure a 47.7 % de casse (IC clusterise [0.443 ; 0.512] sur 1016 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.21 %) : P(cible) 2.4 % x 22.40 % + P(rien) 28.4 % x 7.32 % ne couvrent pas P(stop) 69.2 % x 6.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.657 %) — p(stop avant cible) 0.5199 [0.47 ; 0.57], R/R 2.083, perte reelle 10.753 % (gap inclus), EV -2.3111 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.520, borne haute 0.572 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.31 %) : P(cible) 2.7 % x 22.40 % + P(rien) 45.3 % x 5.89 % ne couvrent pas P(stop) 52.0 % x 10.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 3.65 ATR (stop 16.097 %) — p(stop avant cible) 0.0408 [0.02 ; 0.07], R/R 0.863, perte reelle 25.963 % (gap inclus), EV 1.379 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.11 % > budget 12.00 %
   - 🟢 support a 7.47 ATR (stop 30.497 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.627, perte reelle 35.757 % (gap inclus), EV 1.9592 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.50 % > budget 12.00 %
   - 🔴 support a 12.16 ATR (stop 48.194 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.465, perte reelle 48.194 % (gap inclus), EV 1.9871 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.46 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.19 % > budget 12.00 %
      - ⚠ support DETECTE a 10.55 ATR du spot — compartiment >=6, mesure a 46.5 % de casse (IC clusterise [0.333 ; 0.591] sur 43 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🔴 grid_snapped a 0.26 ATR (stop 2.097 %) — p(stop avant cible) 0.8174 [0.77 ; 0.86], R/R 5.436, perte reelle 4.121 % (gap inclus), EV -1.647 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.817, borne haute 0.855 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.65 %) : P(cible) 2.2 % x 22.40 % + P(rien) 16.1 % x 7.66 % ne couvrent pas P(stop) 81.7 % x 4.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.829 %) — p(stop avant cible) 0.7607 [0.71 ; 0.80], R/R 3.782, perte reelle 5.924 % (gap inclus), EV -2.3134 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.761, borne haute 0.803 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.31 %) : P(cible) 2.4 % x 22.40 % + P(rien) 21.5 % x 7.70 % ne couvrent pas P(stop) 76.1 % x 5.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.714 %) — p(stop avant cible) 0.5799 [0.53 ; 0.63], R/R 2.42, perte reelle 9.258 % (gap inclus), EV -2.2388 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.580, borne haute 0.631 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.24 %) : P(cible) 2.6 % x 22.40 % + P(rien) 39.4 % x 6.44 % ne couvrent pas P(stop) 58.0 % x 9.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.6 %) — p(stop avant cible) 0.4489 [0.40 ; 0.50], R/R 1.52, perte reelle 14.737 % (gap inclus), EV -3.3553 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.36 %) : P(cible) 2.7 % x 22.40 % + P(rien) 52.4 % x 5.05 % ne couvrent pas P(stop) 44.9 % x 14.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.543 %) — p(stop avant cible) 0.3825 [0.33 ; 0.43], R/R 1.206, perte reelle 18.578 % (gap inclus), EV -3.7034 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.21 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.70 %) : P(cible) 2.8 % x 22.40 % + P(rien) 58.9 % x 4.71 % ne couvrent pas P(stop) 38.2 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.486 %) — p(stop avant cible) 0.3231 [0.28 ; 0.37], R/R 1.206, perte reelle 18.578 % (gap inclus), EV -2.6796 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.21 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.68 %) : P(cible) 2.8 % x 22.40 % + P(rien) 64.9 % x 4.15 % ne couvrent pas P(stop) 32.3 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.429 %) — p(stop avant cible) 0.2806 [0.24 ; 0.33], R/R 1.025, perte reelle 21.854 % (gap inclus), EV -2.7792 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.78 %) : P(cible) 2.8 % x 22.40 % + P(rien) 69.1 % x 3.94 % ne couvrent pas P(stop) 28.1 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.371 %) — p(stop avant cible) 0.2524 [0.21 ; 0.30], R/R 1.025, perte reelle 21.854 % (gap inclus), EV -2.1779 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.18 %) : P(cible) 2.8 % x 22.40 % + P(rien) 72.0 % x 3.76 % ne couvrent pas P(stop) 25.2 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 11.314 %) — p(stop avant cible) 0.2002 [0.16 ; 0.24], R/R 1.025, perte reelle 21.854 % (gap inclus), EV -1.1864 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 2.8 % x 22.40 % + P(rien) 77.2 % x 3.32 % ne couvrent pas P(stop) 20.0 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.65 ATR (stop 14.887 %) — p(stop avant cible) 0.0772 [0.05 ; 0.11], R/R 0.863, perte reelle 25.963 % (gap inclus), EV 0.7216 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.90 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.971 %) — p(stop avant cible) 0.0377 [0.02 ; 0.06], R/R 0.627, perte reelle 35.757 % (gap inclus), EV 1.0553 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.99 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.857 %) — p(stop avant cible) 0.027 [0.01 ; 0.05], R/R 0.627, perte reelle 35.757 % (gap inclus), EV 1.3448 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.743 %) — p(stop avant cible) 0.0092 [0.00 ; 0.02], R/R 0.627, perte reelle 35.757 % (gap inclus), EV 1.7527 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.75 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.629 %) — p(stop avant cible) 0.0077 [0.00 ; 0.02], R/R 0.627, perte reelle 35.757 % (gap inclus), EV 1.8024 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.64 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.514 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.627, perte reelle 35.757 % (gap inclus), EV 1.8713 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.52 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.4 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.627, perte reelle 35.757 % (gap inclus), EV 1.9037 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.41 % > budget 12.00 %
   - 🟢 grid_snapped a 7.47 ATR (stop 29.287 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.627, perte reelle 35.757 % (gap inclus), EV 1.945 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.29 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 153.22, ATR14 5.7786 (3.771 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.368 ATR = 1.388 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.189 % | 152.9311 | 91.22 % | 94.08 % | 95.55 % | 96.24 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.377 % | 152.6421 | 83.63 % | 88.06 % | 90.61 % | 92.77 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.566 % | 152.3532 | 76.23 % | 82.43 % | 86.07 % | 88.81 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.754 % | 152.0643 | 70.22 % | 79.17 % | 83.2 % | 86.63 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.943 % | 151.7754 | 64.0 % | 75.12 % | 79.74 % | 83.66 % | 87.36 % | 90.55 % |
| 0.35 ATR | 1.32 % | 151.1975 | 51.87 % | 65.25 % | 70.95 % | 76.34 % | 81.99 % | 86.43 % |
| 0.5 ATR | 1.886 % | 150.3307 | 36.49 % | 52.42 % | 60.08 % | 66.83 % | 74.43 % | 80.3 % |
| 0.75 ATR | 2.829 % | 148.8861 | 20.12 % | 36.53 % | 45.75 % | 54.85 % | 65.37 % | 73.47 % |
| 1.0 ATR | 3.771 % | 147.4414 | 11.34 % | 25.77 % | 34.68 % | 44.36 % | 56.72 % | 65.23 % |
| 1.25 ATR | 4.714 % | 145.9968 | 6.31 % | 17.28 % | 25.3 % | 35.84 % | 48.16 % | 57.79 % |
| 1.5 ATR | 5.657 % | 144.5521 | 2.96 % | 11.25 % | 18.08 % | 27.92 % | 41.09 % | 51.56 % |
| 2.0 ATR | 7.543 % | 141.6629 | 0.79 % | 4.15 % | 8.7 % | 16.34 % | 28.36 % | 40.5 % |
| 2.5 ATR | 9.429 % | 138.7736 | 0.3 % | 2.07 % | 4.35 % | 9.7 % | 20.0 % | 30.95 % |
| 3.0 ATR | 11.314 % | 135.8843 | 0.1 % | 0.89 % | 1.98 % | 5.15 % | 13.13 % | 23.32 % |
| 4.0 ATR | 15.086 % | 130.1057 | 0.1 % | 0.39 % | 1.09 % | 2.38 % | 6.97 % | 13.67 % |
| 6.0 ATR | 22.629 % | 118.5486 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.29 % | 6.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.68 ATR | 0.75 ATR | 1.07 ATR | 1.35 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.62 ATR | 0.83 ATR | 1.02 ATR | 1.17 ATR | 1.59 ATR | 1.94 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.77 ATR | 1.04 ATR | 1.26 ATR | 1.43 ATR | 1.93 ATR | 2.42 ATR |
| **5 s.** | 0.37 ATR | 0.87 ATR | 0.98 ATR | 1.34 ATR | 1.63 ATR | 1.84 ATR | 2.48 ATR | 3.05 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.82 ATR | 2.20 ATR | 2.50 ATR | 3.51 ATR | 4.84 ATR |
| **20 s.** | 0.69 ATR | 1.57 ATR | 1.80 ATR | 2.39 ATR | 2.89 ATR | 3.34 ATR | 4.96 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.417–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.617–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.829 %, prix 148.8854), p(touche) 36.53 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.767–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.771 %, prix 147.4421), p(touche) 34.68 % (en stress 91.18 %)  ✅ optimum identifie (84.8 % des re-echantillons)
- **5 seance(s)** : plage utile 0.985–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.771 %, prix 147.4421), p(touche) 44.36 % (en stress 99.01 %)  ✅ optimum identifie (88.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.362–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.657 %, prix 144.5523), p(touche) 41.09 % (en stress 100.0 %)  ✅ optimum identifie (90.1 % des re-echantillons)
- **20 seance(s)** : plage utile 1.797–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.543 %, prix 141.6626), p(touche) 40.5 % (en stress 99.0 %)  ✅ optimum identifie (86.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.066 | EV/share : €-0.805 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 24 % | T3 9 %
- Kelly (position) : f* 0.341 | ¼-Kelly 0.085 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.9 | bear 85.7 | side 6.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 153.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.304% → cible +1.434% / stop −8.0%, p_fill 92%, n_eff≈37.7) : P(cible|rempli) **42%** · **EV/risk -0.070** (×p_fill ; si rempli -0.61% du capital)
  - **swing** (entrée dip −0.589% → cible +3.206% / stop −3.794%, p_fill 79%, n_eff≈33.2) : P(cible|rempli) **32%** · **EV/risk -0.359** (×p_fill ; si rempli -1.73% du capital)
  - **deep** (entrée dip −0.863% → cible +4.535% / stop −5.706%, p_fill 91%, n_eff≈37.6) : P(cible|rempli) **48%** · **EV/risk -0.154** (×p_fill ; si rempli -0.97% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 53.4  _(neutre)_
- **ADX** : 12.5  _(pas de tendance nette)_
- **MACD** : hist -0.322  _(bearish_recent)_
- **BB** : %B 0.51 · largeur 16.8%
- **ATR** : 5.78 (37.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.172  _(distribution)_
- **Vol ratio** : 0.49  _(volume atone)_
- **Choppiness** : 53.4  _(transition)_
- **MA** : MA20 153.04 · MA50 155.61 · MA200 148.87  _(prix > MA20)_
- **Dist MA** : MA20 +0.1% · MA50 -1.5% · MA200 +2.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (828341 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
