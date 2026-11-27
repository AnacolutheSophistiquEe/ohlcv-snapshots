# RGTI

**Generated** : 2026-11-27T01:27:47.880963+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 8.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $7.85  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 1/125 fenêtres (p_fill pondéré 0 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $7.85 (+16.6% vs entrée) · entrée $6.73 · stop $6.39 · T1 $7.29 · R/R 1.65  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-25 : 7.85 · ATR Wilder 1.01 (12.88 %)_
- **Swing** : plage **6.6 → 6.03** (-15.96 % a -23.15 % sous la cloture, 0.56 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 5.44 (-9.75 % sous le bas ; sous le support 5.95-5.95 (- 0,5 ATR)).
- **Deep** : plage **6.03 → 4.67** (-23.15 % a -40.49 % sous la cloture, 1.35 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 5.95-5.95 (C). stop INDICATIF 3.66 (-21.64 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.32 ATR sous le plus haut 20 s., RSI(2) 54.9. Limite **7.34** (seance suivante), stop catastrophe 3.3, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 6.86-7.03 (B, -10.51 %) ; 5.95-5.95 (C, -24.2 %) ; 1.73-2.21 (B, -71.85 %) ; 1.22-1.53 (A, -80.51 %) ; 0.66-1.15 (A, -85.35 %)
- Resistances reelles au-dessus : 8.35-8.45 (B, 6.37 %) ; 8.92-9.19 (A, 13.63 %) ; 9.5-9.74 (B, 21.02 %) ; 10.05-10.31 (A, 28.03 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.25 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (37.15 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1254).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 37.15 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.186 % | p01 -8.97 % | pire -31.213 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.28** [0.2172 ; 0.3501] _(largeur 13.3 pt, n_eff 173.1)_
   - swing : **0.3697** [0.3201 ; 0.4215] _(largeur 10.1 pt, n_eff 345.7)_
   - deep : **0.3262** [0.2784 ; 0.3769] _(largeur 9.9 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.71 %** | CVaR **-10.76 %** | vol 6.69 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 14.15 % contre 5.57 % aujourd'hui, rapport 2.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -22.63 % vs -22.48 % si l'on extrapolait par √5 _(rapport 1.007 ; < 1 = le √5 surestime)_
- **β de baisse : 1.897** (β de hausse 2.0844, asymétrie 0.9101) vs IWM — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.336× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 7.0087 sur atr_grid (0.75 ATR, 10.717 %) — p(stop avant cible) 0.6205 [0.57 ; 0.67], R/R 5.125, perte reelle 10.87 % (gap inclus), CVaR 12.577 %, EV -1.8106 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0239 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 3.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.621, borne haute 0.670 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 12.58 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 21.434 %) — p(stop avant cible) 0.2213 [0.18 ; 0.27], R/R 2.568, perte reelle 21.696 % (gap inclus), EV -1.4511 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.45 %) : P(cible) 4.1 % x 55.71 % + P(rien) 73.8 % x 1.47 % ne couvrent pas P(stop) 22.1 % x 21.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 3.572 %) — p(stop avant cible) 0.8545 [0.81 ; 0.89], R/R 15.124, perte reelle 3.684 % (gap inclus), EV -0.1466 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 15.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.855, borne haute 0.889 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 2.3 % x 55.71 % + P(rien) 12.2 % x 13.97 % ne couvrent pas P(stop) 85.5 % x 3.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 7.145 %) — p(stop avant cible) 0.7311 [0.68 ; 0.78], R/R 7.628, perte reelle 7.304 % (gap inclus), EV -0.8292 % — **REFUSE**
      - refuse : cible atteinte seulement 3.5 % du temps (< 15 %) meme a 10 seances : le R/R de 7.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.731, borne haute 0.776 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 3.5 % x 55.71 % + P(rien) 23.4 % x 10.93 % ne couvrent pas P(stop) 73.1 % x 7.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 10.717 %) — p(stop avant cible) 0.6205 [0.57 ; 0.67], R/R 5.125, perte reelle 10.87 % (gap inclus), EV -1.8106 % — **REFUSE**
      - refuse : cible atteinte seulement 3.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.621, borne haute 0.670 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.81 %) : P(cible) 3.6 % x 55.71 % + P(rien) 34.3 % x 8.46 % ne couvrent pas P(stop) 62.1 % x 10.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 14.289 %) — p(stop avant cible) 0.4644 [0.41 ; 0.52], R/R 3.848, perte reelle 14.477 % (gap inclus), EV -1.8125 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.81 %) : P(cible) 3.8 % x 55.71 % + P(rien) 49.7 % x 5.59 % ne couvrent pas P(stop) 46.4 % x 14.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 17.862 %) — p(stop avant cible) 0.3321 [0.28 ; 0.38], R/R 3.077, perte reelle 18.108 % (gap inclus), EV -1.7868 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.79 %) : P(cible) 3.9 % x 55.71 % + P(rien) 62.8 % x 3.23 % ne couvrent pas P(stop) 33.2 % x 18.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 25.006 %) — p(stop avant cible) 0.1286 [0.10 ; 0.17], R/R 2.193, perte reelle 25.408 % (gap inclus), EV -1.3084 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 4.1 % x 55.71 % + P(rien) 83.0 % x -0.39 % ne couvrent pas P(stop) 12.9 % x 25.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 28.579 %) — p(stop avant cible) 0.0757 [0.05 ; 0.11], R/R 1.932, perte reelle 28.831 % (gap inclus), EV -1.1745 % — **REFUSE**
      - refuse : cible atteinte seulement 4.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 4.2 % x 55.71 % + P(rien) 88.3 % x -1.49 % ne couvrent pas P(stop) 7.6 % x 28.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 32.151 %) — p(stop avant cible) 0.0518 [0.03 ; 0.08], R/R 1.717, perte reelle 32.456 % (gap inclus), EV -1.2117 % — **REFUSE**
      - refuse : cible atteinte seulement 4.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 4.2 % x 55.71 % + P(rien) 90.6 % x -2.06 % ne couvrent pas P(stop) 5.2 % x 32.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 35.723 %) — p(stop avant cible) 0.0372 [0.02 ; 0.06], R/R 1.552, perte reelle 35.893 % (gap inclus), EV -1.1781 % — **REFUSE**
      - refuse : cible atteinte seulement 4.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 4.2 % x 55.71 % + P(rien) 92.0 % x -2.40 % ne couvrent pas P(stop) 3.7 % x 35.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 39.296 %) — p(stop avant cible) 0.0284 [0.01 ; 0.05], R/R 1.413, perte reelle 39.435 % (gap inclus), EV -1.2173 % — **REFUSE**
      - refuse : cible atteinte seulement 4.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 4.2 % x 55.71 % + P(rien) 92.9 % x -2.65 % ne couvrent pas P(stop) 2.8 % x 39.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 42.868 %) — p(stop avant cible) 0.0165 [0.01 ; 0.03], R/R 1.3, perte reelle 42.868 % (gap inclus), EV -1.1862 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 4.3 % x 55.71 % + P(rien) 94.0 % x -3.07 % ne couvrent pas P(stop) 1.7 % x 42.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 50.013 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 1.077, perte reelle 51.714 % (gap inclus), EV -1.163 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 4.3 % x 55.71 % + P(rien) 95.3 % x -3.56 % ne couvrent pas P(stop) 0.3 % x 51.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 57.157 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.955, perte reelle 58.359 % (gap inclus), EV -1.1534 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 4.3 % x 55.71 % + P(rien) 95.4 % x -3.57 % ne couvrent pas P(stop) 0.3 % x 58.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 64.302 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.866, perte reelle 64.302 % (gap inclus), EV -1.1529 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 4.3 % x 55.71 % + P(rien) 95.5 % x -3.59 % ne couvrent pas P(stop) 0.2 % x 64.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 71.447 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.78, perte reelle 71.447 % (gap inclus), EV -1.1037 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 4.3 % x 55.71 % + P(rien) 95.7 % x -3.67 % ne couvrent pas P(stop) 0.0 % x 71.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 78.591 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.709, perte reelle 78.591 % (gap inclus), EV -1.1037 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 4.3 % x 55.71 % + P(rien) 95.7 % x -3.67 % ne couvrent pas P(stop) 0.0 % x 78.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 85.736 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.65, perte reelle 85.736 % (gap inclus), EV -1.1037 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 4.3 % x 55.71 % + P(rien) 95.7 % x -3.67 % ne couvrent pas P(stop) 0.0 % x 85.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 92.881 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.6, perte reelle 92.881 % (gap inclus), EV -1.1037 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 4.3 % x 55.71 % + P(rien) 95.7 % x -3.67 % ne couvrent pas P(stop) 0.0 % x 92.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 7.85, ATR14 1.1217 (14.289 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.407 ATR = 5.816 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.714 % | 7.7939 | 92.15 % | 94.36 % | 95.67 % | 97.07 % | 97.56 % | 98.56 % |
| 0.1 ATR | 1.429 % | 7.7378 | 86.32 % | 90.84 % | 92.44 % | 95.05 % | 96.04 % | 97.44 % |
| 0.15 ATR | 2.143 % | 7.6817 | 80.99 % | 87.31 % | 89.11 % | 92.22 % | 94.21 % | 96.1 % |
| 0.2 ATR | 2.858 % | 7.6257 | 73.84 % | 82.48 % | 85.38 % | 88.79 % | 91.57 % | 94.46 % |
| 0.25 ATR | 3.572 % | 7.5696 | 67.91 % | 78.35 % | 81.55 % | 85.76 % | 89.04 % | 92.51 % |
| 0.35 ATR | 5.001 % | 7.4574 | 55.43 % | 68.78 % | 74.09 % | 79.7 % | 84.67 % | 89.64 % |
| 0.5 ATR | 7.145 % | 7.2891 | 41.15 % | 57.4 % | 65.22 % | 72.02 % | 79.49 % | 85.33 % |
| 0.75 ATR | 10.717 % | 7.0087 | 21.63 % | 39.48 % | 50.71 % | 59.6 % | 71.37 % | 79.08 % |
| 1.0 ATR | 14.289 % | 6.7283 | 9.46 % | 24.37 % | 34.17 % | 47.47 % | 62.54 % | 72.62 % |
| 1.25 ATR | 17.862 % | 6.4479 | 4.12 % | 14.8 % | 24.4 % | 38.08 % | 53.3 % | 65.33 % |
| 1.5 ATR | 21.434 % | 6.1674 | 1.91 % | 7.55 % | 14.11 % | 26.36 % | 43.55 % | 57.33 % |
| 2.0 ATR | 28.579 % | 5.6066 | 0.3 % | 1.81 % | 4.54 % | 11.41 % | 25.99 % | 41.33 % |
| 2.5 ATR | 35.723 % | 5.0457 | 0.0 % | 0.3 % | 1.21 % | 4.75 % | 15.33 % | 29.03 % |
| 3.0 ATR | 42.868 % | 4.4849 | 0.0 % | 0.1 % | 0.4 % | 1.62 % | 8.02 % | 17.44 % |
| 4.0 ATR | 57.157 % | 3.3631 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 2.03 % | 5.44 % |
| 6.0 ATR | 85.736 % | 1.1197 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.82 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.78 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.60 ATR | 0.67 ATR | 0.86 ATR | 0.99 ATR | 1.11 ATR | 1.42 ATR | 1.72 ATR |
| **3 s.** | 0.34 ATR | 0.76 ATR | 0.84 ATR | 1.03 ATR | 1.24 ATR | 1.36 ATR | 1.72 ATR | 1.98 ATR |
| **5 s.** | 0.44 ATR | 0.95 ATR | 1.07 ATR | 1.36 ATR | 1.54 ATR | 1.71 ATR | 2.11 ATR | 2.48 ATR |
| **10 s.** | 0.64 ATR | 1.33 ATR | 1.46 ATR | 1.80 ATR | 2.05 ATR | 2.28 ATR | 2.87 ATR | 3.50 ATR |
| **20 s.** | 0.91 ATR | 1.73 ATR | 1.89 ATR | 2.34 ATR | 2.67 ATR | 2.89 ATR | 3.62 ATR | 4.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.46–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (7.145 %, prix 7.2891), p(touche) 41.15 % (en stress 85.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.673–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (10.717 %, prix 7.0087), p(touche) 39.48 % (en stress 92.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.836 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile VIDE (borne basse 1.066 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.463 ATR au-dessus du haut de la grille, 1.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (76.4 % des re-echantillons)
- **20 seance(s)** : plage utile VIDE (borne basse 1.885 ATR au-dessus du haut de la grille, 1.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.4 | bear 11.4 | side 83.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→74% · +2.0%→62% · +3.0%→45% · +5.0%→30% · +8.0%→10%
- Range intraday médian 6.39% (p90 11.03%) · excursion haute méd. +2.64% / basse méd. −2.45%
- Profil de vol intra : ouverture 4.544% vs midi 1.307% vs clôture 1.583% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 21% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. -0.493% ; recovery-V 29%
- **σ réalisé intraday** 3.543% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 69% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 11.4051 (VA 11.2514–11.4461 ; dernier close 11.515)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 64% · **stop −4.84%** sous le fill (sous le bruit) · cible +1.64% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.47% · baisse 58% (gap-down >1% 42% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.72%) · haut méd +1.04% · range méd 2.29%
- Excursion ouverture 15min (n=160) : bas méd −1.23% (p90 −3.5%) · haut méd +1.39% · range méd 3.07%
- Excursion ouverture 30min (n=160) : bas méd −1.46% (p90 −4.21%) · haut méd +1.57% · range méd 3.46%
- Excursion ouverture 60min (n=160) : bas méd −1.69% (p90 −4.91%) · haut méd +1.85% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 11.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 73% · séance 83% (132/159) · gap 49% · délai 0.0min · rebond 56% (80/132) (MFE +1.37%)
   - −1.0% : fill 30min 65% · séance 76% (121/159) · gap 42% · délai 0.0min · rebond 62% (76/121) (MFE +1.41%)
   - −1.5% : fill 30min 60% · séance 68% (112/159) · gap 31% · délai 0.0min · rebond 64% (71/112) (MFE +1.58%)
   - −2.0% : fill 30min 54% · séance 62% (102/159) · gap 28% · délai 0.0min · rebond 64% (65/102) (MFE +1.78%)
   - −3.0% : fill 30min 37% · séance 49% (88/159) · gap 11% · délai 2.6min · rebond 64% (61/88) (MFE +1.71%)
   - −4.0% : fill 30min 26% · séance 39% (67/159) · gap 6% · délai 11.9min · rebond 66% (48/67) (MFE +1.75%)
   - −5.0% : fill 30min 10% · séance 28% (53/159) · gap 1% · délai 37.8min · rebond 64% (35/53) (MFE +1.64%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.3% (p90 −1.69%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.55% (p90 −2.09%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −2.13%) → stop au-delà de −1.42% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1023 jambes) : jambe baissière méd −1.27% (p90 −2.97%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (82 séances) :
      · −1.0% : fill 94% (78/82) · rebond 57% (45/78)
      · −2.0% : fill 87% (72/82) · rebond 62% (44/72)
      · −3.0% : fill 73% (65/82) · rebond 62% (43/65)
      · −4.0% : fill 63% (52/82) · rebond 61% (36/52)
      · −5.0% : fill 45% (42/82) · rebond 60% (26/42)
   - **flat** (16 séances) :
      · −1.0% : fill 86% (14/16) · rebond 83% (12/14)
      · −2.0% : fill 55% (10/16) · rebond 92% (9/10)
      · −3.0% : fill 21% (5/16) · rebond 92% (4/5)
      · −4.0% : fill 14% (4/16) · rebond 87% (3/4)
      · −5.0% : fill 8% (3/16) · rebond 100% (3/3)
   - **gap-up** (61 séances) :
      · −1.0% : fill 47% (29/61) · rebond 65% (19/29)
      · −2.0% : fill 29% (20/61) · rebond 60% (12/20)
      · −3.0% : fill 24% (18/61) · rebond 65% (14/18)
      · −4.0% : fill 13% (11/61) · rebond 91% (9/11)
      · −5.0% : fill 9% (8/61) · rebond 78% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 66% si les 15 1res min sont vertes (83 cas) · 22% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 86% si début vert vs 7% si rouge (base 44% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **86%** · continue >prix actuel 47% ; creux résiduel méd -1.47% (q20 -2.26%) → **SL/trailing à −2.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.76% / q75 +3.11% → **scale +1.76% / runner +3.11%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **7%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.13%** (au-delà de la MAE q10 -4.13%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.99% .. +4.08%] · haut q95 +5.52% · bas q05 -5.26%
   - 60min (n=160) : retour [-5.24% .. +5.35%] · haut q95 +6.4% · bas q05 -6.73%
   - 2h (n=160) : retour [-6.01% .. +6.03%] · haut q95 +6.9% · bas q05 -7.02%
   - 4h (n=160) : retour [-6.03% .. +6.35%] · haut q95 +7.93% · bas q05 -7.32%
   - 6h (n=160) : retour [-6.11% .. +7.73%] · haut q95 +9.19% · bas q05 -7.59%
   - session (n=160) : retour [-6.43% .. +7.31%] · haut q95 +9.61% · bas q05 -7.79%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 6.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 10% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.16% (p75 1.63% / p90 2.44%) · ~5.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 15.0 min, n=48)
   - −1.0% → **87%** (reprise méd 35.0 min, n=29)
   - −1.5% → **86%** (reprise méd 48.4 min, n=17)
   - −2.0% → **90%** (reprise méd 15.0 min, n=9)
   - −3.0% → **66%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.44%** (p90, défaut prudent ; serré/agressif −1.63%) ; extension open→close méd +9.37% (q75 +10.69% / q95 +12.08%), MFE méd +10.33% / q90 +12.7%
   - Échelle scale-out : +10.33% (33%) / +12.07% (33%) / +12.7% (34%)
- **DÉSARMER** : repli > **−2.44%** depuis le plus-haut = décay → P(retournement) **13%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.7% : P(retournement après) 0% (mèche méd None%)
- **CONTEXTE** : la dernière heure tient les gains 76% du temps (retour médian dernière heure +0.7%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.5 · part idiosyncratique 0.5
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.6  _(momentum baissier)_
- **ADX** : 36.1  _(tendance etablie)_
- **MACD** : hist -0.162  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 70.8%
- **ATR** : 1.12 (33.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.327  _(distribution)_
- **Vol ratio** : 1.07  _(volume normal)_
- **Choppiness** : 34.3  _(marche directionnel)_
- **MA** : MA20 9.93 · MA50 12.42 · MA200 16.19  _(prix < MA20)_
- **Dist MA** : MA20 -21.0% · MA50 -36.8% · MA200 -51.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (682201 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
