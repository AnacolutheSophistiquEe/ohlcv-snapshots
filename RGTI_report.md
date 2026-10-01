# RGTI

**Generated** : 2026-10-01T00:28:17.758117+00:00  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.73  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $15.73 (+0.5% vs entrée) · entrée $15.65 · stop $14.71 · T1 $16.69 · R/R 1.11  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $15.57–$15.73 (mid $15.65)
- Spot actuel : $15.73 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $14.71 (plancher anti-bruit (R/R<2) ; -6.01 % depuis l'entree)
- Targets : T1 $16.69 · R/R 1.11 | T2 $17.74 · R/R 2.22 | T3 $18.78 · R/R 3.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.71


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.46 %)** : le gap seul le franchit 1.676 % des séances (21 fois sur 1253).
   - exécution **3.432 pt plus bas** dans le cas TYPIQUE (médiane), 8.195 au p90, **24.753 au pire**
   - perte réelle **11.454 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 6.46 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0837 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.113 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5056** [0.4315 ; 0.5795] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5114** [0.4588 ; 0.5638] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5582** [0.5055 ; 0.6099] _(largeur 10.4 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.95 %** | CVaR **-11.33 %** | vol 6.83 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 19.51 % contre 6.39 % aujourd'hui, rapport 3.05)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8463** (β de hausse 1.9918, asymétrie 0.927) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.501× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 15.1325 sur grid_snapped (0.34 ATR, 3.786 %) — p(stop avant cible) 0.8242 [0.78 ; 0.86], R/R 8.914, perte reelle 3.881 % (gap inclus), CVaR 5.275 %, EV 0.2485 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.6172 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 8.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.824, borne haute 0.862 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 5.27 % > budget 3.54 %
- Budget de queue : **3.54 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.171 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 44.7 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.34 ATR (stop 4.785 %) — p(stop avant cible) 0.7901 [0.74 ; 0.83], R/R 7.105, perte reelle 4.869 % (gap inclus), EV 0.1078 % — **REFUSE**
      - refuse : cible atteinte seulement 7.3 % du temps (< 15 %) meme a 10 seances : le R/R de 7.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.790, borne haute 0.831 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.06 % > budget 3.54 %
   - ⚪ atr_based a 1.5 ATR (stop 8.918 %) — p(stop avant cible) 0.6403 [0.59 ; 0.69], R/R 3.804, perte reelle 9.094 % (gap inclus), EV -0.2545 % — **REFUSE**
      - refuse : cible atteinte seulement 9.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.640, borne haute 0.690 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 11.15 % > budget 3.54 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 9.5 % x 34.60 % + P(rien) 26.5 % x 8.63 % ne couvrent pas P(stop) 64.0 % x 9.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 1.41 ATR (stop 11.162 %) — p(stop avant cible) 0.5703 [0.52 ; 0.62], R/R 3.057, perte reelle 11.318 % (gap inclus), EV -0.6906 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.570, borne haute 0.622 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.94 % > budget 3.54 %
      - ⚠ support DETECTE a 0.04 ATR du spot — compartiment <1, mesure a 45.4 % de casse (IC clusterise [0.423 ; 0.484] sur 1130 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 10.1 % x 34.60 % + P(rien) 32.9 % x 6.89 % ne couvrent pas P(stop) 57.0 % x 11.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.42 ATR (stop 23.115 %) — p(stop avant cible) 0.1312 [0.10 ; 0.17], R/R 1.476, perte reelle 23.447 % (gap inclus), EV 0.8222 % — **REFUSE**
      - refuse : cible atteinte seulement 12.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.99 % > budget 3.54 %
   - ⚪ grid_snapped a 0.34 ATR (stop 3.786 %) — p(stop avant cible) 0.8242 [0.78 ; 0.86], R/R 8.914, perte reelle 3.881 % (gap inclus), EV 0.2485 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 8.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.824, borne haute 0.862 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.27 % > budget 3.54 %
   - ⚪ atr_grid a 1.0 ATR (stop 5.945 %) — p(stop avant cible) 0.739 [0.69 ; 0.78], R/R 5.658, perte reelle 6.114 % (gap inclus), EV 0.1078 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.739, borne haute 0.783 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 8.25 % > budget 3.54 %
   - 🔴 grid_snapped a 1.41 ATR (stop 10.163 %) — p(stop avant cible) 0.622 [0.57 ; 0.67], R/R 3.35, perte reelle 10.328 % (gap inclus), EV -0.7726 % — **REFUSE**
      - refuse : cible atteinte seulement 9.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.622, borne haute 0.672 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.17 % > budget 3.54 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.77 %) : P(cible) 9.6 % x 34.60 % + P(rien) 28.2 % x 8.25 % ne couvrent pas P(stop) 62.2 % x 10.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 13.376 %) — p(stop avant cible) 0.4406 [0.39 ; 0.49], R/R 2.553, perte reelle 13.549 % (gap inclus), EV -0.1251 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.89 % > budget 3.54 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 10.6 % x 34.60 % + P(rien) 45.4 % x 4.82 % ne couvrent pas P(stop) 44.1 % x 13.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 14.863 %) — p(stop avant cible) 0.3808 [0.33 ; 0.43], R/R 2.284, perte reelle 15.147 % (gap inclus), EV -0.1369 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.02 % > budget 3.54 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 11.0 % x 34.60 % + P(rien) 50.9 % x 3.56 % ne couvrent pas P(stop) 38.1 % x 15.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 16.349 %) — p(stop avant cible) 0.3226 [0.28 ; 0.37], R/R 2.085, perte reelle 16.596 % (gap inclus), EV 0.2126 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.94 % > budget 3.54 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.835 %) — p(stop avant cible) 0.2641 [0.22 ; 0.31], R/R 1.912, perte reelle 18.093 % (gap inclus), EV 0.3994 % — **REFUSE**
      - refuse : cible atteinte seulement 12.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.20 % > budget 3.54 %
   - 🟢 grid_snapped a 3.42 ATR (stop 22.117 %) — p(stop avant cible) 0.1583 [0.12 ; 0.20], R/R 1.542, perte reelle 22.436 % (gap inclus), EV 0.766 % — **REFUSE**
      - refuse : cible atteinte seulement 12.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.13 % > budget 3.54 %
   - ⚪ atr_grid a 4.5 ATR (stop 26.753 %) — p(stop avant cible) 0.0771 [0.05 ; 0.11], R/R 1.282, perte reelle 26.988 % (gap inclus), EV 1.0285 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.12 % > budget 3.54 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.725 %) — p(stop avant cible) 0.0627 [0.04 ; 0.09], R/R 1.156, perte reelle 29.939 % (gap inclus), EV 1.0177 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.99 % > budget 3.54 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.698 %) — p(stop avant cible) 0.0394 [0.02 ; 0.06], R/R 1.051, perte reelle 32.904 % (gap inclus), EV 1.0799 % — **REFUSE**
      - refuse : cible atteinte seulement 13.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.89 % > budget 3.54 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.67 %) — p(stop avant cible) 0.0248 [0.01 ; 0.05], R/R 0.961, perte reelle 36.007 % (gap inclus), EV 1.136 % — **REFUSE**
      - refuse : cible atteinte seulement 13.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.88 % > budget 3.54 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.643 %) — p(stop avant cible) 0.0137 [0.01 ; 0.03], R/R 0.888, perte reelle 38.963 % (gap inclus), EV 1.1744 % — **REFUSE**
      - refuse : cible atteinte seulement 13.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.14 % > budget 3.54 %
   - ⚪ atr_grid a 7.0 ATR (stop 41.615 %) — p(stop avant cible) 0.0065 [0.00 ; 0.02], R/R 0.831, perte reelle 41.649 % (gap inclus), EV 1.2395 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.03 % > budget 3.54 %
   - ⚪ atr_grid a 7.5 ATR (stop 44.588 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 0.765, perte reelle 45.215 % (gap inclus), EV 1.2302 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.26 % > budget 3.54 %
   - ⚪ atr_grid a 8.0 ATR (stop 47.56 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 0.727, perte reelle 47.56 % (gap inclus), EV 1.2249 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.30 % > budget 3.54 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.728, ATR14 0.935 (5.945 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.408 ATR = 2.426 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.297 % | 15.6812 | 91.94 % | 94.35 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.595 % | 15.6345 | 86.2 % | 90.93 % | 92.33 % | 94.94 % | 95.93 % | 97.43 % |
| 0.15 ATR | 0.892 % | 15.5877 | 80.66 % | 87.2 % | 89.0 % | 92.01 % | 94.0 % | 96.1 % |
| 0.2 ATR | 1.189 % | 15.541 | 74.22 % | 82.66 % | 85.47 % | 88.78 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.486 % | 15.4942 | 68.08 % | 78.33 % | 81.43 % | 85.64 % | 88.82 % | 92.51 % |
| 0.35 ATR | 2.081 % | 15.4007 | 55.69 % | 68.25 % | 73.56 % | 79.37 % | 84.45 % | 89.63 % |
| 0.5 ATR | 2.973 % | 15.2605 | 41.09 % | 56.85 % | 64.48 % | 71.39 % | 78.96 % | 85.52 % |
| 0.75 ATR | 4.459 % | 15.0267 | 21.85 % | 38.91 % | 49.65 % | 58.75 % | 70.63 % | 79.26 % |
| 1.0 ATR | 5.945 % | 14.793 | 9.87 % | 23.99 % | 33.6 % | 46.51 % | 61.69 % | 72.9 % |
| 1.25 ATR | 7.431 % | 14.5592 | 4.23 % | 14.72 % | 23.71 % | 36.8 % | 52.64 % | 65.61 % |
| 1.5 ATR | 8.918 % | 14.3254 | 1.81 % | 7.26 % | 13.72 % | 25.48 % | 42.89 % | 57.49 % |
| 2.0 ATR | 11.89 % | 13.8579 | 0.4 % | 1.81 % | 4.04 % | 10.72 % | 25.2 % | 41.38 % |
| 2.5 ATR | 14.863 % | 13.3904 | 0.1 % | 0.4 % | 1.21 % | 4.35 % | 14.33 % | 29.16 % |
| 3.0 ATR | 17.835 % | 12.9229 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.45 % |
| 4.0 ATR | 23.78 % | 11.9879 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.93 % |
| 6.0 ATR | 35.67 % | 10.1178 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 1.00 ATR | 1.22 ATR |
| **2 s.** | 0.28 ATR | 0.59 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.11 ATR | 1.41 ATR | 1.71 ATR |
| **3 s.** | 0.33 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.22 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.04 ATR | 1.33 ATR | 1.52 ATR | 1.69 ATR | 2.06 ATR | 2.45 ATR |
| **10 s.** | 0.62 ATR | 1.32 ATR | 1.45 ATR | 1.78 ATR | 2.01 ATR | 2.24 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.92 ATR | 1.73 ATR | 1.89 ATR | 2.34 ATR | 2.68 ATR | 2.89 ATR | 3.60 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.46–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.973 %, prix 15.2604), p(touche) 41.09 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (71.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.665–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.459 %, prix 15.0267), p(touche) 38.91 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.822–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.945 %, prix 14.793), p(touche) 33.6 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.039–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.431 %, prix 14.5593), p(touche) 36.8 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.446–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.918 %, prix 14.3254), p(touche) 42.89 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.888–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.89 %, prix 13.8579), p(touche) 41.38 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.079 | EV/share : $-0.073 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 21 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 30.4 | side 64.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 278.0 (= 20 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.317% → cible +2.982% / stop −2.0%, p_fill 89%, n_eff≈97.2) : P(cible|rempli) **34%** · **EV/risk -0.068** (×p_fill ; si rempli -0.15% du capital)
  - **swing** (entrée dip −0.515% → cible +6.681% / stop −5.976%, p_fill 91%, n_eff≈106.7) : P(cible|rempli) **48%** · **EV/risk +0.005** (×p_fill ; si rempli +0.04% du capital)
  - **deep** (entrée dip −0.662% → cible +10.783% / stop −8.977%, p_fill 96%, n_eff≈107.1) : P(cible|rempli) **40%** · **EV/risk -0.141** (×p_fill ; si rempli -1.32% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→65% · +3.0%→47% · +5.0%→32% · +8.0%→11%
- Range intraday médian 6.97% (p90 11.08%) · excursion haute méd. +2.77% / basse méd. −2.46%
- Profil de vol intra : ouverture 4.734% vs midi 1.414% vs clôture 1.642% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 65% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; neutre — autocorr -0.005)_ ; drift intra méd. -0.296% ; recovery-V 24%
- **σ réalisé intraday** 3.774% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 56% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 15.903 (VA 15.823–15.935 ; dernier close 15.78)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 39% · rebond 74% · **stop −5.32%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. -0.33% · baisse 58% (gap-down >1% 39% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −0.86% (p90 −2.89%) · haut méd +1.19% · range méd 2.41%
- Excursion ouverture 15min (n=160) : bas méd −1.23% (p90 −3.64%) · haut méd +1.58% · range méd 3.34%
- Excursion ouverture 30min (n=160) : bas méd −1.49% (p90 −4.52%) · haut méd +1.87% · range méd 3.89%
- Excursion ouverture 60min (n=160) : bas méd −1.69% (p90 −5.52%) · haut méd +2.1% · range méd 4.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.74 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 81% (131/159) · gap 46% · délai 0.0min · rebond 63% (83/131) (MFE +1.58%)
   - −1.0% : fill 30min 62% · séance 71% (120/159) · gap 39% · délai 0.0min · rebond 68% (77/120) (MFE +1.68%)
   - −1.5% : fill 30min 57% · séance 64% (112/159) · gap 28% · délai 0.0min · rebond 70% (74/112) (MFE +2.06%)
   - −2.0% : fill 30min 51% · séance 58% (103/159) · gap 23% · délai 0.2min · rebond 69% (69/103) (MFE +2.18%)
   - −3.0% : fill 30min 35% · séance 49% (90/159) · gap 9% · délai 5.4min · rebond 67% (64/90) (MFE +1.88%)
   - −4.0% : fill 30min 26% · séance 39% (69/159) · gap 6% · délai 14.7min · rebond 74% (51/69) (MFE +2.24%)
   - −5.0% : fill 30min 12% · séance 28% (56/159) · gap 1% · délai 32.8min · rebond 57% (37/56) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −1.97%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.67% (p90 −2.32%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.69% (p90 −2.44%) → stop au-delà de −1.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1085 jambes) : jambe baissière méd −1.28% (p90 −3.02%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 92% (80/84) · rebond 65% (48/80)
      · −2.0% : fill 82% (74/84) · rebond 68% (48/74)
      · −3.0% : fill 70% (67/84) · rebond 62% (45/67)
      · −4.0% : fill 60% (53/84) · rebond 70% (38/53)
      · −5.0% : fill 43% (44/84) · rebond 51% (27/44)
   - **flat** (15 séances) :
      · −1.0% : fill 81% (13/15) · rebond 97% (12/13)
      · −2.0% : fill 56% (10/15) · rebond 90% (9/10)
      · −3.0% : fill 28% (5/15) · rebond 92% (4/5)
      · −4.0% : fill 18% (4/15) · rebond 87% (3/4)
      · −5.0% : fill 11% (3/15) · rebond 100% (3/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 41% (27/60) · rebond 59% (17/27)
      · −2.0% : fill 28% (19/60) · rebond 63% (12/19)
      · −3.0% : fill 27% (18/60) · rebond 78% (15/18)
      · −4.0% : fill 17% (12/60) · rebond 91% (10/12)
      · −5.0% : fill 12% (9/60) · rebond 78% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 72% si les 15 1res min sont vertes (86 cas) · 23% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:29** → P(séance verte=clôture>ouverture) 92% si début vert vs 10% si rouge (base 50% · écart 82 pts) ; prédictivité sature ensuite (plafond brut 94min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **92%** · continue >prix actuel 51% ; creux résiduel méd -1.44% (q20 -2.36%) → **SL/trailing à −2.36%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.85% / q75 +3.48% → **scale +1.85% / runner +3.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **10%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.43%** (au-delà de la MAE q10 -4.43%), cible rebond +1.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.16% .. +4.44%] · haut q95 +5.81% · bas q05 -6.28%
   - 60min (n=160) : retour [-6.17% .. +6.01%] · haut q95 +6.56% · bas q05 -7.01%
   - 2h (n=160) : retour [-6.84% .. +5.99%] · haut q95 +6.83% · bas q05 -7.37%
   - 4h (n=160) : retour [-6.61% .. +6.27%] · haut q95 +8.29% · bas q05 -7.81%
   - 6h (n=160) : retour [-7.14% .. +7.33%] · haut q95 +9.18% · bas q05 -8.5%
   - session (n=160) : retour [-7.1% .. +7.23%] · haut q95 +9.21% · bas q05 -8.57%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 10% vs absente 4% (base 6%)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.8  _(momentum haussier)_
- **ADX** : 10.7  _(pas de tendance nette)_
- **MACD** : hist 0.067  _(pas de croisement recent)_
- **BB** : %B 0.53 · largeur 14.9%
- **ATR** : 0.94 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.152  _(distribution)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 52.8  _(transition)_
- **MA** : MA20 15.66 · MA50 16.13 · MA200 18.42  _(prix > MA20)_
- **Dist MA** : MA20 +0.4% · MA50 -2.5% · MA200 -14.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (854004 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
