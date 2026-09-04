# EVT

**Generated** : 2026-09-04T21:39:07.813684+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.21  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €3.21 (+0.3% vs entrée) · entrée €3.20 · stop €3.15 · T1 €3.26 · R/R 1.2  
> ↳ P(T1 av. stop) 18 % _(réel 5 s)_ · EV/risk -0.356 _(réel 5 s)_ (GBM -0.083) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.19–€3.21 (mid €3.20)
- Spot actuel : €3.21 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €3.15 (stop swing_plan-based (-4.2%))
- Targets : T1 €3.26 · R/R 1.2 | T2 €3.32 · R/R 2.4 | T3 €3.37 · R/R 3.4
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.15


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.2 %)** : le gap seul le franchit 0.942 % des séances (12 fois sur 1274).
   - exécution **2.812 pt plus bas** dans le cas TYPIQUE (médiane), 16.632 au p90, **28.213 au pire**
   - perte réelle **11.103 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 4.2 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.065 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 12 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5022** [0.4282 ; 0.5761] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4742** [0.422 ; 0.5269] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4755** [0.4233 ; 0.5282] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.2 pt), swing (31.3 pt), deep (33.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.89 %** | CVaR **-9.26 %** | vol 3.65 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 6.11 % contre 3.75 % aujourd'hui, rapport 1.63)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1189** (β de hausse 0.9465, asymétrie 1.1821) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.9032 sur atr_grid (2.75 ATR, 9.614 %) — p(stop avant cible) 0.3173 [0.27 ; 0.37], R/R 2.124, perte reelle 18.001 % (gap inclus), CVaR 9.647 %, EV -3.3697 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 0.32 ATR (stop 3.169 %) — p(stop avant cible) 0.7171 [0.67 ; 0.76], R/R 5.51, perte reelle 6.94 % (gap inclus), EV -2.7083 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.717, borne haute 0.763 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.71 %) : P(cible) 0.2 % x 38.24 % + P(rien) 28.0 % x 7.76 % ne couvrent pas P(stop) 71.7 % x 6.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.243 %) — p(stop avant cible) 0.576 [0.52 ; 0.63], R/R 3.264, perte reelle 11.717 % (gap inclus), EV -3.8508 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.576, borne haute 0.627 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.85 %) : P(cible) 0.3 % x 38.24 % + P(rien) 42.1 % x 6.63 % ne couvrent pas P(stop) 57.6 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 0.32 ATR (stop 2.17 %) — p(stop avant cible) 0.8222 [0.78 ; 0.86], R/R 7.828, perte reelle 4.885 % (gap inclus), EV -2.3973 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 7.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.822, borne haute 0.860 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.40 %) : P(cible) 0.2 % x 38.24 % + P(rien) 17.6 % x 8.78 % ne couvrent pas P(stop) 82.2 % x 4.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.622 %) — p(stop avant cible) 0.7762 [0.73 ; 0.82], R/R 6.545, perte reelle 5.843 % (gap inclus), EV -2.4899 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.776, borne haute 0.818 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.49 %) : P(cible) 0.2 % x 38.24 % + P(rien) 22.1 % x 8.82 % ne couvrent pas P(stop) 77.6 % x 5.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.37 %) — p(stop avant cible) 0.6443 [0.59 ; 0.69], R/R 3.264, perte reelle 11.717 % (gap inclus), EV -4.9058 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.644, borne haute 0.693 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.91 %) : P(cible) 0.3 % x 38.24 % + P(rien) 35.3 % x 7.19 % ne couvrent pas P(stop) 64.4 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.118 %) — p(stop avant cible) 0.5166 [0.46 ; 0.57], R/R 2.943, perte reelle 12.996 % (gap inclus), EV -3.7745 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.517, borne haute 0.569 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.77 %) : P(cible) 0.3 % x 38.24 % + P(rien) 48.0 % x 5.86 % ne couvrent pas P(stop) 51.7 % x 13.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.992 %) — p(stop avant cible) 0.4592 [0.41 ; 0.51], R/R 2.363, perte reelle 16.186 % (gap inclus), EV -4.6378 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.64 %) : P(cible) 0.3 % x 38.24 % + P(rien) 53.8 % x 4.96 % ne couvrent pas P(stop) 45.9 % x 16.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.866 %) — p(stop avant cible) 0.4018 [0.35 ; 0.45], R/R 2.124, perte reelle 18.001 % (gap inclus), EV -4.5883 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.59 %) : P(cible) 0.3 % x 38.24 % + P(rien) 59.5 % x 4.23 % ne couvrent pas P(stop) 40.2 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.74 %) — p(stop avant cible) 0.368 [0.32 ; 0.42], R/R 2.124, perte reelle 18.001 % (gap inclus), EV -4.0893 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.09 %) : P(cible) 0.3 % x 38.24 % + P(rien) 62.9 % x 3.83 % ne couvrent pas P(stop) 36.8 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.614 %) — p(stop avant cible) 0.3173 [0.27 ; 0.37], R/R 2.124, perte reelle 18.001 % (gap inclus), EV -3.3697 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.37 %) : P(cible) 0.3 % x 38.24 % + P(rien) 67.9 % x 3.26 % ne couvrent pas P(stop) 31.7 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.487 %) — p(stop avant cible) 0.2934 [0.25 ; 0.34], R/R 1.919, perte reelle 19.926 % (gap inclus), EV -3.6169 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.62 %) : P(cible) 0.3 % x 38.24 % + P(rien) 70.3 % x 2.99 % ne couvrent pas P(stop) 29.3 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.235 %) — p(stop avant cible) 0.2336 [0.19 ; 0.28], R/R 1.691, perte reelle 22.616 % (gap inclus), EV -3.4537 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.45 %) : P(cible) 0.3 % x 38.24 % + P(rien) 76.3 % x 2.23 % ne couvrent pas P(stop) 23.4 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.983 %) — p(stop avant cible) 0.175 [0.14 ; 0.22], R/R 1.416, perte reelle 27.012 % (gap inclus), EV -3.3566 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.36 %) : P(cible) 0.3 % x 38.24 % + P(rien) 82.2 % x 1.51 % ne couvrent pas P(stop) 17.5 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 15.731 %) — p(stop avant cible) 0.1447 [0.11 ; 0.18], R/R 1.416, perte reelle 27.012 % (gap inclus), EV -2.7955 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.80 %) : P(cible) 0.3 % x 38.24 % + P(rien) 85.2 % x 1.16 % ne couvrent pas P(stop) 14.5 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 17.479 %) — p(stop avant cible) 0.1266 [0.09 ; 0.16], R/R 1.416, perte reelle 27.012 % (gap inclus), EV -2.4435 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.44 %) : P(cible) 0.3 % x 38.24 % + P(rien) 87.0 % x 0.98 % ne couvrent pas P(stop) 12.7 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 19.227 %) — p(stop avant cible) 0.1093 [0.08 ; 0.15], R/R 1.416, perte reelle 27.012 % (gap inclus), EV -2.1807 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.18 %) : P(cible) 0.3 % x 38.24 % + P(rien) 88.8 % x 0.73 % ne couvrent pas P(stop) 10.9 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 20.975 %) — p(stop avant cible) 0.1016 [0.07 ; 0.14], R/R 1.416, perte reelle 27.012 % (gap inclus), EV -2.0739 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 0.3 % x 38.24 % + P(rien) 89.5 % x 0.61 % ne couvrent pas P(stop) 10.2 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 22.723 %) — p(stop avant cible) 0.0978 [0.07 ; 0.13], R/R 1.18, perte reelle 32.413 % (gap inclus), EV -2.5651 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.57 %) : P(cible) 0.3 % x 38.24 % + P(rien) 89.9 % x 0.53 % ne couvrent pas P(stop) 9.8 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 24.471 %) — p(stop avant cible) 0.0861 [0.06 ; 0.12], R/R 1.18, perte reelle 32.413 % (gap inclus), EV -2.4041 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.40 %) : P(cible) 0.3 % x 38.24 % + P(rien) 91.1 % x 0.29 % ne couvrent pas P(stop) 8.6 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 26.219 %) — p(stop avant cible) 0.0757 [0.05 ; 0.11], R/R 1.18, perte reelle 32.413 % (gap inclus), EV -2.2986 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.30 %) : P(cible) 0.3 % x 38.24 % + P(rien) 92.1 % x 0.03 % ne couvrent pas P(stop) 7.6 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 27.967 %) — p(stop avant cible) 0.0615 [0.04 ; 0.09], R/R 1.18, perte reelle 32.413 % (gap inclus), EV -2.1975 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 0.3 % x 38.24 % + P(rien) 93.5 % x -0.35 % ne couvrent pas P(stop) 6.2 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.212, ATR14 0.1123 (3.496 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.365 ATR = 1.276 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.175 % | 3.2064 | 88.86 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.35 % | 3.2008 | 81.46 % | 86.87 % | 89.72 % | 92.77 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.524 % | 3.1952 | 75.15 % | 83.02 % | 86.66 % | 90.0 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.699 % | 3.1895 | 68.84 % | 78.97 % | 83.4 % | 87.23 % | 91.94 % | 94.77 % |
| 0.25 ATR | 0.874 % | 3.1839 | 63.12 % | 75.72 % | 80.34 % | 84.85 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.224 % | 3.1727 | 51.68 % | 67.52 % | 73.91 % | 79.9 % | 86.17 % | 91.56 % |
| 0.5 ATR | 1.748 % | 3.1559 | 35.4 % | 54.89 % | 62.94 % | 70.79 % | 80.1 % | 88.24 % |
| 0.75 ATR | 2.622 % | 3.1278 | 19.13 % | 37.91 % | 47.83 % | 59.41 % | 71.74 % | 81.91 % |
| 1.0 ATR | 3.496 % | 3.0997 | 10.16 % | 24.88 % | 36.07 % | 47.52 % | 62.39 % | 75.28 % |
| 1.25 ATR | 4.37 % | 3.0716 | 4.83 % | 17.47 % | 27.57 % | 39.6 % | 55.62 % | 70.05 % |
| 1.5 ATR | 5.244 % | 3.0436 | 3.06 % | 11.35 % | 19.86 % | 31.58 % | 48.56 % | 64.72 % |
| 2.0 ATR | 6.992 % | 2.9874 | 1.48 % | 5.23 % | 9.98 % | 19.5 % | 34.93 % | 52.46 % |
| 2.5 ATR | 8.74 % | 2.9313 | 0.49 % | 2.76 % | 5.83 % | 12.48 % | 27.76 % | 44.62 % |
| 3.0 ATR | 10.487 % | 2.8751 | 0.39 % | 1.68 % | 3.75 % | 9.01 % | 20.9 % | 37.49 % |
| 4.0 ATR | 13.983 % | 2.7629 | 0.2 % | 0.89 % | 1.98 % | 4.55 % | 11.84 % | 24.62 % |
| 6.0 ATR | 20.975 % | 2.5383 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.57 % | 14.27 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.61 ATR | 2.05 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.50 ATR | 2.00 ATR | 2.70 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.46 ATR | 1.77 ATR | 1.98 ATR | 2.86 ATR | 3.90 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.63 ATR | 2.13 ATR | 2.70 ATR | 3.10 ATR | 4.59 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.16 ATR | 2.48 ATR | 3.35 ATR | 3.97 ATR | 4.89 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.412–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (62.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.622 %, prix 3.1278), p(touche) 37.91 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.9 % des re-echantillons)
- **3 seance(s)** : plage utile 0.81–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.496 %, prix 3.0997), p(touche) 36.07 % (en stress 96.08 %)  ✅ optimum identifie (63.1 % des re-echantillons)
- **5 seance(s)** : plage utile 1.08–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.37 %, prix 3.0716), p(touche) 39.6 % (en stress 95.05 %)  ✅ optimum identifie (73.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.631–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.992 %, prix 2.9874), p(touche) 34.93 % (en stress 98.02 %)  ✅ optimum identifie (71.6 % des re-echantillons)
- **20 seance(s)** : plage utile 2.476–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.74 %, prix 2.9313), p(touche) 44.62 % (en stress 98.0 %)  ✅ optimum identifie (84.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.083 | EV/share : €-0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 12 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.5 | bear 5.0 | side 77.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.326% → cible +1.787% / stop −1.499%, p_fill 89%, n_eff≈36.3) : P(cible|rempli) **18%** · **EV/risk -0.356** (×p_fill ; si rempli -0.60% du capital)
  - **swing** (entrée dip −0.704% → cible +3.991% / stop −3.521%, p_fill 84%, n_eff≈34.9) : P(cible|rempli) **39%** · **EV/risk +0.028** (×p_fill ; si rempli +0.12% du capital)
  - **deep** (entrée dip −1.037% → cible +5.647% / stop −5.298%, p_fill 80%, n_eff≈31.2) : P(cible|rempli) **40%** · **EV/risk -0.109** (×p_fill ; si rempli -0.72% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.5  _(momentum baissier)_
- **ADX** : 29.9  _(tendance etablie)_
- **MACD** : hist 0.015  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 20.7%
- **ATR** : 0.11 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.243  _(distribution)_
- **Vol ratio** : 1.32  _(volume normal)_
- **Choppiness** : 57.6  _(transition)_
- **MA** : MA20 3.39 · MA50 3.79 · MA200 4.93  _(prix < MA20)_
- **Dist MA** : MA20 -5.4% · MA50 -15.2% · MA200 -34.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (764970 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
