# RGTI

**Generated** : 2026-10-05T00:28:28.668487+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.25  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (usable=false (intervalle le plus large 28.7 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $15.25 (+3.8% vs entrée) · entrée $14.69 · stop $14.40 · T1 $15.15 · R/R 1.59  
> ↳ ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -186 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $14.65–$14.74 (mid $14.69)
- Spot actuel : $15.25 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : $14.40 (plancher anti-bruit 5 s — stop EV-optimal −2% (first-passage 5 s réel) ; -1.97 % depuis l'entree)
- Targets : T1 $15.15 · R/R 1.59 | T2 $15.60 · R/R 3.14 | T3 $16.06 · R/R 4.72
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.40


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.45 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (14.0 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1254).
   - exécution **2.286 pt plus bas** dans le cas TYPIQUE (médiane), 13.224 au p90, **17.213 au pire**
   - perte réelle **19.597 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 14.0 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0179 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.112 % | p01 -8.97 % | pire -31.213 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4997** [0.4257 ; 0.5737] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4916** [0.4392 ; 0.5442] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5284** [0.4757 ; 0.5806] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (28.7 pt), swing (37.0 pt), deep (36.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.95 %** | CVaR **-11.33 %** | vol 6.83 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 19.47 % contre 6.39 % aujourd'hui, rapport 3.05)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.75 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8458** (β de hausse 1.9959, asymétrie 0.9248) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.502× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 14.1118 sur atr_grid (1.25 ATR, 7.464 %) — p(stop avant cible) 0.6665 [0.62 ; 0.71], R/R 3.018, perte reelle 7.586 % (gap inclus), CVaR 9.077 %, EV -0.3309 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2993 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.666, borne haute 0.715 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **25.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 1.02 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 61.0 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 28.52 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.957 %) — p(stop avant cible) 0.6258 [0.57 ; 0.68], R/R 2.51, perte reelle 9.122 % (gap inclus), EV -0.6736 % — **REFUSE**
      - refuse : p_stop_first 0.626, borne haute 0.676 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 18.3 % x 22.90 % + P(rien) 19.1 % x 4.45 % ne couvrent pas P(stop) 62.6 % x 9.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 2.55 ATR (stop 17.993 %) — p(stop avant cible) 0.2491 [0.21 ; 0.30], R/R 1.254, perte reelle 18.256 % (gap inclus), EV -0.0477 % — **REFUSE**
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 22.4 % x 22.90 % + P(rien) 52.7 % x -1.18 % ne couvrent pas P(stop) 24.9 % x 18.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.99 ATR (stop 20.63 %) — p(stop avant cible) 0.1874 [0.15 ; 0.23], R/R 1.09, perte reelle 20.999 % (gap inclus), EV 0.0935 % — **REFUSE**
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.25 ATR (stop 1.493 %) — p(stop avant cible) 0.9307 [0.90 ; 0.95], R/R 14.636, perte reelle 1.564 % (gap inclus), EV -0.0594 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 14.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.931, borne haute 0.954 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 5.4 % x 22.90 % + P(rien) 1.5 % x 10.14 % ne couvrent pas P(stop) 93.1 % x 1.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.985 %) — p(stop avant cible) 0.8505 [0.81 ; 0.89], R/R 7.492, perte reelle 3.056 % (gap inclus), EV -0.0406 % — **REFUSE**
      - refuse : cible atteinte seulement 9.5 % du temps (< 15 %) meme a 10 seances : le R/R de 7.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.851, borne haute 0.885 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 9.5 % x 22.90 % + P(rien) 5.4 % x 7.05 % ne couvrent pas P(stop) 85.0 % x 3.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.478 %) — p(stop avant cible) 0.7951 [0.75 ; 0.84], R/R 5.011, perte reelle 4.57 % (gap inclus), EV -0.2302 % — **REFUSE**
      - refuse : cible atteinte seulement 12.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.795, borne haute 0.835 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 12.3 % x 22.90 % + P(rien) 8.2 % x 7.17 % ne couvrent pas P(stop) 79.5 % x 4.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 5.971 %) — p(stop avant cible) 0.7275 [0.68 ; 0.77], R/R 3.738, perte reelle 6.126 % (gap inclus), EV -0.3104 % — **REFUSE**
      - refuse : p_stop_first 0.728, borne haute 0.772 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 15.1 % x 22.90 % + P(rien) 12.2 % x 5.65 % ne couvrent pas P(stop) 72.8 % x 6.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 7.464 %) — p(stop avant cible) 0.6665 [0.62 ; 0.71], R/R 3.018, perte reelle 7.586 % (gap inclus), EV -0.3309 % — **REFUSE**
      - refuse : p_stop_first 0.666, borne haute 0.715 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 17.3 % x 22.90 % + P(rien) 16.1 % x 4.77 % ne couvrent pas P(stop) 66.6 % x 7.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 10.449 %) — p(stop avant cible) 0.5894 [0.54 ; 0.64], R/R 2.161, perte reelle 10.594 % (gap inclus), EV -1.1284 % — **REFUSE**
      - refuse : p_stop_first 0.589, borne haute 0.640 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 19.1 % x 22.90 % + P(rien) 21.9 % x 3.37 % ne couvrent pas P(stop) 58.9 % x 10.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 11.942 %) — p(stop avant cible) 0.5173 [0.46 ; 0.57], R/R 1.889, perte reelle 12.118 % (gap inclus), EV -0.9507 % — **REFUSE**
      - refuse : p_stop_first 0.517, borne haute 0.570 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 20.1 % x 22.90 % + P(rien) 28.2 % x 2.55 % ne couvrent pas P(stop) 51.7 % x 12.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 13.435 %) — p(stop avant cible) 0.4307 [0.38 ; 0.48], R/R 1.684, perte reelle 13.594 % (gap inclus), EV -0.5483 % — **REFUSE**
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 20.5 % x 22.90 % + P(rien) 36.5 % x 1.71 % ne couvrent pas P(stop) 43.1 % x 13.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 2.55 ATR (stop 16.99 %) — p(stop avant cible) 0.299 [0.25 ; 0.35], R/R 1.331, perte reelle 17.202 % (gap inclus), EV -0.3158 % — **REFUSE**
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 21.9 % x 22.90 % + P(rien) 48.1 % x -0.41 % ne couvrent pas P(stop) 29.9 % x 17.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 2.99 ATR (stop 19.627 %) — p(stop avant cible) 0.2193 [0.18 ; 0.27], R/R 1.15, perte reelle 19.911 % (gap inclus), EV -0.0323 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 22.8 % x 22.90 % + P(rien) 55.2 % x -1.62 % ne couvrent pas P(stop) 21.9 % x 19.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 23.884 %) — p(stop avant cible) 0.115 [0.08 ; 0.15], R/R 0.947, perte reelle 24.171 % (gap inclus), EV 0.2299 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 26.869 %) — p(stop avant cible) 0.0752 [0.05 ; 0.11], R/R 0.845, perte reelle 27.094 % (gap inclus), EV 0.3468 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.21 % > budget 25.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.855 %) — p(stop avant cible) 0.0588 [0.04 ; 0.09], R/R 0.762, perte reelle 30.066 % (gap inclus), EV 0.3394 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.10 % > budget 25.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.84 %) — p(stop avant cible) 0.0356 [0.02 ; 0.06], R/R 0.693, perte reelle 33.043 % (gap inclus), EV 0.4076 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.57 % > budget 25.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.826 %) — p(stop avant cible) 0.0235 [0.01 ; 0.04], R/R 0.634, perte reelle 36.134 % (gap inclus), EV 0.4496 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.63 % > budget 25.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.811 %) — p(stop avant cible) 0.0125 [0.00 ; 0.03], R/R 0.585, perte reelle 39.111 % (gap inclus), EV 0.4931 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.82 % > budget 25.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 41.797 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 0.548, perte reelle 41.821 % (gap inclus), EV 0.5442 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.64 % > budget 25.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 44.782 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.503, perte reelle 45.481 % (gap inclus), EV 0.5382 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.78 % > budget 25.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 47.768 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.479, perte reelle 47.768 % (gap inclus), EV 0.5421 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.79 % > budget 25.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.25, ATR14 0.9106 (5.971 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.407 ATR = 2.43 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.299 % | 15.2045 | 91.95 % | 94.36 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.597 % | 15.1589 | 86.22 % | 90.94 % | 92.34 % | 94.85 % | 95.94 % | 97.44 % |
| 0.15 ATR | 0.896 % | 15.1134 | 80.68 % | 87.21 % | 89.01 % | 91.92 % | 94.01 % | 96.1 % |
| 0.2 ATR | 1.194 % | 15.0679 | 74.14 % | 82.68 % | 85.48 % | 88.69 % | 91.47 % | 94.46 % |
| 0.25 ATR | 1.493 % | 15.0224 | 68.01 % | 78.35 % | 81.45 % | 85.56 % | 88.83 % | 92.51 % |
| 0.35 ATR | 2.09 % | 14.9313 | 55.53 % | 68.28 % | 73.59 % | 79.29 % | 84.37 % | 89.64 % |
| 0.5 ATR | 2.985 % | 14.7947 | 41.05 % | 56.8 % | 64.52 % | 71.31 % | 78.88 % | 85.33 % |
| 0.75 ATR | 4.478 % | 14.5671 | 21.83 % | 38.77 % | 49.7 % | 58.69 % | 70.56 % | 79.08 % |
| 1.0 ATR | 5.971 % | 14.3394 | 9.86 % | 23.87 % | 33.47 % | 46.36 % | 61.62 % | 72.72 % |
| 1.25 ATR | 7.464 % | 14.1118 | 4.23 % | 14.6 % | 23.59 % | 36.67 % | 52.59 % | 65.44 % |
| 1.5 ATR | 8.956 % | 13.8841 | 1.81 % | 7.15 % | 13.61 % | 25.35 % | 42.74 % | 57.33 % |
| 2.0 ATR | 11.942 % | 13.4289 | 0.4 % | 1.81 % | 4.03 % | 10.71 % | 25.18 % | 41.23 % |
| 2.5 ATR | 14.927 % | 12.9736 | 0.1 % | 0.4 % | 1.21 % | 4.34 % | 14.31 % | 29.03 % |
| 3.0 ATR | 17.913 % | 12.5183 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.33 % |
| 4.0 ATR | 23.884 % | 11.6077 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.82 % |
| 6.0 ATR | 35.826 % | 9.7866 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 1.00 ATR | 1.22 ATR |
| **2 s.** | 0.28 ATR | 0.59 ATR | 0.66 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.33 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.21 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.03 ATR | 1.33 ATR | 1.51 ATR | 1.68 ATR | 2.06 ATR | 2.45 ATR |
| **10 s.** | 0.62 ATR | 1.32 ATR | 1.44 ATR | 1.78 ATR | 2.01 ATR | 2.24 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.91 ATR | 1.73 ATR | 1.88 ATR | 2.34 ATR | 2.67 ATR | 2.89 ATR | 3.59 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.459–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.985 %, prix 14.7948), p(touche) 41.05 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (70.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.664–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.478 %, prix 14.5671), p(touche) 38.77 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.822–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.971 %, prix 14.3394), p(touche) 33.47 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.035–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.464 %, prix 14.1117), p(touche) 36.67 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.443–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.956 %, prix 13.8842), p(touche) 42.74 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.883–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.942 %, prix 13.4288), p(touche) 41.23 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.011 | EV/share : $0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 — | T3 —
- Kelly (position) : f* 0.016 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.6 | side 77.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.654% → cible +3.099% / stop −2.0%, p_fill 36%, n_eff≈41.9) : P(cible|rempli) **13%** · **EV/risk -0.169** (×p_fill ; si rempli -0.93% du capital)
  - **swing** (entrée dip −8.029% → cible +7.259% / stop −6.493%, p_fill 20%, n_eff≈25.4) : P(cible|rempli) **44%** · **EV/risk -0.006** (×p_fill ; si rempli -0.19% du capital)
  - **deep** (entrée dip −12.414% → cible +10.778% / stop −10.226%, p_fill 22%, n_eff≈26.6) : P(cible|rempli) **51%** · **EV/risk +0.031** (×p_fill ; si rempli +1.45% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→77% · +2.0%→64% · +3.0%→46% · +5.0%→31% · +8.0%→10%
- Range intraday médian 6.8% (p90 11.03%) · excursion haute méd. +2.76% / basse méd. −2.46%
- Profil de vol intra : ouverture 4.714% vs midi 1.402% vs clôture 1.624% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 21% · trend ↑0%/↓0% ; spike-down 65% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; neutre — autocorr -0.001)_ ; drift intra méd. -0.541% ; recovery-V 20%
- **σ réalisé intraday** 3.707% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 15.5684 (VA 15.2377–15.7574 ; dernier close 15.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 37% · rebond 75% · **stop −5.27%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 55% (gap-down >1% 36% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.87%) · haut méd +1.18% · range méd 2.39%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.58%) · haut méd +1.56% · range méd 3.3%
- Excursion ouverture 30min (n=160) : bas méd −1.45% (p90 −4.44%) · haut méd +1.84% · range méd 3.8%
- Excursion ouverture 60min (n=160) : bas méd −1.69% (p90 −5.46%) · haut méd +2.09% · range méd 4.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.25 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (130/159) · gap 44% · délai 0.0min · rebond 63% (83/130) (MFE +1.59%)
   - −1.0% : fill 30min 60% · séance 71% (119/159) · gap 36% · délai 0.0min · rebond 70% (78/119) (MFE +1.68%)
   - −1.5% : fill 30min 54% · séance 63% (111/159) · gap 27% · délai 0.0min · rebond 68% (74/111) (MFE +1.92%)
   - −2.0% : fill 30min 48% · séance 57% (102/159) · gap 22% · délai 0.2min · rebond 67% (68/102) (MFE +2.13%)
   - −3.0% : fill 30min 33% · séance 48% (89/159) · gap 8% · délai 8.9min · rebond 65% (63/89) (MFE +1.87%)
   - −4.0% : fill 30min 24% · séance 37% (67/159) · gap 5% · délai 15.3min · rebond 75% (50/67) (MFE +2.24%)
   - −5.0% : fill 30min 12% · séance 26% (54/159) · gap 1% · délai 32.8min · rebond 57% (35/54) (MFE +1.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.86%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.28%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −2.38%) → stop au-delà de −1.65% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1068 jambes) : jambe baissière méd −1.27% (p90 −3.0%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 92% (79/83) · rebond 66% (48/79)
      · −2.0% : fill 82% (73/83) · rebond 68% (48/73)
      · −3.0% : fill 70% (66/83) · rebond 62% (45/66)
      · −4.0% : fill 60% (52/83) · rebond 70% (38/52)
      · −5.0% : fill 43% (43/83) · rebond 50% (26/43)
   - **flat** (16 séances) :
      · −1.0% : fill 84% (14/16) · rebond 98% (13/14)
      · −2.0% : fill 48% (10/16) · rebond 90% (9/10)
      · −3.0% : fill 24% (5/16) · rebond 92% (4/5)
      · −4.0% : fill 16% (4/16) · rebond 87% (3/4)
      · −5.0% : fill 10% (3/16) · rebond 100% (3/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 41% (26/60) · rebond 64% (17/26)
      · −2.0% : fill 30% (19/60) · rebond 53% (11/19)
      · −3.0% : fill 29% (18/60) · rebond 65% (14/18)
      · −4.0% : fill 15% (11/60) · rebond 91% (9/11)
      · −5.0% : fill 10% (8/60) · rebond 78% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 70% si les 15 1res min sont vertes (86 cas) · 21% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 86% si début vert vs 10% si rouge (base 47% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **86%** · continue >prix actuel 47% ; creux résiduel méd -1.49% (q20 -2.51%) → **SL/trailing à −2.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +3.2% → **scale +1.67% / runner +3.2%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **10%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.18%** (au-delà de la MAE q10 -4.18%), cible rebond +1.6% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.03% .. +4.37%] · haut q95 +5.8% · bas q05 -6.04%
   - 60min (n=160) : retour [-6.1% .. +5.82%] · haut q95 +6.56% · bas q05 -7.0%
   - 2h (n=160) : retour [-6.68% .. +5.93%] · haut q95 +6.77% · bas q05 -7.24%
   - 4h (n=160) : retour [-6.76% .. +6.25%] · haut q95 +7.97% · bas q05 -7.75%
   - 6h (n=160) : retour [-6.74% .. +6.96%] · haut q95 +9.18% · bas q05 -8.44%
   - session (n=160) : retour [-7.06% .. +7.17%] · haut q95 +9.19% · bas q05 -8.49%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 1.66% / p90 2.43%) · ~4.04 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.0 min, n=43)
   - −1.0% → **83%** (reprise méd 35.0 min, n=27)
   - −1.5% → **83%** (reprise méd 93.49 min, n=16)
   - −2.0% → **84%** (reprise méd 44.98 min, n=8)
   - −3.0% → **66%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.43%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.12% (q75 +9.53% / q95 +9.89%), MFE méd +9.52% / q90 +11.18%
   - Échelle scale-out : +9.52% (33%) / +10.45% (33%) / +11.18% (34%)
- **DÉSARMER** : repli > **−2.43%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.18% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.12%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.6 · part idiosyncratique 0.4
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 49.8  _(neutre)_
- **ADX** : 9.8  _(pas de tendance nette)_
- **MACD** : hist -0.009  _(bearish_recent)_
- **BB** : %B 0.29 · largeur 14.0%
- **ATR** : 0.91 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.233  _(distribution)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 51.8  _(transition)_
- **MA** : MA20 15.7 · MA50 16.14 · MA200 18.33  _(prix < MA20)_
- **Dist MA** : MA20 -2.9% · MA50 -5.5% · MA200 -16.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (841054 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
