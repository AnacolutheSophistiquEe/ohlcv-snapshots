# EVT

**Generated** : 2026-08-31T00:05:25.027150+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.33  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €3.33 (+1.2% vs entrée) · entrée €3.29 · stop €3.24 · T1 €3.38 · R/R 1.8  
> ↳ P(T1 av. stop) 15 % _(réel 5 s)_ · EV/risk -0.042 _(réel 5 s)_ (GBM -0.07) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.28–€3.30 (mid €3.29)
- Spot actuel : €3.33 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €3.24 (stop swing_plan-based (-6.64%))
- Targets : T1 €3.38 · R/R 1.8 | T2 €3.42 · R/R 2.6 | T3 €3.45 · R/R 3.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.24


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.64 %)** : le gap seul le franchit 0.549 % des séances (7 fois sur 1274).
   - exécution **5.218 pt plus bas** dans le cas TYPIQUE (médiane), 19.292 au p90, **25.773 au pire**
   - perte réelle **14.861 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 6.64 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0452 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5209** [0.4467 ; 0.5945] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4169** [0.3658 ; 0.4694] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4142** [0.3632 ; 0.4667] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.6 pt), swing (41.6 pt), deep (44.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.89 %** | CVaR **-9.26 %** | vol 3.65 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 6.11 % contre 3.79 % aujourd'hui, rapport 1.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1105** (β de hausse 0.9424, asymétrie 1.1783) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 2.9934 sur atr_grid (2.5 ATR, 10.161 %) — p(stop avant cible) 0.3157 [0.27 ; 0.37], R/R 1.836, perte reelle 18.001 % (gap inclus), CVaR 10.192 %, EV -3.1974 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.88 ATR (stop 5.819 %) — p(stop avant cible) 0.5361 [0.48 ; 0.59], R/R 2.821, perte reelle 11.717 % (gap inclus), EV -3.1774 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.536, borne haute 0.588 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.18 %) : P(cible) 0.7 % x 33.05 % + P(rien) 45.7 % x 6.28 % ne couvrent pas P(stop) 53.6 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.15 ATR (stop 6.927 %) — p(stop avant cible) 0.4698 [0.42 ; 0.52], R/R 2.042, perte reelle 16.186 % (gap inclus), EV -4.6069 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.61 %) : P(cible) 0.8 % x 33.05 % + P(rien) 52.2 % x 5.24 % ne couvrent pas P(stop) 47.0 % x 16.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.016 %) — p(stop avant cible) 0.8998 [0.86 ; 0.93], R/R 12.797, perte reelle 2.583 % (gap inclus), EV -1.2742 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 12.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.900, borne haute 0.928 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 0.2 % x 33.05 % + P(rien) 9.8 % x 10.09 % ne couvrent pas P(stop) 90.0 % x 2.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.032 %) — p(stop avant cible) 0.8261 [0.78 ; 0.86], R/R 7.712, perte reelle 4.286 % (gap inclus), EV -1.8869 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 7.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.826, borne haute 0.863 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.89 %) : P(cible) 0.2 % x 33.05 % + P(rien) 17.1 % x 9.17 % ne couvrent pas P(stop) 82.6 % x 4.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.88 ATR (stop 4.794 %) — p(stop avant cible) 0.6074 [0.56 ; 0.66], R/R 2.821, perte reelle 11.717 % (gap inclus), EV -4.1885 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.607, borne haute 0.658 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.19 %) : P(cible) 0.6 % x 33.05 % + P(rien) 38.7 % x 7.07 % ne couvrent pas P(stop) 60.7 % x 11.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.129 %) — p(stop avant cible) 0.3984 [0.35 ; 0.45], R/R 1.836, perte reelle 18.001 % (gap inclus), EV -4.3828 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.38 %) : P(cible) 0.8 % x 33.05 % + P(rien) 59.4 % x 4.26 % ne couvrent pas P(stop) 39.8 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.145 %) — p(stop avant cible) 0.3482 [0.30 ; 0.40], R/R 1.836, perte reelle 18.001 % (gap inclus), EV -3.6743 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 0.8 % x 33.05 % + P(rien) 64.4 % x 3.62 % ne couvrent pas P(stop) 34.8 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.161 %) — p(stop avant cible) 0.3157 [0.27 ; 0.37], R/R 1.836, perte reelle 18.001 % (gap inclus), EV -3.1974 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.20 %) : P(cible) 0.8 % x 33.05 % + P(rien) 67.6 % x 3.29 % ne couvrent pas P(stop) 31.6 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 11.177 %) — p(stop avant cible) 0.2839 [0.24 ; 0.33], R/R 1.659, perte reelle 19.926 % (gap inclus), EV -3.3764 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.38 %) : P(cible) 0.8 % x 33.05 % + P(rien) 70.8 % x 2.85 % ne couvrent pas P(stop) 28.4 % x 19.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 12.193 %) — p(stop avant cible) 0.2411 [0.20 ; 0.29], R/R 1.462, perte reelle 22.616 % (gap inclus), EV -3.4425 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.44 %) : P(cible) 0.8 % x 33.05 % + P(rien) 75.1 % x 2.33 % ne couvrent pas P(stop) 24.1 % x 22.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 14.226 %) — p(stop avant cible) 0.1778 [0.14 ; 0.22], R/R 1.224, perte reelle 27.012 % (gap inclus), EV -3.2953 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.30 %) : P(cible) 0.8 % x 33.05 % + P(rien) 81.4 % x 1.53 % ne couvrent pas P(stop) 17.8 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 16.258 %) — p(stop avant cible) 0.1422 [0.11 ; 0.18], R/R 1.224, perte reelle 27.012 % (gap inclus), EV -2.6449 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.64 %) : P(cible) 0.8 % x 33.05 % + P(rien) 85.0 % x 1.10 % ne couvrent pas P(stop) 14.2 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 18.29 %) — p(stop avant cible) 0.1132 [0.08 ; 0.15], R/R 1.224, perte reelle 27.012 % (gap inclus), EV -2.1313 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.13 %) : P(cible) 0.8 % x 33.05 % + P(rien) 87.9 % x 0.76 % ne couvrent pas P(stop) 11.3 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 20.322 %) — p(stop avant cible) 0.1048 [0.08 ; 0.14], R/R 1.224, perte reelle 27.012 % (gap inclus), EV -2.0153 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.02 %) : P(cible) 0.8 % x 33.05 % + P(rien) 88.7 % x 0.62 % ne couvrent pas P(stop) 10.5 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 22.355 %) — p(stop avant cible) 0.1017 [0.07 ; 0.14], R/R 1.02, perte reelle 32.413 % (gap inclus), EV -2.5337 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.53 %) : P(cible) 0.8 % x 33.05 % + P(rien) 89.0 % x 0.56 % ne couvrent pas P(stop) 10.2 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 24.387 %) — p(stop avant cible) 0.0886 [0.06 ; 0.12], R/R 1.02, perte reelle 32.413 % (gap inclus), EV -2.3524 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.35 %) : P(cible) 0.8 % x 33.05 % + P(rien) 90.3 % x 0.29 % ne couvrent pas P(stop) 8.9 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 26.419 %) — p(stop avant cible) 0.0773 [0.05 ; 0.11], R/R 1.02, perte reelle 32.413 % (gap inclus), EV -2.2417 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.24 %) : P(cible) 0.8 % x 33.05 % + P(rien) 91.5 % x 0.00 % ne couvrent pas P(stop) 7.7 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 28.451 %) — p(stop avant cible) 0.0596 [0.04 ; 0.09], R/R 1.02, perte reelle 32.413 % (gap inclus), EV -2.108 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.11 %) : P(cible) 0.8 % x 33.05 % + P(rien) 93.2 % x -0.47 % ne couvrent pas P(stop) 6.0 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 30.484 %) — p(stop avant cible) 0.0487 [0.03 ; 0.08], R/R 1.02, perte reelle 32.413 % (gap inclus), EV -2.0267 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.03 %) : P(cible) 0.8 % x 33.05 % + P(rien) 94.3 % x -0.75 % ne couvrent pas P(stop) 4.9 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 32.516 %) — p(stop avant cible) 0.0487 [0.03 ; 0.08], R/R 1.017, perte reelle 32.516 % (gap inclus), EV -2.0317 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.03 %) : P(cible) 0.8 % x 33.05 % + P(rien) 94.3 % x -0.75 % ne couvrent pas P(stop) 4.9 % x 32.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.332, ATR14 0.1354 (4.064 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.364 ATR = 1.479 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.203 % | 3.3252 | 88.86 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.406 % | 3.3185 | 81.46 % | 86.97 % | 89.82 % | 92.77 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.61 % | 3.3117 | 75.15 % | 83.12 % | 86.76 % | 90.0 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.813 % | 3.3049 | 68.74 % | 78.97 % | 83.4 % | 87.13 % | 91.94 % | 94.77 % |
| 0.25 ATR | 1.016 % | 3.2981 | 63.02 % | 75.72 % | 80.34 % | 84.75 % | 90.05 % | 93.57 % |
| 0.35 ATR | 1.423 % | 3.2846 | 51.48 % | 67.42 % | 73.72 % | 79.6 % | 86.17 % | 91.56 % |
| 0.5 ATR | 2.032 % | 3.2643 | 35.21 % | 54.69 % | 62.65 % | 70.59 % | 80.1 % | 88.24 % |
| 0.75 ATR | 3.048 % | 3.2304 | 19.03 % | 37.61 % | 47.43 % | 59.21 % | 71.64 % | 81.91 % |
| 1.0 ATR | 4.064 % | 3.1966 | 10.16 % | 24.58 % | 35.67 % | 47.43 % | 62.29 % | 75.28 % |
| 1.25 ATR | 5.081 % | 3.1627 | 4.83 % | 17.37 % | 27.37 % | 39.41 % | 55.62 % | 70.05 % |
| 1.5 ATR | 6.097 % | 3.1289 | 3.06 % | 11.35 % | 19.76 % | 31.39 % | 48.66 % | 64.82 % |
| 2.0 ATR | 8.129 % | 3.0611 | 1.48 % | 5.23 % | 9.98 % | 19.41 % | 35.22 % | 52.66 % |
| 2.5 ATR | 10.161 % | 2.9934 | 0.49 % | 2.76 % | 5.83 % | 12.48 % | 28.06 % | 44.82 % |
| 3.0 ATR | 12.193 % | 2.9257 | 0.39 % | 1.68 % | 3.75 % | 9.01 % | 21.09 % | 37.99 % |
| 4.0 ATR | 16.258 % | 2.7903 | 0.2 % | 0.89 % | 1.98 % | 4.55 % | 11.94 % | 25.13 % |
| 6.0 ATR | 24.387 % | 2.5194 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.57 % | 14.27 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.36 ATR | 0.41 ATR | 0.53 ATR | 0.66 ATR | 0.73 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.64 ATR | 0.84 ATR | 0.99 ATR | 1.16 ATR | 1.61 ATR | 2.05 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.08 ATR | 1.33 ATR | 1.49 ATR | 2.00 ATR | 2.70 ATR |
| **5 s.** | 0.43 ATR | 0.94 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.86 ATR | 3.90 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.64 ATR | 2.15 ATR | 2.72 ATR | 3.12 ATR | 4.61 ATR | hors grille |
| **20 s.** | 1.01 ATR | 2.17 ATR | 2.49 ATR | 3.39 ATR | 4.02 ATR | 4.95 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.41–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (64.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.642–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.048 %, prix 3.2304), p(touche) 37.61 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.8 % des re-echantillons)
- **3 seance(s)** : plage utile 0.802–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.064 %, prix 3.1966), p(touche) 35.67 % (en stress 96.08 %)  ✅ optimum identifie (63.5 % des re-echantillons)
- **5 seance(s)** : plage utile 1.076–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.081 %, prix 3.1627), p(touche) 39.41 % (en stress 95.05 %)  ✅ optimum identifie (72.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.636–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.129 %, prix 3.0611), p(touche) 35.22 % (en stress 98.02 %)  ✅ optimum identifie (71.8 % des re-echantillons)
- **20 seance(s)** : plage utile 2.489–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.161 %, prix 2.9934), p(touche) 44.82 % (en stress 98.0 %)  ✅ optimum identifie (84.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.07 | EV/share : €-0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 11 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 73.3 | bear 5.2 | side 21.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.167% → cible +2.642% / stop −1.5%, p_fill 72%, n_eff≈29.5) : P(cible|rempli) **15%** · **EV/risk -0.042** (×p_fill ; si rempli -0.09% du capital)
  - **swing** (entrée dip −2.576% → cible +3.629% / stop −4.171%, p_fill 49%, n_eff≈18.0) : P(cible|rempli) **35%** · **EV/risk -0.076** (×p_fill ; si rempli -0.65% du capital)
  - **deep** (entrée dip −3.985% → cible +5.132% / stop −6.348%, p_fill 47%, n_eff≈17.2) : P(cible|rempli) **19%** · **EV/risk -0.197** (×p_fill ; si rempli -2.69% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→68% · +2.0%→41% · +3.0%→22% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.64% (p90 6.26%) · excursion haute méd. +1.57% / basse méd. −1.62%
- Profil de vol intra : ouverture 2.524% vs midi 1.175% vs clôture 1.14% _(ouverture ~2.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.084 ; mean-reverting — autocorr -0.17)_ ; drift intra méd. -0.605% ; recovery-V 23%
- **σ réalisé intraday** 2.97% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 74% / whipsaw 45%
- POC intraday (dernière séance, temps-au-prix) : 3.4031 (VA 3.3694–3.4144 ; dernier close 3.33)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 66% · rebond 67% · **stop −2.83%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 39% (gap-down >1% 10% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −2.29%) · haut méd +0.51% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.73%) · haut méd +0.67% · range méd 1.73%
- Excursion ouverture 30min (n=160) : bas méd −0.91% (p90 −2.81%) · haut méd +0.77% · range méd 1.99%
- Excursion ouverture 60min (n=160) : bas méd −0.95% (p90 −3.16%) · haut méd +0.93% · range méd 2.35%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.332 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 77% (130/159) · gap 24% · délai 0.5min · rebond 71% (89/130) (MFE +1.47%)
   - −1.0% : fill 30min 38% · séance 66% (112/159) · gap 10% · délai 6.9min · rebond 67% (75/112) (MFE +1.52%)
   - −1.5% : fill 30min 29% · séance 55% (95/159) · gap 5% · délai 23.4min · rebond 63% (61/95) (MFE +1.48%)
   - −2.0% : fill 30min 19% · séance 42% (78/159) · gap 5% · délai 39.4min · rebond 52% (45/78) (MFE +1.32%)
   - −3.0% : fill 30min 10% · séance 23% (49/159) · gap 4% · délai 50.1min · rebond 64% (35/49) (MFE +1.46%)
   - −4.0% : fill 30min 5% · séance 12% (26/159) · gap 1% · délai 46.7min · rebond 53% (16/26) (MFE +1.13%)
   - −5.0% : fill 30min 3% · séance 7% (15/159) · gap 1% · délai 30.3min · rebond 59% (10/15) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.48%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.31% (p90 −1.66%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −1.85%) → stop au-delà de −1.26% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=811 jambes) : jambe baissière méd −1.06% (p90 −2.3%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 81% (47/55) · rebond 69% (32/47)
      · −2.0% : fill 59% (36/55) · rebond 53% (21/36)
      · −3.0% : fill 37% (25/55) · rebond 68% (18/25)
      · −4.0% : fill 22% (18/55) · rebond 42% (11/18)
      · −5.0% : fill 16% (12/55) · rebond 40% (7/12)
   - **flat** (35 séances) :
      · −1.0% : fill 82% (28/35) · rebond 60% (17/28)
      · −2.0% : fill 55% (20/35) · rebond 42% (9/20)
      · −3.0% : fill 33% (13/35) · rebond 74% (10/13)
      · −4.0% : fill 8% (3/35) · rebond 28% (1/3)
      · −5.0% : fill 2% (1/35) · rebond 100% (1/1)
   - **gap-up** (69 séances) :
      · −1.0% : fill 49% (37/69) · rebond 71% (26/37)
      · −2.0% : fill 26% (22/69) · rebond 60% (15/22)
      · −3.0% : fill 10% (11/69) · rebond 39% (7/11)
      · −4.0% : fill 6% (5/69) · rebond 95% (4/5)
      · −5.0% : fill 4% (2/69) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 60% si les 15 1res min sont vertes (73 cas) · 36% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 60% si début vert vs 37% si rouge (base 48% · écart 22 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **60%** · continue >prix actuel 40% ; creux résiduel méd -1.8% (q20 -2.72%) → **SL/trailing à −2.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.4% → **scale +1.29% / runner +2.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **37%** (continue à baisser 46%) → **RÉDUIRE ~63%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.57%** (au-delà de la MAE q10 -4.57%), cible rebond +1.73% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.63% .. +2.3%] · haut q95 +3.13% · bas q05 -3.93%
   - 60min (n=160) : retour [-3.16% .. +2.6%] · haut q95 +3.37% · bas q05 -4.15%
   - 2h (n=160) : retour [-3.49% .. +2.47%] · haut q95 +3.79% · bas q05 -4.28%
   - 4h (n=160) : retour [-3.39% .. +3.79%] · haut q95 +4.52% · bas q05 -5.06%
   - 6h (n=160) : retour [-3.36% .. +4.61%] · haut q95 +5.27% · bas q05 -5.38%
   - session (n=160) : retour [-4.31% .. +4.08%] · haut q95 +5.89% · bas q05 -5.81%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.91%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 35.8  _(momentum baissier)_
- **ADX** : 29.9  _(tendance etablie)_
- **MACD** : hist 0.024  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 17.1%
- **ATR** : 0.14 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.314  _(distribution)_
- **Vol ratio** : 0.29  _(volume atone)_
- **Choppiness** : 41.2  _(transition)_
- **MA** : MA20 3.45 · MA50 3.94 · MA200 4.98  _(prix < MA20)_
- **Dist MA** : MA20 -3.3% · MA50 -15.5% · MA200 -33.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (896469 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
