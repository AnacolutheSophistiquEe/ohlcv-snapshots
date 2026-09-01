# SMR

**Generated** : 2026-09-01T00:32:08.618791+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $9.27  

> 🟡 **WAIT-FOR-DIP** — spot +1.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $9.27 (+1.1% vs entrée) · entrée $9.17 · stop $8.92 · T1 $9.66 · R/R 1.96  
> ↳ P(T1 av. stop) 24 % _(réel 5 s)_ · EV/risk 0.057 _(réel 5 s)_ (GBM 0.087) · ¼-Kelly 0.026 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.71% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.12–$9.22 (mid $9.17)
- Spot actuel : $9.27 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : $8.92 (stop swing_plan-based (-9.61%))
- Targets : T1 $9.66 · R/R 1.96 | T2 $9.79 · R/R 2.48 | T3 $9.91 · R/R 2.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.92


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.29 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.61 %)** : le gap seul le franchit 0.62 % des séances (7 fois sur 1129).
   - exécution **3.954 pt plus bas** dans le cas TYPIQUE (médiane), 12.859 au p90, **20.713 au pire**
   - perte réelle **15.541 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 9.61 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0368 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.428 % | p01 -6.962 % | pire -30.323 % _(sur 1129 séances)_
- **P(stop avant cible)** _(source : daily, 1130 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5698** [0.4954 ; 0.6419] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.5404** [0.4877 ; 0.5925] _(largeur 10.5 pt, n_eff 345.2)_
   - deep : **0.5513** [0.4986 ; 0.6032] _(largeur 10.5 pt, n_eff 345.2)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.2 pt), swing (33.8 pt), deep (35.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.4 %** | CVaR **-11.92 %** | vol 6.93 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 11.00 % contre 5.92 % aujourd'hui, rapport 1.86)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.96 % vs -18.67 % si l'on extrapolait par √5 _(rapport 1.016 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6029** (β de hausse 1.3622, asymétrie 1.1767) vs IWM — 536 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.982× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 8.1025 sur atr_grid (1.75 ATR, 12.594 %) — p(stop avant cible) 0.4865 [0.43 ; 0.54], R/R 0.855, perte reelle 18.976 % (gap inclus), CVaR 12.617 %, EV -4.1048 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0514 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.62 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.71 ATR (stop 7.995 %) — p(stop avant cible) 0.6727 [0.62 ; 0.72], R/R 1.201, perte reelle 13.499 % (gap inclus), EV -4.714 % — **REFUSE**
      - refuse : p_stop_first 0.673, borne haute 0.721 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.71 %) : P(cible) 26.2 % x 16.21 % + P(rien) 6.5 % x 1.72 % ne couvrent pas P(stop) 67.3 % x 13.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 1.11 ATR (stop 10.862 %) — p(stop avant cible) 0.5479 [0.50 ; 0.60], R/R 0.918, perte reelle 17.667 % (gap inclus), EV -4.7445 % — **REFUSE**
      - refuse : p_stop_first 0.548, borne haute 0.600 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.61 ATR du spot — compartiment <1, mesure a 46.4 % de casse (IC clusterise [0.430 ; 0.496] sur 1146 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.74 %) : P(cible) 31.0 % x 16.21 % + P(rien) 14.2 % x -0.60 % ne couvrent pas P(stop) 54.8 % x 17.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.09 ATR (stop 25.101 %) — p(stop avant cible) 0.1199 [0.09 ; 0.16], R/R 0.535, perte reelle 30.323 % (gap inclus), EV -1.0767 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 35.1 % x 16.21 % + P(rien) 52.9 % x -5.93 % ne couvrent pas P(stop) 12.0 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.799 %) — p(stop avant cible) 0.9112 [0.88 ; 0.94], R/R 4.334, perte reelle 3.741 % (gap inclus), EV -2.0775 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.911, borne haute 0.938 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 8.2 % x 16.21 % + P(rien) 0.7 % x 1.13 % ne couvrent pas P(stop) 91.1 % x 3.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 12.594 %) — p(stop avant cible) 0.4865 [0.43 ; 0.54], R/R 0.855, perte reelle 18.976 % (gap inclus), EV -4.1048 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.10 %) : P(cible) 32.9 % x 16.21 % + P(rien) 18.5 % x -1.09 % ne couvrent pas P(stop) 48.6 % x 18.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 14.394 %) — p(stop avant cible) 0.4226 [0.37 ; 0.48], R/R 0.78, perte reelle 20.78 % (gap inclus), EV -3.4988 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.50 %) : P(cible) 33.8 % x 16.21 % + P(rien) 23.9 % x -0.82 % ne couvrent pas P(stop) 42.3 % x 20.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 16.193 %) — p(stop avant cible) 0.3519 [0.30 ; 0.40], R/R 0.682, perte reelle 23.778 % (gap inclus), EV -3.4601 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.46 %) : P(cible) 34.6 % x 16.21 % + P(rien) 30.2 % x -2.30 % ne couvrent pas P(stop) 35.2 % x 23.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 17.992 %) — p(stop avant cible) 0.2965 [0.25 ; 0.35], R/R 0.535, perte reelle 30.323 % (gap inclus), EV -4.3823 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.38 %) : P(cible) 34.9 % x 16.21 % + P(rien) 35.5 % x -2.95 % ne couvrent pas P(stop) 29.6 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 19.791 %) — p(stop avant cible) 0.2299 [0.19 ; 0.28], R/R 0.535, perte reelle 30.323 % (gap inclus), EV -3.0102 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.01 %) : P(cible) 35.0 % x 16.21 % + P(rien) 42.0 % x -4.09 % ne couvrent pas P(stop) 23.0 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 28.787 %) — p(stop avant cible) 0.0705 [0.05 ; 0.10], R/R 0.535, perte reelle 30.323 % (gap inclus), EV -0.4703 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 35.1 % x 16.21 % + P(rien) 57.8 % x -6.97 % ne couvrent pas P(stop) 7.0 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 32.386 %) — p(stop avant cible) 0.0409 [0.02 ; 0.07], R/R 0.501, perte reelle 32.386 % (gap inclus), EV -0.3509 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 35.1 % x 16.21 % + P(rien) 60.8 % x -7.78 % ne couvrent pas P(stop) 4.1 % x 32.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 35.984 %) — p(stop avant cible) 0.0297 [0.02 ; 0.05], R/R 0.451, perte reelle 35.984 % (gap inclus), EV -0.3732 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 35.1 % x 16.21 % + P(rien) 61.9 % x -8.09 % ne couvrent pas P(stop) 3.0 % x 35.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 39.582 %) — p(stop avant cible) 0.0188 [0.01 ; 0.04], R/R 0.41, perte reelle 39.582 % (gap inclus), EV -0.422 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 35.1 % x 16.21 % + P(rien) 63.0 % x -8.54 % ne couvrent pas P(stop) 1.9 % x 39.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 43.181 %) — p(stop avant cible) 0.0128 [0.00 ; 0.03], R/R 0.376, perte reelle 43.181 % (gap inclus), EV -0.397 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 35.1 % x 16.21 % + P(rien) 63.6 % x -8.72 % ne couvrent pas P(stop) 1.3 % x 43.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 46.779 %) — p(stop avant cible) 0.0081 [0.00 ; 0.02], R/R 0.347, perte reelle 46.779 % (gap inclus), EV -0.4189 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 35.1 % x 16.21 % + P(rien) 64.0 % x -8.96 % ne couvrent pas P(stop) 0.8 % x 46.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 50.378 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.322, perte reelle 50.378 % (gap inclus), EV -0.4115 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 35.1 % x 16.21 % + P(rien) 64.6 % x -9.30 % ne couvrent pas P(stop) 0.2 % x 50.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 53.976 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.3, perte reelle 53.976 % (gap inclus), EV -0.4115 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 35.1 % x 16.21 % + P(rien) 64.8 % x -9.41 % ne couvrent pas P(stop) 0.0 % x 53.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 57.574 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.282, perte reelle 57.574 % (gap inclus), EV -0.407 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 35.1 % x 16.21 % + P(rien) 64.8 % x -9.42 % ne couvrent pas P(stop) 0.0 % x 57.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 9.27, ATR14 0.6671 (7.197 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.429 ATR = 3.087 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.36 % | 9.2366 | 92.64 % | 95.16 % | 96.42 % | 97.11 % | 97.91 % | 98.35 % |
| 0.1 ATR | 0.72 % | 9.2033 | 87.0 % | 91.36 % | 93.31 % | 94.68 % | 96.16 % | 97.41 % |
| 0.15 ATR | 1.08 % | 9.1699 | 81.01 % | 87.1 % | 89.73 % | 91.68 % | 93.84 % | 96.0 % |
| 0.2 ATR | 1.439 % | 9.1366 | 75.49 % | 82.83 % | 86.51 % | 89.25 % | 92.21 % | 94.94 % |
| 0.25 ATR | 1.799 % | 9.1032 | 70.2 % | 79.72 % | 83.85 % | 87.05 % | 90.58 % | 93.76 % |
| 0.35 ATR | 2.519 % | 9.0365 | 58.46 % | 72.12 % | 77.39 % | 82.89 % | 87.56 % | 91.29 % |
| 0.5 ATR | 3.598 % | 8.9364 | 42.46 % | 59.1 % | 67.24 % | 74.34 % | 83.02 % | 88.24 % |
| 0.75 ATR | 5.398 % | 8.7696 | 20.71 % | 37.44 % | 47.87 % | 59.65 % | 72.44 % | 80.59 % |
| 1.0 ATR | 7.197 % | 8.6029 | 11.39 % | 25.92 % | 35.99 % | 49.25 % | 64.53 % | 74.94 % |
| 1.25 ATR | 8.996 % | 8.4361 | 4.72 % | 16.01 % | 25.26 % | 38.61 % | 55.0 % | 68.59 % |
| 1.5 ATR | 10.795 % | 8.2693 | 2.3 % | 9.79 % | 16.26 % | 28.32 % | 45.47 % | 61.88 % |
| 2.0 ATR | 14.394 % | 7.9357 | 0.35 % | 3.23 % | 6.46 % | 14.57 % | 31.4 % | 49.65 % |
| 2.5 ATR | 17.992 % | 7.6021 | 0.12 % | 1.27 % | 2.77 % | 6.82 % | 20.58 % | 38.82 % |
| 3.0 ATR | 21.59 % | 7.2686 | 0.12 % | 0.58 % | 1.73 % | 3.7 % | 11.86 % | 28.82 % |
| 4.0 ATR | 28.787 % | 6.6014 | 0.0 % | 0.23 % | 0.35 % | 1.04 % | 4.53 % | 13.88 % |
| 6.0 ATR | 43.181 % | 5.2671 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.35 % | 1.65 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.48 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.85 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.86 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.20 ATR |
| **5 s.** | 0.49 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.80 ATR | 2.29 ATR | 2.79 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.52 ATR | 1.94 ATR | 2.30 ATR | 2.53 ATR | 3.25 ATR | 3.94 ATR |
| **20 s.** | 1.00 ATR | 1.99 ATR | 2.21 ATR | 2.79 ATR | 3.26 ATR | 3.59 ATR | 4.63 ATR | 5.45 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.476–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.598 %, prix 8.9365), p(touche) 42.46 % (en stress 81.61 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.663–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.398 %, prix 8.7696), p(touche) 37.44 % (en stress 88.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.8 % des re-echantillons)
- **3 seance(s)** : plage utile 0.81–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.197 %, prix 8.6028), p(touche) 35.99 % (en stress 89.66 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.1–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.996 %, prix 8.4361), p(touche) 38.61 % (en stress 95.4 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.517–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.394 %, prix 7.9357), p(touche) 31.4 % (en stress 96.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.215–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.992 %, prix 7.6021), p(touche) 38.82 % (en stress 98.82 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.087 | EV/share : $0.022 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.105 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.9 | bear 7.1 | side 9.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.1% → cible +5.42% / stop −2.709%, p_fill 86%, n_eff≈34.6) : P(cible|rempli) **24%** · **EV/risk +0.057** (×p_fill ; si rempli +0.18% du capital)
  - **swing** (entrée dip −2.412% → cible +12.04% / stop −7.376%, p_fill 76%, n_eff≈30.6) : P(cible|rempli) **33%** · **EV/risk +0.107** (×p_fill ; si rempli +1.03% du capital)
  - **deep** (entrée dip −3.735% → cible +22.969% / stop −11.484%, p_fill 70%, n_eff≈28.4) : P(cible|rempli) **12%** · **EV/risk +0.023** (×p_fill ; si rempli +0.38% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→80% · +2.0%→69% · +3.0%→62% · +5.0%→39% · +8.0%→11%
- Range intraday médian 7.24% (p90 12.17%) · excursion haute méd. +3.65% / basse méd. −3.24%
- Profil de vol intra : ouverture 4.755% vs midi 1.485% vs clôture 1.763% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 80% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.068)_ ; drift intra méd. 0.068% ; recovery-V 38%
- **σ réalisé intraday** 4.599% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 65% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 9.3034 (VA 9.1853–9.4722 ; dernier close 9.275)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 42% · rebond 75% · **stop −4.26%** sous le fill (sous le bruit) · cible +2.38% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.43% · baisse 56% (gap-down >1% 36% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −1.13% (p90 −3.04%) · haut méd +1.14% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −3.84%) · haut méd +1.75% · range méd 3.7%
- Excursion ouverture 30min (n=160) : bas méd −1.67% (p90 −4.67%) · haut méd +2.22% · range méd 4.36%
- Excursion ouverture 60min (n=160) : bas méd −2.16% (p90 −5.51%) · haut méd +2.54% · range méd 5.16%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.29 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 79% (130/159) · gap 49% · délai 0.0min · rebond 65% (82/130) (MFE +1.62%)
   - −1.0% : fill 30min 63% · séance 76% (124/159) · gap 37% · délai 0.0min · rebond 65% (78/124) (MFE +2.08%)
   - −1.5% : fill 30min 59% · séance 72% (117/159) · gap 28% · délai 0.0min · rebond 69% (83/117) (MFE +2.04%)
   - −2.0% : fill 30min 53% · séance 65% (109/159) · gap 24% · délai 0.7min · rebond 66% (75/109) (MFE +1.98%)
   - −3.0% : fill 30min 41% · séance 54% (95/159) · gap 9% · délai 4.6min · rebond 75% (76/95) (MFE +2.04%)
   - −4.0% : fill 30min 33% · séance 49% (85/159) · gap 4% · délai 9.7min · rebond 75% (65/85) (MFE +2.37%)
   - −5.0% : fill 30min 24% · séance 42% (67/159) · gap 2% · délai 23.9min · rebond 75% (50/67) (MFE +2.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −2.68%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.81% (p90 −2.71%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −2.87%) → stop au-delà de −2.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1157 jambes) : jambe baissière méd −1.34% (p90 −3.15%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (87 séances) :
      · −1.0% : fill 99% (86/87) · rebond 63% (54/86)
      · −2.0% : fill 92% (81/87) · rebond 72% (60/81)
      · −3.0% : fill 82% (75/87) · rebond 81% (63/75)
      · −4.0% : fill 76% (68/87) · rebond 81% (55/68)
      · −5.0% : fill 63% (52/87) · rebond 82% (42/52)
   - **flat** (10 séances) :
      · −1.0% : fill 92% (8/10) · rebond 48% (4/8)
      · −2.0% : fill 80% (6/10) · rebond 40% (2/6)
      · −3.0% : fill 80% (6/10) · rebond 50% (3/6)
      · −4.0% : fill 80% (6/10) · rebond 62% (4/6)
      · −5.0% : fill 60% (4/10) · rebond 79% (3/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 46% (30/62) · rebond 74% (20/30)
      · −2.0% : fill 29% (22/62) · rebond 52% (13/22)
      · −3.0% : fill 15% (14/62) · rebond 51% (10/14)
      · −4.0% : fill 12% (11/62) · rebond 35% (6/11)
      · −5.0% : fill 12% (11/62) · rebond 27% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 61% si les 15 1res min sont vertes (73 cas) · 34% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 82% si début vert vs 17% si rouge (base 47% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **82%** · continue >prix actuel 63% ; creux résiduel méd -1.67% (q20 -3.89%) → **SL/trailing à −3.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.26% / q75 +4.15% → **scale +3.26% / runner +4.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.42%** (au-delà de la MAE q10 -5.42%), cible rebond +1.61% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.18% .. +4.71%] · haut q95 +6.18% · bas q05 -5.77%
   - 60min (n=160) : retour [-5.2% .. +4.86%] · haut q95 +6.77% · bas q05 -6.34%
   - 2h (n=160) : retour [-6.23% .. +5.47%] · haut q95 +7.99% · bas q05 -7.99%
   - 4h (n=160) : retour [-7.2% .. +7.11%] · haut q95 +9.05% · bas q05 -8.31%
   - 6h (n=160) : retour [-7.06% .. +8.2%] · haut q95 +10.55% · bas q05 -9.09%
   - session (n=160) : retour [-7.04% .. +9.08%] · haut q95 +10.82% · bas q05 -9.12%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.88%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 44.4  _(momentum baissier)_
- **ADX** : 14.5  _(pas de tendance nette)_
- **MACD** : hist 0.014  _(pas de croisement recent)_
- **BB** : %B 0.39 · largeur 13.5%
- **ATR** : 0.67 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.024  _(neutre)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 64.0  _(marche en range (choppy))_
- **MA** : MA20 9.4 · MA50 9.19 · MA200 13.29  _(prix < MA20)_
- **Dist MA** : MA20 -1.4% · MA50 +0.9% · MA200 -30.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (777590 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
