# RGTI

**Generated** : 2026-09-30T00:30:33.134688+00:00  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.78  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $15.78 (+1.2% vs entrée) · entrée $15.60 · stop $14.68 · T1 $16.19 · R/R 0.64  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +3.5 % ≠ (strike 16.5 − spot 15.78)/spot = +4.6 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $15.48–$15.72 (mid $15.60)
- Spot actuel : $15.78 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $14.68 (plancher anti-bruit (R/R<2) ; -5.90 % depuis l'entree)
- Targets : T1 $16.19 · R/R 0.64 | T2 $16.79 · R/R 1.29 | T3 $17.39 · R/R 1.95
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.68


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.98 %)** : le gap seul le franchit 1.596 % des séances (20 fois sur 1253).
   - exécution **3.204 pt plus bas** dans le cas TYPIQUE (médiane), 8.001 au p90, **24.233 au pire**
   - perte réelle **11.681 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 6.98 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.075 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.113 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3999** [0.3291 ; 0.474] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.4206** [0.3694 ; 0.4731] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3982** [0.3476 ; 0.4505] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 98.3 observations effectives », dont la borne haute a 95 % vaut environ 3.1 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.95 %** | CVaR **-11.33 %** | vol 6.83 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 19.53 % contre 6.39 % aujourd'hui, rapport 3.05)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8454** (β de hausse 1.9881, asymétrie 0.9282) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.491× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 13.9924 sur support (1.49 ATR, 11.328 %) — p(stop avant cible) 0.567 [0.51 ; 0.62], R/R 2.98, perte reelle 11.472 % (gap inclus), CVaR 12.963 %, EV -0.6735 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5154 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.567, borne haute 0.619 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.96 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 17 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 41.9 % de la queue et il ne reste que 294.13 EUR a partager. Prix du risque 0.099 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.4 ATR (stop 4.95 %) — p(stop avant cible) 0.7864 [0.74 ; 0.83], R/R 6.805, perte reelle 5.024 % (gap inclus), EV 0.0083 % — **REFUSE**
      - refuse : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.786, borne haute 0.827 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_based a 1.5 ATR (stop 8.724 %) — p(stop avant cible) 0.647 [0.60 ; 0.70], R/R 3.834, perte reelle 8.916 % (gap inclus), EV -0.2122 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.647, borne haute 0.696 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 9.8 % x 34.19 % + P(rien) 25.5 % x 8.69 % ne couvrent pas P(stop) 64.7 % x 8.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 1.49 ATR (stop 11.328 %) — p(stop avant cible) 0.567 [0.51 ; 0.62], R/R 2.98, perte reelle 11.472 % (gap inclus), EV -0.6735 % — **REFUSE**
      - refuse : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.567, borne haute 0.619 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.96 % > budget 12.00 %
      - ⚠ support DETECTE a 0.36 ATR du spot — compartiment <1, mesure a 49.1 % de casse (IC clusterise [0.457 ; 0.522] sur 1123 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 10.4 % x 34.19 % + P(rien) 32.9 % x 6.88 % ne couvrent pas P(stop) 56.7 % x 11.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.54 ATR (stop 23.242 %) — p(stop avant cible) 0.1286 [0.10 ; 0.17], R/R 1.45, perte reelle 23.576 % (gap inclus), EV 0.809 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.10 % > budget 12.00 %
   - ⚪ grid_snapped a 0.4 ATR (stop 4.048 %) — p(stop avant cible) 0.814 [0.77 ; 0.85], R/R 8.259, perte reelle 4.139 % (gap inclus), EV 0.2312 % — **REFUSE**
      - refuse : cible atteinte seulement 6.9 % du temps (< 15 %) meme a 10 seances : le R/R de 8.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.814, borne haute 0.852 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 5.816 %) — p(stop avant cible) 0.7475 [0.70 ; 0.79], R/R 5.72, perte reelle 5.976 % (gap inclus), EV 0.0898 % — **REFUSE**
      - refuse : cible atteinte seulement 8.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.748, borne haute 0.791 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 grid_snapped a 1.49 ATR (stop 10.427 %) — p(stop avant cible) 0.6068 [0.55 ; 0.66], R/R 3.23, perte reelle 10.583 % (gap inclus), EV -0.7606 % — **REFUSE**
      - refuse : cible atteinte seulement 10.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.607, borne haute 0.657 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 10.2 % x 34.19 % + P(rien) 29.1 % x 7.43 % ne couvrent pas P(stop) 60.7 % x 10.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 13.085 %) — p(stop avant cible) 0.4597 [0.41 ; 0.51], R/R 2.574, perte reelle 13.283 % (gap inclus), EV -0.1467 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 10.9 % x 34.19 % + P(rien) 43.1 % x 5.18 % ne couvrent pas P(stop) 46.0 % x 13.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 14.539 %) — p(stop avant cible) 0.399 [0.35 ; 0.45], R/R 2.314, perte reelle 14.772 % (gap inclus), EV -0.1809 % — **REFUSE**
      - refuse : cible atteinte seulement 11.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 11.3 % x 34.19 % + P(rien) 48.8 % x 3.78 % ne couvrent pas P(stop) 39.9 % x 14.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 15.993 %) — p(stop avant cible) 0.3312 [0.28 ; 0.38], R/R 2.104, perte reelle 16.246 % (gap inclus), EV 0.0854 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.67 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.447 %) — p(stop avant cible) 0.2828 [0.24 ; 0.33], R/R 1.932, perte reelle 17.691 % (gap inclus), EV 0.3327 % — **REFUSE**
      - refuse : cible atteinte seulement 12.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.83 % > budget 12.00 %
   - 🟢 grid_snapped a 3.54 ATR (stop 22.34 %) — p(stop avant cible) 0.1445 [0.11 ; 0.18], R/R 1.508, perte reelle 22.664 % (gap inclus), EV 0.8104 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.28 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 26.171 %) — p(stop avant cible) 0.085 [0.06 ; 0.12], R/R 1.293, perte reelle 26.446 % (gap inclus), EV 0.9986 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.64 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.078 %) — p(stop avant cible) 0.0651 [0.04 ; 0.09], R/R 1.166, perte reelle 29.312 % (gap inclus), EV 1.0118 % — **REFUSE**
      - refuse : cible atteinte seulement 13.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.38 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.986 %) — p(stop avant cible) 0.0435 [0.03 ; 0.07], R/R 1.061, perte reelle 32.212 % (gap inclus), EV 1.0084 % — **REFUSE**
      - refuse : cible atteinte seulement 13.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.75 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.894 %) — p(stop avant cible) 0.0267 [0.01 ; 0.05], R/R 0.968, perte reelle 35.312 % (gap inclus), EV 1.108 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.80 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.802 %) — p(stop avant cible) 0.0155 [0.01 ; 0.03], R/R 0.893, perte reelle 38.269 % (gap inclus), EV 1.1353 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.24 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.71 %) — p(stop avant cible) 0.0098 [0.00 ; 0.02], R/R 0.837, perte reelle 40.829 % (gap inclus), EV 1.1988 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.14 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.618 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 0.784, perte reelle 43.618 % (gap inclus), EV 1.1975 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.15 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.525 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 0.734, perte reelle 46.589 % (gap inclus), EV 1.1878 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.42 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.78, ATR14 0.9177 (5.816 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.407 ATR = 2.367 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.291 % | 15.7341 | 91.94 % | 94.35 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.582 % | 15.6882 | 86.2 % | 90.93 % | 92.33 % | 94.94 % | 95.93 % | 97.43 % |
| 0.15 ATR | 0.872 % | 15.6423 | 80.66 % | 87.2 % | 89.0 % | 92.01 % | 94.0 % | 96.1 % |
| 0.2 ATR | 1.163 % | 15.5965 | 74.22 % | 82.66 % | 85.47 % | 88.78 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.454 % | 15.5506 | 68.08 % | 78.33 % | 81.43 % | 85.64 % | 88.82 % | 92.51 % |
| 0.35 ATR | 2.035 % | 15.4588 | 55.59 % | 68.25 % | 73.56 % | 79.37 % | 84.45 % | 89.63 % |
| 0.5 ATR | 2.908 % | 15.3211 | 40.99 % | 56.85 % | 64.48 % | 71.39 % | 78.96 % | 85.52 % |
| 0.75 ATR | 4.362 % | 15.0917 | 21.85 % | 38.91 % | 49.65 % | 58.75 % | 70.63 % | 79.36 % |
| 1.0 ATR | 5.816 % | 14.8623 | 9.87 % | 23.99 % | 33.7 % | 46.51 % | 61.69 % | 73.0 % |
| 1.25 ATR | 7.27 % | 14.6329 | 4.23 % | 14.72 % | 23.81 % | 36.8 % | 52.74 % | 65.71 % |
| 1.5 ATR | 8.724 % | 14.4034 | 1.81 % | 7.26 % | 13.82 % | 25.48 % | 42.99 % | 57.6 % |
| 2.0 ATR | 11.631 % | 13.9446 | 0.4 % | 1.81 % | 4.04 % | 10.62 % | 25.2 % | 41.48 % |
| 2.5 ATR | 14.539 % | 13.4857 | 0.1 % | 0.4 % | 1.21 % | 4.35 % | 14.33 % | 29.16 % |
| 3.0 ATR | 17.447 % | 13.0269 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.45 % |
| 4.0 ATR | 23.263 % | 12.1091 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.93 % |
| 6.0 ATR | 34.894 % | 10.2737 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 1.00 ATR | 1.22 ATR |
| **2 s.** | 0.28 ATR | 0.59 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.11 ATR | 1.41 ATR | 1.71 ATR |
| **3 s.** | 0.33 ATR | 0.74 ATR | 0.82 ATR | 1.02 ATR | 1.22 ATR | 1.34 ATR | 1.70 ATR | 1.95 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.04 ATR | 1.33 ATR | 1.52 ATR | 1.68 ATR | 2.05 ATR | 2.45 ATR |
| **10 s.** | 0.62 ATR | 1.32 ATR | 1.45 ATR | 1.78 ATR | 2.01 ATR | 2.24 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.92 ATR | 1.74 ATR | 1.89 ATR | 2.34 ATR | 2.68 ATR | 2.89 ATR | 3.60 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.459–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.908 %, prix 15.3211), p(touche) 40.99 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (70.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.665–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.362 %, prix 15.0917), p(touche) 38.91 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.823–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.816 %, prix 14.8622), p(touche) 33.7 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.039–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.27 %, prix 14.6328), p(touche) 36.8 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.448–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.724 %, prix 14.4034), p(touche) 42.99 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.891–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.631 %, prix 13.9446), p(touche) 41.48 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.096 | EV/share : $-0.088 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 38 % | T3 26 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 28.8 | side 66.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 278.0 (= 20 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.533% → cible +1.712% / stop −2.5%, p_fill 86%, n_eff≈95.9) : P(cible|rempli) **56%** · **EV/risk -0.019** (×p_fill ; si rempli -0.06% du capital)
  - **swing** (entrée dip −1.164% → cible +3.829% / stop −5.884%, p_fill 89%, n_eff≈104.8) : P(cible|rempli) **54%** · **EV/risk -0.098** (×p_fill ; si rempli -0.65% du capital)
  - **deep** (entrée dip −1.796% → cible +5.414% / stop −8.884%, p_fill 88%, n_eff≈98.3) : P(cible|rempli) **56%** · **EV/risk -0.094** (×p_fill ; si rempli -0.95% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→79% · +2.0%→64% · +3.0%→46% · +5.0%→31% · +8.0%→11%
- Range intraday médian 7.05% (p90 11.08%) · excursion haute méd. +2.71% / basse méd. −2.75%
- Profil de vol intra : ouverture 4.658% vs midi 1.47% vs clôture 1.678% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 23% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.072)_ ; drift intra méd. 0.055% ; recovery-V 34%
- **σ réalisé intraday** 3.943% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 47% / whipsaw 3%
- POC intraday (dernière séance, temps-au-prix) : 15.2248 (VA 15.1512–15.2668 ; dernier close 15.21)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 42% · rebond 73% · **stop −5.83%** sous le fill (sous le bruit) · cible +1.81% · R/R 0.31 (high win-rate)
- Gaps overnight (n=159) : méd. -0.5% · baisse 61% (gap-down >1% 41% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −1.15% (p90 −2.86%) · haut méd +1.28% · range méd 2.51%
- Excursion ouverture 15min (n=160) : bas méd −1.41% (p90 −3.6%) · haut méd +1.74% · range méd 3.43%
- Excursion ouverture 30min (n=160) : bas méd −1.69% (p90 −4.45%) · haut méd +1.96% · range méd 4.17%
- Excursion ouverture 60min (n=160) : bas méd −2.07% (p90 −5.46%) · haut méd +2.19% · range méd 4.96%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 81% (132/159) · gap 50% · délai 0.0min · rebond 61% (83/132) (MFE +1.86%)
   - −1.0% : fill 30min 64% · séance 72% (123/159) · gap 41% · délai 0.0min · rebond 63% (76/123) (MFE +1.58%)
   - −1.5% : fill 30min 59% · séance 66% (116/159) · gap 32% · délai 0.0min · rebond 63% (73/116) (MFE +1.91%)
   - −2.0% : fill 30min 53% · séance 59% (107/159) · gap 25% · délai 0.0min · rebond 63% (69/107) (MFE +1.73%)
   - −3.0% : fill 30min 43% · séance 53% (96/159) · gap 10% · délai 1.2min · rebond 64% (67/96) (MFE +1.87%)
   - −4.0% : fill 30min 33% · séance 42% (75/159) · gap 5% · délai 6.5min · rebond 73% (53/75) (MFE +1.81%)
   - −5.0% : fill 30min 17% · séance 35% (65/159) · gap 2% · délai 31.2min · rebond 55% (43/65) (MFE +1.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.18%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.86% (p90 −2.72%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.87% (p90 −2.77%) → stop au-delà de −1.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1134 jambes) : jambe baissière méd −1.27% (p90 −3.06%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 90% (81/85) · rebond 56% (45/81)
      · −2.0% : fill 82% (76/85) · rebond 60% (47/76)
      · −3.0% : fill 76% (71/85) · rebond 56% (46/71)
      · −4.0% : fill 63% (57/85) · rebond 71% (39/57)
      · −5.0% : fill 54% (50/85) · rebond 52% (32/50)
   - **flat** (16 séances) :
      · −1.0% : fill 96% (15/16) · rebond 95% (13/15)
      · −2.0% : fill 61% (12/16) · rebond 85% (10/12)
      · −3.0% : fill 42% (7/16) · rebond 89% (5/7)
      · −4.0% : fill 28% (6/16) · rebond 84% (4/6)
      · −5.0% : fill 18% (5/16) · rebond 87% (3/5)
   - **gap-up** (58 séances) :
      · −1.0% : fill 36% (27/58) · rebond 65% (18/27)
      · −2.0% : fill 24% (19/58) · rebond 60% (12/19)
      · −3.0% : fill 22% (18/58) · rebond 90% (16/18)
      · −4.0% : fill 13% (12/58) · rebond 83% (10/12)
      · −5.0% : fill 12% (10/58) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 76% si les 15 1res min sont vertes (81 cas) · 24% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 87% si début vert vs 14% si rouge (base 52% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **87%** · continue >prix actuel 52% ; creux résiduel méd -1.61% (q20 -3.45%) → **SL/trailing à −3.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +4.79% → **scale +1.55% / runner +4.79%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **14%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.22%** (au-delà de la MAE q10 -5.22%), cible rebond +1.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.99% .. +4.59%] · haut q95 +5.93% · bas q05 -5.97%
   - 60min (n=160) : retour [-5.29% .. +5.8%] · haut q95 +6.59% · bas q05 -6.58%
   - 2h (n=160) : retour [-6.23% .. +6.16%] · haut q95 +7.24% · bas q05 -7.33%
   - 4h (n=160) : retour [-6.46% .. +7.46%] · haut q95 +9.18% · bas q05 -7.78%
   - 6h (n=160) : retour [-7.15% .. +8.21%] · haut q95 +9.38% · bas q05 -8.49%
   - session (n=160) : retour [-7.08% .. +8.5%] · haut q95 +10.21% · bas q05 -8.6%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **27%**. Lecture précoce 30 min : signature présente → 12% vs absente 5% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 1.66% / p90 2.43%) · ~4.04 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.0 min, n=43)
   - −1.0% → **83%** (reprise méd 35.0 min, n=27)
   - −1.5% → **83%** (reprise méd 93.49 min, n=16)
   - −2.0% → **84%** (reprise méd 44.98 min, n=8)
   - −3.0% → **66%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.43%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.12% (q75 +9.53% / q95 +9.89%), MFE méd +9.52% / q90 +11.18%
   - Échelle scale-out : +9.52% (33%) / +10.45% (33%) / +11.18% (34%)
- **DÉSARMER** : repli > **−2.43%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.18% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.12%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.62 · part idiosyncratique 0.38
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.5  _(momentum haussier)_
- **ADX** : 10.7  _(pas de tendance nette)_
- **MACD** : hist 0.104  _(pas de croisement recent)_
- **BB** : %B 0.56 · largeur 15.4%
- **ATR** : 0.92 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.119  _(distribution)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 52.1  _(transition)_
- **MA** : MA20 15.63 · MA50 16.12 · MA200 18.48  _(prix > MA20)_
- **Dist MA** : MA20 +1.0% · MA50 -2.1% · MA200 -14.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (861239 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
