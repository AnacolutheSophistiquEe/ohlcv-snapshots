# RHM

**Generated** : 2026-10-01T00:04:18.801563+00:00  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €958.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €958.30 (+0.3% vs entrée) · entrée €955.43 · stop €878.99 · T1 €970.81 · R/R 0.2  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -25 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €953.24–€957.61 (mid €955.43)
- Spot actuel : €958.30 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €878.99 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 €970.81 · R/R 0.2 | T2 €986.20 · R/R 0.4 | T3 €1001.59 · R/R 0.6
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €878.99


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (3.86 %)** : le gap seul le franchit 1.02 % des séances (13 fois sur 1274).
   - exécution **0.673 pt plus bas** dans le cas TYPIQUE (médiane), 3.634 au p90, **18.569 au pire**
   - perte réelle **6.122 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 3.86 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0231 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 13 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.574 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0102** [0.0019 ; 0.0343] _(largeur 3.2 pt, n_eff 173.1)_
   - swing : **0.5018** [0.4493 ; 0.5543] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.6044** [0.5522 ; 0.6549] _(largeur 10.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.86 %** | CVaR **-6.85 %** | vol 3.07 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.83 % contre 3.09 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.83 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.871 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5279** (β de hausse 0.5898, asymétrie 0.895) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.116× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 934.69 sur grid_snapped (0.47 ATR, 2.464 %) — p(stop avant cible) 0.811 [0.77 ; 0.85], R/R 10.917, perte reelle 2.574 % (gap inclus), CVaR 4.232 %, EV -0.1759 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.88 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 10.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.811, borne haute 0.850 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 4.23 % > budget 3.10 %
- Budget de queue : **3.1 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.171 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 44.7 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ role de queue **non etabli** pour cette ligne (l'intervalle contient zero) : le budget vient de son NOTIONNEL seul, pas d'une mesure de co-mouvement.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.47 ATR (stop 3.533 %) — p(stop avant cible) 0.7037 [0.65 ; 0.75], R/R 7.44, perte reelle 3.777 % (gap inclus), EV -0.3416 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 7.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.704, borne haute 0.750 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.81 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 0.4 % x 28.10 % + P(rien) 29.2 % x 7.50 % ne couvrent pas P(stop) 70.4 % x 3.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 0.96 ATR (stop 5.111 %) — p(stop avant cible) 0.6078 [0.56 ; 0.66], R/R 5.134, perte reelle 5.472 % (gap inclus), EV -0.7336 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.608, borne haute 0.658 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 8.98 % > budget 3.10 %
      - ⚠ support DETECTE a 0.37 ATR du spot — compartiment <1, mesure a 45.4 % de casse (IC clusterise [0.423 ; 0.484] sur 1130 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 0.5 % x 28.10 % + P(rien) 38.7 % x 6.33 % ne couvrent pas P(stop) 60.8 % x 5.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.47 ATR (stop 2.464 %) — p(stop avant cible) 0.811 [0.77 ; 0.85], R/R 10.917, perte reelle 2.574 % (gap inclus), EV -0.1759 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 10.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.811, borne haute 0.850 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 4.23 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 0.4 % x 28.10 % + P(rien) 18.4 % x 9.67 % ne couvrent pas P(stop) 81.1 % x 2.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.96 ATR (stop 4.042 %) — p(stop avant cible) 0.6634 [0.61 ; 0.71], R/R 6.543, perte reelle 4.294 % (gap inclus), EV -0.3901 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.663, borne haute 0.712 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 7.10 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 0.4 % x 28.10 % + P(rien) 33.2 % x 7.02 % ne couvrent pas P(stop) 66.3 % x 4.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 5.62 %) — p(stop avant cible) 0.5766 [0.52 ; 0.63], R/R 4.675, perte reelle 6.011 % (gap inclus), EV -0.8524 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.577, borne haute 0.628 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 9.61 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 0.7 % x 28.10 % + P(rien) 41.7 % x 5.81 % ne couvrent pas P(stop) 57.7 % x 6.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 6.423 %) — p(stop avant cible) 0.4955 [0.44 ; 0.55], R/R 4.099, perte reelle 6.855 % (gap inclus), EV -0.8213 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 10.45 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 0.8 % x 28.10 % + P(rien) 49.6 % x 4.72 % ne couvrent pas P(stop) 49.5 % x 6.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 7.226 %) — p(stop avant cible) 0.4396 [0.39 ; 0.49], R/R 3.649, perte reelle 7.699 % (gap inclus), EV -0.859 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 11.11 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 0.8 % x 28.10 % + P(rien) 55.2 % x 4.15 % ne couvrent pas P(stop) 44.0 % x 7.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 8.029 %) — p(stop avant cible) 0.4207 [0.37 ; 0.47], R/R 3.3, perte reelle 8.514 % (gap inclus), EV -1.0684 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 11.77 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 0.8 % x 28.10 % + P(rien) 57.1 % x 3.99 % ne couvrent pas P(stop) 42.1 % x 8.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 8.831 %) — p(stop avant cible) 0.3766 [0.33 ; 0.43], R/R 3.017, perte reelle 9.312 % (gap inclus), EV -1.1245 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.28 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 0.9 % x 28.10 % + P(rien) 61.5 % x 3.47 % ne couvrent pas P(stop) 37.7 % x 9.31 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 9.634 %) — p(stop avant cible) 0.3188 [0.27 ; 0.37], R/R 2.785, perte reelle 10.089 % (gap inclus), EV -1.0918 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.50 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 0.9 % x 28.10 % + P(rien) 67.2 % x 2.79 % ne couvrent pas P(stop) 31.9 % x 10.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 11.24 %) — p(stop avant cible) 0.245 [0.20 ; 0.29], R/R 2.403, perte reelle 11.692 % (gap inclus), EV -1.1256 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.45 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 0.9 % x 28.10 % + P(rien) 74.6 % x 2.00 % ne couvrent pas P(stop) 24.5 % x 11.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 12.846 %) — p(stop avant cible) 0.1777 [0.14 ; 0.22], R/R 2.094, perte reelle 13.419 % (gap inclus), EV -1.1771 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.88 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 0.9 % x 28.10 % + P(rien) 81.3 % x 1.18 % ne couvrent pas P(stop) 17.8 % x 13.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 14.451 %) — p(stop avant cible) 0.1331 [0.10 ; 0.17], R/R 1.866, perte reelle 15.06 % (gap inclus), EV -1.143 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.07 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 0.9 % x 28.10 % + P(rien) 85.8 % x 0.71 % ne couvrent pas P(stop) 13.3 % x 15.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 16.057 %) — p(stop avant cible) 0.0994 [0.07 ; 0.13], R/R 1.681, perte reelle 16.714 % (gap inclus), EV -1.173 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.36 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 0.9 % x 28.10 % + P(rien) 89.2 % x 0.27 % ne couvrent pas P(stop) 9.9 % x 16.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 17.663 %) — p(stop avant cible) 0.0778 [0.05 ; 0.11], R/R 1.538, perte reelle 18.268 % (gap inclus), EV -1.1969 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.61 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 0.9 % x 28.10 % + P(rien) 91.3 % x -0.03 % ne couvrent pas P(stop) 7.8 % x 18.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 19.268 %) — p(stop avant cible) 0.0528 [0.03 ; 0.08], R/R 1.409, perte reelle 19.944 % (gap inclus), EV -1.1694 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.98 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 0.9 % x 28.10 % + P(rien) 93.8 % x -0.39 % ne couvrent pas P(stop) 5.3 % x 19.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 20.874 %) — p(stop avant cible) 0.0405 [0.02 ; 0.07], R/R 1.306, perte reelle 21.514 % (gap inclus), EV -1.1942 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.81 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 0.9 % x 28.10 % + P(rien) 95.1 % x -0.60 % ne couvrent pas P(stop) 4.0 % x 21.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 22.48 %) — p(stop avant cible) 0.0212 [0.01 ; 0.04], R/R 1.208, perte reelle 23.256 % (gap inclus), EV -1.0231 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.53 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 0.9 % x 28.10 % + P(rien) 97.0 % x -0.80 % ne couvrent pas P(stop) 2.1 % x 23.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 24.086 %) — p(stop avant cible) 0.01 [0.00 ; 0.03], R/R 1.125, perte reelle 24.976 % (gap inclus), EV -0.9507 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.49 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 0.9 % x 28.10 % + P(rien) 98.1 % x -0.97 % ne couvrent pas P(stop) 1.0 % x 24.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 25.691 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 1.079, perte reelle 26.046 % (gap inclus), EV -0.9505 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.50 % > budget 3.10 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 0.9 % x 28.10 % + P(rien) 98.5 % x -1.06 % ne couvrent pas P(stop) 0.6 % x 26.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 958.3, ATR14 30.775 (3.211 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.394 ATR = 1.265 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.161 % | 956.7612 | 89.45 % | 92.2 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.321 % | 955.2225 | 83.43 % | 87.96 % | 89.82 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.482 % | 953.6837 | 76.53 % | 83.22 % | 85.87 % | 88.32 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.642 % | 952.145 | 70.02 % | 78.78 % | 81.82 % | 85.25 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.803 % | 950.6062 | 62.52 % | 73.05 % | 76.88 % | 81.19 % | 88.46 % | 91.36 % |
| 0.35 ATR | 1.124 % | 947.5287 | 53.94 % | 66.04 % | 71.44 % | 76.73 % | 85.87 % | 89.25 % |
| 0.5 ATR | 1.606 % | 942.9125 | 40.63 % | 54.99 % | 61.86 % | 69.21 % | 80.3 % | 83.82 % |
| 0.75 ATR | 2.409 % | 935.2187 | 23.47 % | 38.99 % | 47.33 % | 57.62 % | 70.35 % | 77.09 % |
| 1.0 ATR | 3.211 % | 927.525 | 13.02 % | 26.65 % | 36.36 % | 48.51 % | 62.29 % | 70.55 % |
| 1.25 ATR | 4.014 % | 919.8312 | 7.4 % | 17.97 % | 26.38 % | 39.21 % | 54.13 % | 64.22 % |
| 1.5 ATR | 4.817 % | 912.1375 | 3.94 % | 13.13 % | 20.55 % | 31.78 % | 45.87 % | 57.09 % |
| 2.0 ATR | 6.423 % | 896.75 | 1.78 % | 7.01 % | 12.15 % | 20.99 % | 34.33 % | 47.44 % |
| 2.5 ATR | 8.029 % | 881.3625 | 0.49 % | 3.36 % | 6.32 % | 12.48 % | 24.98 % | 38.19 % |
| 3.0 ATR | 9.634 % | 865.975 | 0.1 % | 1.38 % | 3.85 % | 7.72 % | 17.41 % | 32.36 % |
| 4.0 ATR | 12.846 % | 835.2 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.66 % | 20.5 % |
| 6.0 ATR | 19.268 % | 773.65 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.83 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.87 ATR | 1.05 ATR | 1.19 ATR | 1.76 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.31 ATR | 1.53 ATR | 2.18 ATR | 2.77 ATR |
| **5 s.** | 0.39 ATR | 0.96 ATR | 1.09 ATR | 1.46 ATR | 1.81 ATR | 2.06 ATR | 2.76 ATR | 3.61 ATR |
| **10 s.** | 0.63 ATR | 1.38 ATR | 1.54 ATR | 2.07 ATR | 2.50 ATR | 2.83 ATR | 3.85 ATR | 4.93 ATR |
| **20 s.** | 0.83 ATR | 1.87 ATR | 2.13 ATR | 2.94 ATR | 3.62 ATR | 4.06 ATR | 5.24 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.451–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.656–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.409 %, prix 935.2145), p(touche) 38.99 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.211 %, prix 927.529), p(touche) 36.36 % (en stress 95.1 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.094–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.014 %, prix 919.8338), p(touche) 39.21 % (en stress 98.02 %)  ✅ optimum identifie (86.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.538–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.423 %, prix 896.7484), p(touche) 34.33 % (en stress 96.04 %)  ✅ optimum identifie (98.6 % des re-echantillons)
- **20 seance(s)** : plage utile 2.132–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.029 %, prix 881.3581), p(touche) 38.19 % (en stress 98.0 %)  ✅ optimum identifie (98.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.065 | EV/share : €-4.957 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 22 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 80.7 | bear 5.0 | side 14.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.304% → cible +1.611% / stop −8.0%, p_fill 90%, n_eff≈96.2) : P(cible|rempli) **39%** · **EV/risk -0.065** (×p_fill ; si rempli -0.58% du capital)
  - **swing** (entrée dip −0.649% → cible +3.614% / stop −3.232%, p_fill 91%, n_eff≈105.7) : P(cible|rempli) **43%** · **EV/risk -0.093** (×p_fill ; si rempli -0.33% du capital)
  - **deep** (entrée dip −1.006% → cible +9.827% / stop −4.913%, p_fill 86%, n_eff≈96.3) : P(cible|rempli) **15%** · **EV/risk -0.311** (×p_fill ; si rempli -1.77% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→60% · +2.0%→41% · +3.0%→25% · +5.0%→3% · +8.0%→1%
- Range intraday médian 3.82% (p90 6.51%) · excursion haute méd. +1.43% / basse méd. −1.76%
- Profil de vol intra : ouverture 2.333% vs midi 0.891% vs clôture 1.028% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr -0.029)_ ; drift intra méd. -0.64% ; recovery-V 11%
- **σ réalisé intraday** 2.281% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 73% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 954.9975 (VA 949.0275–966.9375 ; dernier close 963.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 26% · rebond 48% · **stop −2.11%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.42% · baisse 27% (gap-down >1% 7% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.75%) · haut méd +0.43% · range méd 1.28%
- Excursion ouverture 15min (n=160) : bas méd −0.88% (p90 −2.03%) · haut méd +0.57% · range méd 1.69%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.15%) · haut méd +0.67% · range méd 1.89%
- Excursion ouverture 60min (n=160) : bas méd −0.94% (p90 −2.42%) · haut méd +0.74% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 960.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 74% (108/159) · gap 16% · délai 1.5min · rebond 48% (55/108) (MFE +0.96%)
   - −1.0% : fill 30min 38% · séance 65% (96/159) · gap 7% · délai 8.5min · rebond 58% (56/96) (MFE +1.2%)
   - −1.5% : fill 30min 23% · séance 53% (78/159) · gap 5% · délai 52.8min · rebond 52% (44/78) (MFE +1.02%)
   - −2.0% : fill 30min 15% · séance 43% (66/159) · gap 2% · délai 93.4min · rebond 54% (39/66) (MFE +1.2%)
   - −3.0% : fill 30min 6% · séance 26% (37/159) · gap 2% · délai 141.3min · rebond 48% (19/37) (MFE +0.99%)
   - −4.0% : fill 30min 2% · séance 12% (21/159) · gap 2% · délai 149.9min · rebond 65% (12/21) (MFE +1.74%)
   - −5.0% : fill 30min 1% · séance 5% (11/159) · gap 1% · délai 307.4min · rebond 92% (10/11) (MFE +2.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −1.35%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.63%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.68%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=550 jambes) : jambe baissière méd −1.03% (p90 −2.42%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 97% (29/30) · rebond 62% (19/29)
      · −2.0% : fill 77% (25/30) · rebond 46% (15/25)
      · −3.0% : fill 53% (14/30) · rebond 33% (7/14)
      · −4.0% : fill 41% (11/30) · rebond 65% (7/11)
      · −5.0% : fill 17% (6/30) · rebond 100% (6/6)
   - **flat** (26 séances) :
      · −1.0% : fill 85% (20/26) · rebond 63% (14/20)
      · −2.0% : fill 48% (11/26) · rebond 71% (8/11)
      · −3.0% : fill 29% (6/26) · rebond 67% (3/6)
      · −4.0% : fill 4% (2/26) · rebond 62% (1/2)
      · −5.0% : fill 4% (2/26) · rebond 62% (1/2)
   - **gap-up** (103 séances) :
      · −1.0% : fill 46% (47/103) · rebond 50% (23/47)
      · −2.0% : fill 29% (30/103) · rebond 49% (16/30)
      · −3.0% : fill 15% (17/103) · rebond 50% (9/17)
      · −4.0% : fill 5% (8/103) · rebond 66% (4/8)
      · −5.0% : fill 1% (3/103) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 51% si les 15 1res min sont vertes (71 cas) · 28% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 64% si début vert vs 20% si rouge (base 38% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 300min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **64%** · continue >prix actuel 45% ; creux résiduel méd -1.2% (q20 -2.69%) → **SL/trailing à −2.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.33% / q75 +1.88% → **scale +1.33% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **20%** (continue à baisser 60%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.43%** (au-delà de la MAE q10 -3.43%), cible rebond +1.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.6% .. +2.77%] · haut q95 +3.17% · bas q05 -2.98%
   - 60min (n=160) : retour [-2.48% .. +3.04%] · haut q95 +3.93% · bas q05 -3.38%
   - 2h (n=160) : retour [-3.2% .. +2.7%] · haut q95 +4.09% · bas q05 -3.83%
   - 4h (n=160) : retour [-3.21% .. +2.69%] · haut q95 +4.49% · bas q05 -4.14%
   - 6h (n=160) : retour [-3.59% .. +3.05%] · haut q95 +4.53% · bas q05 -4.32%
   - session (n=160) : retour [-4.07% .. +3.3%] · haut q95 +4.73% · bas q05 -4.89%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.24 · part idiosyncratique 0.76
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.0  _(momentum baissier)_
- **ADX** : 28.6  _(tendance etablie)_
- **MACD** : hist -2.597  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 11.4%
- **ATR** : 30.77 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.254  _(distribution)_
- **Vol ratio** : 0.49  _(volume atone)_
- **Choppiness** : 55.5  _(transition)_
- **MA** : MA20 1007.35 · MA50 1087.76 · MA200 1340.23  _(prix < MA20)_
- **Dist MA** : MA20 -4.9% · MA50 -11.9% · MA200 -28.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (851337 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
