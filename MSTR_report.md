# MSTR

**Generated** : 2026-09-09T00:35:05.927768+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $136.51  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $136.51 (+1.0% vs entrée) · entrée $135.22 · stop $124.98 · T1 $146.01 · R/R 1.05  
> ↳ P(T1 av. stop) 55 % _(réel 5 s)_ · EV/risk 0.273 _(réel 5 s)_ (GBM -0.046) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -9.0 % ≠ (strike 130.0 − spot 136.51)/spot = -4.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 70.5 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $133.92–$136.51 (mid $135.22)
- Spot actuel : $136.51 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $124.98 (stop swing_plan-based (-8.44%))
- Targets : T1 $146.01 · R/R 1.05 | T2 $156.81 · R/R 2.11 | T3 $167.61 · R/R 3.16
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $124.98


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.44 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1253).
   - exécution **2.959 pt plus bas** dans le cas TYPIQUE (médiane), 18.297 au p90, **18.932 au pire**
   - perte réelle **14.455 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 8.44 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0432 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.493 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.278** [0.2153 ; 0.348] _(largeur 13.3 pt, n_eff 173.1)_
   - swing : **0.3788** [0.3288 ; 0.4308] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3731** [0.3233 ; 0.425] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.4 pt), swing (32.2 pt), deep (30.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.66 %** | CVaR **-10.34 %** | vol 5.49 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.56 % contre 5.12 % aujourd'hui, rapport 1.67)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.67 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3345** (β de hausse 1.8349, asymétrie 1.2722) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 121.1618 sur atr_based (1.5 ATR, 11.243 %) — p(stop avant cible) 0.3976 [0.35 ; 0.45], R/R 2.367, perte reelle 17.215 % (gap inclus), CVaR 11.272 %, EV -1.6301 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 4.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.03 ATR (stop 2.604 %) — p(stop avant cible) 0.8743 [0.84 ; 0.91], R/R 8.549, perte reelle 4.766 % (gap inclus), EV -2.2956 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 8.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.874, borne haute 0.906 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.03 ATR du spot — compartiment <1, mesure a 49.4 % de casse (IC clusterise [0.461 ; 0.528] sur 1205 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.30 %) : P(cible) 2.2 % x 40.74 % + P(rien) 10.3 % x 9.32 % ne couvrent pas P(stop) 87.4 % x 4.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 11.243 %) — p(stop avant cible) 0.3976 [0.35 ; 0.45], R/R 2.367, perte reelle 17.215 % (gap inclus), EV -1.6301 % — **REFUSE**
      - refuse : cible atteinte seulement 4.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.63 %) : P(cible) 4.4 % x 40.74 % + P(rien) 55.9 % x 6.15 % ne couvrent pas P(stop) 39.8 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.68 ATR (stop 14.996 %) — p(stop avant cible) 0.2761 [0.23 ; 0.33], R/R 1.51, perte reelle 26.975 % (gap inclus), EV -3.0488 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.05 %) : P(cible) 4.5 % x 40.74 % + P(rien) 67.9 % x 3.80 % ne couvrent pas P(stop) 27.6 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.97 ATR (stop 17.145 %) — p(stop avant cible) 0.217 [0.18 ; 0.26], R/R 1.51, perte reelle 26.975 % (gap inclus), EV -2.0585 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.16 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 4.5 % x 40.74 % + P(rien) 73.8 % x 2.67 % ne couvrent pas P(stop) 21.7 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.16 ATR (stop 26.104 %) — p(stop avant cible) 0.0812 [0.06 ; 0.11], R/R 1.51, perte reelle 26.975 % (gap inclus), EV -0.268 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 4.5 % x 40.74 % + P(rien) 87.4 % x 0.11 % ne couvrent pas P(stop) 8.1 % x 26.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.748 %) — p(stop avant cible) 0.784 [0.74 ; 0.82], R/R 6.126, perte reelle 6.651 % (gap inclus), EV -1.6208 % — **REFUSE**
      - refuse : cible atteinte seulement 3.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.784, borne haute 0.825 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.62 %) : P(cible) 3.5 % x 40.74 % + P(rien) 18.1 % x 11.91 % ne couvrent pas P(stop) 78.4 % x 6.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.622 %) — p(stop avant cible) 0.6734 [0.62 ; 0.72], R/R 4.715, perte reelle 8.642 % (gap inclus), EV -1.3783 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.673, borne haute 0.721 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.38 %) : P(cible) 4.1 % x 40.74 % + P(rien) 28.6 % x 9.74 % ne couvrent pas P(stop) 67.3 % x 8.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 7.496 %) — p(stop avant cible) 0.5613 [0.51 ; 0.61], R/R 3.521, perte reelle 11.572 % (gap inclus), EV -1.4059 % — **REFUSE**
      - refuse : cible atteinte seulement 4.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.561, borne haute 0.613 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.41 %) : P(cible) 4.2 % x 40.74 % + P(rien) 39.6 % x 8.48 % ne couvrent pas P(stop) 56.1 % x 11.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 9.369 %) — p(stop avant cible) 0.4832 [0.43 ; 0.54], R/R 2.367, perte reelle 17.215 % (gap inclus), EV -3.0254 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.03 %) : P(cible) 4.3 % x 40.74 % + P(rien) 47.4 % x 7.50 % ne couvrent pas P(stop) 48.3 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 18.739 %) — p(stop avant cible) 0.1935 [0.15 ; 0.24], R/R 1.51, perte reelle 26.975 % (gap inclus), EV -1.7093 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.71 %) : P(cible) 4.5 % x 40.74 % + P(rien) 76.2 % x 2.21 % ne couvrent pas P(stop) 19.4 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 20.613 %) — p(stop avant cible) 0.1667 [0.13 ; 0.21], R/R 1.51, perte reelle 26.975 % (gap inclus), EV -1.2652 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 4.5 % x 40.74 % + P(rien) 78.8 % x 1.78 % ne couvrent pas P(stop) 16.7 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 29.982 %) — p(stop avant cible) 0.0462 [0.03 ; 0.07], R/R 1.359, perte reelle 29.982 % (gap inclus), EV -0.2128 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 4.5 % x 40.74 % + P(rien) 90.9 % x -0.72 % ne couvrent pas P(stop) 4.6 % x 29.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 33.73 %) — p(stop avant cible) 0.022 [0.01 ; 0.04], R/R 1.208, perte reelle 33.73 % (gap inclus), EV -0.149 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 4.5 % x 40.74 % + P(rien) 93.3 % x -1.32 % ne couvrent pas P(stop) 2.2 % x 33.73 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 37.478 %) — p(stop avant cible) 0.0065 [0.00 ; 0.02], R/R 1.087, perte reelle 37.478 % (gap inclus), EV -0.0263 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 4.5 % x 40.74 % + P(rien) 94.9 % x -1.70 % ne couvrent pas P(stop) 0.7 % x 37.48 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 41.225 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.988, perte reelle 41.225 % (gap inclus), EV 0.0155 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.23 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 44.973 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.906, perte reelle 44.973 % (gap inclus), EV 0.0324 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.97 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 48.721 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.836, perte reelle 48.721 % (gap inclus), EV 0.0316 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.72 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 52.469 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.777, perte reelle 52.469 % (gap inclus), EV 0.0304 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 52.47 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 56.216 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.725, perte reelle 56.216 % (gap inclus), EV 0.03 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.22 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 59.964 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.679, perte reelle 59.964 % (gap inclus), EV 0.0285 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 59.96 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 136.51, ATR14 10.2321 (7.496 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.395 ATR = 2.961 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.375 % | 135.9984 | 94.16 % | 96.57 % | 97.07 % | 97.67 % | 98.07 % | 98.67 % |
| 0.1 ATR | 0.75 % | 135.4868 | 88.12 % | 91.94 % | 93.44 % | 94.74 % | 96.65 % | 97.33 % |
| 0.15 ATR | 1.124 % | 134.9752 | 81.27 % | 87.0 % | 89.61 % | 91.71 % | 94.11 % | 95.59 % |
| 0.2 ATR | 1.499 % | 134.4636 | 73.72 % | 81.75 % | 84.86 % | 88.07 % | 91.36 % | 93.74 % |
| 0.25 ATR | 1.874 % | 133.952 | 67.88 % | 77.92 % | 82.04 % | 86.15 % | 89.13 % | 92.2 % |
| 0.35 ATR | 2.623 % | 132.9287 | 55.09 % | 68.75 % | 75.18 % | 80.79 % | 85.67 % | 89.53 % |
| 0.5 ATR | 3.748 % | 131.3939 | 38.27 % | 55.34 % | 63.37 % | 71.18 % | 78.46 % | 84.7 % |
| 0.75 ATR | 5.622 % | 128.8359 | 19.34 % | 37.6 % | 47.02 % | 57.84 % | 67.89 % | 77.41 % |
| 1.0 ATR | 7.496 % | 126.2779 | 9.37 % | 25.2 % | 34.71 % | 46.31 % | 58.84 % | 70.33 % |
| 1.25 ATR | 9.369 % | 123.7198 | 4.13 % | 14.52 % | 25.03 % | 36.0 % | 49.8 % | 62.94 % |
| 1.5 ATR | 11.243 % | 121.1618 | 2.11 % | 8.67 % | 17.36 % | 29.02 % | 42.99 % | 57.08 % |
| 2.0 ATR | 14.991 % | 116.0457 | 0.2 % | 3.12 % | 7.37 % | 16.18 % | 31.3 % | 47.23 % |
| 2.5 ATR | 18.739 % | 110.9296 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.44 % | 37.58 % |
| 3.0 ATR | 22.487 % | 105.8136 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 28.03 % |
| 4.0 ATR | 29.982 % | 95.5814 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 18.07 % |
| 6.0 ATR | 44.973 % | 75.1171 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.40 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.12 ATR | 1.44 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.25 ATR | 1.41 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.92 ATR | 1.03 ATR | 1.36 ATR | 1.66 ATR | 1.85 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.58 ATR | 1.24 ATR | 1.43 ATR | 1.93 ATR | 2.32 ATR | 2.60 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.83 ATR | 1.86 ATR | 2.12 ATR | 2.74 ATR | 3.30 ATR | 3.81 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.44–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.748 %, prix 131.3936), p(touche) 38.27 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.622 %, prix 128.8354), p(touche) 37.6 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.791–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.496 %, prix 126.2772), p(touche) 34.71 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.032–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.369 %, prix 123.7204), p(touche) 36.0 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.426–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.243 %, prix 121.1622), p(touche) 42.99 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.116–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (18.739 %, prix 110.9294), p(touche) 37.58 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.046 | EV/share : $-0.468 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 12 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 18.2 | bear 34.5 | side 47.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 410.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.508% → cible +3.571% / stop −3.5%, p_fill 86%, n_eff≈38.9) : P(cible|rempli) **39%** · **EV/risk +0.117** (×p_fill ; si rempli +0.48% du capital)
  - **swing** (entrée dip −0.944% → cible +7.985% / stop −7.567%, p_fill 83%, n_eff≈34.3) : P(cible|rempli) **55%** · **EV/risk +0.273** (×p_fill ; si rempli +2.50% du capital)
  - **deep** (entrée dip −1.276% → cible +11.293% / stop −11.389%, p_fill 83%, n_eff≈35.1) : P(cible|rempli) **65%** · **EV/risk +0.384** (×p_fill ; si rempli +5.25% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 70.4  _(surachat)_
- **ADX** : 39.1  _(tendance etablie)_
- **MACD** : hist 2.172  _(pas de croisement recent)_
- **BB** : %B 0.77 · largeur 60.1%
- **ATR** : 10.23 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.212  _(accumulation)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 39.4  _(transition)_
- **MA** : MA20 117.48 · MA50 104.59 · MA200 138.73  _(prix > MA20)_
- **Dist MA** : MA20 +16.2% · MA50 +30.5% · MA200 -1.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (774976 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
