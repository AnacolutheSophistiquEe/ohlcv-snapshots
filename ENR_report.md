# ENR

**Generated** : 2026-11-25T01:08:08.844701+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €117.55  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)  
> ↳ spot €117.55 (+0.7% vs entrée) · entrée €116.69 · stop €113.24 · T1 €123.57 · R/R 1.99  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-24 : 117.55 · ATR Wilder 7.06 (6.01 %)_
- **Swing** : plage **108.76 → 103.08** (-7.47 % a -12.31 % sous la cloture, 0.8 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 103.21-104.4 (B). stop INDICATIF 95.03 (-7.81 % sous le bas ; sous le support 98.56-100.32 (- 0,5 ATR)).
- **Deep** : plage **103.08 → 91.96** (-12.31 % a -21.77 % sous la cloture, 1.57 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 98.56-100.32 (A) ; 94.0-95.27 (A) ; 89.3-92.68 (A). stop INDICATIF 82.18 (-10.63 % sous le bas ; sous le support 85.71-89.14 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.86 ATR sous le plus haut 20 s., RSI(2) 27.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 109.88-110.92 (A, -5.64 %) ; 103.21-104.4 (B, -11.18 %) ; 98.56-100.32 (A, -14.66 %) ; 94.0-95.27 (A, -18.95 %) ; 89.3-92.68 (A, -21.15 %) ; 85.71-89.14 (A, -24.17 %)
- Resistances reelles au-dessus : 122.83-124.46 (A, 4.49 %) ; 130.89-133.85 (A, 11.35 %) ; 135.1-138.15 (A, 14.93 %) ; 138.68-140.18 (A, 17.98 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.83 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.96 %)** : le gap seul le franchit 0.314 % des séances (4 fois sur 1274).
   - exécution **6.943 pt plus bas** dans le cas TYPIQUE (médiane), 21.921 au p90, **27.797 au pire**
   - perte réelle **18.578 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 7.96 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0333 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.407 % | p01 -5.39 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2418** [0.1826 ; 0.3095] _(largeur 12.7 pt, n_eff 173.1)_
   - swing : **0.344** [0.2954 ; 0.3952] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.3407** [0.2922 ; 0.3918] _(largeur 10.0 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-5.06 %** | CVaR **-7.09 %** | vol 3.33 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 2.15 % contre 3.46 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.02 % vs -10.3 % si l'on extrapolait par √5 _(rapport 0.876 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3116** (β de hausse 1.0694, asymétrie 1.2265) vs GDAXI — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 108.6839 sur grid_snapped (0.89 ATR, 7.542 %) — p(stop avant cible) 0.4545 [0.40 ; 0.51], R/R 4.353, perte reelle 8.158 % (gap inclus), CVaR 12.684 %, EV -1.2219 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0497 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 12.68 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.56 ATR (stop 6.38 %) — p(stop avant cible) 0.5381 [0.49 ; 0.59], R/R 5.234, perte reelle 6.785 % (gap inclus), EV -1.203 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.538, borne haute 0.590 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 0.1 % x 35.52 % + P(rien) 46.1 % x 5.23 % ne couvrent pas P(stop) 53.8 % x 6.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 0.89 ATR (stop 8.443 %) — p(stop avant cible) 0.398 [0.35 ; 0.45], R/R 3.885, perte reelle 9.142 % (gap inclus), EV -1.2578 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.19 % > budget 12.00 %
      - ⚠ support DETECTE a 0.46 ATR du spot — compartiment <1, mesure a 49.2 % de casse (IC clusterise [0.458 ; 0.523] sur 1200 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 0.1 % x 35.52 % + P(rien) 60.1 % x 3.90 % ne couvrent pas P(stop) 39.8 % x 9.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.585 %) — p(stop avant cible) 0.8812 [0.84 ; 0.91], R/R 21.593, perte reelle 1.645 % (gap inclus), EV -0.3283 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 21.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.881, borne haute 0.912 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.0 % x 35.52 % + P(rien) 11.8 % x 9.35 % ne couvrent pas P(stop) 88.1 % x 1.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+35.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.56 ATR (stop 5.479 %) — p(stop avant cible) 0.6058 [0.55 ; 0.66], R/R 6.196, perte reelle 5.732 % (gap inclus), EV -1.0672 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.606, borne haute 0.656 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 0.1 % x 35.52 % + P(rien) 39.3 % x 6.02 % ne couvrent pas P(stop) 60.6 % x 5.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.89 ATR (stop 7.542 %) — p(stop avant cible) 0.4545 [0.40 ; 0.51], R/R 4.353, perte reelle 8.158 % (gap inclus), EV -1.2219 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 0.1 % x 35.52 % + P(rien) 54.4 % x 4.49 % ne couvrent pas P(stop) 45.5 % x 8.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.5 ATR (stop 9.511 %) — p(stop avant cible) 0.3498 [0.30 ; 0.40], R/R 3.507, perte reelle 10.128 % (gap inclus), EV -1.221 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 0.1 % x 35.52 % + P(rien) 64.9 % x 3.52 % ne couvrent pas P(stop) 35.0 % x 10.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 11.096 %) — p(stop avant cible) 0.246 [0.20 ; 0.29], R/R 3.021, perte reelle 11.757 % (gap inclus), EV -0.9215 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 0.1 % x 35.52 % + P(rien) 75.3 % x 2.57 % ne couvrent pas P(stop) 24.6 % x 11.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 12.682 %) — p(stop avant cible) 0.1731 [0.14 ; 0.22], R/R 2.689, perte reelle 13.208 % (gap inclus), EV -0.5278 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.1 % x 35.52 % + P(rien) 82.6 % x 2.08 % ne couvrent pas P(stop) 17.3 % x 13.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 14.267 %) — p(stop avant cible) 0.1057 [0.08 ; 0.14], R/R 2.377, perte reelle 14.942 % (gap inclus), EV -0.157 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.1 % x 35.52 % + P(rien) 89.3 % x 1.55 % ne couvrent pas P(stop) 10.6 % x 14.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 15.852 %) — p(stop avant cible) 0.053 [0.03 ; 0.08], R/R 2.118, perte reelle 16.768 % (gap inclus), EV 0.1538 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.82 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 17.437 %) — p(stop avant cible) 0.0392 [0.02 ; 0.06], R/R 1.957, perte reelle 18.15 % (gap inclus), EV 0.2592 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.15 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 19.022 %) — p(stop avant cible) 0.0288 [0.01 ; 0.05], R/R 1.802, perte reelle 19.706 % (gap inclus), EV 0.2988 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.80 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 22.193 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 1.42, perte reelle 25.008 % (gap inclus), EV 0.3883 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.81 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 25.363 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.268, perte reelle 28.009 % (gap inclus), EV 0.4438 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.35 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 28.533 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 1.197, perte reelle 29.669 % (gap inclus), EV 0.4498 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.26 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 31.704 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 1.076, perte reelle 33.019 % (gap inclus), EV 0.4686 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.89 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 34.874 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 1.009, perte reelle 35.214 % (gap inclus), EV 0.4664 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.94 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 38.045 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.933, perte reelle 38.045 % (gap inclus), EV 0.4669 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.96 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 41.215 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.862, perte reelle 41.215 % (gap inclus), EV 0.4672 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.90 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 44.385 %) — p(stop avant cible) 0.0003 [0.00 ; 0.01], R/R 0.8, perte reelle 44.385 % (gap inclus), EV 0.4702 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.82 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 47.556 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.747, perte reelle 47.556 % (gap inclus), EV 0.475 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.77 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 50.726 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.7, perte reelle 50.726 % (gap inclus), EV 0.475 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.77 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 117.55, ATR14 7.4536 (6.341 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 2.327 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.317 % | 117.1773 | 91.52 % | 94.27 % | 95.85 % | 96.44 % | 97.51 % | 98.19 % |
| 0.1 ATR | 0.634 % | 116.8046 | 83.83 % | 88.45 % | 90.91 % | 92.97 % | 95.02 % | 96.08 % |
| 0.15 ATR | 0.951 % | 116.432 | 76.43 % | 82.63 % | 86.26 % | 89.01 % | 91.74 % | 93.87 % |
| 0.2 ATR | 1.268 % | 116.0593 | 70.41 % | 79.27 % | 83.2 % | 86.93 % | 89.95 % | 92.56 % |
| 0.25 ATR | 1.585 % | 115.6866 | 63.51 % | 74.83 % | 79.45 % | 83.66 % | 87.96 % | 91.26 % |
| 0.35 ATR | 2.219 % | 114.9413 | 51.78 % | 65.15 % | 70.65 % | 76.34 % | 82.79 % | 87.44 % |
| 0.5 ATR | 3.17 % | 113.8232 | 36.39 % | 52.02 % | 59.98 % | 67.33 % | 75.52 % | 81.71 % |
| 0.75 ATR | 4.756 % | 111.9598 | 19.72 % | 35.93 % | 45.65 % | 55.15 % | 66.57 % | 75.08 % |
| 1.0 ATR | 6.341 % | 110.0964 | 11.24 % | 26.16 % | 35.28 % | 45.45 % | 58.71 % | 67.84 % |
| 1.25 ATR | 7.926 % | 108.233 | 6.21 % | 17.57 % | 25.69 % | 36.63 % | 50.15 % | 60.4 % |
| 1.5 ATR | 9.511 % | 106.3696 | 2.96 % | 11.45 % | 18.58 % | 28.91 % | 42.99 % | 54.07 % |
| 2.0 ATR | 12.682 % | 102.6429 | 0.79 % | 4.34 % | 9.19 % | 17.33 % | 29.95 % | 42.81 % |
| 2.5 ATR | 15.852 % | 98.9161 | 0.3 % | 2.07 % | 4.25 % | 10.2 % | 20.8 % | 32.86 % |
| 3.0 ATR | 19.022 % | 95.1893 | 0.1 % | 0.89 % | 2.08 % | 5.35 % | 13.43 % | 24.92 % |
| 4.0 ATR | 25.363 % | 87.7357 | 0.1 % | 0.39 % | 1.19 % | 2.48 % | 7.06 % | 14.17 % |
| 6.0 ATR | 38.045 % | 72.8286 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.93 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.34 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.03 ATR | 1.18 ATR | 1.60 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.77 ATR | 1.06 ATR | 1.27 ATR | 1.45 ATR | 1.96 ATR | 2.42 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 1.01 ATR | 1.37 ATR | 1.67 ATR | 1.89 ATR | 2.52 ATR | 3.12 ATR |
| **10 s.** | 0.52 ATR | 1.25 ATR | 1.43 ATR | 1.88 ATR | 2.27 ATR | 2.55 ATR | 3.54 ATR | 4.85 ATR |
| **20 s.** | 0.75 ATR | 1.68 ATR | 1.90 ATR | 2.49 ATR | 3.00 ATR | 3.46 ATR | 5.01 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.416 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.609–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.756 %, prix 111.9593), p(touche) 35.93 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.766–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.341 %, prix 110.0962), p(touche) 35.28 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (86.1 % des re-echantillons)
- **5 seance(s)** : plage utile 1.013–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.926 %, prix 108.233), p(touche) 36.63 % (en stress 96.04 %)  ✅ optimum identifie (90.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.43–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.511 %, prix 106.3698), p(touche) 42.99 % (en stress 100.0 %)  ✅ optimum identifie (93.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.903–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.682 %, prix 102.6423), p(touche) 42.81 % (en stress 99.0 %)  ✅ optimum identifie (89.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 23.4 | bear 71.5 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.74% → cible +5.904% / stop −2.952%, p_fill 79%, n_eff≈83.0) : P(cible|rempli) **2%** · **EV/risk -0.177** (×p_fill ; si rempli -0.66% du capital)
  - **swing** (entrée dip −1.619% → cible +6.855% / stop −6.445%, p_fill 71%, n_eff≈83.4) : P(cible|rempli) **15%** · **EV/risk -0.168** (×p_fill ; si rempli -1.52% du capital)
  - **deep** (entrée dip −2.499% → cible +18.358% / stop −9.755%, p_fill 72%, n_eff≈82.9) : P(cible|rempli) **2%** · **EV/risk -0.167** (×p_fill ; si rempli -2.25% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→34% · +3.0%→15% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.62% (p90 6.06%) · excursion haute méd. +1.37% / basse méd. −1.89%
- Profil de vol intra : ouverture 1.961% vs midi 0.824% vs clôture 1.048% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 61% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. -0.864% ; recovery-V 25%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 83% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 121.5065 (VA 120.2185–123.5995 ; dernier close 118.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 18% · rebond 57% · **stop −4.86%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.22 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 38% (gap-down >1% 20% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.49% (p90 −1.69%) · haut méd +0.49% · range méd 1.14%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.05%) · haut méd +0.58% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.19%) · haut méd +0.62% · range méd 1.69%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.35%) · haut méd +0.68% · range méd 1.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 118.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 70% (115/159) · gap 30% · délai 0.2min · rebond 48% (59/115) (MFE +0.88%)
   - −1.0% : fill 30min 40% · séance 66% (107/159) · gap 20% · délai 8.6min · rebond 51% (59/107) (MFE +1.04%)
   - −1.5% : fill 30min 29% · séance 53% (88/159) · gap 13% · délai 12.6min · rebond 55% (48/88) (MFE +1.28%)
   - −2.0% : fill 30min 23% · séance 44% (73/159) · gap 9% · délai 20.7min · rebond 50% (41/73) (MFE +1.0%)
   - −3.0% : fill 30min 10% · séance 29% (48/159) · gap 3% · délai 251.6min · rebond 40% (24/48) (MFE +0.66%)
   - −4.0% : fill 30min 6% · séance 18% (32/159) · gap 2% · délai 200.1min · rebond 57% (20/32) (MFE +1.05%)
   - −5.0% : fill 30min 4% · séance 13% (24/159) · gap 0% · délai 397.7min · rebond 38% (11/24) (MFE +0.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.17%) → stop au-delà de −1.55% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.63%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.66%) → stop au-delà de −0.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=526 jambes) : jambe baissière méd −1.04% (p90 −2.31%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (53/54) · rebond 41% (26/53)
      · −2.0% : fill 84% (41/54) · rebond 49% (20/41)
      · −3.0% : fill 59% (30/54) · rebond 40% (14/30)
      · −4.0% : fill 39% (22/54) · rebond 75% (16/22)
      · −5.0% : fill 30% (18/54) · rebond 47% (10/18)
   - **flat** (18 séances) :
      · −1.0% : fill 59% (13/18) · rebond 64% (9/13)
      · −2.0% : fill 33% (8/18) · rebond 68% (6/8)
      · −3.0% : fill 20% (5/18) · rebond 48% (3/5)
      · −4.0% : fill 6% (3/18) · rebond 59% (2/3)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 46% (41/87) · rebond 61% (24/41)
      · −2.0% : fill 23% (24/87) · rebond 46% (15/24)
      · −3.0% : fill 13% (13/87) · rebond 36% (7/13)
      · −4.0% : fill 9% (7/87) · rebond 11% (2/7)
      · −5.0% : fill 5% (4/87) · rebond 12% (1/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 61% si les 15 1res min sont vertes (71 cas) · 30% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 43% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **72%** · continue >prix actuel 56% ; creux résiduel méd -1.18% (q20 -2.25%) → **SL/trailing à −2.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.1% → **scale +1.08% / runner +2.1%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **21%** (continue à baisser 57%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.96%** (au-delà de la MAE q10 -4.96%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.97% .. +1.62%] · haut q95 +2.08% · bas q05 -2.65%
   - 60min (n=160) : retour [-2.5% .. +1.42%] · haut q95 +2.41% · bas q05 -3.07%
   - 2h (n=160) : retour [-2.53% .. +2.22%] · haut q95 +2.56% · bas q05 -3.58%
   - 4h (n=160) : retour [-2.61% .. +2.42%] · haut q95 +3.02% · bas q05 -4.04%
   - 6h (n=160) : retour [-3.22% .. +3.06%] · haut q95 +3.68% · bas q05 -4.31%
   - session (n=160) : retour [-5.78% .. +2.83%] · haut q95 +4.66% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.37%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.57 · part idiosyncratique 0.43
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.6  _(neutre)_
- **ADX** : 16.7  _(pas de tendance nette)_
- **MACD** : hist -0.074  _(bearish_recent)_
- **BB** : %B 0.17 · largeur 19.8%
- **ATR** : 7.45 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.133  _(distribution)_
- **Vol ratio** : 0.43  _(volume atone)_
- **Choppiness** : 55.4  _(transition)_
- **MA** : MA20 125.89 · MA50 133.58 · MA200 152.41  _(prix < MA20)_
- **Dist MA** : MA20 -6.6% · MA50 -12.0% · MA200 -22.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (517705 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
