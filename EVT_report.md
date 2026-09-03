# EVT

**Generated** : 2026-09-03T21:39:22.020769+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.27  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €3.27 (+0.6% vs entrée) · entrée €3.25 · stop €2.99 · T1 €3.38 · R/R 0.5  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.088 _(réel 5 s)_ (GBM -0.073) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.24–€3.26 (mid €3.25)
- Spot actuel : €3.27 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : €2.99 (stop swing_plan-based (-5.11%))
- Targets : T1 €3.38 · R/R 0.5 | T2 €3.40 · R/R 0.58 | T3 €3.42 · R/R 0.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €2.99


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.11 %)** : le gap seul le franchit 0.863 % des séances (11 fois sur 1274).
   - exécution **2.002 pt plus bas** dans le cas TYPIQUE (médiane), 16.501 au p90, **27.303 au pire**
   - perte réelle **11.717 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 5.11 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.057 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0216** [0.007 ; 0.0518] _(largeur 4.5 pt, n_eff 173.1)_
   - swing : **0.4673** [0.4152 ; 0.52] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4708** [0.4186 ; 0.5235] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (36.5 pt), deep (39.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.89 %** | CVaR **-9.26 %** | vol 3.65 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 6.12 % contre 3.76 % aujourd'hui, rapport 1.63)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1189** (β de hausse 0.9431, asymétrie 1.1864) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.9625 sur atr_grid (2.75 ATR, 9.515 %) — p(stop avant cible) 0.32 [0.27 ; 0.37], R/R 1.978, perte reelle 18.001 % (gap inclus), CVaR 9.548 %, EV -3.3878 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.5 ATR (stop 3.815 %) — p(stop avant cible) 0.6839 [0.63 ; 0.73], R/R 3.959, perte reelle 8.996 % (gap inclus), EV -3.7081 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.684, borne haute 0.731 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.71 %) : P(cible) 0.3 % x 35.61 % + P(rien) 31.3 % x 7.47 % ne couvrent pas P(stop) 68.4 % x 9.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 0.87 ATR (stop 5.076 %) — p(stop avant cible) 0.585 [0.53 ; 0.64], R/R 3.04, perte reelle 11.717 % (gap inclus), EV -3.9118 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.585, borne haute 0.636 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.91 %) : P(cible) 0.3 % x 35.61 % + P(rien) 41.2 % x 6.86 % ne couvrent pas P(stop) 58.5 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.865 %) — p(stop avant cible) 0.9115 [0.88 ; 0.94], R/R 15.857, perte reelle 2.246 % (gap inclus), EV -1.0435 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 15.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.911, borne haute 0.938 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 0.1 % x 35.61 % + P(rien) 8.7 % x 11.01 % ne couvrent pas P(stop) 91.1 % x 2.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.5 ATR (stop 2.77 %) — p(stop avant cible) 0.7678 [0.72 ; 0.81], R/R 5.823, perte reelle 6.116 % (gap inclus), EV -2.6095 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.768, borne haute 0.810 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.61 %) : P(cible) 0.3 % x 35.61 % + P(rien) 22.9 % x 8.64 % ne couvrent pas P(stop) 76.8 % x 6.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.325 %) — p(stop avant cible) 0.6461 [0.59 ; 0.70], R/R 3.208, perte reelle 11.103 % (gap inclus), EV -4.5519 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.646, borne haute 0.695 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.55 %) : P(cible) 0.3 % x 35.61 % + P(rien) 35.1 % x 7.14 % ne couvrent pas P(stop) 64.6 % x 11.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.055 %) — p(stop avant cible) 0.5256 [0.47 ; 0.58], R/R 2.74, perte reelle 12.996 % (gap inclus), EV -3.8637 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.526, borne haute 0.578 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.86 %) : P(cible) 0.5 % x 35.61 % + P(rien) 46.9 % x 5.92 % ne couvrent pas P(stop) 52.6 % x 13.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.92 %) — p(stop avant cible) 0.4648 [0.41 ; 0.52], R/R 2.2, perte reelle 16.186 % (gap inclus), EV -4.6766 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.68 %) : P(cible) 0.5 % x 35.61 % + P(rien) 53.0 % x 5.02 % ne couvrent pas P(stop) 46.5 % x 16.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.785 %) — p(stop avant cible) 0.4054 [0.35 ; 0.46], R/R 1.978, perte reelle 18.001 % (gap inclus), EV -4.618 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.62 %) : P(cible) 0.5 % x 35.61 % + P(rien) 58.9 % x 4.23 % ne couvrent pas P(stop) 40.5 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.65 %) — p(stop avant cible) 0.3716 [0.32 ; 0.42], R/R 1.978, perte reelle 18.001 % (gap inclus), EV -4.1223 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.12 %) : P(cible) 0.5 % x 35.61 % + P(rien) 62.3 % x 3.82 % ne couvrent pas P(stop) 37.2 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.515 %) — p(stop avant cible) 0.32 [0.27 ; 0.37], R/R 1.978, perte reelle 18.001 % (gap inclus), EV -3.3878 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.39 %) : P(cible) 0.5 % x 35.61 % + P(rien) 67.5 % x 3.24 % ne couvrent pas P(stop) 32.0 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.38 %) — p(stop avant cible) 0.3014 [0.25 ; 0.35], R/R 1.787, perte reelle 19.926 % (gap inclus), EV -3.7263 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.73 %) : P(cible) 0.5 % x 35.61 % + P(rien) 69.3 % x 3.02 % ne couvrent pas P(stop) 30.1 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.111 %) — p(stop avant cible) 0.2402 [0.20 ; 0.29], R/R 1.575, perte reelle 22.616 % (gap inclus), EV -3.5301 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.14 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.53 %) : P(cible) 0.5 % x 35.61 % + P(rien) 75.4 % x 2.27 % ne couvrent pas P(stop) 24.0 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.841 %) — p(stop avant cible) 0.1833 [0.15 ; 0.23], R/R 1.318, perte reelle 27.012 % (gap inclus), EV -3.5217 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 0.5 % x 35.61 % + P(rien) 81.1 % x 1.53 % ne couvrent pas P(stop) 18.3 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 15.571 %) — p(stop avant cible) 0.1486 [0.11 ; 0.19], R/R 1.318, perte reelle 27.012 % (gap inclus), EV -2.8565 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.86 %) : P(cible) 0.5 % x 35.61 % + P(rien) 84.6 % x 1.14 % ne couvrent pas P(stop) 14.9 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 17.301 %) — p(stop avant cible) 0.1281 [0.10 ; 0.17], R/R 1.318, perte reelle 27.012 % (gap inclus), EV -2.4573 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.46 %) : P(cible) 0.5 % x 35.61 % + P(rien) 86.7 % x 0.94 % ne couvrent pas P(stop) 12.8 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 19.031 %) — p(stop avant cible) 0.1099 [0.08 ; 0.15], R/R 1.318, perte reelle 27.012 % (gap inclus), EV -2.1786 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.18 %) : P(cible) 0.5 % x 35.61 % + P(rien) 88.5 % x 0.68 % ne couvrent pas P(stop) 11.0 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 20.761 %) — p(stop avant cible) 0.1023 [0.07 ; 0.14], R/R 1.318, perte reelle 27.012 % (gap inclus), EV -2.0736 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 0.5 % x 35.61 % + P(rien) 89.2 % x 0.56 % ne couvrent pas P(stop) 10.2 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 22.491 %) — p(stop avant cible) 0.0985 [0.07 ; 0.13], R/R 1.099, perte reelle 32.413 % (gap inclus), EV -2.5675 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.57 %) : P(cible) 0.5 % x 35.61 % + P(rien) 89.6 % x 0.49 % ne couvrent pas P(stop) 9.8 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 24.221 %) — p(stop avant cible) 0.0866 [0.06 ; 0.12], R/R 1.099, perte reelle 32.413 % (gap inclus), EV -2.4041 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.40 %) : P(cible) 0.5 % x 35.61 % + P(rien) 90.8 % x 0.24 % ne couvrent pas P(stop) 8.7 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 25.951 %) — p(stop avant cible) 0.0775 [0.05 ; 0.11], R/R 1.099, perte reelle 32.413 % (gap inclus), EV -2.3101 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.31 %) : P(cible) 0.5 % x 35.61 % + P(rien) 91.7 % x 0.01 % ne couvrent pas P(stop) 7.8 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 27.681 %) — p(stop avant cible) 0.0665 [0.04 ; 0.10], R/R 1.099, perte reelle 32.413 % (gap inclus), EV -2.2224 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.22 %) : P(cible) 0.5 % x 35.61 % + P(rien) 92.8 % x -0.28 % ne couvrent pas P(stop) 6.7 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.274, ATR14 0.1133 (3.46 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.366 ATR = 1.266 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.173 % | 3.2683 | 88.86 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.346 % | 3.2627 | 81.46 % | 86.97 % | 89.72 % | 92.77 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.519 % | 3.257 | 75.15 % | 83.12 % | 86.66 % | 90.0 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.692 % | 3.2513 | 68.84 % | 79.07 % | 83.4 % | 87.23 % | 91.94 % | 94.77 % |
| 0.25 ATR | 0.865 % | 3.2457 | 63.12 % | 75.81 % | 80.34 % | 84.85 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.211 % | 3.2343 | 51.78 % | 67.62 % | 73.91 % | 79.9 % | 86.17 % | 91.56 % |
| 0.5 ATR | 1.73 % | 3.2174 | 35.4 % | 54.89 % | 62.85 % | 70.79 % | 80.1 % | 88.24 % |
| 0.75 ATR | 2.595 % | 3.189 | 19.13 % | 37.91 % | 47.73 % | 59.41 % | 71.74 % | 81.91 % |
| 1.0 ATR | 3.46 % | 3.1607 | 10.16 % | 24.88 % | 35.97 % | 47.52 % | 62.39 % | 75.28 % |
| 1.25 ATR | 4.325 % | 3.1324 | 4.83 % | 17.47 % | 27.57 % | 39.5 % | 55.62 % | 70.05 % |
| 1.5 ATR | 5.19 % | 3.1041 | 3.06 % | 11.35 % | 19.86 % | 31.49 % | 48.56 % | 64.72 % |
| 2.0 ATR | 6.92 % | 3.0474 | 1.48 % | 5.23 % | 9.98 % | 19.41 % | 35.02 % | 52.46 % |
| 2.5 ATR | 8.65 % | 2.9908 | 0.49 % | 2.76 % | 5.83 % | 12.48 % | 27.86 % | 44.62 % |
| 3.0 ATR | 10.38 % | 2.9341 | 0.39 % | 1.68 % | 3.75 % | 9.01 % | 21.0 % | 37.59 % |
| 4.0 ATR | 13.841 % | 2.8209 | 0.2 % | 0.89 % | 1.98 % | 4.55 % | 11.94 % | 24.72 % |
| 6.0 ATR | 20.761 % | 2.5943 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.57 % | 14.27 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.05 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.50 ATR | 2.00 ATR | 2.70 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.86 ATR | 3.90 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.63 ATR | 2.14 ATR | 2.71 ATR | 3.11 ATR | 4.61 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.16 ATR | 2.48 ATR | 3.36 ATR | 3.98 ATR | 4.90 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.412–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (62.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.595 %, prix 3.189), p(touche) 37.91 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (66.0 % des re-echantillons)
- **3 seance(s)** : plage utile 0.808–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.46 %, prix 3.1607), p(touche) 35.97 % (en stress 96.08 %)  ✅ optimum identifie (63.8 % des re-echantillons)
- **5 seance(s)** : plage utile 1.079–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.325 %, prix 3.1324), p(touche) 39.5 % (en stress 95.05 %)  ✅ optimum identifie (74.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.631–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.92 %, prix 3.0474), p(touche) 35.02 % (en stress 98.02 %)  ✅ optimum identifie (72.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.476–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.65 %, prix 2.9908), p(touche) 44.62 % (en stress 98.0 %)  ✅ optimum identifie (84.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.073 | EV/share : €-0.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 9 % | T2 5 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.5 | bear 5.0 | side 76.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.749% → cible +4.016% / stop −8.001%, p_fill 82%, n_eff≈33.8) : P(cible|rempli) **3%** · **EV/risk -0.088** (×p_fill ; si rempli -0.86% du capital)
  - **swing** (entrée dip −1.65% → cible +3.981% / stop −3.519%, p_fill 65%, n_eff≈26.1) : P(cible|rempli) **44%** · **EV/risk +0.019** (×p_fill ; si rempli +0.10% du capital)
  - **deep** (entrée dip −2.54% → cible +5.632% / stop −5.325%, p_fill 55%, n_eff≈21.5) : P(cible|rempli) **22%** · **EV/risk -0.222** (×p_fill ; si rempli -2.14% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→68% · +2.0%→40% · +3.0%→21% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.64% (p90 6.26%) · excursion haute méd. +1.53% / basse méd. −1.65%
- Profil de vol intra : ouverture 2.484% vs midi 1.192% vs clôture 1.156% _(ouverture ~2.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.091 ; mean-reverting — autocorr -0.18)_ ; drift intra méd. -0.791% ; recovery-V 20%
- **σ réalisé intraday** 2.934% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 76% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 3.2093 (VA 3.2031–3.2341 ; dernier close 3.166)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 56% · rebond 66% · **stop −2.56%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 41% (gap-down >1% 9% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −2.25%) · haut méd +0.44% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.68%) · haut méd +0.67% · range méd 1.73%
- Excursion ouverture 30min (n=160) : bas méd −0.91% (p90 −2.78%) · haut méd +0.77% · range méd 1.97%
- Excursion ouverture 60min (n=160) : bas méd −0.94% (p90 −3.02%) · haut méd +0.93% · range méd 2.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.15 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 78% (130/159) · gap 23% · délai 0.5min · rebond 67% (88/130) (MFE +1.42%)
   - −1.0% : fill 30min 39% · séance 67% (112/159) · gap 9% · délai 6.9min · rebond 64% (74/112) (MFE +1.44%)
   - −1.5% : fill 30min 30% · séance 56% (95/159) · gap 5% · délai 23.5min · rebond 66% (62/95) (MFE +1.4%)
   - −2.0% : fill 30min 20% · séance 44% (78/159) · gap 5% · délai 39.1min · rebond 52% (44/78) (MFE +1.29%)
   - −3.0% : fill 30min 10% · séance 24% (49/159) · gap 3% · délai 59.4min · rebond 66% (35/49) (MFE +1.5%)
   - −4.0% : fill 30min 4% · séance 11% (26/159) · gap 1% · délai 46.7min · rebond 53% (16/26) (MFE +1.13%)
   - −5.0% : fill 30min 3% · séance 7% (15/159) · gap 1% · délai 30.3min · rebond 59% (10/15) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −2.45%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.31% (p90 −1.66%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −1.85%) → stop au-delà de −1.26% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=810 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 81% (47/55) · rebond 69% (32/47)
      · −2.0% : fill 59% (36/55) · rebond 53% (21/36)
      · −3.0% : fill 37% (25/55) · rebond 68% (18/25)
      · −4.0% : fill 22% (18/55) · rebond 42% (11/18)
      · −5.0% : fill 16% (12/55) · rebond 40% (7/12)
   - **flat** (36 séances) :
      · −1.0% : fill 85% (29/36) · rebond 49% (17/29)
      · −2.0% : fill 62% (21/36) · rebond 44% (9/21)
      · −3.0% : fill 35% (13/36) · rebond 79% (10/13)
      · −4.0% : fill 7% (3/36) · rebond 28% (1/3)
      · −5.0% : fill 2% (1/36) · rebond 100% (1/1)
   - **gap-up** (68 séances) :
      · −1.0% : fill 49% (36/68) · rebond 71% (25/36)
      · −2.0% : fill 26% (21/68) · rebond 60% (14/21)
      · −3.0% : fill 10% (11/68) · rebond 39% (7/11)
      · −4.0% : fill 6% (5/68) · rebond 95% (4/5)
      · −5.0% : fill 4% (2/68) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 58% si les 15 1res min sont vertes (73 cas) · 35% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 57% si début vert vs 36% si rouge (base 46% · écart 21 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **57%** · continue >prix actuel 39% ; creux résiduel méd -1.83% (q20 -2.79%) → **SL/trailing à −2.79%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.27% / q75 +2.35% → **scale +1.27% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **36%** (continue à baisser 48%) → **RÉDUIRE ~64%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.47%** (au-delà de la MAE q10 -4.47%), cible rebond +1.72% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.62% .. +2.27%] · haut q95 +3.04% · bas q05 -3.92%
   - 60min (n=160) : retour [-3.1% .. +2.54%] · haut q95 +3.27% · bas q05 -4.08%
   - 2h (n=160) : retour [-3.48% .. +2.4%] · haut q95 +3.75% · bas q05 -4.25%
   - 4h (n=160) : retour [-3.35% .. +3.74%] · haut q95 +4.43% · bas q05 -4.48%
   - 6h (n=160) : retour [-3.34% .. +4.49%] · haut q95 +5.26% · bas q05 -5.28%
   - session (n=160) : retour [-4.19% .. +4.05%] · haut q95 +5.8% · bas q05 -5.68%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.91%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 40.6  _(momentum baissier)_
- **ADX** : 29.9  _(tendance etablie)_
- **MACD** : hist 0.018  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 20.0%
- **ATR** : 0.11 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.249  _(distribution)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 57.0  _(transition)_
- **MA** : MA20 3.41 · MA50 3.82 · MA200 4.94  _(prix < MA20)_
- **Dist MA** : MA20 -3.9% · MA50 -14.3% · MA200 -33.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (764665 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
