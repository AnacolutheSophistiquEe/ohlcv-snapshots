# SOFI

**Generated** : 2026-10-08T00:34:23.600796+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.66  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (3 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $15.66 (+0.8% vs entrée) · entrée $15.53 · stop $14.28 · T1 $15.79 · R/R 0.21  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +1.5 % ≠ (strike 16.0 − spot 15.66)/spot = +2.2 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -92 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.50–$15.55 (mid $15.53)
- Spot actuel : $15.66 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $14.28 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.05 % depuis l'entree)
- Targets : T1 $15.79 · R/R 0.21 | T2 $16.06 · R/R 0.42 | T3 $16.33 · R/R 0.64
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.28


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.31 %)** : le gap seul le franchit 1.756 % des séances (22 fois sur 1253).
   - exécution **1.492 pt plus bas** dans le cas TYPIQUE (médiane), 4.439 au p90, **5.795 au pire**
   - perte réelle **7.351 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 5.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0358 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0117** [0.0025 ; 0.0368] _(largeur 3.4 pt, n_eff 173.1)_
   - swing : **0.5694** [0.5168 ; 0.6208] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.529** [0.4763 ; 0.5812] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 83.1 observations effectives », dont la borne haute a 95 % vaut environ 3.6 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1080 séances)** : VaR **-5.88 %** | CVaR **-8.34 %** | vol 3.93 %/j
   - _fenêtre arrêtée : rupture de regime a 1140 seances en arriere (volatilite 5.50 % contre 3.43 % aujourd'hui, rapport 1.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8284** (β de hausse 1.7173, asymétrie 1.0647) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.366× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 14.4532 sur atr_grid (2.25 ATR, 7.706 %) — p(stop avant cible) 0.4622 [0.41 ; 0.51], R/R 7.688, perte reelle 8.073 % (gap inclus), CVaR 10.766 %, EV -0.9288 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.44 ATR (stop 3.649 %) — p(stop avant cible) 0.7494 [0.70 ; 0.79], R/R 15.721, perte reelle 3.948 % (gap inclus), EV -0.8311 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 15.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.749, borne haute 0.793 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 0.0 % x 62.06 % + P(rien) 25.1 % x 8.49 % ne couvrent pas P(stop) 74.9 % x 3.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ sr_based a 1.1 ATR (stop 5.902 %) — p(stop avant cible) 0.5931 [0.54 ; 0.64], R/R 9.947, perte reelle 6.24 % (gap inclus), EV -0.8629 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.593, borne haute 0.644 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 0.0 % x 62.06 % + P(rien) 40.7 % x 6.98 % ne couvrent pas P(stop) 59.3 % x 6.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 1.45 ATR (stop 7.115 %) — p(stop avant cible) 0.5061 [0.45 ; 0.56], R/R 8.33, perte reelle 7.451 % (gap inclus), EV -0.8903 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.506, borne haute 0.559 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 0.0 % x 62.06 % + P(rien) 49.4 % x 5.83 % ne couvrent pas P(stop) 50.6 % x 7.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.44 ATR (stop 2.543 %) — p(stop avant cible) 0.8565 [0.82 ; 0.89], R/R 22.486, perte reelle 2.76 % (gap inclus), EV -0.8245 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 22.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.857, borne haute 0.890 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 0.0 % x 62.06 % + P(rien) 14.3 % x 10.74 % ne couvrent pas P(stop) 85.7 % x 2.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 1.1 ATR (stop 4.796 %) — p(stop avant cible) 0.6634 [0.61 ; 0.71], R/R 12.059, perte reelle 5.147 % (gap inclus), EV -0.7762 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 12.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.663, borne haute 0.712 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 0.0 % x 62.06 % + P(rien) 33.7 % x 7.84 % ne couvrent pas P(stop) 66.3 % x 5.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 7.706 %) — p(stop avant cible) 0.4622 [0.41 ; 0.51], R/R 7.688, perte reelle 8.073 % (gap inclus), EV -0.9288 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 0.0 % x 62.06 % + P(rien) 53.8 % x 5.21 % ne couvrent pas P(stop) 46.2 % x 8.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 8.563 %) — p(stop avant cible) 0.4157 [0.36 ; 0.47], R/R 6.904, perte reelle 8.989 % (gap inclus), EV -1.0356 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 0.0 % x 62.06 % + P(rien) 58.4 % x 4.62 % ne couvrent pas P(stop) 41.6 % x 8.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 9.419 %) — p(stop avant cible) 0.3629 [0.31 ; 0.41], R/R 6.265, perte reelle 9.906 % (gap inclus), EV -1.183 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 0.0 % x 62.06 % + P(rien) 63.7 % x 3.79 % ne couvrent pas P(stop) 36.3 % x 9.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 10.275 %) — p(stop avant cible) 0.322 [0.27 ; 0.37], R/R 5.797, perte reelle 10.706 % (gap inclus), EV -1.0913 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 0.0 % x 62.06 % + P(rien) 67.8 % x 3.48 % ne couvrent pas P(stop) 32.2 % x 10.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 11.988 %) — p(stop avant cible) 0.2302 [0.19 ; 0.28], R/R 5.046, perte reelle 12.299 % (gap inclus), EV -0.8421 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.84 %) : P(cible) 0.0 % x 62.06 % + P(rien) 77.0 % x 2.58 % ne couvrent pas P(stop) 23.0 % x 12.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 13.7 %) — p(stop avant cible) 0.1632 [0.13 ; 0.20], R/R 4.454, perte reelle 13.934 % (gap inclus), EV -0.5664 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 0.0 % x 62.06 % + P(rien) 83.7 % x 2.04 % ne couvrent pas P(stop) 16.3 % x 13.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 15.413 %) — p(stop avant cible) 0.1109 [0.08 ; 0.15], R/R 3.996, perte reelle 15.531 % (gap inclus), EV -0.3984 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 0.0 % x 62.06 % + P(rien) 88.9 % x 1.49 % ne couvrent pas P(stop) 11.1 % x 15.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 17.125 %) — p(stop avant cible) 0.0711 [0.05 ; 0.10], R/R 3.599, perte reelle 17.243 % (gap inclus), EV -0.3212 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.0 % x 62.06 % + P(rien) 92.9 % x 0.97 % ne couvrent pas P(stop) 7.1 % x 17.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 18.838 %) — p(stop avant cible) 0.0541 [0.03 ; 0.08], R/R 3.285, perte reelle 18.891 % (gap inclus), EV -0.3187 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.0 % x 62.06 % + P(rien) 94.6 % x 0.74 % ne couvrent pas P(stop) 5.4 % x 18.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 20.55 %) — p(stop avant cible) 0.0432 [0.03 ; 0.07], R/R 3.013, perte reelle 20.599 % (gap inclus), EV -0.3492 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 0.0 % x 62.06 % + P(rien) 95.7 % x 0.57 % ne couvrent pas P(stop) 4.3 % x 20.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 22.263 %) — p(stop avant cible) 0.0296 [0.02 ; 0.05], R/R 2.765, perte reelle 22.444 % (gap inclus), EV -0.3577 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.0 % x 62.06 % + P(rien) 97.0 % x 0.32 % ne couvrent pas P(stop) 3.0 % x 22.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 23.975 %) — p(stop avant cible) 0.0221 [0.01 ; 0.04], R/R 2.563, perte reelle 24.214 % (gap inclus), EV -0.3609 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.0 % x 62.06 % + P(rien) 97.8 % x 0.18 % ne couvrent pas P(stop) 2.2 % x 24.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.5 ATR (stop 25.688 %) — p(stop avant cible) 0.0143 [0.01 ; 0.03], R/R 2.405, perte reelle 25.801 % (gap inclus), EV -0.3148 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 0.0 % x 62.06 % + P(rien) 98.6 % x 0.05 % ne couvrent pas P(stop) 1.4 % x 25.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 8.0 ATR (stop 27.4 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 2.263, perte reelle 27.427 % (gap inclus), EV -0.2363 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 0.0 % x 62.06 % + P(rien) 99.6 % x -0.14 % ne couvrent pas P(stop) 0.4 % x 27.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+62.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.66, ATR14 0.5364 (3.425 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.378 ATR = 1.295 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.171 % | 15.6332 | 92.85 % | 95.77 % | 97.07 % | 97.47 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.343 % | 15.6064 | 85.1 % | 89.31 % | 92.03 % | 93.33 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.514 % | 15.5795 | 78.85 % | 84.58 % | 87.99 % | 90.39 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.685 % | 15.5527 | 71.6 % | 79.33 % | 83.35 % | 86.86 % | 90.55 % | 93.33 % |
| 0.25 ATR | 0.856 % | 15.5259 | 66.26 % | 74.9 % | 80.02 % | 84.23 % | 89.02 % | 91.99 % |
| 0.35 ATR | 1.199 % | 15.4723 | 52.87 % | 65.22 % | 72.05 % | 78.46 % | 85.57 % | 88.81 % |
| 0.5 ATR | 1.713 % | 15.3918 | 37.56 % | 53.12 % | 61.55 % | 69.26 % | 79.57 % | 84.7 % |
| 0.75 ATR | 2.569 % | 15.2577 | 20.44 % | 36.69 % | 46.82 % | 57.13 % | 70.02 % | 78.13 % |
| 1.0 ATR | 3.425 % | 15.1236 | 8.76 % | 24.5 % | 33.91 % | 45.1 % | 59.86 % | 69.61 % |
| 1.25 ATR | 4.281 % | 14.9895 | 4.23 % | 15.12 % | 24.02 % | 35.69 % | 50.81 % | 63.14 % |
| 1.5 ATR | 5.138 % | 14.8555 | 2.01 % | 9.48 % | 16.65 % | 27.4 % | 42.99 % | 56.78 % |
| 2.0 ATR | 6.85 % | 14.5873 | 0.7 % | 4.44 % | 8.38 % | 15.27 % | 29.57 % | 45.79 % |
| 2.5 ATR | 8.563 % | 14.3191 | 0.3 % | 1.92 % | 3.94 % | 9.5 % | 19.72 % | 36.04 % |
| 3.0 ATR | 10.275 % | 14.0509 | 0.1 % | 0.91 % | 2.83 % | 6.17 % | 13.72 % | 28.34 % |
| 4.0 ATR | 13.7 % | 13.5145 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.42 % | 14.68 % |
| 6.0 ATR | 20.55 % | 12.4418 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.94 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.23 ATR | 1.39 ATR | 1.90 ATR | 2.38 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.00 ATR | 1.33 ATR | 1.60 ATR | 1.80 ATR | 2.46 ATR | 3.32 ATR |
| **10 s.** | 0.62 ATR | 1.28 ATR | 1.44 ATR | 1.87 ATR | 2.23 ATR | 2.49 ATR | 3.59 ATR | 4.74 ATR |
| **20 s.** | 0.84 ATR | 1.81 ATR | 2.04 ATR | 2.70 ATR | 3.25 ATR | 3.61 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.427–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.713 %, prix 15.3917), p(touche) 37.56 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.569 %, prix 15.2577), p(touche) 36.69 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.785–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.425 %, prix 15.1236), p(touche) 33.91 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.003–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.281 %, prix 14.9896), p(touche) 35.69 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.436–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.138 %, prix 14.8554), p(touche) 42.99 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.041–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.563 %, prix 14.319), p(touche) 36.04 % (en stress 98.98 %)  ✅ optimum identifie (75.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 6.8 | bear 13.5 | side 79.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.859% → cible +1.727% / stop −8.0%, p_fill 79%, n_eff≈83.1) : P(cible|rempli) **39%** · **EV/risk -0.036** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −1.885% → cible +3.903% / stop −3.49%, p_fill 67%, n_eff≈78.9) : P(cible|rempli) **48%** · **EV/risk +0.041** (×p_fill ; si rempli +0.21% du capital)
  - **deep** (entrée dip −2.912% → cible +5.577% / stop −5.292%, p_fill 68%, n_eff≈76.2) : P(cible|rempli) **52%** · **EV/risk +0.063** (×p_fill ; si rempli +0.49% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→64% · +2.0%→42% · +3.0%→30% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.06% (p90 6.61%) · excursion haute méd. +1.52% / basse méd. −2.06%
- Profil de vol intra : ouverture 2.849% vs midi 0.819% vs clôture 0.934% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 20% · trend ↑1%/↓0% ; spike-down 62% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.153 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.686% ; recovery-V 22%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 64% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 15.8262 (VA 15.8138–15.9262 ; dernier close 15.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 15% · rebond 61% · **stop −2.1%** sous le fill (sous le bruit) · cible +1.97% · R/R 0.94 (high win-rate)
- Gaps overnight (n=159) : méd. 0.17% · baisse 43% (gap-down >1% 22% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.59%) · haut méd +0.65% · range méd 1.42%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −2.37%) · haut méd +0.79% · range méd 2.05%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −3.24%) · haut méd +0.86% · range méd 2.37%
- Excursion ouverture 60min (n=160) : bas méd −1.22% (p90 −3.59%) · haut méd +0.99% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 76% (120/159) · gap 30% · délai 0.1min · rebond 56% (69/120) (MFE +1.22%)
   - −1.0% : fill 30min 49% · séance 63% (105/159) · gap 22% · délai 1.5min · rebond 49% (57/105) (MFE +0.93%)
   - −1.5% : fill 30min 41% · séance 55% (94/159) · gap 19% · délai 6.8min · rebond 59% (61/94) (MFE +1.3%)
   - −2.0% : fill 30min 30% · séance 43% (73/159) · gap 8% · délai 9.8min · rebond 63% (50/73) (MFE +1.47%)
   - −3.0% : fill 30min 7% · séance 30% (52/159) · gap 2% · délai 78.7min · rebond 49% (32/52) (MFE +1.02%)
   - −4.0% : fill 30min 5% · séance 15% (30/159) · gap 1% · délai 86.8min · rebond 61% (19/30) (MFE +1.97%)
   - −5.0% : fill 30min 2% · séance 7% (15/159) · gap 1% · délai 208.5min · rebond 44% (8/15) (MFE +0.67%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.78%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.87%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.43%) → stop au-delà de −1.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=612 jambes) : jambe baissière méd −1.0% (p90 −2.74%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 98% (63/64) · rebond 49% (35/63)
      · −2.0% : fill 85% (54/64) · rebond 68% (37/54)
      · −3.0% : fill 59% (39/64) · rebond 49% (25/39)
      · −4.0% : fill 35% (25/64) · rebond 69% (17/25)
      · −5.0% : fill 15% (13/64) · rebond 52% (7/13)
   - **flat** (24 séances) :
      · −1.0% : fill 76% (16/24) · rebond 31% (6/16)
      · −2.0% : fill 39% (8/24) · rebond 53% (5/8)
      · −3.0% : fill 33% (7/24) · rebond 44% (3/7)
      · −4.0% : fill 11% (3/24) · rebond 30% (1/3)
      · −5.0% : fill 7% (1/24) · rebond 0% (0/1)
   - **gap-up** (71 séances) :
      · −1.0% : fill 32% (26/71) · rebond 65% (16/26)
      · −2.0% : fill 13% (11/71) · rebond 56% (8/11)
      · −3.0% : fill 7% (6/71) · rebond 60% (4/6)
      · −4.0% : fill 2% (2/71) · rebond 20% (1/2)
      · −5.0% : fill 0% (1/71) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 39% en base · 65% si les 15 1res min sont vertes (72 cas) · 22% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 71% si début vert vs 19% si rouge (base 39% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **71%** · continue >prix actuel 51% ; creux résiduel méd -1.51% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +2.64% → **scale +1.8% / runner +2.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **19%** (continue à baisser 63%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.79%** (au-delà de la MAE q10 -2.79%), cible rebond +1.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.96% .. +3.18%] · haut q95 +3.88% · bas q05 -3.58%
   - 60min (n=160) : retour [-3.13% .. +3.65%] · haut q95 +4.44% · bas q05 -3.99%
   - 2h (n=160) : retour [-3.52% .. +3.76%] · haut q95 +4.95% · bas q05 -4.15%
   - 4h (n=160) : retour [-3.89% .. +4.27%] · haut q95 +5.43% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.24% .. +4.07%] · haut q95 +5.44% · bas q05 -5.17%
   - session (n=160) : retour [-4.42% .. +4.63%] · haut q95 +5.47% · bas q05 -5.19%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.73%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.0  _(momentum baissier)_
- **ADX** : 14.9  _(pas de tendance nette)_
- **MACD** : hist -0.062  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 15.5%
- **ATR** : 0.54 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.349  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 41.5  _(transition)_
- **MA** : MA20 16.52 · MA50 17.4 · MA200 18.79  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 -10.0% · MA200 -16.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (854321 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
