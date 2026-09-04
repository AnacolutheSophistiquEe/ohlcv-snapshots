# MSTR

**Generated** : 2026-09-04T22:01:00.423253+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $142.80  

> 🟡 **WAIT-FOR-DIP** — spot +1.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $142.80 (+1.2% vs entrée) · entrée $141.16 · stop $134.89 · T1 $153.70 · R/R 2.0  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk 0.063 _(réel 5 s)_ (GBM -0.062) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.44% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 127 % hors [0,100] (R² max 0.70). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 71.2 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $140.16–$142.16 (mid $141.16)
- Spot actuel : $142.80 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $134.89 (stop swing_plan-based (-9.58%))
- Targets : T1 $153.70 · R/R 2.0 | T2 $154.90 · R/R 2.19 | T3 $156.11 · R/R 2.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $134.89


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.37 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.58 %)** : le gap seul le franchit 0.478 % des séances (6 fois sur 1254).
   - exécution **3.733 pt plus bas** dans le cas TYPIQUE (médiane), 17.395 au p90, **17.792 au pire**
   - perte réelle **17.215 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 9.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0365 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.488 % | p01 -7.774 % | pire -27.372 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1893** [0.1364 ; 0.2525] _(largeur 11.6 pt, n_eff 173.1)_
   - swing : **0.4078** [0.3569 ; 0.4602] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3917** [0.3413 ; 0.4439] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (27.4 pt), swing (36.0 pt), deep (35.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.66 %** | CVaR **-10.34 %** | vol 5.49 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.51 % contre 5.10 % aujourd'hui, rapport 1.67)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.67 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3398** (β de hausse 1.8349, asymétrie 1.2751) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 127.6862 sur atr_based (1.5 ATR, 10.584 %) — p(stop avant cible) 0.4301 [0.38 ; 0.48], R/R 1.887, perte reelle 17.215 % (gap inclus), CVaR 10.616 %, EV -2.4673 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 6.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 0.65 ATR (stop 6.428 %) — p(stop avant cible) 0.6245 [0.57 ; 0.67], R/R 3.433, perte reelle 9.463 % (gap inclus), EV -1.3365 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.625, borne haute 0.674 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.34 %) : P(cible) 6.5 % x 32.49 % + P(rien) 31.1 % x 7.93 % ne couvrent pas P(stop) 62.5 % x 9.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.584 %) — p(stop avant cible) 0.4301 [0.38 ; 0.48], R/R 1.887, perte reelle 17.215 % (gap inclus), EV -2.4673 % — **REFUSE**
      - refuse : cible atteinte seulement 6.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.47 %) : P(cible) 6.9 % x 32.49 % + P(rien) 50.1 % x 5.38 % ne couvrent pas P(stop) 43.0 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.62 ATR (stop 20.329 %) — p(stop avant cible) 0.1687 [0.13 ; 0.21], R/R 1.204, perte reelle 26.975 % (gap inclus), EV -1.6555 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 7.1 % x 32.49 % + P(rien) 76.0 % x 0.77 % ne couvrent pas P(stop) 16.9 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.83 ATR (stop 28.893 %) — p(stop avant cible) 0.0613 [0.04 ; 0.09], R/R 1.124, perte reelle 28.893 % (gap inclus), EV -0.6566 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 7.1 % x 32.49 % + P(rien) 86.8 % x -1.37 % ne couvrent pas P(stop) 6.1 % x 28.89 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 5.27 ATR (stop 39.058 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.832, perte reelle 39.058 % (gap inclus), EV -0.3521 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 7.1 % x 32.49 % + P(rien) 92.7 % x -2.79 % ne couvrent pas P(stop) 0.2 % x 39.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.764 %) — p(stop avant cible) 0.9117 [0.88 ; 0.94], R/R 8.797, perte reelle 3.693 % (gap inclus), EV -2.0127 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 8.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.912, borne haute 0.938 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.01 %) : P(cible) 2.2 % x 32.49 % + P(rien) 6.7 % x 9.75 % ne couvrent pas P(stop) 91.2 % x 3.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 8.82 %) — p(stop avant cible) 0.5053 [0.45 ; 0.56], R/R 2.247, perte reelle 14.455 % (gap inclus), EV -2.3014 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.505, borne haute 0.558 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.30 %) : P(cible) 6.8 % x 32.49 % + P(rien) 42.7 % x 6.55 % ne couvrent pas P(stop) 50.5 % x 14.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 12.348 %) — p(stop avant cible) 0.3654 [0.32 ; 0.42], R/R 1.416, perte reelle 22.94 % (gap inclus), EV -3.6587 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.66 %) : P(cible) 7.0 % x 32.49 % + P(rien) 56.5 % x 4.35 % ne couvrent pas P(stop) 36.5 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 14.112 %) — p(stop avant cible) 0.3089 [0.26 ; 0.36], R/R 1.416, perte reelle 22.94 % (gap inclus), EV -2.6973 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.70 %) : P(cible) 7.0 % x 32.49 % + P(rien) 62.1 % x 3.39 % ne couvrent pas P(stop) 30.9 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 15.876 %) — p(stop avant cible) 0.2508 [0.21 ; 0.30], R/R 1.204, perte reelle 26.975 % (gap inclus), EV -2.9987 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.00 %) : P(cible) 7.0 % x 32.49 % + P(rien) 67.9 % x 2.18 % ne couvrent pas P(stop) 25.1 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 24.696 %) — p(stop avant cible) 0.1024 [0.07 ; 0.14], R/R 1.204, perte reelle 26.975 % (gap inclus), EV -0.8499 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 7.1 % x 32.49 % + P(rien) 82.7 % x -0.48 % ne couvrent pas P(stop) 10.2 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 31.752 %) — p(stop avant cible) 0.0314 [0.02 ; 0.05], R/R 1.023, perte reelle 31.752 % (gap inclus), EV -0.5335 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 7.1 % x 32.49 % + P(rien) 89.8 % x -2.05 % ne couvrent pas P(stop) 3.1 % x 31.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 35.28 %) — p(stop avant cible) 0.0146 [0.01 ; 0.03], R/R 0.921, perte reelle 35.28 % (gap inclus), EV -0.4351 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 7.1 % x 32.49 % + P(rien) 91.4 % x -2.44 % ne couvrent pas P(stop) 1.5 % x 35.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 42.336 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.767, perte reelle 42.336 % (gap inclus), EV -0.3327 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 7.1 % x 32.49 % + P(rien) 92.8 % x -2.82 % ne couvrent pas P(stop) 0.1 % x 42.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 45.864 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.708, perte reelle 45.864 % (gap inclus), EV -0.3269 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 7.1 % x 32.49 % + P(rien) 92.9 % x -2.83 % ne couvrent pas P(stop) 0.0 % x 45.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 49.392 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.658, perte reelle 49.392 % (gap inclus), EV -0.3277 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 7.1 % x 32.49 % + P(rien) 92.9 % x -2.83 % ne couvrent pas P(stop) 0.0 % x 49.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 52.92 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.614, perte reelle 52.92 % (gap inclus), EV -0.3288 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 52.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 7.1 % x 32.49 % + P(rien) 92.9 % x -2.83 % ne couvrent pas P(stop) 0.0 % x 52.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 56.448 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.576, perte reelle 56.448 % (gap inclus), EV -0.3291 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 7.1 % x 32.49 % + P(rien) 92.9 % x -2.83 % ne couvrent pas P(stop) 0.0 % x 56.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 142.8, ATR14 10.0759 (7.056 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.395 ATR = 2.787 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.353 % | 142.2962 | 94.27 % | 96.68 % | 97.08 % | 97.68 % | 98.07 % | 98.67 % |
| 0.1 ATR | 0.706 % | 141.7924 | 88.23 % | 92.04 % | 93.45 % | 94.75 % | 96.65 % | 97.33 % |
| 0.15 ATR | 1.058 % | 141.2886 | 81.39 % | 87.11 % | 89.62 % | 91.72 % | 94.11 % | 95.59 % |
| 0.2 ATR | 1.411 % | 140.7848 | 73.74 % | 81.87 % | 84.88 % | 88.08 % | 91.37 % | 93.74 % |
| 0.25 ATR | 1.764 % | 140.281 | 67.91 % | 78.05 % | 82.16 % | 86.16 % | 89.14 % | 92.21 % |
| 0.35 ATR | 2.47 % | 139.2734 | 55.03 % | 68.68 % | 75.2 % | 80.81 % | 85.69 % | 89.54 % |
| 0.5 ATR | 3.528 % | 137.7621 | 38.23 % | 55.29 % | 63.41 % | 71.21 % | 78.48 % | 84.72 % |
| 0.75 ATR | 5.292 % | 135.2431 | 19.32 % | 37.56 % | 46.98 % | 57.88 % | 68.02 % | 77.44 % |
| 1.0 ATR | 7.056 % | 132.7241 | 9.36 % | 25.18 % | 34.68 % | 46.26 % | 58.78 % | 70.15 % |
| 1.25 ATR | 8.82 % | 130.2051 | 4.12 % | 14.5 % | 25.0 % | 35.96 % | 49.75 % | 62.77 % |
| 1.5 ATR | 10.584 % | 127.6862 | 2.11 % | 8.66 % | 17.34 % | 28.99 % | 42.94 % | 57.03 % |
| 2.0 ATR | 14.112 % | 122.6482 | 0.2 % | 3.12 % | 7.36 % | 16.16 % | 31.27 % | 47.18 % |
| 2.5 ATR | 17.64 % | 117.6103 | 0.1 % | 0.91 % | 2.42 % | 8.69 % | 21.42 % | 37.54 % |
| 3.0 ATR | 21.168 % | 112.5723 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.52 % | 28.0 % |
| 4.0 ATR | 28.224 % | 102.4964 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.19 % | 18.05 % |
| 6.0 ATR | 42.336 % | 82.3446 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.40 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.12 ATR | 1.44 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.25 ATR | 1.41 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.92 ATR | 1.03 ATR | 1.36 ATR | 1.66 ATR | 1.85 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.58 ATR | 1.24 ATR | 1.42 ATR | 1.93 ATR | 2.32 ATR | 2.60 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.83 ATR | 1.86 ATR | 2.11 ATR | 2.74 ATR | 3.30 ATR | 3.80 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.44–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.528 %, prix 137.762), p(touche) 38.23 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.292 %, prix 135.243), p(touche) 37.56 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.79–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.056 %, prix 132.724), p(touche) 34.68 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.031–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.82 %, prix 130.205), p(touche) 35.96 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.424–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.584 %, prix 127.6861), p(touche) 42.94 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.113–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.64 %, prix 117.6101), p(touche) 37.54 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.062 | EV/share : $-0.391 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 16 % | T3 16 %
- Kelly (position) : f* 0.061 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.7 | bear 26.0 | side 57.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 571.0 (= 4 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.15% → cible +8.882% / stop −4.441%, p_fill 76%, n_eff≈30.5) : P(cible|rempli) **7%** · **EV/risk +0.063** (×p_fill ; si rempli +0.37% du capital)
  - **swing** (entrée dip −2.524% → cible +7.89% / stop −7.239%, p_fill 63%, n_eff≈27.1) : P(cible|rempli) **47%** · **EV/risk +0.190** (×p_fill ; si rempli +2.17% du capital)
  - **deep** (entrée dip −3.896% → cible +11.158% / stop −11.013%, p_fill 52%, n_eff≈26.1) : P(cible|rempli) **61%** · **EV/risk +0.188** (×p_fill ; si rempli +4.00% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→57% · +3.0%→42% · +5.0%→16% · +8.0%→10%
- Range intraday médian 5.55% (p90 10.3%) · excursion haute méd. +2.46% / basse méd. −2.4%
- Profil de vol intra : ouverture 3.464% vs midi 1.203% vs clôture 1.358% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.0)_ ; drift intra méd. 0.611% ; recovery-V 31%
- **σ réalisé intraday** 3.71% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 81% / bas 60% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 126.2064 (VA 123.6984–127.6171 ; dernier close 124.91)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 74% · **stop −4.23%** sous le fill (sous le bruit) · cible +1.76% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 52% (gap-down >1% 41% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.05%) · haut méd +0.75% · range méd 1.81%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −2.99%) · haut méd +1.2% · range méd 2.49%
- Excursion ouverture 30min (n=160) : bas méd −1.29% (p90 −3.25%) · haut méd +1.39% · range méd 3.15%
- Excursion ouverture 60min (n=160) : bas méd −1.71% (p90 −3.6%) · haut méd +1.78% · range méd 3.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 124.88 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 74% (122/159) · gap 45% · délai 0.0min · rebond 49% (60/122) (MFE +0.93%)
   - −1.0% : fill 30min 60% · séance 70% (117/159) · gap 41% · délai 0.0min · rebond 53% (65/117) (MFE +1.02%)
   - −1.5% : fill 30min 53% · séance 64% (109/159) · gap 34% · délai 0.0min · rebond 56% (64/109) (MFE +1.4%)
   - −2.0% : fill 30min 47% · séance 57% (99/159) · gap 28% · délai 0.0min · rebond 58% (60/99) (MFE +1.16%)
   - −3.0% : fill 30min 32% · séance 48% (79/159) · gap 14% · délai 1.2min · rebond 56% (47/79) (MFE +1.6%)
   - −4.0% : fill 30min 20% · séance 38% (65/159) · gap 4% · délai 27.6min · rebond 70% (44/65) (MFE +1.79%)
   - −5.0% : fill 30min 14% · séance 27% (47/159) · gap 3% · délai 31.0min · rebond 74% (34/47) (MFE +1.76%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.49%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.01% (p90 −2.48%) → stop au-delà de −2.1% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.07% (p90 −2.46%) → stop au-delà de −2.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=962 jambes) : jambe baissière méd −1.13% (p90 −2.72%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 100% (78/78) · rebond 45% (37/78)
      · −2.0% : fill 93% (72/78) · rebond 56% (41/72)
      · −3.0% : fill 83% (64/78) · rebond 58% (38/64)
      · −4.0% : fill 68% (54/78) · rebond 71% (37/54)
      · −5.0% : fill 50% (41/78) · rebond 76% (31/41)
   - **flat** (19 séances) :
      · −1.0% : fill 71% (15/19) · rebond 79% (12/15)
      · −2.0% : fill 46% (10/19) · rebond 60% (7/10)
      · −3.0% : fill 28% (5/19) · rebond 35% (2/5)
      · −4.0% : fill 11% (3/19) · rebond 51% (2/3)
      · −5.0% : fill 9% (2/19) · rebond 0% (0/2)
   - **gap-up** (62 séances) :
      · −1.0% : fill 31% (24/62) · rebond 63% (16/24)
      · −2.0% : fill 16% (17/62) · rebond 66% (12/17)
      · −3.0% : fill 11% (10/62) · rebond 57% (7/10)
      · −4.0% : fill 10% (8/62) · rebond 68% (5/8)
      · −5.0% : fill 5% (4/62) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 54% si les 15 1res min sont vertes (82 cas) · 38% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:33** → P(séance verte=clôture>ouverture) 79% si début vert vs 15% si rouge (base 46% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **79%** · continue >prix actuel 43% ; creux résiduel méd -1.49% (q20 -3.22%) → **SL/trailing à −3.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.55% → **scale +1.59% / runner +2.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **15%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.76%** (au-delà de la MAE q10 -4.76%), cible rebond +1.62% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.3% .. +3.71%] · haut q95 +3.94% · bas q05 -3.65%
   - 60min (n=160) : retour [-4.43% .. +5.41%] · haut q95 +5.67% · bas q05 -4.97%
   - 2h (n=160) : retour [-4.31% .. +6.52%] · haut q95 +7.99% · bas q05 -5.05%
   - 4h (n=160) : retour [-5.56% .. +8.45%] · haut q95 +10.1% · bas q05 -6.74%
   - 6h (n=160) : retour [-5.77% .. +7.44%] · haut q95 +10.17% · bas q05 -7.15%
   - session (n=160) : retour [-5.05% .. +6.6%] · haut q95 +10.17% · bas q05 -7.27%


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
- **DÉSARMER** : repli > **−3.53%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 221.98 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.97% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.51%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 71.2  _(surachat)_
- **ADX** : 37.5  _(tendance etablie)_
- **MACD** : hist 2.711  _(pas de croisement recent)_
- **BB** : %B 0.89 · largeur 60.9%
- **ATR** : 10.08 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.212  _(accumulation)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 37.5  _(marche directionnel)_
- **MA** : MA20 115.52 · MA50 103.5 · MA200 139.09  _(prix > MA20)_
- **Dist MA** : MA20 +23.6% · MA50 +38.0% · MA200 +2.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (769490 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
