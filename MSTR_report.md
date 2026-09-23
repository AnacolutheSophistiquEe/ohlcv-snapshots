# MSTR

**Generated** : 2026-09-23T00:31:56.259501+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $167.31  

> 🟡 **WAIT-FOR-DIP** — spot +5.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $167.31 (+5.2% vs entrée) · entrée $159.06 · stop $149.14 · T1 $172.53 · R/R 1.36  
> ↳ P(T1 av. stop) 53 % _(réel 5 s)_ · EV/risk 0.118 _(réel 5 s)_ (GBM 0.014) · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -16.3 % ≠ (strike 141.0 − spot 167.31)/spot = -15.7 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 515 % hors [0,100] (R² max 0.80). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 70.8 > 70 (surachat) ; %B 1.08 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $156.36–$161.75 (mid $159.06)
- Spot actuel : $167.31 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : $149.14 (stop swing_plan-based (-10.86%))
- Targets : T1 $172.53 · R/R 1.36 | T2 $185.99 · R/R 2.71 | T3 $199.46 · R/R 4.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $149.14


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.54 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.86 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **2.453 pt plus bas** dans le cas TYPIQUE (médiane), 16.115 au p90, **16.512 au pire**
   - perte réelle **17.215 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 10.86 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0304 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.43 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2808** [0.2179 ; 0.351] _(largeur 13.3 pt, n_eff 173.1)_
   - swing : **0.4486** [0.3968 ; 0.5013] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4384** [0.3868 ; 0.491] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (38.4 pt), swing (49.1 pt), deep (41.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.01 %** | CVaR **-9.02 %** | vol 4.9 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.05 % contre 5.37 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.67 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3615** (β de hausse 1.8181, asymétrie 1.2989) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 154.9162 sur atr_grid (1.25 ATR, 7.408 %) — p(stop avant cible) 0.5557 [0.50 ; 0.61], R/R 1.661, perte reelle 11.572 % (gap inclus), CVaR 7.461 %, EV -2.2008 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1044 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.556, borne haute 0.607 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **7.77 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.313 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 45.0 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.889 %) — p(stop avant cible) 0.4851 [0.43 ; 0.54], R/R 1.268, perte reelle 15.156 % (gap inclus), EV -2.9115 % — **REFUSE**
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.93 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.91 %) : P(cible) 17.8 % x 19.22 % + P(rien) 33.7 % x 3.03 % ne couvrent pas P(stop) 48.5 % x 15.16 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.61 ATR (stop 12.796 %) — p(stop avant cible) 0.3306 [0.28 ; 0.38], R/R 0.838, perte reelle 22.94 % (gap inclus), EV -3.3363 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.82 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.34 %) : P(cible) 18.9 % x 19.22 % + P(rien) 48.0 % x 1.29 % ne couvrent pas P(stop) 33.1 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.26 ATR (stop 16.618 %) — p(stop avant cible) 0.2172 [0.18 ; 0.26], R/R 0.712, perte reelle 26.975 % (gap inclus), EV -2.5499 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.63 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.55 %) : P(cible) 19.2 % x 19.22 % + P(rien) 59.1 % x -0.65 % ne couvrent pas P(stop) 21.7 % x 26.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.13 ATR (stop 21.8 %) — p(stop avant cible) 0.137 [0.10 ; 0.18], R/R 0.712, perte reelle 26.975 % (gap inclus), EV -1.2802 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.81 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 19.3 % x 19.22 % + P(rien) 67.0 % x -1.92 % ne couvrent pas P(stop) 13.7 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 4.64 ATR (stop 30.707 %) — p(stop avant cible) 0.0355 [0.02 ; 0.06], R/R 0.626, perte reelle 30.707 % (gap inclus), EV -0.5331 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.71 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 19.3 % x 19.22 % + P(rien) 77.2 % x -4.08 % ne couvrent pas P(stop) 3.5 % x 30.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.13 ATR (stop 33.664 %) — p(stop avant cible) 0.0208 [0.01 ; 0.04], R/R 0.571, perte reelle 33.664 % (gap inclus), EV -0.5278 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.66 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 19.3 % x 19.22 % + P(rien) 78.6 % x -4.49 % ne couvrent pas P(stop) 2.1 % x 33.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.482 %) — p(stop avant cible) 0.9348 [0.91 ; 0.96], R/R 5.669, perte reelle 3.39 % (gap inclus), EV -2.2334 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.935, borne haute 0.957 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.23 %) : P(cible) 4.0 % x 19.22 % + P(rien) 2.5 % x 6.52 % ne couvrent pas P(stop) 93.5 % x 3.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.963 %) — p(stop avant cible) 0.8374 [0.80 ; 0.87], R/R 3.701, perte reelle 5.192 % (gap inclus), EV -2.2626 % — **REFUSE**
      - refuse : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.837, borne haute 0.873 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.26 %) : P(cible) 8.5 % x 19.22 % + P(rien) 7.8 % x 5.88 % ne couvrent pas P(stop) 83.7 % x 5.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.445 %) — p(stop avant cible) 0.7192 [0.67 ; 0.76], R/R 2.688, perte reelle 7.149 % (gap inclus), EV -1.6637 % — **REFUSE**
      - refuse : cible atteinte seulement 14.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.719, borne haute 0.765 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 14.3 % x 19.22 % + P(rien) 13.8 % x 5.32 % ne couvrent pas P(stop) 71.9 % x 7.15 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.926 %) — p(stop avant cible) 0.6266 [0.57 ; 0.68], R/R 2.123, perte reelle 9.05 % (gap inclus), EV -1.5677 % — **REFUSE**
      - refuse : p_stop_first 0.627, borne haute 0.676 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 16.2 % x 19.22 % + P(rien) 21.2 % x 4.70 % ne couvrent pas P(stop) 62.7 % x 9.05 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.408 %) — p(stop avant cible) 0.5557 [0.50 ; 0.61], R/R 1.661, perte reelle 11.572 % (gap inclus), EV -2.2008 % — **REFUSE**
      - refuse : p_stop_first 0.556, borne haute 0.607 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 17.0 % x 19.22 % + P(rien) 27.4 % x 3.49 % ne couvrent pas P(stop) 55.6 % x 11.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.61 ATR (stop 11.338 %) — p(stop avant cible) 0.3713 [0.32 ; 0.42], R/R 1.045, perte reelle 18.395 % (gap inclus), EV -2.3207 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.37 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.32 %) : P(cible) 18.8 % x 19.22 % + P(rien) 44.0 % x 2.02 % ne couvrent pas P(stop) 37.1 % x 18.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.26 ATR (stop 15.16 %) — p(stop avant cible) 0.2596 [0.22 ; 0.31], R/R 0.712, perte reelle 26.975 % (gap inclus), EV -3.2334 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.18 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.23 %) : P(cible) 19.1 % x 19.22 % + P(rien) 55.0 % x 0.18 % ne couvrent pas P(stop) 26.0 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.13 ATR (stop 20.342 %) — p(stop avant cible) 0.1581 [0.12 ; 0.20], R/R 0.712, perte reelle 26.975 % (gap inclus), EV -1.5976 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.35 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 19.3 % x 19.22 % + P(rien) 64.9 % x -1.59 % ne couvrent pas P(stop) 15.8 % x 26.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 23.704 %) — p(stop avant cible) 0.1109 [0.08 ; 0.15], R/R 0.712, perte reelle 26.975 % (gap inclus), EV -0.9776 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.71 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 19.3 % x 19.22 % + P(rien) 69.6 % x -2.43 % ne couvrent pas P(stop) 11.1 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 4.64 ATR (stop 29.25 %) — p(stop avant cible) 0.0514 [0.03 ; 0.08], R/R 0.657, perte reelle 29.25 % (gap inclus), EV -0.6473 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.25 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 19.3 % x 19.22 % + P(rien) 75.6 % x -3.77 % ne couvrent pas P(stop) 5.1 % x 29.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 5.13 ATR (stop 32.206 %) — p(stop avant cible) 0.0294 [0.02 ; 0.05], R/R 0.597, perte reelle 32.206 % (gap inclus), EV -0.5631 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.21 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 19.3 % x 19.22 % + P(rien) 77.8 % x -4.27 % ne couvrent pas P(stop) 2.9 % x 32.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 35.557 %) — p(stop avant cible) 0.0137 [0.01 ; 0.03], R/R 0.54, perte reelle 35.557 % (gap inclus), EV -0.4623 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.56 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 19.3 % x 19.22 % + P(rien) 79.3 % x -4.64 % ne couvrent pas P(stop) 1.4 % x 35.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 38.52 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 0.499, perte reelle 38.52 % (gap inclus), EV -0.4113 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.52 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 19.3 % x 19.22 % + P(rien) 80.1 % x -4.86 % ne couvrent pas P(stop) 0.6 % x 38.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 41.483 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.463, perte reelle 41.483 % (gap inclus), EV -0.3713 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.48 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 19.3 % x 19.22 % + P(rien) 80.6 % x -5.00 % ne couvrent pas P(stop) 0.1 % x 41.48 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 44.446 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.432, perte reelle 44.446 % (gap inclus), EV -0.3567 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.45 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 19.3 % x 19.22 % + P(rien) 80.7 % x -5.03 % ne couvrent pas P(stop) 0.0 % x 44.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 47.409 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.405, perte reelle 47.409 % (gap inclus), EV -0.3578 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.41 % > budget 7.77 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 19.3 % x 19.22 % + P(rien) 80.7 % x -5.03 % ne couvrent pas P(stop) 0.0 % x 47.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 167.31, ATR14 9.915 (5.926 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.395 ATR = 2.341 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.296 % | 166.8142 | 94.06 % | 96.57 % | 97.07 % | 97.78 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.593 % | 166.3185 | 88.22 % | 92.04 % | 93.54 % | 94.94 % | 96.65 % | 97.33 % |
| 0.15 ATR | 0.889 % | 165.8227 | 81.37 % | 87.2 % | 89.91 % | 92.01 % | 94.21 % | 95.59 % |
| 0.2 ATR | 1.185 % | 165.327 | 73.72 % | 81.75 % | 85.07 % | 88.37 % | 91.46 % | 93.63 % |
| 0.25 ATR | 1.482 % | 164.8312 | 67.77 % | 77.92 % | 82.24 % | 86.35 % | 89.13 % | 92.09 % |
| 0.35 ATR | 2.074 % | 163.8397 | 55.09 % | 68.85 % | 75.48 % | 81.09 % | 85.67 % | 89.53 % |
| 0.5 ATR | 2.963 % | 162.3525 | 38.27 % | 55.34 % | 63.57 % | 71.49 % | 78.35 % | 84.7 % |
| 0.75 ATR | 4.445 % | 159.8737 | 19.44 % | 37.7 % | 47.23 % | 58.24 % | 67.99 % | 77.1 % |
| 1.0 ATR | 5.926 % | 157.395 | 9.37 % | 25.3 % | 34.91 % | 46.51 % | 58.94 % | 70.23 % |
| 1.25 ATR | 7.408 % | 154.9162 | 4.13 % | 14.62 % | 25.13 % | 36.0 % | 50.0 % | 62.83 % |
| 1.5 ATR | 8.889 % | 152.4375 | 2.11 % | 8.77 % | 17.46 % | 29.12 % | 42.99 % | 56.98 % |
| 2.0 ATR | 11.852 % | 147.48 | 0.2 % | 3.12 % | 7.37 % | 16.18 % | 31.2 % | 47.13 % |
| 2.5 ATR | 14.815 % | 142.5225 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.44 % | 37.58 % |
| 3.0 ATR | 17.778 % | 137.565 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 28.03 % |
| 4.0 ATR | 23.704 % | 127.65 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 18.07 % |
| 6.0 ATR | 35.557 % | 107.82 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.40 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.58 ATR | 0.65 ATR | 0.84 ATR | 1.01 ATR | 1.12 ATR | 1.45 ATR | 1.83 ATR |
| **3 s.** | 0.36 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.25 ATR | 1.42 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.45 ATR | 0.93 ATR | 1.04 ATR | 1.36 ATR | 1.66 ATR | 1.85 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.58 ATR | 1.25 ATR | 1.43 ATR | 1.92 ATR | 2.32 ATR | 2.60 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.83 ATR | 1.85 ATR | 2.11 ATR | 2.74 ATR | 3.30 ATR | 3.81 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.44–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.963 %, prix 162.3526), p(touche) 38.27 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.647–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.445 %, prix 159.8731), p(touche) 37.7 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.795–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.926 %, prix 157.3952), p(touche) 34.91 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.036–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.408 %, prix 154.9157), p(touche) 36.0 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.428–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.889 %, prix 152.4378), p(touche) 42.99 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.112–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (14.815 %, prix 142.523), p(touche) 37.58 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.014 | EV/share : $0.138 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 13 % | T3 5 %
- Kelly (position) : f* 0.006 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 32.2 | bear 23.0 | side 44.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 502.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.238% → cible +3.787% / stop −3.5%, p_fill 43%, n_eff≈21.7) : P(cible|rempli) **18%** · **EV/risk -0.015** (×p_fill ; si rempli -0.12% du capital)
  - **swing** (entrée dip −4.934% → cible +8.467% / stop −6.234%, p_fill 23%, n_eff≈13.3) : P(cible|rempli) **53%** · **EV/risk +0.118** (×p_fill ; si rempli +3.17% du capital)
  - **deep** (entrée dip −7.621% → cible +11.975% / stop −9.623%, p_fill 16%, n_eff≈19.0) : P(cible|rempli) **28%** · **EV/risk -0.003** (×p_fill ; si rempli -0.19% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→59% · +3.0%→44% · +5.0%→18% · +8.0%→10%
- Range intraday médian 5.55% (p90 10.31%) · excursion haute méd. +2.54% / basse méd. −2.28%
- Profil de vol intra : ouverture 3.455% vs midi 1.19% vs clôture 1.377% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑2%/↓0% ; spike-down 70% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; neutre — autocorr -0.013)_ ; drift intra méd. 1.293% ; recovery-V 29%
- **σ réalisé intraday** 3.641% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 80% / bas 52% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 142.0446 (VA 141.0741–144.3091 ; dernier close 142.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 75% · **stop −4.03%** sous le fill (sous le bruit) · cible +1.96% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 53% (gap-down >1% 43% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.0%) · haut méd +0.76% · range méd 1.83%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.91%) · haut méd +1.21% · range méd 2.57%
- Excursion ouverture 30min (n=160) : bas méd −1.28% (p90 −3.23%) · haut méd +1.43% · range méd 3.13%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −3.57%) · haut méd +1.82% · range méd 3.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 142.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 74% (121/159) · gap 46% · délai 0.0min · rebond 46% (58/121) (MFE +0.56%)
   - −1.0% : fill 30min 60% · séance 69% (116/159) · gap 43% · délai 0.0min · rebond 50% (63/116) (MFE +1.01%)
   - −1.5% : fill 30min 53% · séance 64% (109/159) · gap 34% · délai 0.0min · rebond 59% (64/109) (MFE +1.35%)
   - −2.0% : fill 30min 48% · séance 58% (99/159) · gap 29% · délai 0.0min · rebond 60% (60/99) (MFE +1.43%)
   - −3.0% : fill 30min 32% · séance 48% (80/159) · gap 15% · délai 1.2min · rebond 58% (48/80) (MFE +1.67%)
   - −4.0% : fill 30min 21% · séance 38% (66/159) · gap 6% · délai 17.9min · rebond 71% (45/66) (MFE +1.9%)
   - −5.0% : fill 30min 15% · séance 28% (48/159) · gap 5% · délai 21.4min · rebond 75% (35/48) (MFE +1.96%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.8% (p90 −2.45%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −2.43%) → stop au-delà de −2.01% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.93% (p90 −2.39%) → stop au-delà de −2.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=964 jambes) : jambe baissière méd −1.1% (p90 −2.68%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (79 séances) :
      · −1.0% : fill 100% (79/79) · rebond 42% (36/79)
      · −2.0% : fill 93% (73/79) · rebond 60% (42/73)
      · −3.0% : fill 81% (65/79) · rebond 60% (39/65)
      · −4.0% : fill 67% (55/79) · rebond 73% (38/55)
      · −5.0% : fill 50% (42/79) · rebond 78% (32/42)
   - **flat** (17 séances) :
      · −1.0% : fill 70% (13/17) · rebond 80% (11/13)
      · −2.0% : fill 45% (9/17) · rebond 60% (6/9)
      · −3.0% : fill 28% (5/17) · rebond 35% (2/5)
      · −4.0% : fill 12% (3/17) · rebond 51% (2/3)
      · −5.0% : fill 9% (2/17) · rebond 0% (0/2)
   - **gap-up** (63 séances) :
      · −1.0% : fill 30% (24/63) · rebond 63% (16/24)
      · −2.0% : fill 15% (17/63) · rebond 66% (12/17)
      · −3.0% : fill 10% (10/63) · rebond 57% (7/10)
      · −4.0% : fill 9% (8/63) · rebond 68% (5/8)
      · −5.0% : fill 4% (4/63) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 55% si les 15 1res min sont vertes (85 cas) · 38% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:33** → P(séance verte=clôture>ouverture) 81% si début vert vs 15% si rouge (base 48% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **81%** · continue >prix actuel 47% ; creux résiduel méd -1.39% (q20 -2.95%) → **SL/trailing à −2.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.83% / q75 +2.83% → **scale +1.83% / runner +2.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **15%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.74%** (au-delà de la MAE q10 -4.74%), cible rebond +1.49% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.29% .. +3.69%] · haut q95 +3.94% · bas q05 -3.65%
   - 60min (n=160) : retour [-4.26% .. +5.6%] · haut q95 +5.86% · bas q05 -4.96%
   - 2h (n=160) : retour [-4.29% .. +8.45%] · haut q95 +8.77% · bas q05 -5.05%
   - 4h (n=160) : retour [-5.44% .. +9.36%] · haut q95 +10.32% · bas q05 -6.45%
   - 6h (n=160) : retour [-5.5% .. +8.47%] · haut q95 +10.93% · bas q05 -7.06%
   - session (n=160) : retour [-5.0% .. +8.29%] · haut q95 +10.93% · bas q05 -7.09%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0.6% / strong 6.2%) · base = 11 séances trend-up (n_eff 6.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **38%**. Lecture précoce 30 min : signature présente → 23% vs absente 1% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.54% / p90 2.99%) · ~3.89 replis/séance, durée méd 35.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 19.22 min, n=40)
   - −1.0% → **61%** (reprise méd 35.89 min, n=19)
   - −1.5% → **46%** (reprise méd 37.49 min, n=15)
   - −2.0% → **20%** (reprise méd 89.44 min, n=9)
   - −3.0% → **41%** (reprise méd 89.44 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.99%** (p90, défaut prudent ; serré/agressif −1.54%) ; extension open→close méd +8.34% (q75 +10.86% / q95 +15.58%), MFE méd +10.26% / q90 +13.74%
   - Échelle scale-out : +10.26% (33%) / +13.11% (33%) / +13.74% (34%)
- **DÉSARMER** : repli > **−2.99%** depuis le plus-haut = décay → P(retournement) **59%** (préavis méd 221.98 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.74% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.51%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
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

- **RSI** : 70.8  _(surachat)_
- **ADX** : 41.3  _(tendance tres forte)_
- **MACD** : hist 2.74  _(bullish_recent)_
- **BB** : %B 1.08 · largeur 38.9%
- **ATR** : 9.91 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.253  _(accumulation)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 38.9  _(transition)_
- **MA** : MA20 136.34 · MA50 113.8 · MA200 136.87  _(prix > MA20)_
- **Dist MA** : MA20 +22.7% · MA50 +47.0% · MA200 +22.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (860384 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
