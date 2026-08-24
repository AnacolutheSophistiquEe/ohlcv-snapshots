# MSTR

**Generated** : 2026-08-24T00:23:07.954649+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $119.25  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot $119.25 (+0.5% vs entrée) · entrée $118.71 · stop $113.96 · T1 $121.79 · R/R 0.65  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk 0.04 _(réel 5 s)_ (GBM -0.051) · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23215 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 71.7 > 70 (surachat) ; %B 1.28 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $118.17–$119.25 (mid $118.71)
- Spot actuel : $119.25 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $113.96 (stop swing_plan-based (-8.63%))
- Targets : T1 $121.79 · R/R 0.65 | T2 $124.86 · R/R 1.29 | T3 $127.94 · R/R 1.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $113.96


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.21 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.63 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1254).
   - exécution **2.769 pt plus bas** dans le cas TYPIQUE (médiane), 18.107 au p90, **18.742 au pire**
   - perte réelle **14.455 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 8.63 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0418 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.428 % | p01 -7.774 % | pire -27.372 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1563** [0.1081 ; 0.2159] _(largeur 10.8 pt, n_eff 173.1)_
   - swing : **0.5484** [0.4957 ; 0.6003] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5736** [0.521 ; 0.6249] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.0 pt), swing (30.8 pt), deep (30.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.92 %** | CVaR **-10.5 %** | vol 5.46 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.37 % contre 4.79 % aujourd'hui, rapport 1.75)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.76 % si l'on extrapolait par √5 _(rapport 0.957 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3312** (β de hausse 1.8634, asymétrie 1.2511) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 113.1945 sur support (0.47 ATR, 5.078 %) — p(stop avant cible) 0.7326 [0.68 ; 0.78], R/R 3.365, perte reelle 8.128 % (gap inclus), CVaR 5.187 %, EV -2.8891 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5482 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.733, borne haute 0.777 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 5.19 % > budget 4.57 %
- Budget de queue : **4.57 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.47 ATR (stop 5.078 %) — p(stop avant cible) 0.7326 [0.68 ; 0.78], R/R 3.365, perte reelle 8.128 % (gap inclus), EV -2.8891 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.733, borne haute 0.777 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.19 % > budget 4.57 %
      - ⚠ support DETECTE a 0.30 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.89 %) : P(cible) 5.1 % x 27.35 % + P(rien) 21.6 % x 7.67 % ne couvrent pas P(stop) 73.3 % x 8.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 7.68 %) — p(stop avant cible) 0.5877 [0.54 ; 0.64], R/R 2.311, perte reelle 11.838 % (gap inclus), EV -3.4031 % — **REFUSE**
      - refuse : cible atteinte seulement 6.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 7.73 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.40 %) : P(cible) 6.2 % x 27.35 % + P(rien) 35.0 % x 5.30 % ne couvrent pas P(stop) 58.8 % x 11.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.47 ATR (stop 15.334 %) — p(stop avant cible) 0.2913 [0.25 ; 0.34], R/R 1.014, perte reelle 26.975 % (gap inclus), EV -5.2069 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.35 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.21 %) : P(cible) 6.5 % x 27.35 % + P(rien) 64.3 % x 1.34 % ne couvrent pas P(stop) 29.1 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.92 ATR (stop 27.879 %) — p(stop avant cible) 0.0694 [0.05 ; 0.10], R/R 0.981, perte reelle 27.879 % (gap inclus), EV -2.3299 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.88 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.33 %) : P(cible) 6.6 % x 27.35 % + P(rien) 86.5 % x -2.55 % ne couvrent pas P(stop) 6.9 % x 27.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.12 %) — p(stop avant cible) 0.7315 [0.68 ; 0.78], R/R 3.337, perte reelle 8.197 % (gap inclus), EV -2.9343 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.732, borne haute 0.776 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.23 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.93 %) : P(cible) 5.1 % x 27.35 % + P(rien) 21.7 % x 7.62 % ne couvrent pas P(stop) 73.2 % x 8.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 10.24 %) — p(stop avant cible) 0.4683 [0.42 ; 0.52], R/R 1.589, perte reelle 17.215 % (gap inclus), EV -4.491 % — **REFUSE**
      - refuse : cible atteinte seulement 6.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.27 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.49 %) : P(cible) 6.4 % x 27.35 % + P(rien) 46.8 % x 3.91 % ne couvrent pas P(stop) 46.8 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 17.92 %) — p(stop avant cible) 0.2195 [0.18 ; 0.27], R/R 1.014, perte reelle 26.975 % (gap inclus), EV -4.0314 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.93 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.03 %) : P(cible) 6.6 % x 27.35 % + P(rien) 71.4 % x 0.11 % ne couvrent pas P(stop) 21.9 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 20.48 %) — p(stop avant cible) 0.178 [0.14 ; 0.22], R/R 1.014, perte reelle 26.975 % (gap inclus), EV -3.3958 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.49 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.40 %) : P(cible) 6.6 % x 27.35 % + P(rien) 75.6 % x -0.54 % ne couvrent pas P(stop) 17.8 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 23.04 %) — p(stop avant cible) 0.1426 [0.11 ; 0.18], R/R 1.014, perte reelle 26.975 % (gap inclus), EV -2.907 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.05 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.91 %) : P(cible) 6.6 % x 27.35 % + P(rien) 79.1 % x -1.10 % ne couvrent pas P(stop) 14.3 % x 26.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 30.721 %) — p(stop avant cible) 0.0401 [0.02 ; 0.06], R/R 0.89, perte reelle 30.721 % (gap inclus), EV -2.2092 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.72 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.21 %) : P(cible) 6.6 % x 27.35 % + P(rien) 89.4 % x -3.12 % ne couvrent pas P(stop) 4.0 % x 30.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 33.281 %) — p(stop avant cible) 0.0301 [0.02 ; 0.05], R/R 0.822, perte reelle 33.281 % (gap inclus), EV -2.2369 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.28 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.24 %) : P(cible) 6.6 % x 27.35 % + P(rien) 90.4 % x -3.37 % ne couvrent pas P(stop) 3.0 % x 33.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 35.841 %) — p(stop avant cible) 0.0154 [0.01 ; 0.03], R/R 0.763, perte reelle 35.841 % (gap inclus), EV -2.1304 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.84 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.13 %) : P(cible) 6.6 % x 27.35 % + P(rien) 91.8 % x -3.69 % ne couvrent pas P(stop) 1.5 % x 35.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 38.401 %) — p(stop avant cible) 0.0066 [0.00 ; 0.02], R/R 0.712, perte reelle 38.401 % (gap inclus), EV -2.0714 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.40 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.07 %) : P(cible) 6.6 % x 27.35 % + P(rien) 92.7 % x -3.91 % ne couvrent pas P(stop) 0.7 % x 38.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 40.961 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.668, perte reelle 40.961 % (gap inclus), EV -2.0229 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.96 % > budget 4.57 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.02 %) : P(cible) 6.6 % x 27.35 % + P(rien) 93.3 % x -4.06 % ne couvrent pas P(stop) 0.1 % x 40.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.051 | EV/share : $-0.241 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 15 % | T3 15 %
- Kelly (position) : f* 0.074 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.4 | bear 10.4 | side 11.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 238.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.448% → cible +2.591% / stop −4.0%, p_fill 92%, n_eff≈40.1) : P(cible|rempli) **46%** · **EV/risk +0.040** (×p_fill ; si rempli +0.18% du capital)
  - **swing** (entrée dip −1.001% → cible +15.413% / stop −7.707%, p_fill 84%, n_eff≈36.0) : P(cible|rempli) **15%** · **EV/risk +0.045** (×p_fill ; si rempli +0.42% du capital)
  - **deep** (entrée dip −1.47% → cible +8.193% / stop −7.795%, p_fill 86%, n_eff≈37.5) : P(cible|rempli) **56%** · **EV/risk +0.121** (×p_fill ; si rempli +1.10% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→72% · +2.0%→56% · +3.0%→40% · +5.0%→15% · +8.0%→8%
- Range intraday médian 5.44% (p90 9.85%) · excursion haute méd. +2.41% / basse méd. −2.6%
- Profil de vol intra : ouverture 3.394% vs midi 1.211% vs clôture 1.366% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; neutre — autocorr -0.003)_ ; drift intra méd. 0.265% ; recovery-V 22%
- **σ réalisé intraday** 3.736% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 79% / bas 60% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 120.1996 (VA 118.8924–120.4901 ; dernier close 119.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 77% · **stop −4.68%** sous le fill (sous le bruit) · cible +1.66% · R/R 0.35 (high win-rate)
- Gaps overnight (n=159) : méd. -0.03% · baisse 50% (gap-down >1% 38% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.12%) · haut méd +0.71% · range méd 1.77%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.9%) · haut méd +1.18% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.28% (p90 −3.44%) · haut méd +1.37% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.58% (p90 −3.66%) · haut méd +1.72% · range méd 3.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 119.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 75% (124/159) · gap 44% · délai 0.0min · rebond 50% (61/124) (MFE +1.01%)
   - −1.0% : fill 30min 58% · séance 69% (118/159) · gap 38% · délai 0.0min · rebond 57% (68/118) (MFE +1.08%)
   - −1.5% : fill 30min 50% · séance 64% (109/159) · gap 31% · délai 0.0min · rebond 59% (64/109) (MFE +1.51%)
   - −2.0% : fill 30min 46% · séance 57% (99/159) · gap 24% · délai 0.0min · rebond 62% (63/99) (MFE +1.4%)
   - −3.0% : fill 30min 31% · séance 46% (77/159) · gap 13% · délai 2.0min · rebond 60% (47/77) (MFE +1.66%)
   - −4.0% : fill 30min 21% · séance 38% (64/159) · gap 5% · délai 18.1min · rebond 63% (40/64) (MFE +1.65%)
   - −5.0% : fill 30min 14% · séance 27% (47/159) · gap 3% · délai 31.7min · rebond 77% (34/47) (MFE +1.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.8% (p90 −2.46%) → stop au-delà de −1.75% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −2.68%) → stop au-delà de −1.84% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.95% (p90 −2.54%) → stop au-delà de −1.83% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=972 jambes) : jambe baissière méd −1.13% (p90 −2.69%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 100% (76/77) · rebond 52% (38/76)
      · −2.0% : fill 91% (70/77) · rebond 60% (41/70)
      · −3.0% : fill 80% (62/77) · rebond 60% (37/62)
      · −4.0% : fill 66% (52/77) · rebond 65% (34/52)
      · −5.0% : fill 50% (40/77) · rebond 80% (30/40)
   - **flat** (18 séances) :
      · −1.0% : fill 69% (15/18) · rebond 74% (11/15)
      · −2.0% : fill 52% (11/18) · rebond 61% (8/11)
      · −3.0% : fill 22% (5/18) · rebond 55% (3/5)
      · −4.0% : fill 14% (4/18) · rebond 7% (1/4)
      · −5.0% : fill 11% (3/18) · rebond 9% (1/3)
   - **gap-up** (64 séances) :
      · −1.0% : fill 34% (27/64) · rebond 63% (19/27)
      · −2.0% : fill 18% (18/64) · rebond 71% (14/18)
      · −3.0% : fill 12% (10/64) · rebond 57% (7/10)
      · −4.0% : fill 11% (8/64) · rebond 68% (5/8)
      · −5.0% : fill 5% (4/64) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 53% si les 15 1res min sont vertes (82 cas) · 36% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 71% si début vert vs 21% si rouge (base 45% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **71%** · continue >prix actuel 47% ; creux résiduel méd -1.78% (q20 -3.88%) → **SL/trailing à −3.88%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +3.57% → **scale +1.69% / runner +3.57%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **21%** (continue à baisser 53%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.71%** (au-delà de la MAE q10 -4.71%), cible rebond +2.34% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.36% .. +3.61%] · haut q95 +3.97% · bas q05 -3.82%
   - 60min (n=160) : retour [-4.73% .. +3.98%] · haut q95 +5.43% · bas q05 -5.04%
   - 2h (n=160) : retour [-4.37% .. +5.62%] · haut q95 +6.54% · bas q05 -5.18%
   - 4h (n=160) : retour [-5.7% .. +7.99%] · haut q95 +9.02% · bas q05 -6.89%
   - 6h (n=160) : retour [-5.9% .. +6.91%] · haut q95 +9.84% · bas q05 -7.3%
   - session (n=160) : retour [-5.09% .. +6.26%] · haut q95 +9.84% · bas q05 -7.78%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 4.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **22%**. Lecture précoce 30 min : signature présente → 12% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.22% (p75 2.61% / p90 4.03%) · ~3.12 replis/séance, durée méd 49.07 min. P(nouveau plus-haut après repli) :
   - −0.5% → **75%** (reprise méd 15.0 min, n=30)
   - −1.0% → **57%** (reprise méd 38.91 min, n=17)
   - −1.5% → **43%** (reprise méd 74.97 min, n=13)
   - −2.0% → **28%** (reprise méd 89.44 min, n=8)
   - −3.0% → **41%** (reprise méd 89.44 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−4.03%** (p90, défaut prudent ; serré/agressif −2.61%) ; extension open→close méd +8.28% (q75 +9.94% / q95 +16.06%), MFE méd +11.04% / q90 +15.91%
   - Échelle scale-out : +11.04% (33%) / +12.88% (33%) / +15.91% (34%)
- **DÉSARMER** : repli > **−4.03%** depuis le plus-haut = décay → P(retournement) **29%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +15.91% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 98% du temps (retour médian dernière heure +0.79%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : extreme
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

- **RSI** : 71.7  _(surachat)_
- **ADX** : 15.4  _(pas de tendance nette)_
- **MACD** : hist 2.723  _(pas de croisement recent)_
- **BB** : %B 1.28 · largeur 26.7%
- **ATR** : 6.11 (9.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.169  _(accumulation)_
- **Vol ratio** : 2.2  _(volume au-dessus de la moyenne)_
- **Choppiness** : 39.4  _(transition)_
- **MA** : MA20 98.57 · MA50 99.78 · MA200 143.95  _(prix > MA20)_
- **Dist MA** : MA20 +21.0% · MA50 +19.5% · MA200 -17.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (829772 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
