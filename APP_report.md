# APP

**Generated** : 2026-08-22T18:31:07.385237+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $305.77  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $305.77 (+0.5% vs entrée) · entrée $304.36 · stop $298.41 · T1 $313.84 · R/R 1.59  
> ↳ P(T1 av. stop) 25 % · EV/risk -0.419 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.17). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.
>   - **[LOW]** meta — meta.currency absent — symbole devise déduit du ticker (fallback).


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : — | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $302.95–$305.77 (mid $304.36)
- Spot actuel : $305.77 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $298.41 (stop swing_plan-based (-7.41%))
- Targets : T1 $313.84 · R/R 1.59 | T2 $323.31 · R/R 3.18 | T3 $332.79 · R/R 4.78
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $298.41


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.06 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.41 %)** : le gap seul le franchit 0.957 % des séances (12 fois sur 1254).
   - exécution **4.673 pt plus bas** dans le cas TYPIQUE (médiane), 10.932 au p90, **11.582 au pire**
   - perte réelle **12.346 %** en moyenne _(tirée par la queue)_, jusqu'à **18.992 %** — au lieu des 7.41 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0472 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 12 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.246 % | p01 -7.103 % | pire -18.992 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1651** [0.1156 ; 0.2257] _(largeur 11.0 pt, n_eff 173.1)_
   - swing : **0.5398** [0.4871 ; 0.5918] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5655** [0.5129 ; 0.617] _(largeur 10.4 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-6.47 %** | CVaR **-10.31 %** | vol 4.85 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 7.29 % contre 4.51 % aujourd'hui, rapport 1.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.38 % vs -15.6 % si l'on extrapolait par √5 _(rapport 1.05 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2203** (β de hausse 1.8743, asymétrie 1.1846) vs SPY — 575 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 292.765 sur support (0.13 ATR, 4.253 %) — p(stop avant cible) 0.7397 [0.69 ; 0.78], R/R 4.98, perte reelle 7.513 % (gap inclus), CVaR 4.352 %, EV -1.8624 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4637 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.740, borne haute 0.784 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 4.35 % > budget 4.19 %
- Budget de queue : **4.19 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.13 ATR (stop 4.253 %) — p(stop avant cible) 0.7397 [0.69 ; 0.78], R/R 4.98, perte reelle 7.513 % (gap inclus), EV -1.8624 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.740, borne haute 0.784 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 4.35 % > budget 4.19 %
      - ⚠ support DETECTE a 0.13 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.86 %) : P(cible) 1.1 % x 37.41 % + P(rien) 24.9 % x 13.16 % ne couvrent pas P(stop) 74.0 % x 7.51 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 9.723 %) — p(stop avant cible) 0.5035 [0.45 ; 0.56], R/R 2.651, perte reelle 14.112 % (gap inclus), EV -1.5183 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.503, borne haute 0.556 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 9.75 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.52 %) : P(cible) 1.5 % x 37.41 % + P(rien) 48.1 % x 10.43 % ne couvrent pas P(stop) 50.3 % x 14.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.482 %) — p(stop avant cible) 0.6623 [0.61 ; 0.71], R/R 3.322, perte reelle 11.261 % (gap inclus), EV -3.0198 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.662, borne haute 0.711 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.54 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.02 %) : P(cible) 1.4 % x 37.41 % + P(rien) 32.4 % x 12.10 % ne couvrent pas P(stop) 66.2 % x 11.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 11.343 %) — p(stop avant cible) 0.4281 [0.38 ; 0.48], R/R 2.568, perte reelle 14.568 % (gap inclus), EV -0.8064 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 11.36 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 1.5 % x 37.41 % + P(rien) 55.7 % x 8.73 % ne couvrent pas P(stop) 42.8 % x 14.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 12.963 %) — p(stop avant cible) 0.3747 [0.32 ; 0.43], R/R 2.159, perte reelle 17.326 % (gap inclus), EV -1.1632 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.97 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 1.5 % x 37.41 % + P(rien) 61.0 % x 7.80 % ne couvrent pas P(stop) 37.5 % x 17.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 16.204 %) — p(stop avant cible) 0.2928 [0.25 ; 0.34], R/R 1.98, perte reelle 18.898 % (gap inclus), EV -0.8092 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.21 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 1.5 % x 37.41 % + P(rien) 69.2 % x 6.00 % ne couvrent pas P(stop) 29.3 % x 18.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 19.445 %) — p(stop avant cible) 0.1893 [0.15 ; 0.23], R/R 1.924, perte reelle 19.445 % (gap inclus), EV -0.0593 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.44 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 1.5 % x 37.41 % + P(rien) 79.5 % x 3.84 % ne couvrent pas P(stop) 18.9 % x 19.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 22.686 %) — p(stop avant cible) 0.1142 [0.08 ; 0.15], R/R 1.649, perte reelle 22.686 % (gap inclus), EV -0.1349 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 22.69 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 1.5 % x 37.41 % + P(rien) 87.1 % x 2.17 % ne couvrent pas P(stop) 11.4 % x 22.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 25.927 %) — p(stop avant cible) 0.0533 [0.03 ; 0.08], R/R 1.443, perte reelle 25.927 % (gap inclus), EV -0.1135 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.93 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 1.5 % x 37.41 % + P(rien) 93.2 % x 0.75 % ne couvrent pas P(stop) 5.3 % x 25.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 29.168 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 1.283, perte reelle 29.168 % (gap inclus), EV -0.1528 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.17 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 1.5 % x 37.41 % + P(rien) 95.2 % x 0.25 % ne couvrent pas P(stop) 3.3 % x 29.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 32.409 %) — p(stop avant cible) 0.0202 [0.01 ; 0.04], R/R 1.154, perte reelle 32.409 % (gap inclus), EV -0.1753 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.41 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 1.5 % x 37.41 % + P(rien) 96.5 % x -0.09 % ne couvrent pas P(stop) 2.0 % x 32.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 35.649 %) — p(stop avant cible) 0.0114 [0.00 ; 0.03], R/R 1.049, perte reelle 35.649 % (gap inclus), EV -0.0645 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.65 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 1.5 % x 37.41 % + P(rien) 97.3 % x -0.23 % ne couvrent pas P(stop) 1.1 % x 35.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 38.89 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 0.962, perte reelle 38.89 % (gap inclus), EV -0.0656 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.89 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 1.5 % x 37.41 % + P(rien) 97.8 % x -0.37 % ne couvrent pas P(stop) 0.7 % x 38.89 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 42.131 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.888, perte reelle 42.131 % (gap inclus), EV -0.0519 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.13 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 1.5 % x 37.41 % + P(rien) 98.1 % x -0.49 % ne couvrent pas P(stop) 0.3 % x 42.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 45.372 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.825, perte reelle 45.372 % (gap inclus), EV -0.0394 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.37 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 1.5 % x 37.41 % + P(rien) 98.5 % x -0.62 % ne couvrent pas P(stop) 0.0 % x 45.37 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 48.613 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.77, perte reelle 48.613 % (gap inclus), EV -0.0394 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.61 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 1.5 % x 37.41 % + P(rien) 98.5 % x -0.62 % ne couvrent pas P(stop) 0.0 % x 48.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 51.854 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.721, perte reelle 51.854 % (gap inclus), EV -0.0394 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.85 % > budget 4.19 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 1.5 % x 37.41 % + P(rien) 98.5 % x -0.62 % ne couvrent pas P(stop) 0.0 % x 51.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : $-0.048 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 12 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.8 | bear 37.8 | side 53.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : stretched_down
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

- **RSI** : 22.1  _(survente)_
- **ADX** : 35.8  _(tendance etablie)_
- **MACD** : hist -0.526  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 53.5%
- **ATR** : 19.82 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.175  _(distribution)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 26.2  _(marche directionnel)_
- **MA** : MA20 354.52 · MA50 427.25 · MA200 500.17  _(prix < MA20)_
- **Dist MA** : MA20 -13.8% · MA50 -28.4% · MA200 -38.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (732190 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
