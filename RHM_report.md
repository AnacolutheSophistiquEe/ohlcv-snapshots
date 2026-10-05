# RHM

**Generated** : 2026-10-05T00:05:29.709475+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €956.90  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €956.90 (+0.3% vs entrée) · entrée €954.03 · stop €877.71 · T1 €968.49 · R/R 0.19  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk -0.053 _(réel 5 s)_ (GBM -0.056) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €951.94–€956.12 (mid €954.03)
- Spot actuel : €956.90 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €877.71 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 €968.49 · R/R 0.19 | T2 €982.96 · R/R 0.38 | T3 €997.42 · R/R 0.57
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €877.71


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (3.59 %)** : le gap seul le franchit 1.177 % des séances (15 fois sur 1274).
   - exécution **0.747 pt plus bas** dans le cas TYPIQUE (médiane), 3.546 au p90, **18.839 au pire**
   - perte réelle **5.794 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 3.59 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.026 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.01** [0.0018 ; 0.034] _(largeur 3.2 pt, n_eff 173.1)_
   - swing : **0.527** [0.4743 ; 0.5792] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.6084** [0.5562 ; 0.6588] _(largeur 10.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-4.63 %** | CVaR **-6.46 %** | vol 2.84 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 1.65 % contre 3.08 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.83 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.871 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5282** (β de hausse 0.5899, asymétrie 0.8953) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.12× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 891.8107 sur atr_grid (2.25 ATR, 6.802 %) — p(stop avant cible) 0.4847 [0.43 ; 0.54], R/R 3.91, perte reelle 7.249 % (gap inclus), CVaR 10.749 %, EV -0.9382 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9453 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **16.92 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 1.02 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 61.0 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ role de queue **non etabli** pour cette ligne (l'intervalle contient zero) : le budget vient de son NOTIONNEL seul, pas d'une mesure de co-mouvement.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.44 ATR (stop 3.036 %) — p(stop avant cible) 0.7479 [0.70 ; 0.79], R/R 8.664, perte reelle 3.272 % (gap inclus), EV -0.3844 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 8.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.748, borne haute 0.791 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 0.4 % x 28.34 % + P(rien) 24.8 % x 7.81 % ne couvrent pas P(stop) 74.8 % x 3.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 0.97 ATR (stop 4.636 %) — p(stop avant cible) 0.6351 [0.58 ; 0.68], R/R 5.744, perte reelle 4.935 % (gap inclus), EV -0.5965 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.635, borne haute 0.684 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.34 ATR du spot — compartiment <1, mesure a 46.3 % de casse (IC clusterise [0.432 ; 0.495] sur 1140 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 0.5 % x 28.34 % + P(rien) 36.0 % x 6.66 % ne couvrent pas P(stop) 63.5 % x 4.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.44 ATR (stop 2.244 %) — p(stop avant cible) 0.83 [0.79 ; 0.87], R/R 12.054, perte reelle 2.351 % (gap inclus), EV -0.1426 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 12.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.830, borne haute 0.867 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.4 % x 28.34 % + P(rien) 16.6 % x 10.22 % ne couvrent pas P(stop) 83.0 % x 2.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.97 ATR (stop 3.844 %) — p(stop avant cible) 0.6842 [0.63 ; 0.73], R/R 6.925, perte reelle 4.093 % (gap inclus), EV -0.4072 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.684, borne haute 0.732 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 0.4 % x 28.34 % + P(rien) 31.1 % x 7.28 % ne couvrent pas P(stop) 68.4 % x 4.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 5.291 %) — p(stop avant cible) 0.5976 [0.55 ; 0.65], R/R 4.983, perte reelle 5.688 % (gap inclus), EV -0.825 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.598, borne haute 0.648 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 0.6 % x 28.34 % + P(rien) 39.6 % x 6.05 % ne couvrent pas P(stop) 59.8 % x 5.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 6.046 %) — p(stop avant cible) 0.5367 [0.48 ; 0.59], R/R 4.368, perte reelle 6.49 % (gap inclus), EV -0.8792 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.537, borne haute 0.589 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 0.8 % x 28.34 % + P(rien) 45.5 % x 5.21 % ne couvrent pas P(stop) 53.7 % x 6.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 6.802 %) — p(stop avant cible) 0.4847 [0.43 ; 0.54], R/R 3.91, perte reelle 7.249 % (gap inclus), EV -0.9382 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 0.8 % x 28.34 % + P(rien) 50.7 % x 4.62 % ne couvrent pas P(stop) 48.5 % x 7.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 7.558 %) — p(stop avant cible) 0.4368 [0.39 ; 0.49], R/R 3.52, perte reelle 8.053 % (gap inclus), EV -1.0117 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 0.8 % x 28.34 % + P(rien) 55.5 % x 4.10 % ne couvrent pas P(stop) 43.7 % x 8.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 8.314 %) — p(stop avant cible) 0.4035 [0.35 ; 0.46], R/R 3.227, perte reelle 8.784 % (gap inclus), EV -1.1821 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 0.8 % x 28.34 % + P(rien) 58.8 % x 3.62 % ne couvrent pas P(stop) 40.4 % x 8.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 9.069 %) — p(stop avant cible) 0.3567 [0.31 ; 0.41], R/R 2.963, perte reelle 9.566 % (gap inclus), EV -1.1971 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 0.8 % x 28.34 % + P(rien) 63.5 % x 3.12 % ne couvrent pas P(stop) 35.7 % x 9.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 10.581 %) — p(stop avant cible) 0.2607 [0.22 ; 0.31], R/R 2.564, perte reelle 11.053 % (gap inclus), EV -1.1467 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 0.8 % x 28.34 % + P(rien) 73.1 % x 2.05 % ne couvrent pas P(stop) 26.1 % x 11.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 12.093 %) — p(stop avant cible) 0.1977 [0.16 ; 0.24], R/R 2.25, perte reelle 12.597 % (gap inclus), EV -1.171 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 0.8 % x 28.34 % + P(rien) 79.4 % x 1.37 % ne couvrent pas P(stop) 19.8 % x 12.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 13.604 %) — p(stop avant cible) 0.1506 [0.12 ; 0.19], R/R 1.987, perte reelle 14.263 % (gap inclus), EV -1.2046 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 0.8 % x 28.34 % + P(rien) 84.1 % x 0.85 % ne couvrent pas P(stop) 15.1 % x 14.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 15.116 %) — p(stop avant cible) 0.126 [0.09 ; 0.16], R/R 1.8, perte reelle 15.743 % (gap inclus), EV -1.2513 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.8 % x 28.34 % + P(rien) 86.6 % x 0.58 % ne couvrent pas P(stop) 12.6 % x 15.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 16.627 %) — p(stop avant cible) 0.094 [0.07 ; 0.13], R/R 1.642, perte reelle 17.258 % (gap inclus), EV -1.2788 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.81 % > budget 16.92 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 0.8 % x 28.34 % + P(rien) 89.8 % x 0.12 % ne couvrent pas P(stop) 9.4 % x 17.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 18.139 %) — p(stop avant cible) 0.0638 [0.04 ; 0.09], R/R 1.507, perte reelle 18.806 % (gap inclus), EV -1.2322 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.99 % > budget 16.92 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.23 %) : P(cible) 0.8 % x 28.34 % + P(rien) 92.8 % x -0.29 % ne couvrent pas P(stop) 6.4 % x 18.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 19.651 %) — p(stop avant cible) 0.0505 [0.03 ; 0.08], R/R 1.396, perte reelle 20.304 % (gap inclus), EV -1.2536 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.31 % > budget 16.92 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.8 % x 28.34 % + P(rien) 94.1 % x -0.49 % ne couvrent pas P(stop) 5.1 % x 20.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 21.162 %) — p(stop avant cible) 0.0361 [0.02 ; 0.06], R/R 1.299, perte reelle 21.823 % (gap inclus), EV -1.231 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.53 % > budget 16.92 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.23 %) : P(cible) 0.8 % x 28.34 % + P(rien) 95.6 % x -0.71 % ne couvrent pas P(stop) 3.6 % x 21.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 22.674 %) — p(stop avant cible) 0.017 [0.01 ; 0.03], R/R 1.202, perte reelle 23.579 % (gap inclus), EV -1.0418 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.85 % > budget 16.92 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 0.8 % x 28.34 % + P(rien) 97.5 % x -0.90 % ne couvrent pas P(stop) 1.7 % x 23.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 24.185 %) — p(stop avant cible) 0.0099 [0.00 ; 0.02], R/R 1.133, perte reelle 25.028 % (gap inclus), EV -1.0223 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.45 % > budget 16.92 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 0.8 % x 28.34 % + P(rien) 98.2 % x -1.03 % ne couvrent pas P(stop) 1.0 % x 25.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 956.9, ATR14 28.9286 (3.023 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.393 ATR = 1.188 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.151 % | 955.4536 | 89.45 % | 92.2 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.302 % | 954.0072 | 83.43 % | 87.96 % | 89.82 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.453 % | 952.5607 | 76.53 % | 83.22 % | 85.87 % | 88.32 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.605 % | 951.1143 | 69.92 % | 78.78 % | 81.82 % | 85.25 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.756 % | 949.6679 | 62.43 % | 73.05 % | 76.88 % | 81.19 % | 88.46 % | 91.36 % |
| 0.35 ATR | 1.058 % | 946.775 | 53.75 % | 66.04 % | 71.44 % | 76.73 % | 85.87 % | 89.25 % |
| 0.5 ATR | 1.512 % | 942.4357 | 40.63 % | 55.08 % | 61.96 % | 69.21 % | 80.3 % | 83.82 % |
| 0.75 ATR | 2.267 % | 935.2036 | 23.47 % | 38.99 % | 47.33 % | 57.62 % | 70.35 % | 77.09 % |
| 1.0 ATR | 3.023 % | 927.9714 | 13.02 % | 26.65 % | 36.46 % | 48.51 % | 62.29 % | 70.55 % |
| 1.25 ATR | 3.779 % | 920.7393 | 7.4 % | 17.97 % | 26.38 % | 39.41 % | 54.13 % | 64.22 % |
| 1.5 ATR | 4.535 % | 913.5072 | 3.94 % | 13.13 % | 20.55 % | 31.88 % | 46.07 % | 57.29 % |
| 2.0 ATR | 6.046 % | 899.0429 | 1.78 % | 7.01 % | 12.15 % | 21.09 % | 34.53 % | 47.64 % |
| 2.5 ATR | 7.558 % | 884.5786 | 0.49 % | 3.36 % | 6.32 % | 12.48 % | 24.98 % | 38.39 % |
| 3.0 ATR | 9.069 % | 870.1143 | 0.1 % | 1.38 % | 3.85 % | 7.72 % | 17.41 % | 32.56 % |
| 4.0 ATR | 12.093 % | 841.1857 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.66 % | 20.6 % |
| 6.0 ATR | 18.139 % | 783.3286 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.83 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.87 ATR | 1.05 ATR | 1.19 ATR | 1.76 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.09 ATR | 1.31 ATR | 1.53 ATR | 2.18 ATR | 2.77 ATR |
| **5 s.** | 0.39 ATR | 0.96 ATR | 1.10 ATR | 1.46 ATR | 1.82 ATR | 2.06 ATR | 2.76 ATR | 3.61 ATR |
| **10 s.** | 0.63 ATR | 1.38 ATR | 1.55 ATR | 2.08 ATR | 2.50 ATR | 2.83 ATR | 3.85 ATR | 4.93 ATR |
| **20 s.** | 0.83 ATR | 1.88 ATR | 2.14 ATR | 2.96 ATR | 3.63 ATR | 4.07 ATR | 5.24 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.45–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.657–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.267 %, prix 935.2071), p(touche) 38.99 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.804–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.023 %, prix 927.9729), p(touche) 36.46 % (en stress 95.1 %)  ✅ optimum identifie (60.8 % des re-echantillons)
- **5 seance(s)** : plage utile 1.096–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.779 %, prix 920.7388), p(touche) 39.41 % (en stress 98.02 %)  ✅ optimum identifie (85.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.546–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.046 %, prix 899.0458), p(touche) 34.53 % (en stress 96.04 %)  ✅ optimum identifie (98.6 % des re-echantillons)
- **20 seance(s)** : plage utile 2.143–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.558 %, prix 884.5775), p(touche) 38.39 % (en stress 98.0 %)  ✅ optimum identifie (98.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.056 | EV/share : €-4.292 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 24 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 6.9 | side 8.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.304% → cible +1.516% / stop −8.0%, p_fill 91%, n_eff≈96.2) : P(cible|rempli) **44%** · **EV/risk -0.053** (×p_fill ; si rempli -0.47% du capital)
  - **swing** (entrée dip −0.567% → cible +3.399% / stop −3.04%, p_fill 91%, n_eff≈105.7) : P(cible|rempli) **42%** · **EV/risk -0.119** (×p_fill ; si rempli -0.40% du capital)
  - **deep** (entrée dip −0.878% → cible +9.871% / stop −4.935%, p_fill 91%, n_eff≈101.3) : P(cible|rempli) **16%** · **EV/risk -0.295** (×p_fill ; si rempli -1.61% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→42% · +3.0%→25% · +5.0%→3% · +8.0%→1%
- Range intraday médian 3.8% (p90 6.51%) · excursion haute méd. +1.53% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.349% vs midi 0.894% vs clôture 1.023% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 7% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. -0.537% ; recovery-V 10%
- **σ réalisé intraday** 2.314% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 64% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 954.8875 (VA 951.8125–962.2675 ; dernier close 959.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 24% · rebond 48% · **stop −2.11%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.4% · baisse 30% (gap-down >1% 7% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.74%) · haut méd +0.44% · range méd 1.28%
- Excursion ouverture 15min (n=160) : bas méd −0.86% (p90 −2.06%) · haut méd +0.6% · range méd 1.7%
- Excursion ouverture 30min (n=160) : bas méd −0.94% (p90 −2.14%) · haut méd +0.75% · range méd 1.9%
- Excursion ouverture 60min (n=160) : bas méd −0.96% (p90 −2.41%) · haut méd +0.82% · range méd 2.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 956.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 74% (109/159) · gap 17% · délai 1.1min · rebond 51% (57/109) (MFE +1.03%)
   - −1.0% : fill 30min 40% · séance 65% (97/159) · gap 7% · délai 9.5min · rebond 60% (57/97) (MFE +1.23%)
   - −1.5% : fill 30min 25% · séance 53% (79/159) · gap 5% · délai 33.3min · rebond 55% (45/79) (MFE +1.15%)
   - −2.0% : fill 30min 16% · séance 43% (66/159) · gap 2% · délai 76.1min · rebond 56% (39/66) (MFE +1.22%)
   - −3.0% : fill 30min 6% · séance 24% (37/159) · gap 2% · délai 141.3min · rebond 48% (19/37) (MFE +0.99%)
   - −4.0% : fill 30min 2% · séance 11% (21/159) · gap 1% · délai 149.9min · rebond 65% (12/21) (MFE +1.74%)
   - −5.0% : fill 30min 0% · séance 5% (11/159) · gap 0% · délai 307.4min · rebond 92% (10/11) (MFE +2.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −1.32%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.62%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.68%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=561 jambes) : jambe baissière méd −1.02% (p90 −2.36%) · ~7.7 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (31 séances) :
      · −1.0% : fill 97% (30/31) · rebond 65% (20/30)
      · −2.0% : fill 70% (25/31) · rebond 46% (15/25)
      · −3.0% : fill 48% (14/31) · rebond 33% (7/14)
      · −4.0% : fill 38% (11/31) · rebond 65% (7/11)
      · −5.0% : fill 15% (6/31) · rebond 100% (6/6)
   - **flat** (27 séances) :
      · −1.0% : fill 86% (21/27) · rebond 66% (15/21)
      · −2.0% : fill 52% (12/27) · rebond 75% (9/12)
      · −3.0% : fill 27% (6/27) · rebond 67% (3/6)
      · −4.0% : fill 4% (2/27) · rebond 62% (1/2)
      · −5.0% : fill 4% (2/27) · rebond 62% (1/2)
   - **gap-up** (101 séances) :
      · −1.0% : fill 45% (46/101) · rebond 50% (22/46)
      · −2.0% : fill 28% (29/101) · rebond 49% (15/29)
      · −3.0% : fill 15% (17/101) · rebond 50% (9/17)
      · −4.0% : fill 5% (8/101) · rebond 66% (4/8)
      · −5.0% : fill 1% (3/101) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 49% si les 15 1res min sont vertes (73 cas) · 28% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 58% si début vert vs 20% si rouge (base 38% · écart 38 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **58%** · continue >prix actuel 45% ; creux résiduel méd -1.43% (q20 -2.65%) → **SL/trailing à −2.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.37% / q75 +2.51% → **scale +1.37% / runner +2.51%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **20%** (continue à baisser 61%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.38%** (au-delà de la MAE q10 -3.38%), cible rebond +1.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.57% .. +2.77%] · haut q95 +3.12% · bas q05 -2.92%
   - 60min (n=160) : retour [-2.47% .. +2.88%] · haut q95 +3.76% · bas q05 -3.36%
   - 2h (n=160) : retour [-3.19% .. +2.58%] · haut q95 +4.0% · bas q05 -3.76%
   - 4h (n=160) : retour [-3.2% .. +2.65%] · haut q95 +4.43% · bas q05 -4.1%
   - 6h (n=160) : retour [-3.5% .. +3.02%] · haut q95 +4.52% · bas q05 -4.31%
   - session (n=160) : retour [-4.02% .. +3.3%] · haut q95 +4.58% · bas q05 -4.8%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.21 · part idiosyncratique 0.79
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 40.0  _(momentum baissier)_
- **ADX** : 30.7  _(tendance etablie)_
- **MACD** : hist -2.177  _(pas de croisement recent)_
- **BB** : %B 0.15 · largeur 11.5%
- **ATR** : 28.93 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.248  _(distribution)_
- **Vol ratio** : 1.18  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 997.18 · MA50 1084.69 · MA200 1334.51  _(prix < MA20)_
- **Dist MA** : MA20 -4.0% · MA50 -11.8% · MA200 -28.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (842027 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
