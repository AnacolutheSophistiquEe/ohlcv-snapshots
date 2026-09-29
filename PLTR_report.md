# PLTR

**Generated** : 2026-09-29T00:36:02.461691+00:00  
**Santé technique** : 10/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $187.56  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $187.56 (+8.5% vs entrée) · entrée $172.82 · stop $167.09 · T1 $179.32 · R/R 1.13  
> ↳ P(T1 av. stop) 57 % · EV/risk -0.019 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -3.8 % ≠ (strike 182.5 − spot 187.56)/spot = -2.7 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 72.9 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $171.52–$174.12 (mid $172.82)
- Spot actuel : $187.56 (+8.5% au-dessus de la zone — repli à attendre)
- Stop : $167.09 (plancher anti-bruit (R/R<2) ; -3.32 % depuis l'entree)
- Targets : T1 $179.32 · R/R 1.13 | T2 $185.81 · R/R 2.27 | T3 $192.31 · R/R 3.4
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $167.09


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.91 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **1.863 pt plus bas** dans le cas TYPIQUE (médiane), 5.718 au p90, **7.022 au pire**
   - perte réelle **13.763 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 10.91 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0114 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.861 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4774** [0.4039 ; 0.5517] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4972** [0.4447 ; 0.5497] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4341** [0.3826 ; 0.4867] _(largeur 10.4 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.14 %** | CVaR **-8.41 %** | vol 4.27 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.31 % vs -13.73 % si l'on extrapolait par √5 _(rapport 0.969 ; < 1 = le √5 surestime)_
- **β de baisse : 1.684** (β de hausse 1.421, asymétrie 1.185) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.769× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 167.4945 sur atr_grid (3.5 ATR, 10.698 %) — p(stop avant cible) 0.1652 [0.13 ; 0.21], R/R 0.184, perte reelle 13.763 % (gap inclus), CVaR 10.71 %, EV -0.4025 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.585 %) — p(stop avant cible) 0.3413 [0.29 ; 0.39], R/R 0.325, perte reelle 7.779 % (gap inclus), EV -1.0027 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 65.6 % x 2.53 % + P(rien) 0.3 % x -3.22 % ne couvrent pas P(stop) 34.1 % x 7.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 4.21 ATR (stop 14.888 %) — p(stop avant cible) 0.0733 [0.05 ; 0.10], R/R 0.141, perte reelle 17.932 % (gap inclus), EV -0.0518 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 80.6 % x 2.53 % + P(rien) 12.1 % x -6.43 % ne couvrent pas P(stop) 7.3 % x 17.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 4.77 ATR (stop 16.601 %) — p(stop avant cible) 0.0601 [0.04 ; 0.09], R/R 0.141, perte reelle 17.932 % (gap inclus), EV 0.1023 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.60 % > budget 12.00 %
   - 🟢 support a 6.98 ATR (stop 23.335 %) — p(stop avant cible) 0.0131 [0.00 ; 0.03], R/R 0.109, perte reelle 23.335 % (gap inclus), EV 0.3046 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.34 % > budget 12.00 %
   - 🟢 support a 12.15 ATR (stop 39.154 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.065, perte reelle 39.154 % (gap inclus), EV 0.3838 % — **REFUSE**
      - refuse : R/R 0.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.15 % > budget 12.00 %
   - 🟢 support a 14.16 ATR (stop 45.296 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.056, perte reelle 45.296 % (gap inclus), EV 0.3836 % — **REFUSE**
      - refuse : R/R 0.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.30 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.764 %) — p(stop avant cible) 0.7343 [0.69 ; 0.78], R/R 1.155, perte reelle 2.193 % (gap inclus), EV -0.9376 % — **REFUSE**
      - refuse : p_stop_first 0.734, borne haute 0.779 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 26.6 % x 2.53 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 73.4 % x 2.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.528 %) — p(stop avant cible) 0.6058 [0.55 ; 0.66], R/R 0.839, perte reelle 3.017 % (gap inclus), EV -0.8296 % — **REFUSE**
      - refuse : p_stop_first 0.606, borne haute 0.656 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 39.4 % x 2.53 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 60.6 % x 3.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.292 %) — p(stop avant cible) 0.5001 [0.45 ; 0.55], R/R 0.624, perte reelle 4.058 % (gap inclus), EV -0.7637 % — **REFUSE**
      - refuse : p_stop_first 0.500, borne haute 0.553 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 50.0 % x 2.53 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 50.0 % x 4.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.057 %) — p(stop avant cible) 0.4559 [0.40 ; 0.51], R/R 0.47, perte reelle 5.385 % (gap inclus), EV -1.0774 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 54.4 % x 2.53 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 45.6 % x 5.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 3.821 %) — p(stop avant cible) 0.4027 [0.35 ; 0.46], R/R 0.377, perte reelle 6.717 % (gap inclus), EV -1.1926 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 59.7 % x 2.53 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 40.3 % x 6.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 5.349 %) — p(stop avant cible) 0.2989 [0.25 ; 0.35], R/R 0.282, perte reelle 8.963 % (gap inclus), EV -0.9276 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 69.4 % x 2.53 % + P(rien) 0.7 % x -0.86 % ne couvrent pas P(stop) 29.9 % x 8.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 6.113 %) — p(stop avant cible) 0.2624 [0.22 ; 0.31], R/R 0.254, perte reelle 9.984 % (gap inclus), EV -0.7849 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 72.7 % x 2.53 % + P(rien) 1.1 % x -0.57 % ne couvrent pas P(stop) 26.2 % x 9.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 6.877 %) — p(stop avant cible) 0.2246 [0.18 ; 0.27], R/R 0.23, perte reelle 11.024 % (gap inclus), EV -0.5453 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 76.5 % x 2.53 % + P(rien) 1.1 % x -0.57 % ne couvrent pas P(stop) 22.5 % x 11.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 7.642 %) — p(stop avant cible) 0.2137 [0.17 ; 0.26], R/R 0.211, perte reelle 11.982 % (gap inclus), EV -0.6155 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 77.2 % x 2.53 % + P(rien) 1.4 % x -0.70 % ne couvrent pas P(stop) 21.4 % x 11.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 8.406 %) — p(stop avant cible) 0.1977 [0.16 ; 0.24], R/R 0.202, perte reelle 12.528 % (gap inclus), EV -0.5371 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 78.1 % x 2.53 % + P(rien) 2.1 % x -1.79 % ne couvrent pas P(stop) 19.8 % x 12.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 9.17 %) — p(stop avant cible) 0.186 [0.15 ; 0.23], R/R 0.193, perte reelle 13.126 % (gap inclus), EV -0.5144 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 78.4 % x 2.53 % + P(rien) 3.0 % x -1.90 % ne couvrent pas P(stop) 18.6 % x 13.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 10.698 %) — p(stop avant cible) 0.1652 [0.13 ; 0.21], R/R 0.184, perte reelle 13.763 % (gap inclus), EV -0.4025 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 79.0 % x 2.53 % + P(rien) 4.4 % x -2.94 % ne couvrent pas P(stop) 16.5 % x 13.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 4.21 ATR (stop 13.796 %) — p(stop avant cible) 0.0944 [0.07 ; 0.13], R/R 0.155, perte reelle 16.302 % (gap inclus), EV -0.121 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 80.3 % x 2.53 % + P(rien) 10.3 % x -5.98 % ne couvrent pas P(stop) 9.4 % x 16.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 4.77 ATR (stop 15.509 %) — p(stop avant cible) 0.0651 [0.04 ; 0.09], R/R 0.141, perte reelle 17.932 % (gap inclus), EV 0.0614 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.51 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.34 %) — p(stop avant cible) 0.0553 [0.03 ; 0.08], R/R 0.138, perte reelle 18.34 % (gap inclus), EV 0.1158 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.34 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.868 %) — p(stop avant cible) 0.0346 [0.02 ; 0.06], R/R 0.127, perte reelle 19.868 % (gap inclus), EV 0.2075 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.87 % > budget 12.00 %
   - 🟢 grid_snapped a 6.98 ATR (stop 22.243 %) — p(stop avant cible) 0.0169 [0.01 ; 0.03], R/R 0.114, perte reelle 22.243 % (gap inclus), EV 0.285 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.24 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 22.925 %) — p(stop avant cible) 0.0134 [0.00 ; 0.03], R/R 0.11, perte reelle 22.925 % (gap inclus), EV 0.3026 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.93 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 24.453 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 0.104, perte reelle 24.453 % (gap inclus), EV 0.3483 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.45 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 187.56, ATR14 5.733 (3.057 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.36 ATR = 1.1 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.153 % | 187.2733 | 92.65 % | 95.16 % | 95.96 % | 96.76 % | 98.07 % | 98.67 % |
| 0.1 ATR | 0.306 % | 186.9867 | 84.69 % | 89.31 % | 91.22 % | 93.43 % | 95.02 % | 96.41 % |
| 0.15 ATR | 0.458 % | 186.7 | 77.14 % | 83.67 % | 85.97 % | 89.79 % | 92.38 % | 94.25 % |
| 0.2 ATR | 0.611 % | 186.4134 | 69.18 % | 78.23 % | 81.74 % | 86.35 % | 90.24 % | 92.51 % |
| 0.25 ATR | 0.764 % | 186.1267 | 62.24 % | 73.59 % | 77.6 % | 82.91 % | 87.91 % | 90.97 % |
| 0.35 ATR | 1.07 % | 185.5534 | 50.96 % | 65.42 % | 71.04 % | 78.06 % | 83.84 % | 87.99 % |
| 0.5 ATR | 1.528 % | 184.6935 | 36.05 % | 52.72 % | 59.64 % | 69.06 % | 77.95 % | 83.47 % |
| 0.75 ATR | 2.292 % | 183.2602 | 19.44 % | 35.08 % | 44.6 % | 55.41 % | 66.97 % | 76.28 % |
| 1.0 ATR | 3.057 % | 181.827 | 8.96 % | 22.78 % | 32.49 % | 43.88 % | 56.4 % | 67.35 % |
| 1.25 ATR | 3.821 % | 180.3937 | 4.43 % | 15.42 % | 23.21 % | 34.07 % | 46.44 % | 58.52 % |
| 1.5 ATR | 4.585 % | 178.9605 | 2.11 % | 10.48 % | 17.36 % | 26.59 % | 39.84 % | 54.0 % |
| 2.0 ATR | 6.113 % | 176.094 | 0.6 % | 3.73 % | 9.38 % | 15.77 % | 29.07 % | 40.55 % |
| 2.5 ATR | 7.642 % | 173.2275 | 0.1 % | 1.51 % | 3.33 % | 9.3 % | 19.41 % | 30.29 % |
| 3.0 ATR | 9.17 % | 170.361 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 12.226 % | 164.628 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 18.34 % | 153.162 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.09 ATR | 1.54 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.39 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.29 ATR | 1.57 ATR | 1.80 ATR | 2.45 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.16 ATR | 1.30 ATR | 1.82 ATR | 2.21 ATR | 2.47 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.79 ATR | 1.65 ATR | 1.83 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.41–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.528 %, prix 184.6941), p(touche) 36.05 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.609–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.292 %, prix 183.2611), p(touche) 35.08 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.743–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.292 %, prix 183.2611), p(touche) 44.6 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.976–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.057 %, prix 181.8263), p(touche) 43.88 % (en stress 100.0 %)  ✅ optimum identifie (81.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.305–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.585 %, prix 178.9604), p(touche) 39.84 % (en stress 100.0 %)  ✅ optimum identifie (88.1 % des re-echantillons)
- **20 seance(s)** : plage utile 1.835–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (9.17 %, prix 170.3607), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : $-0.045 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 23 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 55.4 | bear 24.8 | side 19.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 563.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=17, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→49% · +3.0%→30% · +5.0%→11% · +8.0%→4%
- Range intraday médian 4.13% (p90 7.39%) · excursion haute méd. +1.92% / basse méd. −1.67%
- Profil de vol intra : ouverture 3.101% vs midi 0.751% vs clôture 0.844% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 74% · range 24% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.151 ; neutre — autocorr 0.004)_ ; drift intra méd. 0.512% ; recovery-V 20%
- **σ réalisé intraday** 2.612% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 50% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 174.1906 (VA 173.9824–176.0649 ; dernier close 174.31)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 21% · rebond 52% · **stop −3.93%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.27 (high win-rate)
- Gaps overnight (n=159) : méd. -0.28% · baisse 56% (gap-down >1% 30% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.04%) · haut méd +0.97% · range méd 1.91%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.79%) · haut méd +1.18% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.01% (p90 −3.47%) · haut méd +1.3% · range méd 2.71%
- Excursion ouverture 60min (n=160) : bas méd −1.16% (p90 −3.55%) · haut méd +1.39% · range méd 3.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 174.33 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 76% (119/159) · gap 42% · délai 0.0min · rebond 55% (64/119) (MFE +1.16%)
   - −1.0% : fill 30min 56% · séance 66% (109/159) · gap 30% · délai 0.0min · rebond 62% (65/109) (MFE +1.34%)
   - −1.5% : fill 30min 44% · séance 54% (91/159) · gap 20% · délai 0.1min · rebond 62% (56/91) (MFE +1.27%)
   - −2.0% : fill 30min 38% · séance 49% (80/159) · gap 10% · délai 1.4min · rebond 63% (50/80) (MFE +1.35%)
   - −3.0% : fill 30min 23% · séance 32% (58/159) · gap 6% · délai 4.6min · rebond 54% (28/58) (MFE +1.36%)
   - −4.0% : fill 30min 15% · séance 21% (39/159) · gap 3% · délai 8.2min · rebond 52% (18/39) (MFE +1.06%)
   - −5.0% : fill 30min 7% · séance 14% (28/159) · gap 1% · délai 28.8min · rebond 45% (13/28) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.72%) → stop au-delà de −1.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −1.71%) → stop au-delà de −1.1% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −1.28%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=552 jambes) : jambe baissière méd −1.07% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 89% (72/77) · rebond 61% (43/72)
      · −2.0% : fill 72% (59/77) · rebond 64% (36/59)
      · −3.0% : fill 54% (45/77) · rebond 52% (22/45)
      · −4.0% : fill 37% (32/77) · rebond 54% (15/32)
      · −5.0% : fill 26% (24/77) · rebond 50% (12/24)
   - **flat** (24 séances) :
      · −1.0% : fill 72% (20/24) · rebond 41% (9/20)
      · −2.0% : fill 57% (14/24) · rebond 62% (9/14)
      · −3.0% : fill 31% (10/24) · rebond 58% (5/10)
      · −4.0% : fill 18% (6/24) · rebond 41% (3/6)
      · −5.0% : fill 10% (3/24) · rebond 9% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 33% (17/58) · rebond 83% (13/17)
      · −2.0% : fill 15% (7/58) · rebond 57% (5/7)
      · −3.0% : fill 4% (3/58) · rebond 71% (1/3)
      · −4.0% : fill 1% (1/58) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 70% si les 15 1res min sont vertes (83 cas) · 30% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 85% si début vert vs 17% si rouge (base 52% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **85%** · continue >prix actuel 55% ; creux résiduel méd -0.84% (q20 -1.49%) → **SL/trailing à −1.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +2.18% → **scale +1.06% / runner +2.18%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **17%** (continue à baisser 51%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.77%** (au-delà de la MAE q10 -2.77%), cible rebond +1.18% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.41% .. +4.57%] · haut q95 +4.99% · bas q05 -3.97%
   - 60min (n=160) : retour [-3.45% .. +5.92%] · haut q95 +6.29% · bas q05 -4.19%
   - 2h (n=160) : retour [-4.1% .. +6.18%] · haut q95 +6.97% · bas q05 -4.51%
   - 4h (n=160) : retour [-4.41% .. +5.88%] · haut q95 +6.96% · bas q05 -5.82%
   - 6h (n=160) : retour [-4.59% .. +6.51%] · haut q95 +7.39% · bas q05 -6.3%
   - session (n=160) : retour [-4.24% .. +5.84%] · haut q95 +7.69% · bas q05 -6.3%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 3.1% / strong 4.4%) · base = 12 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **40%**. Lecture précoce 30 min : signature présente → 19% vs absente 4% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.13% / p90 1.49%) · ~2.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 43.27 min, n=37)
   - −1.0% → **51%** (reprise méd 65.0 min, n=11)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.49%** (p90, défaut prudent ; serré/agressif −1.13%) ; extension open→close méd +4.31% (q75 +7.51% / q95 +12.13%), MFE méd +5.25% / q90 +12.03%
   - Échelle scale-out : +5.25% (33%) / +7.95% (33%) / +12.03% (34%)
- **DÉSARMER** : repli > **−1.49%** depuis le plus-haut = décay → P(retournement) **82%** (préavis méd 214.54 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.03% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 58% du temps (retour médian dernière heure +0.19%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 72.9  _(surachat)_
- **ADX** : 25.8  _(tendance etablie)_
- **MACD** : hist 0.776  _(bullish_recent)_
- **BB** : %B 0.77 · largeur 18.9%
- **ATR** : 5.73 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.111  _(accumulation)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 37.1  _(marche directionnel)_
- **MA** : MA20 178.47 · MA50 165.03 · MA200 152.05  _(prix > MA20)_
- **Dist MA** : MA20 +5.1% · MA50 +13.7% · MA200 +23.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (861441 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
