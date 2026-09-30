# ENR

**Generated** : 2026-09-30T00:10:57.703960+00:00  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €145.54  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €145.54 (+0.4% vs entrée) · entrée €144.92 · stop €142.74 · T1 €147.11 · R/R 1.0  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €144.48–€145.36 (mid €144.92)
- Spot actuel : €145.54 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : €142.74 (plancher anti-bruit 5 s — stop EV-optimal −1.5% (first-passage 5 s réel) ; -1.50 % depuis l'entree)
- Targets : T1 €147.11 · R/R 1.0 | T2 €149.31 · R/R 2.01 | T3 €151.50 · R/R 3.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €142.74


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.59 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.48 %)** : le gap seul le franchit 1.413 % des séances (18 fois sur 1274).
   - exécution **1.375 pt plus bas** dans le cas TYPIQUE (médiane), 9.916 au p90, **31.277 au pire**
   - perte réelle **8.475 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 4.48 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0564 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
- Chocs d'ouverture : p05 -2.33 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4956** [0.4217 ; 0.5696] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4944** [0.4419 ; 0.547] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4858** [0.4334 ; 0.5384] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 89.4 observations effectives », dont la borne haute a 95 % vaut environ 3.4 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 93.6 observations effectives », dont la borne haute a 95 % vaut environ 3.2 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.63 %** | CVaR **-6.59 %** | vol 3.19 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.95 % contre 3.02 % aujourd'hui, rapport 1.97)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3566** (β de hausse 1.0895, asymétrie 1.2452) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.34× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 132.6686 sur atr_grid (2.5 ATR, 8.844 %) — p(stop avant cible) 0.3297 [0.28 ; 0.38], R/R 3.178, perte reelle 9.122 % (gap inclus), CVaR 10.679 %, EV -0.3201 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9647 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.58 ATR (stop 4.121 %) — p(stop avant cible) 0.6579 [0.61 ; 0.71], R/R 6.831, perte reelle 4.244 % (gap inclus), EV -0.1655 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.658, borne haute 0.706 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.5 % x 28.99 % + P(rien) 33.7 % x 7.34 % ne couvrent pas P(stop) 65.8 % x 4.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 5.306 %) — p(stop avant cible) 0.6013 [0.55 ; 0.65], R/R 5.264, perte reelle 5.508 % (gap inclus), EV -0.5386 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.601, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.5 % x 28.99 % + P(rien) 39.3 % x 6.66 % ne couvrent pas P(stop) 60.1 % x 5.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 2.97 ATR (stop 12.564 %) — p(stop avant cible) 0.1276 [0.10 ; 0.17], R/R 2.186, perte reelle 13.263 % (gap inclus), EV 0.3947 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.35 % > budget 12.00 %
   - 🔴 support a 6.89 ATR (stop 26.423 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 1.02, perte reelle 28.411 % (gap inclus), EV 1.1316 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.65 % > budget 12.00 %
      - ⚠ support DETECTE a 0.48 ATR du spot — compartiment <1, mesure a 49.1 % de casse (IC clusterise [0.457 ; 0.522] sur 1123 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 10.01 ATR (stop 37.472 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.774, perte reelle 37.472 % (gap inclus), EV 1.1603 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.10 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.884 %) — p(stop avant cible) 0.9366 [0.91 ; 0.96], R/R 31.03, perte reelle 0.934 % (gap inclus), EV -0.1923 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 31.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.937, borne haute 0.959 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.1 % x 28.99 % + P(rien) 6.2 % x 10.37 % ne couvrent pas P(stop) 93.7 % x 0.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.58 ATR (stop 3.124 %) — p(stop avant cible) 0.7498 [0.70 ; 0.79], R/R 8.907, perte reelle 3.255 % (gap inclus), EV -0.2142 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 8.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.750, borne haute 0.793 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.4 % x 28.99 % + P(rien) 24.6 % x 8.54 % ne couvrent pas P(stop) 75.0 % x 3.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 6.191 %) — p(stop avant cible) 0.532 [0.48 ; 0.58], R/R 4.54, perte reelle 6.385 % (gap inclus), EV -0.5467 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.532, borne haute 0.584 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 0.5 % x 28.99 % + P(rien) 46.3 % x 5.83 % ne couvrent pas P(stop) 53.2 % x 6.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 7.075 %) — p(stop avant cible) 0.4718 [0.42 ; 0.52], R/R 3.971, perte reelle 7.3 % (gap inclus), EV -0.5847 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 0.5 % x 28.99 % + P(rien) 52.3 % x 5.17 % ne couvrent pas P(stop) 47.2 % x 7.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 7.96 %) — p(stop avant cible) 0.3999 [0.35 ; 0.45], R/R 3.534, perte reelle 8.205 % (gap inclus), EV -0.3835 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 0.5 % x 28.99 % + P(rien) 59.5 % x 4.61 % ne couvrent pas P(stop) 40.0 % x 8.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 8.844 %) — p(stop avant cible) 0.3297 [0.28 ; 0.38], R/R 3.178, perte reelle 9.122 % (gap inclus), EV -0.3201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.5 % x 28.99 % + P(rien) 66.5 % x 3.81 % ne couvrent pas P(stop) 33.0 % x 9.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 2.97 ATR (stop 11.567 %) — p(stop avant cible) 0.1685 [0.13 ; 0.21], R/R 2.4, perte reelle 12.079 % (gap inclus), EV 0.1577 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.29 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 14.15 %) — p(stop avant cible) 0.0741 [0.05 ; 0.11], R/R 1.881, perte reelle 15.412 % (gap inclus), EV 0.6997 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.02 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 15.919 %) — p(stop avant cible) 0.0404 [0.02 ; 0.07], R/R 1.666, perte reelle 17.399 % (gap inclus), EV 0.9002 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.47 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.688 %) — p(stop avant cible) 0.0291 [0.02 ; 0.05], R/R 1.543, perte reelle 18.788 % (gap inclus), EV 0.9584 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.07 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.457 %) — p(stop avant cible) 0.0203 [0.01 ; 0.04], R/R 1.411, perte reelle 20.553 % (gap inclus), EV 1.0116 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.51 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.225 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 1.177, perte reelle 24.622 % (gap inclus), EV 1.0641 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.15 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 22.994 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 1.102, perte reelle 26.301 % (gap inclus), EV 1.0974 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.90 % > budget 12.00 %
   - 🔴 grid_snapped a 6.89 ATR (stop 25.425 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 1.034, perte reelle 28.032 % (gap inclus), EV 1.1331 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.62 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 28.301 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.981, perte reelle 29.563 % (gap inclus), EV 1.1403 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.49 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 145.54, ATR14 5.1486 (3.538 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.298 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.177 % | 145.2826 | 91.52 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.354 % | 145.0251 | 83.83 % | 88.15 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.531 % | 144.7677 | 76.33 % | 82.33 % | 85.87 % | 88.51 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.708 % | 144.5103 | 70.41 % | 79.07 % | 83.0 % | 86.34 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.884 % | 144.2529 | 63.91 % | 74.73 % | 79.35 % | 83.17 % | 87.36 % | 90.45 % |
| 0.35 ATR | 1.238 % | 143.738 | 51.78 % | 64.86 % | 70.36 % | 75.74 % | 81.99 % | 86.33 % |
| 0.5 ATR | 1.769 % | 142.9657 | 36.39 % | 51.73 % | 59.49 % | 66.24 % | 74.33 % | 80.2 % |
| 0.75 ATR | 2.653 % | 141.6786 | 19.63 % | 35.83 % | 45.16 % | 54.26 % | 65.27 % | 73.27 % |
| 1.0 ATR | 3.538 % | 140.3914 | 11.05 % | 25.47 % | 34.19 % | 43.86 % | 56.62 % | 64.92 % |
| 1.25 ATR | 4.422 % | 139.1043 | 6.11 % | 17.28 % | 24.9 % | 35.54 % | 48.16 % | 57.29 % |
| 1.5 ATR | 5.306 % | 137.8171 | 2.76 % | 11.06 % | 17.79 % | 27.72 % | 40.9 % | 50.95 % |
| 2.0 ATR | 7.075 % | 135.2429 | 0.79 % | 3.95 % | 8.6 % | 16.24 % | 28.06 % | 39.8 % |
| 2.5 ATR | 8.844 % | 132.6686 | 0.3 % | 1.97 % | 3.95 % | 9.41 % | 19.4 % | 30.15 % |
| 3.0 ATR | 10.613 % | 130.0943 | 0.1 % | 0.79 % | 1.88 % | 4.85 % | 12.34 % | 22.41 % |
| 4.0 ATR | 14.15 % | 124.9457 | 0.1 % | 0.39 % | 1.09 % | 2.28 % | 6.27 % | 12.46 % |
| 6.0 ATR | 21.225 % | 114.6486 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 1.05 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.01 ATR | 1.17 ATR | 1.57 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.75 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.92 ATR | 2.39 ATR |
| **5 s.** | 0.36 ATR | 0.85 ATR | 0.97 ATR | 1.33 ATR | 1.62 ATR | 1.84 ATR | 2.46 ATR | 2.98 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.18 ATR | 2.46 ATR | 3.39 ATR | 4.62 ATR |
| **20 s.** | 0.69 ATR | 1.54 ATR | 1.77 ATR | 2.35 ATR | 2.83 ATR | 3.24 ATR | 4.69 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.606–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.653 %, prix 141.6788), p(touche) 35.83 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.754–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.538 %, prix 140.3908), p(touche) 34.19 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (84.8 % des re-echantillons)
- **5 seance(s)** : plage utile 0.973–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.538 %, prix 140.3908), p(touche) 43.86 % (en stress 99.01 %)  ✅ optimum identifie (90.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.359–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.306 %, prix 137.8176), p(touche) 40.9 % (en stress 100.0 %)  ✅ optimum identifie (92.2 % des re-echantillons)
- **20 seance(s)** : plage utile 1.767–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.075 %, prix 135.243), p(touche) 39.8 % (en stress 99.0 %)  ✅ optimum identifie (88.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.074 | EV/share : €-0.161 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 21 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.7 | bear 5.0 | side 11.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.426% → cible +1.514% / stop −1.5%, p_fill 87%, n_eff≈92.5) : P(cible|rempli) **39%** · **EV/risk -0.147** (×p_fill ; si rempli -0.25% du capital)
  - **swing** (entrée dip −0.943% → cible +3.384% / stop −3.571%, p_fill 77%, n_eff≈89.4) : P(cible|rempli) **30%** · **EV/risk -0.334** (×p_fill ; si rempli -1.55% du capital)
  - **deep** (entrée dip −1.454% → cible +4.786% / stop −5.385%, p_fill 84%, n_eff≈93.6) : P(cible|rempli) **41%** · **EV/risk -0.215** (×p_fill ; si rempli -1.38% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→77% · +1.0%→63% · +2.0%→43% · +3.0%→22% · +5.0%→7% · +8.0%→2%
- Range intraday médian 4.0% (p90 6.11%) · excursion haute méd. +1.59% / basse méd. −1.81%
- Profil de vol intra : ouverture 2.101% vs midi 0.955% vs clôture 1.127% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑1%/↓0% ; spike-down 57% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; neutre — autocorr -0.021)_ ; drift intra méd. -0.473% ; recovery-V 14%
- **σ réalisé intraday** 2.433% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 69% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 147.6975 (VA 146.6265–147.9355 ; dernier close 146.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 18% · rebond 64% · **stop −3.24%** sous le fill (sous le bruit) · cible +1.21% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 32% (gap-down >1% 18% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.62% (p90 −1.67%) · haut méd +0.43% · range méd 1.16%
- Excursion ouverture 15min (n=160) : bas méd −0.8% (p90 −2.21%) · haut méd +0.59% · range méd 1.57%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.28%) · haut méd +0.64% · range méd 1.93%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.61%) · haut méd +0.74% · range méd 2.02%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 146.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 72% (114/159) · gap 24% · délai 0.4min · rebond 59% (63/114) (MFE +1.19%)
   - −1.0% : fill 30min 45% · séance 67% (105/159) · gap 18% · délai 7.0min · rebond 62% (62/105) (MFE +1.52%)
   - −1.5% : fill 30min 30% · séance 52% (86/159) · gap 14% · délai 10.2min · rebond 61% (50/86) (MFE +1.52%)
   - −2.0% : fill 30min 20% · séance 42% (72/159) · gap 9% · délai 45.6min · rebond 63% (47/72) (MFE +1.46%)
   - −3.0% : fill 30min 10% · séance 27% (49/159) · gap 3% · délai 213.6min · rebond 51% (30/49) (MFE +1.01%)
   - −4.0% : fill 30min 6% · séance 18% (35/159) · gap 1% · délai 115.2min · rebond 64% (24/35) (MFE +1.21%)
   - −5.0% : fill 30min 2% · séance 14% (25/159) · gap 0% · délai 398.2min · rebond 36% (13/25) (MFE +0.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.58%) → stop au-delà de −1.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −1.6%) → stop au-delà de −0.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −0.98%) → stop au-delà de −0.75% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=542 jambes) : jambe baissière méd −1.09% (p90 −2.59%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 98% (48/49) · rebond 57% (26/48)
      · −2.0% : fill 72% (36/49) · rebond 46% (20/36)
      · −3.0% : fill 58% (28/49) · rebond 37% (15/28)
      · −4.0% : fill 47% (23/49) · rebond 69% (17/23)
      · −5.0% : fill 37% (18/49) · rebond 40% (11/18)
   - **flat** (15 séances) :
      · −1.0% : fill 85% (13/15) · rebond 91% (11/13)
      · −2.0% : fill 51% (8/15) · rebond 88% (6/8)
      · −3.0% : fill 25% (5/15) · rebond 76% (3/5)
      · −4.0% : fill 14% (4/15) · rebond 52% (2/4)
      · −5.0% : fill 11% (3/15) · rebond 0% (0/3)
   - **gap-up** (95 séances) :
      · −1.0% : fill 48% (44/95) · rebond 57% (25/44)
      · −2.0% : fill 25% (28/95) · rebond 76% (21/28)
      · −3.0% : fill 12% (16/95) · rebond 74% (12/16)
      · −4.0% : fill 5% (8/95) · rebond 50% (5/8)
      · −5.0% : fill 3% (4/95) · rebond 40% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 75% si les 15 1res min sont vertes (73 cas) · 20% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:26** → P(séance verte=clôture>ouverture) 76% si début vert vs 20% si rouge (base 44% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **76%** · continue >prix actuel 56% ; creux résiduel méd -1.13% (q20 -2.17%) → **SL/trailing à −2.17%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.25% → **scale +1.46% / runner +2.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.96%** (au-delà de la MAE q10 -3.96%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.05% .. +1.96%] · haut q95 +2.66% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.48% .. +2.32%] · haut q95 +2.68% · bas q05 -2.96%
   - 2h (n=160) : retour [-2.79% .. +2.64%] · haut q95 +2.91% · bas q05 -3.6%
   - 4h (n=160) : retour [-3.16% .. +2.62%] · haut q95 +3.69% · bas q05 -3.98%
   - 6h (n=160) : retour [-3.7% .. +3.24%] · haut q95 +4.12% · bas q05 -4.58%
   - session (n=160) : retour [-4.9% .. +3.89%] · haut q95 +5.14% · bas q05 -6.19%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 1.3% / strong 3.7%) · base = 8 séances trend-up (n_eff 5.9)
- **ARMER** : fenêtre la + prédictive = **20 min** → P(reste trend-up à la clôture) **11%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.82% (p75 1.18% / p90 1.45%) · ~3.0 replis/séance, durée méd 71.64 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 40.0 min, n=23)
   - −1.0% → **100%** (reprise méd 84.77 min, n=8)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.18%) ; extension open→close méd +4.6% (q75 +6.8% / q95 +8.61%), MFE méd +5.37% / q90 +9.14%
   - Échelle scale-out : +5.37% (33%) / +7.17% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.34%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.58 · part idiosyncratique 0.42
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.4  _(neutre)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist 0.742  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 12.3%
- **ATR** : 5.15 (29.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.145  _(distribution)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 55.2  _(transition)_
- **MA** : MA20 142.56 · MA50 147.73 · MA200 152.89  _(prix > MA20)_
- **Dist MA** : MA20 +2.1% · MA50 -1.5% · MA200 -4.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (846398 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
