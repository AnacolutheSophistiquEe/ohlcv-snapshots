# CEG

**Generated** : 2026-09-23T00:41:53.151909+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $263.45  

> 🟡 **WAIT-FOR-DIP** — spot +4.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $263.45 (+4.3% vs entrée) · entrée $252.65 · stop $248.86 · T1 $256.37 · R/R 0.98  
> ↳ P(T1 av. stop) 62 % · EV/risk 0.515 · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +1.1 % ≠ (strike 265.0 − spot 263.45)/spot = +0.6 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $251.90–$253.39 (mid $252.65)
- Spot actuel : $263.45 (+4.3% au-dessus de la zone — repli à attendre)
- Stop : $248.86 (stop swing_plan-based (-12.3%))
- Targets : T1 $256.37 · R/R 0.98 | T2 $260.10 · R/R 1.97 | T3 $263.83 · R/R 2.95
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $248.86


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.96 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.3 %)** : le gap seul le franchit 0.085 % des séances (1 fois sur 1172).
   - exécution **3.524 pt plus bas** dans le cas TYPIQUE (médiane), 3.524 au p90, **3.524 au pire**
   - perte réelle **15.824 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 12.3 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.003 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.839 % | p01 -4.435 % | pire -15.824 % _(sur 1172 séances)_
- **P(stop avant cible)** _(source : daily, 1173 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4582** [0.3852 ; 0.5326] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4016** [0.3509 ; 0.4539] _(largeur 10.3 pt, n_eff 345.4)_
   - deep : **0.3228** [0.2751 ; 0.3734] _(largeur 9.8 pt, n_eff 345.4)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.28 %** | CVaR **-6.31 %** | vol 2.87 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.22 % contre 2.70 % aujourd'hui, rapport 1.94)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.07 % vs -9.59 % si l'on extrapolait par √5 _(rapport 1.049 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1818** (β de hausse 1.1943, asymétrie 0.9896) vs SPY — 540 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 252.6475 sur atr_grid (1.0 ATR, 4.1 %) — p(stop avant cible) 0.6135 [0.56 ; 0.66], R/R 6.811, perte reelle 6.193 % (gap inclus), CVaR 4.129 %, EV -1.0477 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2286 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.614, borne haute 0.664 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 4.13 % > budget 4.04 %
- Budget de queue : **4.04 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.313 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 45.0 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.151 %) — p(stop avant cible) 0.4954 [0.44 ; 0.55], R/R 4.521, perte reelle 9.329 % (gap inclus), EV -1.7528 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 6.16 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.75 %) : P(cible) 0.1 % x 42.18 % + P(rien) 50.3 % x 5.59 % ne couvrent pas P(stop) 49.5 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.025 %) — p(stop avant cible) 0.8981 [0.86 ; 0.93], R/R 18.975, perte reelle 2.223 % (gap inclus), EV -1.0683 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 18.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.898, borne haute 0.927 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 0.0 % x 42.18 % + P(rien) 10.2 % x 9.11 % ne couvrent pas P(stop) 89.8 % x 2.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.05 %) — p(stop avant cible) 0.7954 [0.75 ; 0.84], R/R 10.959, perte reelle 3.849 % (gap inclus), EV -1.2369 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 10.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.795, borne haute 0.835 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 0.1 % x 42.18 % + P(rien) 20.4 % x 8.75 % ne couvrent pas P(stop) 79.5 % x 3.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.075 %) — p(stop avant cible) 0.688 [0.64 ; 0.74], R/R 7.735, perte reelle 5.453 % (gap inclus), EV -1.2738 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.688, borne haute 0.735 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 0.1 % x 42.18 % + P(rien) 31.1 % x 7.80 % ne couvrent pas P(stop) 68.8 % x 5.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 4.1 %) — p(stop avant cible) 0.6135 [0.56 ; 0.66], R/R 6.811, perte reelle 6.193 % (gap inclus), EV -1.0477 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.614, borne haute 0.664 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 4.13 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 0.1 % x 42.18 % + P(rien) 38.5 % x 7.00 % ne couvrent pas P(stop) 61.4 % x 6.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 5.125 %) — p(stop avant cible) 0.5587 [0.51 ; 0.61], R/R 5.356, perte reelle 7.875 % (gap inclus), EV -1.5723 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.559, borne haute 0.610 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.14 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 0.1 % x 42.18 % + P(rien) 44.0 % x 6.30 % ne couvrent pas P(stop) 55.9 % x 7.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 7.176 %) — p(stop avant cible) 0.4236 [0.37 ; 0.48], R/R 3.762, perte reelle 11.211 % (gap inclus), EV -1.8609 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 7.19 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.86 %) : P(cible) 0.1 % x 42.18 % + P(rien) 57.5 % x 4.93 % ne couvrent pas P(stop) 42.4 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.201 %) — p(stop avant cible) 0.356 [0.31 ; 0.41], R/R 3.277, perte reelle 12.871 % (gap inclus), EV -1.8209 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 8.21 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.82 %) : P(cible) 0.1 % x 42.18 % + P(rien) 64.3 % x 4.21 % ne couvrent pas P(stop) 35.6 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.226 %) — p(stop avant cible) 0.3121 [0.27 ; 0.36], R/R 3.277, perte reelle 12.871 % (gap inclus), EV -1.3763 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 9.23 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.38 %) : P(cible) 0.1 % x 42.18 % + P(rien) 68.7 % x 3.77 % ne couvrent pas P(stop) 31.2 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.251 %) — p(stop avant cible) 0.2714 [0.23 ; 0.32], R/R 2.666, perte reelle 15.824 % (gap inclus), EV -1.7469 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.26 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.75 %) : P(cible) 0.1 % x 42.18 % + P(rien) 72.7 % x 3.43 % ne couvrent pas P(stop) 27.1 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 11.276 %) — p(stop avant cible) 0.2339 [0.19 ; 0.28], R/R 2.666, perte reelle 15.824 % (gap inclus), EV -1.3251 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.28 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.33 %) : P(cible) 0.1 % x 42.18 % + P(rien) 76.5 % x 3.04 % ne couvrent pas P(stop) 23.4 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 12.301 %) — p(stop avant cible) 0.2015 [0.16 ; 0.25], R/R 2.666, perte reelle 15.824 % (gap inclus), EV -0.9773 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.30 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 0.1 % x 42.18 % + P(rien) 79.7 % x 2.71 % ne couvrent pas P(stop) 20.2 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 14.351 %) — p(stop avant cible) 0.1367 [0.10 ; 0.18], R/R 2.666, perte reelle 15.824 % (gap inclus), EV -0.3693 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.35 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 0.1 % x 42.18 % + P(rien) 86.2 % x 2.02 % ne couvrent pas P(stop) 13.7 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 16.402 %) — p(stop avant cible) 0.0681 [0.05 ; 0.10], R/R 2.572, perte reelle 16.402 % (gap inclus), EV -0.0907 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.40 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.1 % x 42.18 % + P(rien) 93.1 % x 1.04 % ne couvrent pas P(stop) 6.8 % x 16.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 18.452 %) — p(stop avant cible) 0.0413 [0.02 ; 0.07], R/R 2.286, perte reelle 18.452 % (gap inclus), EV -0.1008 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.45 % > budget 4.04 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.1 % x 42.18 % + P(rien) 95.7 % x 0.63 % ne couvrent pas P(stop) 4.1 % x 18.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 20.502 %) — p(stop avant cible) 0.0174 [0.01 ; 0.04], R/R 2.057, perte reelle 20.502 % (gap inclus), EV 0.0232 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.50 % > budget 4.04 %
   - ⚪ atr_grid a 5.5 ATR (stop 22.552 %) — p(stop avant cible) 0.0095 [0.00 ; 0.02], R/R 1.87, perte reelle 22.552 % (gap inclus), EV 0.0625 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.55 % > budget 4.04 %
   - ⚪ atr_grid a 6.0 ATR (stop 24.602 %) — p(stop avant cible) 0.0076 [0.00 ; 0.02], R/R 1.715, perte reelle 24.602 % (gap inclus), EV 0.0788 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.60 % > budget 4.04 %
   - ⚪ atr_grid a 6.5 ATR (stop 26.653 %) — p(stop avant cible) 0.0064 [0.00 ; 0.02], R/R 1.583, perte reelle 26.653 % (gap inclus), EV 0.0748 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.65 % > budget 4.04 %
   - ⚪ atr_grid a 7.0 ATR (stop 28.703 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 1.47, perte reelle 28.703 % (gap inclus), EV 0.0746 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.70 % > budget 4.04 %
   - ⚪ atr_grid a 7.5 ATR (stop 30.753 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.372, perte reelle 30.753 % (gap inclus), EV 0.0844 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.75 % > budget 4.04 %
   - ⚪ atr_grid a 8.0 ATR (stop 32.803 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.286, perte reelle 32.803 % (gap inclus), EV 0.0843 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.80 % > budget 4.04 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 263.45, ATR14 10.8025 (4.1 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.389 ATR = 1.595 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.205 % | 262.9099 | 91.56 % | 94.51 % | 95.49 % | 96.59 % | 97.56 % | 97.98 % |
| 0.1 ATR | 0.41 % | 262.3698 | 85.53 % | 90.34 % | 92.31 % | 93.94 % | 95.57 % | 96.75 % |
| 0.15 ATR | 0.615 % | 261.8296 | 79.06 % | 86.06 % | 88.35 % | 90.42 % | 93.69 % | 95.41 % |
| 0.2 ATR | 0.82 % | 261.2895 | 72.15 % | 80.68 % | 83.96 % | 86.56 % | 91.25 % | 94.06 % |
| 0.25 ATR | 1.025 % | 260.7494 | 65.24 % | 75.08 % | 79.12 % | 82.82 % | 88.48 % | 92.05 % |
| 0.35 ATR | 1.435 % | 259.6691 | 53.95 % | 65.64 % | 71.21 % | 76.43 % | 83.94 % | 88.47 % |
| 0.5 ATR | 2.05 % | 258.0488 | 38.93 % | 52.69 % | 59.23 % | 65.86 % | 76.63 % | 82.64 % |
| 0.75 ATR | 3.075 % | 255.3481 | 20.29 % | 36.55 % | 44.95 % | 52.97 % | 66.11 % | 75.59 % |
| 1.0 ATR | 4.1 % | 252.6475 | 11.18 % | 23.93 % | 33.08 % | 43.06 % | 57.03 % | 69.2 % |
| 1.25 ATR | 5.125 % | 249.9469 | 5.7 % | 16.03 % | 24.18 % | 35.35 % | 50.94 % | 63.05 % |
| 1.5 ATR | 6.151 % | 247.2463 | 2.74 % | 10.65 % | 17.36 % | 28.96 % | 44.19 % | 57.11 % |
| 2.0 ATR | 8.201 % | 241.845 | 0.88 % | 4.39 % | 9.34 % | 18.06 % | 31.34 % | 45.8 % |
| 2.5 ATR | 10.251 % | 236.4438 | 0.44 % | 2.31 % | 4.84 % | 11.12 % | 21.04 % | 35.83 % |
| 3.0 ATR | 12.301 % | 231.0425 | 0.0 % | 1.1 % | 2.86 % | 7.05 % | 15.5 % | 28.0 % |
| 4.0 ATR | 16.402 % | 220.24 | 0.0 % | 0.22 % | 0.88 % | 2.75 % | 6.87 % | 14.0 % |
| 6.0 ATR | 24.602 % | 198.635 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.78 % | 2.69 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.05 ATR | 1.31 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.12 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.00 ATR | 1.23 ATR | 1.40 ATR | 1.96 ATR | 2.48 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.95 ATR | 1.34 ATR | 1.68 ATR | 1.91 ATR | 2.64 ATR | 3.48 ATR |
| **10 s.** | 0.54 ATR | 1.28 ATR | 1.47 ATR | 1.94 ATR | 2.31 ATR | 2.59 ATR | 3.64 ATR | 4.61 ATR |
| **20 s.** | 0.77 ATR | 1.81 ATR | 2.04 ATR | 2.68 ATR | 3.21 ATR | 3.57 ATR | 4.71 ATR | 5.59 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.05 %, prix 258.0493), p(touche) 38.93 % (en stress 81.52 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.619–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.075 %, prix 255.3489), p(touche) 36.55 % (en stress 88.04 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.749–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.075 %, prix 255.3489), p(touche) 44.95 % (en stress 97.8 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.951–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.1 %, prix 252.6486), p(touche) 43.06 % (en stress 96.7 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.47–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.151 %, prix 247.2452), p(touche) 44.19 % (en stress 98.9 %)  ✅ optimum identifie (73.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.04–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.251 %, prix 236.4438), p(touche) 35.83 % (en stress 95.56 %)  ✅ optimum identifie (87.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.108 | EV/share : $0.409 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 18 % | T3 6 %
- Kelly (position) : f* 0.09 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.8 | bear 27.7 | side 60.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 40.5  _(momentum baissier)_
- **ADX** : 21.3  _(pas de tendance nette)_
- **MACD** : hist -3.214  _(pas de croisement recent)_
- **BB** : %B 0.25 · largeur 19.7%
- **ATR** : 10.8 (28.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.281  _(distribution)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 38.2  _(marche directionnel)_
- **MA** : MA20 276.85 · MA50 271.28 · MA200 291.05  _(prix < MA20)_
- **Dist MA** : MA20 -4.8% · MA50 -2.9% · MA200 -9.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (851663 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
