# MSTR

**Generated** : 2026-09-01T00:23:35.034922+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $132.94  

> 🟡 **WAIT-FOR-DIP** — spot +6.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $132.94 (+6.9% vs entrée) · entrée $124.39 · stop $115.99 · T1 $132.30 · R/R 0.94  
> ↳ P(T1 av. stop) 43 % _(réel 5 s)_ · EV/risk 0.003 _(réel 5 s)_ (GBM -0.043) · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 123 % hors [0,100] (R² max 0.70). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 71.6 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $122.81–$125.97 (mid $124.39)
- Spot actuel : $132.94 (+6.9% au-dessus de la zone — repli à attendre)
- Stop : $115.99 (stop swing_plan-based (-12.75%))
- Targets : T1 $132.30 · R/R 0.94 | T2 $140.20 · R/R 1.88 | T3 $148.11 · R/R 2.82
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $115.99


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.21 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.75 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **13.828 pt plus bas** dans le cas TYPIQUE (médiane), 14.463 au p90, **14.622 au pire**
   - perte réelle **22.94 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 12.75 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0244 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.43 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2377** [0.179 ; 0.3051] _(largeur 12.6 pt, n_eff 173.1)_
   - swing : **0.4156** [0.3645 ; 0.4681] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4018** [0.3511 ; 0.4541] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.1 pt), swing (45.6 pt), deep (48.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.77 %** | CVaR **-10.4 %** | vol 5.47 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.43 % contre 4.84 % aujourd'hui, rapport 1.74)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.77 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3368** (β de hausse 1.8541, asymétrie 1.2604) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 120.3422 sur atr_based (1.5 ATR, 9.476 %) — p(stop avant cible) 0.4792 [0.43 ; 0.53], R/R 0.797, perte reelle 17.215 % (gap inclus), CVaR 9.513 %, EV -4.1463 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 19 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 61.4 % de la queue et il ne reste que 29.65 EUR a partager. Prix du risque 0.019 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.476 %) — p(stop avant cible) 0.4792 [0.43 ; 0.53], R/R 0.797, perte reelle 17.215 % (gap inclus), EV -4.1463 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.15 %) : P(cible) 27.5 % x 13.72 % + P(rien) 24.6 % x 1.33 % ne couvrent pas P(stop) 47.9 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.97 ATR (stop 15.304 %) — p(stop avant cible) 0.2666 [0.22 ; 0.32], R/R 0.509, perte reelle 26.975 % (gap inclus), EV -3.9984 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.00 %) : P(cible) 29.1 % x 13.72 % + P(rien) 44.2 % x -1.81 % ne couvrent pas P(stop) 26.7 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.43 ATR (stop 24.503 %) — p(stop avant cible) 0.0953 [0.07 ; 0.13], R/R 0.509, perte reelle 26.975 % (gap inclus), EV -1.5164 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.52 %) : P(cible) 29.3 % x 13.72 % + P(rien) 61.2 % x -4.84 % ne couvrent pas P(stop) 9.5 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.21 ATR (stop 35.756 %) — p(stop avant cible) 0.0149 [0.01 ; 0.03], R/R 0.384, perte reelle 35.756 % (gap inclus), EV -1.0872 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 29.3 % x 13.72 % + P(rien) 69.2 % x -6.62 % ne couvrent pas P(stop) 1.5 % x 35.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.579 %) — p(stop avant cible) 0.9273 [0.90 ; 0.95], R/R 3.932, perte reelle 3.49 % (gap inclus), EV -2.2844 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.927, borne haute 0.951 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.28 %) : P(cible) 6.8 % x 13.72 % + P(rien) 0.5 % x 4.85 % ne couvrent pas P(stop) 92.7 % x 3.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.159 %) — p(stop avant cible) 0.8159 [0.77 ; 0.85], R/R 2.44, perte reelle 5.624 % (gap inclus), EV -2.3537 % — **REFUSE**
      - refuse : p_stop_first 0.816, borne haute 0.854 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.35 %) : P(cible) 15.6 % x 13.72 % + P(rien) 2.9 % x 3.54 % ne couvrent pas P(stop) 81.6 % x 5.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.738 %) — p(stop avant cible) 0.7096 [0.66 ; 0.76], R/R 1.806, perte reelle 7.596 % (gap inclus), EV -2.2014 % — **REFUSE**
      - refuse : p_stop_first 0.710, borne haute 0.756 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 20.5 % x 13.72 % + P(rien) 8.5 % x 4.37 % ne couvrent pas P(stop) 71.0 % x 7.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.318 %) — p(stop avant cible) 0.6283 [0.58 ; 0.68], R/R 1.466, perte reelle 9.362 % (gap inclus), EV -2.1962 % — **REFUSE**
      - refuse : p_stop_first 0.628, borne haute 0.678 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 23.7 % x 13.72 % + P(rien) 13.4 % x 3.19 % ne couvrent pas P(stop) 62.8 % x 9.36 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.897 %) — p(stop avant cible) 0.5334 [0.48 ; 0.59], R/R 1.067, perte reelle 12.861 % (gap inclus), EV -2.8219 % — **REFUSE**
      - refuse : p_stop_first 0.533, borne haute 0.586 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.82 %) : P(cible) 27.0 % x 13.72 % + P(rien) 19.6 % x 1.67 % ne couvrent pas P(stop) 53.3 % x 12.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.97 ATR (stop 14.337 %) — p(stop avant cible) 0.2968 [0.25 ; 0.35], R/R 0.598, perte reelle 22.94 % (gap inclus), EV -3.3351 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.34 %) : P(cible) 29.0 % x 13.72 % + P(rien) 41.3 % x -1.23 % ne couvrent pas P(stop) 29.7 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 17.373 %) — p(stop avant cible) 0.2002 [0.16 ; 0.24], R/R 0.509, perte reelle 26.975 % (gap inclus), EV -2.9591 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.96 %) : P(cible) 29.2 % x 13.72 % + P(rien) 50.8 % x -3.09 % ne couvrent pas P(stop) 20.0 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 18.953 %) — p(stop avant cible) 0.1756 [0.14 ; 0.22], R/R 0.509, perte reelle 26.975 % (gap inclus), EV -2.6156 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.62 %) : P(cible) 29.2 % x 13.72 % + P(rien) 53.2 % x -3.55 % ne couvrent pas P(stop) 17.6 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.43 ATR (stop 23.537 %) — p(stop avant cible) 0.1116 [0.08 ; 0.15], R/R 0.509, perte reelle 26.975 % (gap inclus), EV -1.6617 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 29.3 % x 13.72 % + P(rien) 59.6 % x -4.48 % ne couvrent pas P(stop) 11.2 % x 26.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 28.429 %) — p(stop avant cible) 0.0592 [0.04 ; 0.09], R/R 0.483, perte reelle 28.429 % (gap inclus), EV -1.2944 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.29 %) : P(cible) 29.3 % x 13.72 % + P(rien) 64.8 % x -5.61 % ne couvrent pas P(stop) 5.9 % x 28.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 5.21 ATR (stop 34.79 %) — p(stop avant cible) 0.02 [0.01 ; 0.04], R/R 0.394, perte reelle 34.79 % (gap inclus), EV -1.1295 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 29.3 % x 13.72 % + P(rien) 68.7 % x -6.49 % ne couvrent pas P(stop) 2.0 % x 34.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 37.905 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 0.362, perte reelle 37.905 % (gap inclus), EV -1.0244 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 29.3 % x 13.72 % + P(rien) 70.0 % x -6.86 % ne couvrent pas P(stop) 0.6 % x 37.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 41.064 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.334, perte reelle 41.064 % (gap inclus), EV -0.9852 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.99 %) : P(cible) 29.3 % x 13.72 % + P(rien) 70.6 % x -7.03 % ne couvrent pas P(stop) 0.1 % x 41.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 44.223 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.31, perte reelle 44.223 % (gap inclus), EV -0.9727 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 29.3 % x 13.72 % + P(rien) 70.7 % x -7.06 % ne couvrent pas P(stop) 0.0 % x 44.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 47.381 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.29, perte reelle 47.381 % (gap inclus), EV -0.9702 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 29.3 % x 13.72 % + P(rien) 70.7 % x -7.06 % ne couvrent pas P(stop) 0.0 % x 47.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 50.54 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.271, perte reelle 50.54 % (gap inclus), EV -0.971 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 29.3 % x 13.72 % + P(rien) 70.7 % x -7.06 % ne couvrent pas P(stop) 0.0 % x 50.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 132.94, ATR14 8.3985 (6.318 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.396 ATR = 2.502 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.316 % | 132.5201 | 94.36 % | 96.67 % | 97.07 % | 97.67 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.632 % | 132.1002 | 88.32 % | 92.04 % | 93.44 % | 94.84 % | 96.75 % | 97.33 % |
| 0.15 ATR | 0.948 % | 131.6802 | 81.47 % | 87.1 % | 89.61 % | 91.81 % | 94.21 % | 95.59 % |
| 0.2 ATR | 1.264 % | 131.2603 | 73.82 % | 81.85 % | 84.86 % | 88.17 % | 91.46 % | 93.74 % |
| 0.25 ATR | 1.579 % | 130.8404 | 68.08 % | 78.12 % | 82.14 % | 86.25 % | 89.23 % | 92.2 % |
| 0.35 ATR | 2.211 % | 130.0005 | 55.19 % | 68.75 % | 75.28 % | 80.99 % | 85.77 % | 89.53 % |
| 0.5 ATR | 3.159 % | 128.7407 | 38.17 % | 55.34 % | 63.47 % | 71.39 % | 78.56 % | 84.8 % |
| 0.75 ATR | 4.738 % | 126.6411 | 19.34 % | 37.6 % | 47.02 % | 58.14 % | 68.29 % | 77.52 % |
| 1.0 ATR | 6.318 % | 124.5415 | 9.37 % | 25.1 % | 34.81 % | 46.51 % | 59.15 % | 70.33 % |
| 1.25 ATR | 7.897 % | 122.4418 | 4.13 % | 14.52 % | 25.13 % | 36.2 % | 50.1 % | 63.04 % |
| 1.5 ATR | 9.476 % | 120.3422 | 2.11 % | 8.67 % | 17.36 % | 29.02 % | 43.19 % | 57.19 % |
| 2.0 ATR | 12.635 % | 116.143 | 0.2 % | 3.12 % | 7.37 % | 16.18 % | 31.4 % | 47.33 % |
| 2.5 ATR | 15.794 % | 111.9437 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.44 % | 37.58 % |
| 3.0 ATR | 18.953 % | 107.7444 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 28.03 % |
| 4.0 ATR | 25.27 % | 99.3459 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 18.07 % |
| 6.0 ATR | 37.905 % | 82.5489 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.40 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.12 ATR | 1.44 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.70 ATR | 0.79 ATR | 1.05 ATR | 1.25 ATR | 1.42 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.04 ATR | 1.36 ATR | 1.66 ATR | 1.85 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.44 ATR | 1.93 ATR | 2.32 ATR | 2.60 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.84 ATR | 1.86 ATR | 2.12 ATR | 2.74 ATR | 3.30 ATR | 3.81 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.44–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.159 %, prix 128.7404), p(touche) 38.17 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.738 %, prix 126.6413), p(touche) 37.6 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.791–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.318 %, prix 124.5409), p(touche) 34.81 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.037–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.897 %, prix 122.4417), p(touche) 36.2 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.435–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.476 %, prix 120.3426), p(touche) 43.19 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.119–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.794 %, prix 111.9435), p(touche) 37.58 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.043 | EV/share : $-0.357 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 18 % | T3 9 %
- Kelly (position) : f* 0.008 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 53.8 | bear 22.5 | side 23.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 399.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.927% → cible +5.575% / stop −4.0%, p_fill 39%, n_eff≈16.1) : P(cible|rempli) **5%** · **EV/risk +0.018** (×p_fill ; si rempli +0.18% du capital)
  - **swing** (entrée dip −6.433% → cible +6.354% / stop −6.752%, p_fill 13%, n_eff≈15.7) : P(cible|rempli) **43%** · **EV/risk +0.003** (×p_fill ; si rempli +0.13% du capital)
  - **deep** (entrée dip −9.933% → cible +8.986% / stop −10.522%, p_fill 14%, n_eff≈13.7) : P(cible|rempli) **46%** · **EV/risk -0.028** (×p_fill ; si rempli -2.15% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→75% · +2.0%→57% · +3.0%→42% · +5.0%→16% · +8.0%→10%
- Range intraday médian 5.59% (p90 10.3%) · excursion haute méd. +2.46% / basse méd. −2.51%
- Profil de vol intra : ouverture 3.466% vs midi 1.231% vs clôture 1.352% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr 0.004)_ ; drift intra méd. 0.628% ; recovery-V 28%
- **σ réalisé intraday** 3.752% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 79% / bas 56% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 127.1821 (VA 126.4689–131.6994 ; dernier close 127.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 72% · **stop −4.48%** sous le fill (sous le bruit) · cible +1.51% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 52% (gap-down >1% 41% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −0.89% (p90 −2.06%) · haut méd +0.78% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.83%) · haut méd +1.22% · range méd 2.49%
- Excursion ouverture 30min (n=160) : bas méd −1.28% (p90 −3.27%) · haut méd +1.44% · range méd 3.15%
- Excursion ouverture 60min (n=160) : bas méd −1.61% (p90 −3.62%) · haut méd +1.84% · range méd 3.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 127.31 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 73% (122/159) · gap 45% · délai 0.0min · rebond 49% (60/122) (MFE +0.94%)
   - −1.0% : fill 30min 58% · séance 69% (117/159) · gap 41% · délai 0.0min · rebond 53% (65/117) (MFE +1.02%)
   - −1.5% : fill 30min 53% · séance 65% (110/159) · gap 34% · délai 0.0min · rebond 58% (65/110) (MFE +1.49%)
   - −2.0% : fill 30min 47% · séance 57% (100/159) · gap 28% · délai 0.0min · rebond 60% (61/100) (MFE +1.31%)
   - −3.0% : fill 30min 31% · séance 48% (79/159) · gap 12% · délai 1.9min · rebond 58% (47/79) (MFE +1.67%)
   - −4.0% : fill 30min 19% · séance 38% (65/159) · gap 4% · délai 29.0min · rebond 68% (43/65) (MFE +1.75%)
   - −5.0% : fill 30min 13% · séance 26% (47/159) · gap 3% · délai 39.2min · rebond 72% (33/47) (MFE +1.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.8% (p90 −2.28%) → stop au-delà de −1.82% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −2.49%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.01% (p90 −2.48%) → stop au-delà de −1.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=970 jambes) : jambe baissière méd −1.13% (p90 −2.72%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 100% (78/78) · rebond 47% (37/78)
      · −2.0% : fill 93% (72/78) · rebond 59% (41/72)
      · −3.0% : fill 83% (64/78) · rebond 61% (38/64)
      · −4.0% : fill 67% (54/78) · rebond 69% (36/54)
      · −5.0% : fill 48% (41/78) · rebond 73% (30/41)
   - **flat** (19 séances) :
      · −1.0% : fill 71% (15/19) · rebond 79% (12/15)
      · −2.0% : fill 46% (10/19) · rebond 60% (7/10)
      · −3.0% : fill 28% (5/19) · rebond 35% (2/5)
      · −4.0% : fill 11% (3/19) · rebond 51% (2/3)
      · −5.0% : fill 9% (2/19) · rebond 0% (0/2)
   - **gap-up** (62 séances) :
      · −1.0% : fill 28% (24/62) · rebond 57% (16/24)
      · −2.0% : fill 17% (18/62) · rebond 67% (13/18)
      · −3.0% : fill 12% (10/62) · rebond 57% (7/10)
      · −4.0% : fill 10% (8/62) · rebond 68% (5/8)
      · −5.0% : fill 5% (4/62) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 54% si les 15 1res min sont vertes (82 cas) · 37% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:33** → P(séance verte=clôture>ouverture) 79% si début vert vs 13% si rouge (base 46% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **79%** · continue >prix actuel 43% ; creux résiduel méd -1.49% (q20 -3.22%) → **SL/trailing à −3.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.55% → **scale +1.59% / runner +2.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **13%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.84%** (au-delà de la MAE q10 -4.84%), cible rebond +1.62% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.31% .. +3.73%] · haut q95 +3.94% · bas q05 -3.66%
   - 60min (n=160) : retour [-4.53% .. +5.45%] · haut q95 +5.68% · bas q05 -4.99%
   - 2h (n=160) : retour [-4.33% .. +6.69%] · haut q95 +8.34% · bas q05 -5.05%
   - 4h (n=160) : retour [-5.63% .. +8.54%] · haut q95 +10.12% · bas q05 -6.79%
   - 6h (n=160) : retour [-5.9% .. +7.69%] · haut q95 +10.19% · bas q05 -7.21%
   - session (n=160) : retour [-5.09% .. +6.89%] · haut q95 +10.19% · bas q05 -7.41%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 15% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 2.61% / p90 3.53%) · ~3.99 replis/séance, durée méd 49.8 min. P(nouveau plus-haut après repli) :
   - −0.5% → **75%** (reprise méd 15.0 min, n=31)
   - −1.0% → **54%** (reprise méd 21.99 min, n=18)
   - −1.5% → **46%** (reprise méd 37.49 min, n=15)
   - −2.0% → **20%** (reprise méd 89.44 min, n=9)
   - −3.0% → **41%** (reprise méd 89.44 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.53%** (p90, défaut prudent ; serré/agressif −2.61%) ; extension open→close méd +8.34% (q75 +9.19% / q95 +15.39%), MFE méd +10.26% / q90 +14.97%
   - Échelle scale-out : +10.26% (33%) / +12.41% (33%) / +14.97% (34%)
- **DÉSARMER** : repli > **−3.53%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 221.98 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.97% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.51%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 71.6  _(surachat)_
- **ADX** : 30.6  _(tendance etablie)_
- **MACD** : hist 3.622  _(pas de croisement recent)_
- **BB** : %B 0.91 · largeur 55.7%
- **ATR** : 8.4 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.157  _(accumulation)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 33.9  _(marche directionnel)_
- **MA** : MA20 108.38 · MA50 100.64 · MA200 140.55  _(prix > MA20)_
- **Dist MA** : MA20 +22.7% · MA50 +32.1% · MA200 -5.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (792272 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
