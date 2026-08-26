# RHM

**Generated** : 2026-08-26T00:01:18.793689+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €1116.40  

> 🟡 **WAIT-FOR-DIP** — spot +4.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €1116.40 (+4.3% vs entrée) · entrée €1070.42 · stop €1049.02 · T1 €1083.81 · R/R 0.63  
> ↳ P(T1 av. stop) 64 % · EV/risk 0.282 · ¼-Kelly 0.033 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1067.75–€1073.10 (mid €1070.42)
- Spot actuel : €1116.40 (+4.3% au-dessus de la zone — repli à attendre)
- Stop : €1049.02 (stop swing_plan-based (-13.27%))
- Targets : T1 €1083.81 · R/R 0.63 | T2 €1097.19 · R/R 1.25 | T3 €1110.57 · R/R 1.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1049.02


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (13.27 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1274).
   - exécution **9.159 pt plus bas** dans le cas TYPIQUE (médiane), 9.159 au p90, **9.159 au pire**
   - perte réelle **22.429 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 13.27 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0072 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3385** [0.2711 ; 0.4112] _(largeur 14.0 pt, n_eff 173.1)_
   - swing : **0.3447** [0.2961 ; 0.3959] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.3023** [0.2557 ; 0.3522] _(largeur 9.7 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (49.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.86 %** | CVaR **-6.85 %** | vol 3.06 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 2.06 % contre 3.33 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.61 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.847 ; < 1 = le √5 surestime)_
- **β de baisse : 0.4971** (β de hausse 0.5891, asymétrie 0.8439) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.159× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 987.2679 sur atr_grid (2.75 ATR, 11.567 %) — p(stop avant cible) 0.2432 [0.20 ; 0.29], R/R 1.659, perte reelle 22.429 % (gap inclus), CVaR 11.576 %, EV -2.8811 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.11 ATR (stop 2.375 %) — p(stop avant cible) 0.7965 [0.75 ; 0.84], R/R 8.81, perte reelle 4.223 % (gap inclus), EV -1.1974 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 8.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.796, borne haute 0.836 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 0.1 % x 37.20 % + P(rien) 20.3 % x 10.55 % ne couvrent pas P(stop) 79.7 % x 4.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 6.309 %) — p(stop avant cible) 0.4841 [0.43 ; 0.54], R/R 2.457, perte reelle 15.141 % (gap inclus), EV -4.2097 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.21 %) : P(cible) 0.1 % x 37.20 % + P(rien) 51.4 % x 5.96 % ne couvrent pas P(stop) 48.4 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.0 ATR (stop 18.714 %) — p(stop avant cible) 0.0659 [0.04 ; 0.10], R/R 1.659, perte reelle 22.429 % (gap inclus), EV -0.595 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 0.1 % x 37.20 % + P(rien) 93.2 % x 0.89 % ne couvrent pas P(stop) 6.6 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.11 ATR (stop 1.727 %) — p(stop avant cible) 0.8529 [0.81 ; 0.89], R/R 11.294, perte reelle 3.294 % (gap inclus), EV -1.1364 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 11.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.853, borne haute 0.887 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 0.1 % x 37.20 % + P(rien) 14.6 % x 11.25 % ne couvrent pas P(stop) 85.3 % x 3.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.155 %) — p(stop avant cible) 0.7205 [0.67 ; 0.77], R/R 7.173, perte reelle 5.187 % (gap inclus), EV -1.2517 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.721, borne haute 0.766 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.1 % x 37.20 % + P(rien) 27.9 % x 8.82 % ne couvrent pas P(stop) 72.0 % x 5.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 4.206 %) — p(stop avant cible) 0.6308 [0.58 ; 0.68], R/R 5.481, perte reelle 6.788 % (gap inclus), EV -1.3882 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.631, borne haute 0.680 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.39 %) : P(cible) 0.1 % x 37.20 % + P(rien) 36.9 % x 7.78 % ne couvrent pas P(stop) 63.1 % x 6.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 5.258 %) — p(stop avant cible) 0.5632 [0.51 ; 0.61], R/R 3.071, perte reelle 12.114 % (gap inclus), EV -3.7977 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.563, borne haute 0.615 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.80 %) : P(cible) 0.1 % x 37.20 % + P(rien) 43.6 % x 6.88 % ne couvrent pas P(stop) 56.3 % x 12.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 7.361 %) — p(stop avant cible) 0.4051 [0.35 ; 0.46], R/R 2.457, perte reelle 15.141 % (gap inclus), EV -3.0812 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.08 %) : P(cible) 0.1 % x 37.20 % + P(rien) 59.3 % x 5.05 % ne couvrent pas P(stop) 40.5 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.412 %) — p(stop avant cible) 0.3811 [0.33 ; 0.43], R/R 1.659, perte reelle 22.429 % (gap inclus), EV -5.5255 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.53 %) : P(cible) 0.1 % x 37.20 % + P(rien) 61.7 % x 4.80 % ne couvrent pas P(stop) 38.1 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.464 %) — p(stop avant cible) 0.3273 [0.28 ; 0.38], R/R 1.659, perte reelle 22.429 % (gap inclus), EV -4.4115 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.41 %) : P(cible) 0.1 % x 37.20 % + P(rien) 67.1 % x 4.28 % ne couvrent pas P(stop) 32.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.515 %) — p(stop avant cible) 0.2757 [0.23 ; 0.32], R/R 1.659, perte reelle 22.429 % (gap inclus), EV -3.4967 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.50 %) : P(cible) 0.1 % x 37.20 % + P(rien) 72.3 % x 3.64 % ne couvrent pas P(stop) 27.6 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 11.567 %) — p(stop avant cible) 0.2432 [0.20 ; 0.29], R/R 1.659, perte reelle 22.429 % (gap inclus), EV -2.8811 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.88 %) : P(cible) 0.1 % x 37.20 % + P(rien) 75.5 % x 3.33 % ne couvrent pas P(stop) 24.3 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 12.618 %) — p(stop avant cible) 0.1967 [0.16 ; 0.24], R/R 1.659, perte reelle 22.429 % (gap inclus), EV -2.2041 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 0.1 % x 37.20 % + P(rien) 80.2 % x 2.68 % ne couvrent pas P(stop) 19.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 14.721 %) — p(stop avant cible) 0.139 [0.11 ; 0.18], R/R 1.659, perte reelle 22.429 % (gap inclus), EV -1.3763 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.38 %) : P(cible) 0.1 % x 37.20 % + P(rien) 86.0 % x 1.96 % ne couvrent pas P(stop) 13.9 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.0 ATR (stop 18.066 %) — p(stop avant cible) 0.0776 [0.05 ; 0.11], R/R 1.659, perte reelle 22.429 % (gap inclus), EV -0.6915 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 0.1 % x 37.20 % + P(rien) 92.1 % x 1.08 % ne couvrent pas P(stop) 7.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 21.031 %) — p(stop avant cible) 0.0471 [0.03 ; 0.07], R/R 1.659, perte reelle 22.429 % (gap inclus), EV -0.4757 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 21.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 0.1 % x 37.20 % + P(rien) 95.1 % x 0.55 % ne couvrent pas P(stop) 4.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 23.134 %) — p(stop avant cible) 0.0155 [0.01 ; 0.03], R/R 1.608, perte reelle 23.134 % (gap inclus), EV -0.1561 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 23.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.1 % x 37.20 % + P(rien) 98.3 % x 0.15 % ne couvrent pas P(stop) 1.6 % x 23.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 25.237 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 1.474, perte reelle 25.237 % (gap inclus), EV -0.1432 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.1 % x 37.20 % + P(rien) 99.1 % x -0.02 % ne couvrent pas P(stop) 0.7 % x 25.24 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 27.34 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 1.361, perte reelle 27.34 % (gap inclus), EV -0.0958 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.1 % x 37.20 % + P(rien) 99.3 % x -0.00 % ne couvrent pas P(stop) 0.5 % x 27.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 29.443 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 1.264, perte reelle 29.443 % (gap inclus), EV -0.088 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.1 % x 37.20 % + P(rien) 99.4 % x -0.01 % ne couvrent pas P(stop) 0.5 % x 29.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 31.546 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.179, perte reelle 31.546 % (gap inclus), EV 0.0716 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.55 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 33.649 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.106, perte reelle 33.649 % (gap inclus), EV 0.0716 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.65 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1116.4, ATR14 46.9571 (4.206 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.393 ATR = 1.653 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.21 % | 1114.0522 | 89.25 % | 92.1 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.421 % | 1111.7043 | 83.23 % | 87.76 % | 89.72 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.631 % | 1109.3565 | 76.13 % | 82.82 % | 85.57 % | 88.22 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.841 % | 1107.0086 | 69.63 % | 78.38 % | 81.52 % | 85.15 % | 90.95 % | 93.17 % |
| 0.25 ATR | 1.052 % | 1104.6607 | 62.43 % | 72.75 % | 76.58 % | 80.99 % | 88.36 % | 91.36 % |
| 0.35 ATR | 1.472 % | 1099.965 | 53.94 % | 65.94 % | 71.15 % | 76.63 % | 85.77 % | 89.25 % |
| 0.5 ATR | 2.103 % | 1092.9215 | 40.34 % | 54.69 % | 61.36 % | 68.81 % | 80.1 % | 83.62 % |
| 0.75 ATR | 3.155 % | 1081.1822 | 23.67 % | 38.99 % | 46.94 % | 57.23 % | 70.35 % | 76.98 % |
| 1.0 ATR | 4.206 % | 1069.4429 | 13.02 % | 26.75 % | 36.17 % | 48.12 % | 62.09 % | 70.45 % |
| 1.25 ATR | 5.258 % | 1057.7036 | 7.5 % | 18.07 % | 26.48 % | 38.81 % | 53.83 % | 64.12 % |
| 1.5 ATR | 6.309 % | 1045.9643 | 3.94 % | 13.13 % | 20.75 % | 31.49 % | 45.77 % | 56.78 % |
| 2.0 ATR | 8.412 % | 1022.4857 | 1.78 % | 7.01 % | 12.15 % | 20.79 % | 34.03 % | 47.04 % |
| 2.5 ATR | 10.515 % | 999.0072 | 0.49 % | 3.36 % | 6.42 % | 12.67 % | 24.88 % | 37.79 % |
| 3.0 ATR | 12.618 % | 975.5286 | 0.1 % | 1.38 % | 3.85 % | 7.62 % | 17.01 % | 31.16 % |
| 4.0 ATR | 16.824 % | 928.5714 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.46 % | 20.0 % |
| 6.0 ATR | 25.237 % | 834.6572 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.84 ATR | 1.14 ATR | 1.43 ATR |
| **2 s.** | 0.23 ATR | 0.57 ATR | 0.65 ATR | 0.87 ATR | 1.05 ATR | 1.19 ATR | 1.76 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.31 ATR | 1.54 ATR | 2.19 ATR | 2.78 ATR |
| **5 s.** | 0.38 ATR | 0.95 ATR | 1.08 ATR | 1.45 ATR | 1.80 ATR | 2.05 ATR | 2.76 ATR | 3.60 ATR |
| **10 s.** | 0.63 ATR | 1.37 ATR | 1.53 ATR | 2.06 ATR | 2.49 ATR | 2.81 ATR | 3.82 ATR | 4.90 ATR |
| **20 s.** | 0.83 ATR | 1.85 ATR | 2.11 ATR | 2.86 ATR | 3.55 ATR | 4.00 ATR | 5.21 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.449–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.654–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.155 %, prix 1081.1776), p(touche) 38.99 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.795–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.206 %, prix 1069.4442), p(touche) 36.17 % (en stress 95.1 %)  ✅ optimum identifie (65.8 % des re-echantillons)
- **5 seance(s)** : plage utile 1.084–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.258 %, prix 1057.6997), p(touche) 38.81 % (en stress 98.02 %)  ✅ optimum identifie (86.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.533–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.412 %, prix 1022.4885), p(touche) 34.03 % (en stress 96.04 %)  ✅ optimum identifie (99.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.11–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.515 %, prix 999.0106), p(touche) 37.79 % (en stress 98.0 %)  ✅ optimum identifie (99.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.077 | EV/share : €1.645 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 37 % | T3 22 %
- Kelly (position) : f* 0.132 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 49.1 | bear 43.9 | side 7.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.122% → cible +1.25% / stop −2.0%, p_fill 10%, n_eff≈9.3) : P(cible|rempli) **77%** · **EV/risk +0.023** (×p_fill ; si rempli +0.45% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→70% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.17% (p90 6.98%) · excursion haute méd. +2.05% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.674% vs midi 0.943% vs clôture 1.127% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.09 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. -0.194% ; recovery-V 23%
- **σ réalisé intraday** 2.742% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 60% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 1151.1575 (VA 1148.5825–1154.2475 ; dernier close 1152.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 42% · rebond 66% · **stop −3.11%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.58% · baisse 30% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.74%) · haut méd +0.57% · range méd 1.39%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −2.0%) · haut méd +0.67% · range méd 1.8%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.19%) · haut méd +0.88% · range méd 2.07%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −2.62%) · haut méd +1.0% · range méd 2.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1155.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 47% · séance 67% (102/159) · gap 20% · délai 1.0min · rebond 59% (57/102) (MFE +1.19%)
   - −1.0% : fill 30min 36% · séance 60% (90/159) · gap 10% · délai 6.4min · rebond 67% (56/90) (MFE +1.3%)
   - −1.5% : fill 30min 26% · séance 48% (76/159) · gap 7% · délai 21.6min · rebond 63% (45/76) (MFE +1.39%)
   - −2.0% : fill 30min 18% · séance 42% (63/159) · gap 4% · délai 46.9min · rebond 66% (40/63) (MFE +1.6%)
   - −3.0% : fill 30min 7% · séance 21% (31/159) · gap 3% · délai 138.0min · rebond 50% (16/31) (MFE +0.97%)
   - −4.0% : fill 30min 4% · séance 15% (23/159) · gap 2% · délai 174.9min · rebond 69% (14/23) (MFE +1.69%)
   - −5.0% : fill 30min 1% · séance 8% (12/159) · gap 1% · délai 301.9min · rebond 92% (11/12) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.61%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.44% (p90 −1.76%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.77%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=533 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (33 séances) :
      · −1.0% : fill 95% (32/33) · rebond 79% (24/32)
      · −2.0% : fill 83% (28/33) · rebond 66% (19/28)
      · −3.0% : fill 44% (13/33) · rebond 60% (8/13)
      · −4.0% : fill 37% (11/33) · rebond 72% (8/11)
      · −5.0% : fill 25% (7/33) · rebond 100% (7/7)
   - **flat** (17 séances) :
      · −1.0% : fill 77% (11/17) · rebond 75% (9/11)
      · −2.0% : fill 46% (6/17) · rebond 83% (5/6)
      · −3.0% : fill 12% (2/17) · rebond 0% (0/2)
      · −4.0% : fill 12% (2/17) · rebond 62% (1/2)
      · −5.0% : fill 12% (2/17) · rebond 62% (1/2)
   - **gap-up** (109 séances) :
      · −1.0% : fill 45% (47/109) · rebond 55% (23/47)
      · −2.0% : fill 28% (29/109) · rebond 61% (16/29)
      · −3.0% : fill 15% (16/109) · rebond 49% (8/16)
      · −4.0% : fill 8% (10/109) · rebond 67% (5/10)
      · −5.0% : fill 2% (3/109) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 62% si les 15 1res min sont vertes (77 cas) · 33% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:37** → P(séance verte=clôture>ouverture) 73% si début vert vs 19% si rouge (base 47% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 44% ; creux résiduel méd -1.21% (q20 -2.72%) → **SL/trailing à −2.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.76% / q75 +1.81% → **scale +0.76% / runner +1.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **19%** (continue à baisser 59%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.7%** (au-delà de la MAE q10 -3.7%), cible rebond +0.95% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +3.27%] · haut q95 +3.75% · bas q05 -3.11%
   - 60min (n=160) : retour [-2.78% .. +3.22%] · haut q95 +4.4% · bas q05 -3.85%
   - 2h (n=160) : retour [-3.2% .. +3.04%] · haut q95 +4.4% · bas q05 -4.48%
   - 4h (n=160) : retour [-3.4% .. +3.3%] · haut q95 +4.87% · bas q05 -4.63%
   - 6h (n=160) : retour [-4.15% .. +3.3%] · haut q95 +4.95% · bas q05 -5.04%
   - session (n=160) : retour [-5.21% .. +3.79%] · haut q95 +5.07% · bas q05 -5.93%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 32.1  _(momentum baissier)_
- **ADX** : 19.4  _(pas de tendance nette)_
- **MACD** : hist -8.325  _(bearish_recent)_
- **BB** : %B 0.08 · largeur 9.9%
- **ATR** : 46.96 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.171  _(distribution)_
- **Vol ratio** : 0.22  _(volume atone)_
- **Choppiness** : 62.1  _(marche en range (choppy))_
- **MA** : MA20 1164.99 · MA50 1092.93 · MA200 1412.01  _(prix < MA20)_
- **Dist MA** : MA20 -4.2% · MA50 +2.1% · MA200 -20.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (817561 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
