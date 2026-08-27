# EVT

**Generated** : 2026-08-27T21:39:06.023038+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.38  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €3.38 (+0.3% vs entrée) · entrée €3.37 · stop €3.32 · T1 €3.43 · R/R 1.2  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.313 _(réel 5 s)_ (GBM -0.013) · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.36–€3.38 (mid €3.37)
- Spot actuel : €3.38 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €3.32 (stop swing_plan-based (-4.91%))
- Targets : T1 €3.43 · R/R 1.2 | T2 €3.48 · R/R 2.2 | T3 €3.54 · R/R 3.4
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.32


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.91 %)** : le gap seul le franchit 0.863 % des séances (11 fois sur 1274).
   - exécution **2.202 pt plus bas** dans le cas TYPIQUE (médiane), 16.701 au p90, **27.503 au pire**
   - perte réelle **11.717 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 4.91 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0588 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4999** [0.4259 ; 0.5739] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4052** [0.3544 ; 0.4576] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3934** [0.343 ; 0.4456] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.0 pt), swing (31.7 pt), deep (31.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-5.11 %** | CVaR **-9.26 %** | vol 3.8 %/j
   - _fenêtre arrêtée : rupture de regime a 1260 seances en arriere (volatilite 2.13 % contre 3.91 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1105** (β de hausse 0.9425, asymétrie 1.1783) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 3.0491 sur atr_grid (2.25 ATR, 9.897 %) — p(stop avant cible) 0.3254 [0.28 ; 0.38], R/R 2.691, perte reelle 18.001 % (gap inclus), CVaR 9.929 %, EV -3.2895 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.03 ATR (stop 2.042 %) — p(stop avant cible) 0.8249 [0.78 ; 0.86], R/R 11.3, perte reelle 4.286 % (gap inclus), EV -1.8612 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.825, borne haute 0.862 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.03 ATR du spot — compartiment <1, mesure a 47.6 % de casse (IC clusterise [0.446 ; 0.507] sur 1212 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.86 %) : P(cible) 0.0 % x 48.43 % + P(rien) 17.5 % x 9.48 % ne couvrent pas P(stop) 82.5 % x 4.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.05 ATR (stop 6.528 %) — p(stop avant cible) 0.4897 [0.44 ; 0.54], R/R 3.259, perte reelle 14.861 % (gap inclus), EV -4.2336 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.23 %) : P(cible) 0.0 % x 48.43 % + P(rien) 51.0 % x 5.93 % ne couvrent pas P(stop) 49.0 % x 14.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.4 ATR (stop 8.07 %) — p(stop avant cible) 0.395 [0.34 ; 0.45], R/R 2.691, perte reelle 18.001 % (gap inclus), EV -4.3092 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.31 %) : P(cible) 0.0 % x 48.43 % + P(rien) 60.5 % x 4.60 % ne couvrent pas P(stop) 39.5 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 0.03 ATR (stop 1.438 %) — p(stop avant cible) 0.866 [0.83 ; 0.90], R/R 14.54, perte reelle 3.331 % (gap inclus), EV -1.4946 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 14.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.866, borne haute 0.899 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.49 %) : P(cible) 0.0 % x 48.43 % + P(rien) 13.4 % x 10.26 % ne couvrent pas P(stop) 86.6 % x 3.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.299 %) — p(stop avant cible) 0.6996 [0.65 ; 0.75], R/R 6.547, perte reelle 7.398 % (gap inclus), EV -2.7653 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.700, borne haute 0.746 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.77 %) : P(cible) 0.0 % x 48.43 % + P(rien) 30.0 % x 7.97 % ne couvrent pas P(stop) 70.0 % x 7.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.05 ATR (stop 5.924 %) — p(stop avant cible) 0.5269 [0.47 ; 0.58], R/R 4.133, perte reelle 11.717 % (gap inclus), EV -3.0874 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.527, borne haute 0.579 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.09 %) : P(cible) 0.0 % x 48.43 % + P(rien) 47.3 % x 6.49 % ne couvrent pas P(stop) 52.7 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.4 ATR (stop 7.466 %) — p(stop avant cible) 0.4222 [0.37 ; 0.47], R/R 2.691, perte reelle 18.001 % (gap inclus), EV -4.6769 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.68 %) : P(cible) 0.0 % x 48.43 % + P(rien) 57.7 % x 5.03 % ne couvrent pas P(stop) 42.2 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.798 %) — p(stop avant cible) 0.3667 [0.32 ; 0.42], R/R 2.691, perte reelle 18.001 % (gap inclus), EV -3.8918 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.89 %) : P(cible) 0.0 % x 48.43 % + P(rien) 63.3 % x 4.25 % ne couvrent pas P(stop) 36.7 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.897 %) — p(stop avant cible) 0.3254 [0.28 ; 0.38], R/R 2.691, perte reelle 18.001 % (gap inclus), EV -3.2895 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.29 %) : P(cible) 0.0 % x 48.43 % + P(rien) 67.4 % x 3.78 % ne couvrent pas P(stop) 32.5 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.997 %) — p(stop avant cible) 0.2915 [0.25 ; 0.34], R/R 2.431, perte reelle 19.926 % (gap inclus), EV -3.4396 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.44 %) : P(cible) 0.0 % x 48.43 % + P(rien) 70.8 % x 3.32 % ne couvrent pas P(stop) 29.1 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 12.097 %) — p(stop avant cible) 0.2485 [0.21 ; 0.30], R/R 2.141, perte reelle 22.616 % (gap inclus), EV -3.5208 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 0.0 % x 48.43 % + P(rien) 75.1 % x 2.77 % ne couvrent pas P(stop) 24.9 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 13.197 %) — p(stop avant cible) 0.2028 [0.16 ; 0.25], R/R 2.141, perte reelle 22.616 % (gap inclus), EV -2.8555 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.86 %) : P(cible) 0.0 % x 48.43 % + P(rien) 79.7 % x 2.15 % ne couvrent pas P(stop) 20.3 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 15.396 %) — p(stop avant cible) 0.1531 [0.12 ; 0.19], R/R 1.793, perte reelle 27.012 % (gap inclus), EV -2.8113 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.81 %) : P(cible) 0.0 % x 48.43 % + P(rien) 84.7 % x 1.54 % ne couvrent pas P(stop) 15.3 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 17.595 %) — p(stop avant cible) 0.1248 [0.09 ; 0.16], R/R 1.793, perte reelle 27.012 % (gap inclus), EV -2.2803 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.28 %) : P(cible) 0.0 % x 48.43 % + P(rien) 87.5 % x 1.22 % ne couvrent pas P(stop) 12.5 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 19.795 %) — p(stop avant cible) 0.1107 [0.08 ; 0.15], R/R 1.793, perte reelle 27.012 % (gap inclus), EV -2.0792 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 0.0 % x 48.43 % + P(rien) 88.9 % x 1.00 % ne couvrent pas P(stop) 11.1 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 21.994 %) — p(stop avant cible) 0.1025 [0.07 ; 0.14], R/R 1.494, perte reelle 32.413 % (gap inclus), EV -2.5265 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.53 %) : P(cible) 0.0 % x 48.43 % + P(rien) 89.7 % x 0.87 % ne couvrent pas P(stop) 10.2 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 24.194 %) — p(stop avant cible) 0.0891 [0.06 ; 0.12], R/R 1.494, perte reelle 32.413 % (gap inclus), EV -2.3413 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.34 %) : P(cible) 0.0 % x 48.43 % + P(rien) 91.0 % x 0.58 % ne couvrent pas P(stop) 8.9 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 26.393 %) — p(stop avant cible) 0.0777 [0.05 ; 0.11], R/R 1.494, perte reelle 32.413 % (gap inclus), EV -2.2287 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.23 %) : P(cible) 0.0 % x 48.43 % + P(rien) 92.2 % x 0.29 % ne couvrent pas P(stop) 7.8 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 28.593 %) — p(stop avant cible) 0.0599 [0.04 ; 0.09], R/R 1.494, perte reelle 32.413 % (gap inclus), EV -2.0944 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.09 %) : P(cible) 0.0 % x 48.43 % + P(rien) 94.0 % x -0.18 % ne couvrent pas P(stop) 6.0 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 30.792 %) — p(stop avant cible) 0.049 [0.03 ; 0.08], R/R 1.494, perte reelle 32.413 % (gap inclus), EV -2.0147 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.01 %) : P(cible) 0.0 % x 48.43 % + P(rien) 95.1 % x -0.47 % ne couvrent pas P(stop) 4.9 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 32.991 %) — p(stop avant cible) 0.049 [0.03 ; 0.08], R/R 1.468, perte reelle 32.991 % (gap inclus), EV -2.043 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.04 %) : P(cible) 0.0 % x 48.43 % + P(rien) 95.1 % x -0.47 % ne couvrent pas P(stop) 4.9 % x 32.99 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 35.191 %) — p(stop avant cible) 0.0436 [0.03 ; 0.07], R/R 1.376, perte reelle 35.191 % (gap inclus), EV -2.116 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 0.0 % x 48.43 % + P(rien) 95.6 % x -0.63 % ne couvrent pas P(stop) 4.4 % x 35.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.384, ATR14 0.1489 (4.399 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.365 ATR = 1.606 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.22 % | 3.3766 | 88.86 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.44 % | 3.3691 | 81.46 % | 87.07 % | 89.82 % | 92.77 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.66 % | 3.3617 | 75.25 % | 83.22 % | 86.76 % | 90.0 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.88 % | 3.3542 | 68.84 % | 79.07 % | 83.4 % | 87.13 % | 91.94 % | 94.77 % |
| 0.25 ATR | 1.1 % | 3.3468 | 63.12 % | 75.81 % | 80.34 % | 84.75 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.54 % | 3.3319 | 51.58 % | 67.52 % | 73.81 % | 79.6 % | 86.17 % | 91.56 % |
| 0.5 ATR | 2.199 % | 3.3096 | 35.31 % | 54.79 % | 62.75 % | 70.59 % | 80.1 % | 88.24 % |
| 0.75 ATR | 3.299 % | 3.2724 | 19.03 % | 37.61 % | 47.53 % | 59.21 % | 71.64 % | 81.91 % |
| 1.0 ATR | 4.399 % | 3.2351 | 10.16 % | 24.58 % | 35.67 % | 47.43 % | 62.19 % | 75.38 % |
| 1.25 ATR | 5.499 % | 3.1979 | 4.83 % | 17.37 % | 27.37 % | 39.41 % | 55.52 % | 70.15 % |
| 1.5 ATR | 6.598 % | 3.1607 | 3.06 % | 11.35 % | 19.76 % | 31.39 % | 48.56 % | 64.92 % |
| 2.0 ATR | 8.798 % | 3.0863 | 1.48 % | 5.23 % | 9.98 % | 19.41 % | 35.22 % | 52.76 % |
| 2.5 ATR | 10.997 % | 3.0119 | 0.49 % | 2.76 % | 5.83 % | 12.48 % | 28.06 % | 44.92 % |
| 3.0 ATR | 13.197 % | 2.9374 | 0.39 % | 1.68 % | 3.75 % | 9.01 % | 21.09 % | 38.09 % |
| 4.0 ATR | 17.595 % | 2.7886 | 0.2 % | 0.89 % | 1.98 % | 4.55 % | 11.94 % | 25.23 % |
| 6.0 ATR | 26.393 % | 2.4909 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.57 % | 14.27 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.73 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.64 ATR | 0.84 ATR | 0.99 ATR | 1.16 ATR | 1.61 ATR | 2.05 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.08 ATR | 1.33 ATR | 1.49 ATR | 2.00 ATR | 2.70 ATR |
| **5 s.** | 0.43 ATR | 0.94 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.86 ATR | 3.90 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.63 ATR | 2.15 ATR | 2.72 ATR | 3.12 ATR | 4.61 ATR | hors grille |
| **20 s.** | 1.02 ATR | 2.18 ATR | 2.50 ATR | 3.40 ATR | 4.04 ATR | 4.95 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.411–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (61.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.642–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.299 %, prix 3.2724), p(touche) 37.61 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (66.8 % des re-echantillons)
- **3 seance(s)** : plage utile 0.803–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.399 %, prix 3.2351), p(touche) 35.67 % (en stress 96.08 %)  ✅ optimum identifie (63.2 % des re-echantillons)
- **5 seance(s)** : plage utile 1.076–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.499 %, prix 3.1979), p(touche) 39.41 % (en stress 95.05 %)  ✅ optimum identifie (71.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.633–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.798 %, prix 3.0863), p(touche) 35.22 % (en stress 98.02 %)  ✅ optimum identifie (71.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.495–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.997 %, prix 3.0119), p(touche) 44.92 % (en stress 98.0 %)  ✅ optimum identifie (85.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : €-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 18 % | T3 6 %
- Kelly (position) : f* 0.037 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.6 | bear 6.5 | side 79.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.315% → cible +1.622% / stop −1.5%, p_fill 89%, n_eff≈36.2) : P(cible|rempli) **25%** · **EV/risk -0.313** (×p_fill ; si rempli -0.53% du capital)
  - **swing** (entrée dip −0.51% → cible +3.618% / stop −4.423%, p_fill 87%, n_eff≈35.7) : P(cible|rempli) **49%** · **EV/risk -0.044** (×p_fill ; si rempli -0.23% du capital)
  - **deep** (entrée dip −0.661% → cible +5.12% / stop −6.643%, p_fill 84%, n_eff≈35.5) : P(cible|rempli) **59%** · **EV/risk +0.052** (×p_fill ; si rempli +0.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→69% · +2.0%→44% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.8% (p90 6.57%) · excursion haute méd. +1.74% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.692% vs midi 1.22% vs clôture 1.193% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.09 ; mean-reverting — autocorr -0.134)_ ; drift intra méd. -0.771% ; recovery-V 27%
- **σ réalisé intraday** 3.137% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 72% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 3.3443 (VA 3.3227–3.3569 ; dernier close 3.348)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−0.5%** sous le close veille · fill 79% · rebond 76% · **stop −3.3%** sous le fill (sous le bruit) · cible +1.62% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 39% (gap-down >1% 11% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.34%) · haut méd +0.49% · range méd 1.47%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.83%) · haut méd +0.75% · range méd 1.78%
- Excursion ouverture 30min (n=160) : bas méd −1.05% (p90 −2.83%) · haut méd +0.81% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.26%) · haut méd +0.95% · range méd 2.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.356 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 79% (131/159) · gap 24% · délai 0.4min · rebond 76% (91/131) (MFE +1.62%)
   - −1.0% : fill 30min 40% · séance 66% (112/159) · gap 11% · délai 6.4min · rebond 70% (74/112) (MFE +1.56%)
   - −1.5% : fill 30min 32% · séance 56% (96/159) · gap 6% · délai 19.3min · rebond 67% (61/96) (MFE +1.57%)
   - −2.0% : fill 30min 20% · séance 45% (80/159) · gap 6% · délai 36.8min · rebond 55% (47/80) (MFE +1.43%)
   - −3.0% : fill 30min 11% · séance 25% (51/159) · gap 4% · délai 50.1min · rebond 64% (36/51) (MFE +1.45%)
   - −4.0% : fill 30min 5% · séance 13% (28/159) · gap 1% · délai 46.7min · rebond 54% (18/28) (MFE +1.15%)
   - −5.0% : fill 30min 4% · séance 8% (16/159) · gap 1% · délai 35.6min · rebond 59% (11/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −2.49%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.36% (p90 −1.72%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.89%) → stop au-delà de −1.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=813 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 86% (49/56) · rebond 73% (32/49)
      · −2.0% : fill 61% (38/56) · rebond 59% (23/38)
      · −3.0% : fill 42% (27/56) · rebond 68% (19/27)
      · −4.0% : fill 26% (20/56) · rebond 43% (13/20)
      · −5.0% : fill 18% (13/56) · rebond 42% (8/13)
   - **flat** (35 séances) :
      · −1.0% : fill 80% (27/35) · rebond 67% (17/27)
      · −2.0% : fill 60% (20/35) · rebond 42% (9/20)
      · −3.0% : fill 36% (13/35) · rebond 74% (10/13)
      · −4.0% : fill 8% (3/35) · rebond 28% (1/3)
      · −5.0% : fill 2% (1/35) · rebond 100% (1/1)
   - **gap-up** (68 séances) :
      · −1.0% : fill 49% (36/68) · rebond 69% (25/36)
      · −2.0% : fill 28% (22/68) · rebond 60% (15/22)
      · −3.0% : fill 10% (11/68) · rebond 39% (7/11)
      · −4.0% : fill 6% (5/68) · rebond 95% (4/5)
      · −5.0% : fill 4% (2/68) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 62% si les 15 1res min sont vertes (72 cas) · 37% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 66% si début vert vs 35% si rouge (base 48% · écart 31 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.75% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.56% / q75 +2.43% → **scale +1.56% / runner +2.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **35%** (continue à baisser 51%) → **RÉDUIRE ~65%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.58%** (au-delà de la MAE q10 -4.58%), cible rebond +1.6% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +2.3%] · haut q95 +3.38% · bas q05 -3.94%
   - 60min (n=160) : retour [-3.32% .. +2.7%] · haut q95 +3.45% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.68% .. +2.64%] · haut q95 +3.9% · bas q05 -4.81%
   - 4h (n=160) : retour [-3.48% .. +3.03%] · haut q95 +3.94% · bas q05 -6.47%
   - 6h (n=160) : retour [-3.71% .. +3.37%] · haut q95 +4.79% · bas q05 -6.47%
   - session (n=160) : retour [-4.59% .. +4.21%] · haut q95 +6.42% · bas q05 -7.0%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 46.9  _(neutre)_
- **ADX** : 30.5  _(tendance etablie)_
- **MACD** : hist 0.023  _(pas de croisement recent)_
- **BB** : %B 0.39 · largeur 16.9%
- **ATR** : 0.15 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.318  _(distribution)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 44.7  _(transition)_
- **MA** : MA20 3.45 · MA50 3.97 · MA200 4.99  _(prix < MA20)_
- **Dist MA** : MA20 -1.9% · MA50 -14.7% · MA200 -32.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (865190 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
