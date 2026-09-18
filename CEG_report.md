# CEG

**Generated** : 2026-09-18T00:42:49.370018+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $262.69  

> 🟡 **WAIT-FOR-DIP** — spot +4.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $262.69 (+4.3% vs entrée) · entrée $251.91 · stop $248.14 · T1 $255.37 · R/R 0.92  
> ↳ P(T1 av. stop) 62 % · EV/risk 0.476 · ¼-Kelly 0.026 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +4.0 % ≠ (strike 270.0 − spot 262.69)/spot = +2.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $251.22–$252.61 (mid $251.91)
- Spot actuel : $262.69 (+4.3% au-dessus de la zone — repli à attendre)
- Stop : $248.14 (stop swing_plan-based (-12.31%))
- Targets : T1 $255.37 · R/R 0.92 | T2 $258.83 · R/R 1.84 | T3 $262.29 · R/R 2.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $248.14


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.97 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.31 %)** : le gap seul le franchit 0.086 % des séances (1 fois sur 1169).
   - exécution **3.514 pt plus bas** dans le cas TYPIQUE (médiane), 3.514 au p90, **3.514 au pire**
   - perte réelle **15.824 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 12.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.003 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.844 % | p01 -4.435 % | pire -15.824 % _(sur 1169 séances)_
- **P(stop avant cible)** _(source : daily, 1170 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4332** [0.361 ; 0.5076] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3799** [0.3299 ; 0.4319] _(largeur 10.2 pt, n_eff 345.4)_
   - deep : **0.3108** [0.2637 ; 0.361] _(largeur 9.7 pt, n_eff 345.4)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.28 %** | CVaR **-6.31 %** | vol 2.86 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.29 % contre 2.74 % aujourd'hui, rapport 1.93)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.91 % vs -9.6 % si l'on extrapolait par √5 _(rapport 1.032 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1808** (β de hausse 1.1864, asymétrie 0.9953) vs SPY — 539 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 233.0572 sur atr_grid (2.75 ATR, 11.281 %) — p(stop avant cible) 0.2263 [0.18 ; 0.27], R/R 2.692, perte reelle 15.824 % (gap inclus), CVaR 11.285 %, EV -1.1033 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.153 %) — p(stop avant cible) 0.4866 [0.43 ; 0.54], R/R 4.566, perte reelle 9.329 % (gap inclus), EV -1.6209 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.62 %) : P(cible) 0.1 % x 42.60 % + P(rien) 51.2 % x 5.59 % ne couvrent pas P(stop) 48.7 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.026 %) — p(stop avant cible) 0.8963 [0.86 ; 0.93], R/R 19.161, perte reelle 2.223 % (gap inclus), EV -1.0479 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 19.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.896, borne haute 0.925 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 0.0 % x 42.60 % + P(rien) 10.4 % x 9.11 % ne couvrent pas P(stop) 89.6 % x 2.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.051 %) — p(stop avant cible) 0.7918 [0.75 ; 0.83], R/R 11.067, perte reelle 3.849 % (gap inclus), EV -1.1911 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 11.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.792, borne haute 0.832 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.1 % x 42.60 % + P(rien) 20.7 % x 8.75 % ne couvrent pas P(stop) 79.2 % x 3.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.077 %) — p(stop avant cible) 0.6825 [0.63 ; 0.73], R/R 7.811, perte reelle 5.453 % (gap inclus), EV -1.2004 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.682, borne haute 0.730 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 0.1 % x 42.60 % + P(rien) 31.6 % x 7.80 % ne couvrent pas P(stop) 68.2 % x 5.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 4.102 %) — p(stop avant cible) 0.606 [0.55 ; 0.66], R/R 6.878, perte reelle 6.193 % (gap inclus), EV -0.9458 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.606, borne haute 0.656 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 0.1 % x 42.60 % + P(rien) 39.3 % x 7.01 % ne couvrent pas P(stop) 60.6 % x 6.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 5.128 %) — p(stop avant cible) 0.551 [0.50 ; 0.60], R/R 5.409, perte reelle 7.875 % (gap inclus), EV -1.4626 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.551, borne haute 0.603 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.46 %) : P(cible) 0.1 % x 42.60 % + P(rien) 44.8 % x 6.30 % ne couvrent pas P(stop) 55.1 % x 7.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 7.179 %) — p(stop avant cible) 0.4135 [0.36 ; 0.47], R/R 3.799, perte reelle 11.211 % (gap inclus), EV -1.6974 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.70 %) : P(cible) 0.1 % x 42.60 % + P(rien) 58.5 % x 4.93 % ne couvrent pas P(stop) 41.3 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.204 %) — p(stop avant cible) 0.3447 [0.30 ; 0.40], R/R 3.309, perte reelle 12.871 % (gap inclus), EV -1.6273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.63 %) : P(cible) 0.1 % x 42.60 % + P(rien) 65.4 % x 4.21 % ne couvrent pas P(stop) 34.5 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.23 %) — p(stop avant cible) 0.3001 [0.25 ; 0.35], R/R 3.309, perte reelle 12.871 % (gap inclus), EV -1.1761 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 0.1 % x 42.60 % + P(rien) 69.9 % x 3.77 % ne couvrent pas P(stop) 30.0 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.255 %) — p(stop avant cible) 0.2586 [0.21 ; 0.31], R/R 2.692, perte reelle 15.824 % (gap inclus), EV -1.5002 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.50 %) : P(cible) 0.1 % x 42.60 % + P(rien) 74.0 % x 3.43 % ne couvrent pas P(stop) 25.9 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 11.281 %) — p(stop avant cible) 0.2263 [0.18 ; 0.27], R/R 2.692, perte reelle 15.824 % (gap inclus), EV -1.1033 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 0.1 % x 42.60 % + P(rien) 77.2 % x 3.14 % ne couvrent pas P(stop) 22.6 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 12.306 %) — p(stop avant cible) 0.1934 [0.15 ; 0.24], R/R 2.692, perte reelle 15.824 % (gap inclus), EV -0.7507 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 0.1 % x 42.60 % + P(rien) 80.5 % x 2.80 % ne couvrent pas P(stop) 19.3 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 14.357 %) — p(stop avant cible) 0.1332 [0.10 ; 0.17], R/R 2.692, perte reelle 15.824 % (gap inclus), EV -0.1639 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.1 % x 42.60 % + P(rien) 86.6 % x 2.18 % ne couvrent pas P(stop) 13.3 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 16.408 %) — p(stop avant cible) 0.0634 [0.04 ; 0.09], R/R 2.596, perte reelle 16.408 % (gap inclus), EV 0.1226 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.41 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 18.459 %) — p(stop avant cible) 0.0421 [0.02 ; 0.07], R/R 2.308, perte reelle 18.459 % (gap inclus), EV 0.0951 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.46 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 20.51 %) — p(stop avant cible) 0.0177 [0.01 ; 0.04], R/R 2.077, perte reelle 20.51 % (gap inclus), EV 0.223 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.51 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 22.561 %) — p(stop avant cible) 0.0097 [0.00 ; 0.02], R/R 1.888, perte reelle 22.561 % (gap inclus), EV 0.2621 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.56 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 24.612 %) — p(stop avant cible) 0.0077 [0.00 ; 0.02], R/R 1.731, perte reelle 24.612 % (gap inclus), EV 0.2802 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.61 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 26.663 %) — p(stop avant cible) 0.0065 [0.00 ; 0.02], R/R 1.598, perte reelle 26.663 % (gap inclus), EV 0.2756 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.66 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 28.714 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 1.483, perte reelle 28.714 % (gap inclus), EV 0.2746 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 30.765 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.385, perte reelle 30.765 % (gap inclus), EV 0.2859 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.76 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 32.816 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.298, perte reelle 32.816 % (gap inclus), EV 0.2854 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.82 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 262.69, ATR14 10.7756 (4.102 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.388 ATR = 1.592 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.205 % | 262.1512 | 91.53 % | 94.49 % | 95.48 % | 96.57 % | 97.56 % | 97.98 % |
| 0.1 ATR | 0.41 % | 261.6124 | 85.48 % | 90.31 % | 92.28 % | 93.92 % | 95.56 % | 96.74 % |
| 0.15 ATR | 0.615 % | 261.0737 | 78.99 % | 86.01 % | 88.31 % | 90.39 % | 93.67 % | 95.39 % |
| 0.2 ATR | 0.82 % | 260.5349 | 72.06 % | 80.62 % | 83.9 % | 86.52 % | 91.22 % | 94.04 % |
| 0.25 ATR | 1.026 % | 259.9961 | 65.13 % | 75.0 % | 79.05 % | 82.76 % | 88.44 % | 92.02 % |
| 0.35 ATR | 1.436 % | 258.9186 | 53.8 % | 65.53 % | 71.11 % | 76.35 % | 83.89 % | 88.43 % |
| 0.5 ATR | 2.051 % | 257.3022 | 38.72 % | 52.53 % | 59.1 % | 65.75 % | 76.56 % | 82.58 % |
| 0.75 ATR | 3.077 % | 254.6083 | 20.35 % | 36.34 % | 44.76 % | 52.82 % | 66.0 % | 75.51 % |
| 1.0 ATR | 4.102 % | 251.9144 | 11.22 % | 24.01 % | 32.97 % | 42.87 % | 56.89 % | 69.1 % |
| 1.25 ATR | 5.128 % | 249.2206 | 5.72 % | 16.08 % | 24.15 % | 35.14 % | 50.78 % | 62.92 % |
| 1.5 ATR | 6.153 % | 246.5267 | 2.75 % | 10.68 % | 17.42 % | 28.84 % | 44.0 % | 56.97 % |
| 2.0 ATR | 8.204 % | 241.1389 | 0.88 % | 4.41 % | 9.37 % | 17.9 % | 31.11 % | 45.73 % |
| 2.5 ATR | 10.255 % | 235.7511 | 0.44 % | 2.31 % | 4.85 % | 11.05 % | 20.78 % | 35.96 % |
| 3.0 ATR | 12.306 % | 230.3633 | 0.0 % | 1.1 % | 2.87 % | 6.96 % | 15.22 % | 28.09 % |
| 4.0 ATR | 16.408 % | 219.5878 | 0.0 % | 0.22 % | 0.88 % | 2.76 % | 6.67 % | 14.04 % |
| 6.0 ATR | 24.612 % | 198.0366 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.78 % | 2.7 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.05 ATR | 1.31 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.00 ATR | 1.23 ATR | 1.40 ATR | 1.96 ATR | 2.48 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.95 ATR | 1.33 ATR | 1.68 ATR | 1.90 ATR | 2.63 ATR | 3.47 ATR |
| **10 s.** | 0.54 ATR | 1.28 ATR | 1.46 ATR | 1.93 ATR | 2.30 ATR | 2.57 ATR | 3.61 ATR | 4.57 ATR |
| **20 s.** | 0.77 ATR | 1.81 ATR | 2.04 ATR | 2.69 ATR | 3.22 ATR | 3.58 ATR | 4.71 ATR | 5.59 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.438–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.051 %, prix 257.3022), p(touche) 38.72 % (en stress 82.42 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.616–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.077 %, prix 254.607), p(touche) 36.34 % (en stress 87.91 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.746–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.077 %, prix 254.607), p(touche) 44.76 % (en stress 97.8 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.946–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.102 %, prix 251.9145), p(touche) 42.87 % (en stress 96.7 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.463–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.153 %, prix 246.5267), p(touche) 44.0 % (en stress 98.89 %)  ✅ optimum identifie (74.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.037–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.255 %, prix 235.7511), p(touche) 35.96 % (en stress 95.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (88.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.106 | EV/share : $0.402 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 23 % | T3 6 %
- Kelly (position) : f* 0.104 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 28.9 | bear 13.8 | side 57.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→72% · +2.0%→41% · +3.0%→19% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.29% (p90 5.36%) · excursion haute méd. +1.62% / basse méd. −1.05%
- Profil de vol intra : ouverture 2.272% vs midi 0.634% vs clôture 0.766% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑2%/↓0% ; spike-down 43% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.145 ; mean-reverting — autocorr -0.05)_ ; drift intra méd. 0.205% ; recovery-V 6%
- **σ réalisé intraday** 2.217% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 60% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 294.8769 (VA 290.6501–297.1824 ; dernier close 298.95)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 41% · **stop −2.19%** sous le fill (sous le bruit) · cible +0.73% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 37% (gap-down >1% 11% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.78%) · haut méd +0.88% · range méd 1.53%
- Excursion ouverture 15min (n=160) : bas méd −0.6% (p90 −2.1%) · haut méd +1.05% · range méd 1.91%
- Excursion ouverture 30min (n=160) : bas méd −0.65% (p90 −2.52%) · haut méd +1.26% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −0.84% (p90 −2.75%) · haut méd +1.39% · range méd 2.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 298.96 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 62% (105/159) · gap 19% · délai 1.4min · rebond 57% (61/105) (MFE +1.13%)
   - −1.0% : fill 30min 32% · séance 49% (88/159) · gap 11% · délai 5.3min · rebond 47% (46/88) (MFE +0.97%)
   - −1.5% : fill 30min 24% · séance 38% (70/159) · gap 8% · délai 10.4min · rebond 45% (36/70) (MFE +0.86%)
   - −2.0% : fill 30min 20% · séance 33% (59/159) · gap 3% · délai 15.3min · rebond 53% (33/59) (MFE +1.07%)
   - −3.0% : fill 30min 6% · séance 16% (31/159) · gap 1% · délai 46.4min · rebond 41% (13/31) (MFE +0.73%)
   - −4.0% : fill 30min 3% · séance 9% (18/159) · gap 1% · délai 42.9min · rebond 63% (11/18) (MFE +1.2%)
   - −5.0% : fill 30min 2% · séance 4% (11/159) · gap 0% · délai 46.0min · rebond 88% (9/11) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −0.98%) → stop au-delà de −0.82% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −0.98%) → stop au-delà de −0.87% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.52% (p90 −1.17%) → stop au-delà de −0.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.06% (p90 −2.57%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 82% (38/42) · rebond 68% (25/38)
      · −2.0% : fill 65% (31/42) · rebond 56% (18/31)
      · −3.0% : fill 32% (16/42) · rebond 27% (6/16)
      · −4.0% : fill 28% (13/42) · rebond 64% (8/13)
      · −5.0% : fill 14% (9/42) · rebond 87% (7/9)
   - **flat** (28 séances) :
      · −1.0% : fill 53% (20/28) · rebond 12% (5/20)
      · −2.0% : fill 34% (12/28) · rebond 46% (6/12)
      · −3.0% : fill 16% (7/28) · rebond 22% (2/7)
      · −4.0% : fill 5% (3/28) · rebond 42% (2/3)
      · −5.0% : fill 1% (1/28) · rebond 100% (1/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 32% (30/89) · rebond 41% (16/30)
      · −2.0% : fill 18% (16/89) · rebond 51% (9/16)
      · −3.0% : fill 8% (8/89) · rebond 80% (5/8)
      · −4.0% : fill 1% (2/89) · rebond 76% (1/2)
      · −5.0% : fill 0% (1/89) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 64% si les 15 1res min sont vertes (93 cas) · 36% si rouges (67 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 85% si début vert vs 9% si rouge (base 52% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **85%** · continue >prix actuel 49% ; creux résiduel méd -0.97% (q20 -1.87%) → **SL/trailing à −1.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.92% / q75 +1.46% → **scale +0.92% / runner +1.46%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **9%** (continue à baisser 67%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.33%** (au-delà de la MAE q10 -2.33%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.08% .. +2.26%] · haut q95 +2.56% · bas q05 -3.33%
   - 60min (n=160) : retour [-3.64% .. +2.77%] · haut q95 +3.06% · bas q05 -4.54%
   - 2h (n=160) : retour [-3.69% .. +3.01%] · haut q95 +4.2% · bas q05 -4.61%
   - 4h (n=160) : retour [-2.93% .. +3.48%] · haut q95 +4.39% · bas q05 -4.64%
   - 6h (n=160) : retour [-3.85% .. +3.99%] · haut q95 +5.02% · bas q05 -4.7%
   - session (n=160) : retour [-3.6% .. +3.78%] · haut q95 +5.18% · bas q05 -4.7%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 5.6% / strong 2.5%) · base = 13 séances trend-up (n_eff 8.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **46%**. Lecture précoce 30 min : signature présente → 19% vs absente 6% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.09% (p75 1.89% / p90 2.34%) · ~1.0 replis/séance, durée méd 156.17 min. P(nouveau plus-haut après repli) :
   - −0.5% → **66%** (reprise méd 24.0 min, n=25)
   - −1.0% → **65%** (reprise méd 179.97 min, n=12)
   - −1.5% → **48%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.34%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +3.6% (q75 +4.62% / q95 +6.15%), MFE méd +4.44% / q90 +5.76%
   - Échelle scale-out : +4.44% (33%) / +5.28% (33%) / +5.76% (34%)
- **DÉSARMER** : repli > **−2.34%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.76% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 97% du temps (retour médian dernière heure +0.44%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 38.3  _(momentum baissier)_
- **ADX** : 19.3  _(pas de tendance nette)_
- **MACD** : hist -3.763  _(bearish_recent)_
- **BB** : %B 0.16 · largeur 16.9%
- **ATR** : 10.78 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.24  _(distribution)_
- **Vol ratio** : 1.07  _(volume normal)_
- **Choppiness** : 41.0  _(transition)_
- **MA** : MA20 278.79 · MA50 270.85 · MA200 292.54  _(prix < MA20)_
- **Dist MA** : MA20 -5.8% · MA50 -3.0% · MA200 -10.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (760424 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
