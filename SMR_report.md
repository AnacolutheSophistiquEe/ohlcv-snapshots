# SMR

**Generated** : 2026-11-25T01:29:21.155111+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $3.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)  
> ↳ spot $3.30 (+17.0% vs entrée) · entrée $2.82 · stop $2.68 · T1 $3.06 · R/R 1.71  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +13.3 % ≠ (strike 4.0 − spot 3.30)/spot = +21.2 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-24 : 3.3 · ATR Wilder 0.4558 (13.81 %)_
- **Swing** : plage **2.76 → 2.45** (-16.51 % a -25.67 % sous la cloture, 0.66 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 2.45-2.55 (B). stop INDICATIF 1.65 (-32.64 % sous le bas ; sous le support 1.88-1.88 (- 0,5 ATR)).
- **Deep** : plage **2.45 → 1.69** (-25.67 % a -48.65 % sous la cloture, 1.66 ATR) — touchee 45 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1.88-1.88 (C). stop INDICATIF 1.24 (-26.9 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.17 ATR sous le plus haut 20 s., RSI(2) 18.3. Limite **3.07** (seance suivante), stop catastrophe 1.25, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 2.81-2.9 (B, -12.12 %) ; 2.45-2.55 (B, -22.7 %) ; 1.88-1.88 (C, -43.03 %)
- Resistances reelles au-dessus : 3.48-3.5 (B, 5.45 %) ; 3.76-3.79 (A, 13.94 %) ; 4.61-4.69 (C, 39.7 %) ; 5.2-5.3 (B, 57.58 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.15 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (37.37 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1189).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 37.37 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.628 % | p01 -6.991 % | pire -30.323 % _(sur 1189 séances)_
- **P(stop avant cible)** _(source : daily, 1190 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3077** [0.2426 ; 0.3792] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.367** [0.3175 ; 0.4188] _(largeur 10.1 pt, n_eff 345.5)_
   - deep : **0.3695** [0.3199 ; 0.4213] _(largeur 10.1 pt, n_eff 345.5)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-9.52 %** | CVaR **-12.14 %** | vol 6.86 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 11.00 % contre 5.77 % aujourd'hui, rapport 1.91)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.59 % vs -18.75 % si l'on extrapolait par √5 _(rapport 1.044 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6879** (β de hausse 1.4151, asymétrie 1.1927) vs IWM — 567 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.713× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 3.0622 sur atr_grid (0.5 ATR, 7.207 %) — p(stop avant cible) 0.7528 [0.71 ; 0.80], R/R 2.63, perte reelle 7.422 % (gap inclus), CVaR 9.63 %, EV -2.1996 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5709 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.753, borne haute 0.796 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 21.621 %) — p(stop avant cible) 0.233 [0.19 ; 0.28], R/R 0.897, perte reelle 21.758 % (gap inclus), EV -3.6098 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.61 %) : P(cible) 22.4 % x 19.52 % + P(rien) 54.3 % x -5.37 % ne couvrent pas P(stop) 23.3 % x 21.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 3.603 %) — p(stop avant cible) 0.8728 [0.83 ; 0.90], R/R 5.274, perte reelle 3.701 % (gap inclus), EV -1.2458 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.873, borne haute 0.905 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 9.7 % x 19.52 % + P(rien) 3.0 % x 2.89 % ne couvrent pas P(stop) 87.3 % x 3.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 7.207 %) — p(stop avant cible) 0.7528 [0.71 ; 0.80], R/R 2.63, perte reelle 7.422 % (gap inclus), EV -2.1996 % — **REFUSE**
      - refuse : p_stop_first 0.753, borne haute 0.796 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 16.1 % x 19.52 % + P(rien) 8.6 % x 2.84 % ne couvrent pas P(stop) 75.3 % x 7.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 10.81 %) — p(stop avant cible) 0.6159 [0.56 ; 0.67], R/R 1.79, perte reelle 10.901 % (gap inclus), EV -2.8692 % — **REFUSE**
      - refuse : p_stop_first 0.616, borne haute 0.666 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.87 %) : P(cible) 19.7 % x 19.52 % + P(rien) 18.7 % x -0.03 % ne couvrent pas P(stop) 61.6 % x 10.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 14.413 %) — p(stop avant cible) 0.4826 [0.43 ; 0.54], R/R 1.343, perte reelle 14.528 % (gap inclus), EV -3.1248 % — **REFUSE**
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.12 %) : P(cible) 21.8 % x 19.52 % + P(rien) 30.0 % x -1.21 % ne couvrent pas P(stop) 48.3 % x 14.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 18.017 %) — p(stop avant cible) 0.3607 [0.31 ; 0.41], R/R 1.074, perte reelle 18.165 % (gap inclus), EV -3.5479 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.55 %) : P(cible) 22.3 % x 19.52 % + P(rien) 41.6 % x -3.23 % ne couvrent pas P(stop) 36.1 % x 18.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 25.223 %) — p(stop avant cible) 0.1545 [0.12 ; 0.20], R/R 0.769, perte reelle 25.392 % (gap inclus), EV -3.6349 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.63 %) : P(cible) 22.4 % x 19.52 % + P(rien) 62.1 % x -6.58 % ne couvrent pas P(stop) 15.4 % x 25.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 28.827 %) — p(stop avant cible) 0.094 [0.07 ; 0.13], R/R 0.669, perte reelle 29.184 % (gap inclus), EV -3.5776 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.58 %) : P(cible) 22.4 % x 19.52 % + P(rien) 68.2 % x -7.65 % ne couvrent pas P(stop) 9.4 % x 29.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 32.43 %) — p(stop avant cible) 0.0405 [0.02 ; 0.07], R/R 0.6, perte reelle 32.524 % (gap inclus), EV -3.4767 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.48 %) : P(cible) 22.4 % x 19.52 % + P(rien) 73.5 % x -8.90 % ne couvrent pas P(stop) 4.0 % x 32.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 36.034 %) — p(stop avant cible) 0.0269 [0.01 ; 0.05], R/R 0.541, perte reelle 36.061 % (gap inclus), EV -3.5236 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 22.4 % x 19.52 % + P(rien) 74.9 % x -9.26 % ne couvrent pas P(stop) 2.7 % x 36.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 39.637 %) — p(stop avant cible) 0.0134 [0.00 ; 0.03], R/R 0.491, perte reelle 39.786 % (gap inclus), EV -3.5406 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.54 %) : P(cible) 22.4 % x 19.52 % + P(rien) 76.2 % x -9.69 % ne couvrent pas P(stop) 1.3 % x 39.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 43.24 %) — p(stop avant cible) 0.0091 [0.00 ; 0.02], R/R 0.45, perte reelle 43.421 % (gap inclus), EV -3.5218 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 22.4 % x 19.52 % + P(rien) 76.6 % x -9.80 % ne couvrent pas P(stop) 0.9 % x 43.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 50.447 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.387, perte reelle 50.447 % (gap inclus), EV -3.5267 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.53 %) : P(cible) 22.4 % x 19.52 % + P(rien) 77.4 % x -10.13 % ne couvrent pas P(stop) 0.1 % x 50.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 57.654 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.339, perte reelle 57.654 % (gap inclus), EV -3.524 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 22.4 % x 19.52 % + P(rien) 77.5 % x -10.19 % ne couvrent pas P(stop) 0.0 % x 57.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 64.86 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.301, perte reelle 64.86 % (gap inclus), EV -3.524 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 22.4 % x 19.52 % + P(rien) 77.5 % x -10.19 % ne couvrent pas P(stop) 0.0 % x 64.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 72.067 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.271, perte reelle 72.067 % (gap inclus), EV -3.524 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 22.4 % x 19.52 % + P(rien) 77.5 % x -10.19 % ne couvrent pas P(stop) 0.0 % x 72.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 79.274 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.246, perte reelle 79.274 % (gap inclus), EV -3.524 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 22.4 % x 19.52 % + P(rien) 77.5 % x -10.19 % ne couvrent pas P(stop) 0.0 % x 79.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 86.481 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.226, perte reelle 86.481 % (gap inclus), EV -3.524 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 22.4 % x 19.52 % + P(rien) 77.5 % x -10.19 % ne couvrent pas P(stop) 0.0 % x 86.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 93.687 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.208, perte reelle 93.687 % (gap inclus), EV -3.524 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.52 %) : P(cible) 22.4 % x 19.52 % + P(rien) 77.5 % x -10.19 % ne couvrent pas P(stop) 0.0 % x 93.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.3, ATR14 0.4756 (14.413 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.427 ATR = 6.155 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.721 % | 3.2762 | 92.79 % | 95.26 % | 96.44 % | 97.19 % | 98.04 % | 98.46 % |
| 0.1 ATR | 1.441 % | 3.2524 | 87.08 % | 91.59 % | 93.53 % | 94.92 % | 96.41 % | 97.58 % |
| 0.15 ATR | 2.162 % | 3.2287 | 80.95 % | 87.18 % | 89.86 % | 92.0 % | 94.24 % | 96.26 % |
| 0.2 ATR | 2.883 % | 3.2049 | 75.24 % | 82.87 % | 86.62 % | 89.51 % | 92.72 % | 95.27 % |
| 0.25 ATR | 3.603 % | 3.1811 | 70.08 % | 79.74 % | 84.03 % | 87.24 % | 91.09 % | 94.18 % |
| 0.35 ATR | 5.045 % | 3.1335 | 58.45 % | 72.41 % | 77.67 % | 83.03 % | 88.15 % | 91.87 % |
| 0.5 ATR | 7.207 % | 3.0622 | 42.09 % | 59.27 % | 67.42 % | 74.49 % | 83.8 % | 89.01 % |
| 0.75 ATR | 10.81 % | 2.9433 | 20.56 % | 37.93 % | 48.11 % | 60.43 % | 73.26 % | 81.87 % |
| 1.0 ATR | 14.413 % | 2.8244 | 11.09 % | 26.08 % | 36.46 % | 50.27 % | 65.54 % | 76.26 % |
| 1.25 ATR | 18.017 % | 2.7054 | 4.63 % | 16.27 % | 25.89 % | 39.35 % | 56.09 % | 70.11 % |
| 1.5 ATR | 21.62 % | 2.5865 | 2.26 % | 9.91 % | 16.94 % | 29.41 % | 47.07 % | 63.63 % |
| 2.0 ATR | 28.827 % | 2.3487 | 0.32 % | 3.23 % | 6.9 % | 15.68 % | 32.72 % | 50.88 % |
| 2.5 ATR | 36.034 % | 2.1109 | 0.11 % | 1.4 % | 3.24 % | 7.78 % | 21.85 % | 40.22 % |
| 3.0 ATR | 43.24 % | 1.8731 | 0.11 % | 0.54 % | 1.83 % | 4.22 % | 12.93 % | 30.55 % |
| 4.0 ATR | 57.654 % | 1.3974 | 0.0 % | 0.22 % | 0.32 % | 1.19 % | 5.33 % | 15.49 % |
| 6.0 ATR | 86.481 % | 0.4461 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.33 % | 1.76 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.04 ATR | 1.24 ATR |
| **2 s.** | 0.32 ATR | 0.61 ATR | 0.67 ATR | 0.85 ATR | 1.03 ATR | 1.16 ATR | 1.50 ATR | 1.87 ATR |
| **3 s.** | 0.39 ATR | 0.73 ATR | 0.82 ATR | 1.08 ATR | 1.27 ATR | 1.42 ATR | 1.85 ATR | 2.26 ATR |
| **5 s.** | 0.49 ATR | 1.01 ATR | 1.12 ATR | 1.41 ATR | 1.66 ATR | 1.84 ATR | 2.36 ATR | 2.89 ATR |
| **10 s.** | 0.71 ATR | 1.42 ATR | 1.57 ATR | 1.99 ATR | 2.35 ATR | 2.60 ATR | 3.39 ATR | 4.13 ATR |
| **20 s.** | 1.05 ATR | 2.04 ATR | 2.28 ATR | 2.87 ATR | 3.37 ATR | 3.70 ATR | 4.80 ATR | 5.53 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.473 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (61.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.667–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (10.81 %, prix 2.9433), p(touche) 37.93 % (en stress 89.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (78.2 % des re-echantillons)
- **3 seance(s)** : plage utile VIDE (borne basse 0.817 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile VIDE (borne basse 1.121 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.572 ATR au-dessus du haut de la grille, 1.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.276 ATR au-dessus du haut de la grille, 1.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.9 | bear 79.4 | side 14.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→59% · +3.0%→53% · +5.0%→30% · +8.0%→10%
- Range intraday médian 6.64% (p90 11.55%) · excursion haute méd. +3.06% / basse méd. −3.1%
- Profil de vol intra : ouverture 4.446% vs midi 1.324% vs clôture 1.662% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.146 ; mean-reverting — autocorr -0.071)_ ; drift intra méd. -0.609% ; recovery-V 26%
- **σ réalisé intraday** 3.955% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 38% / bas 59% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 5.4224 (VA 5.3244–5.4224 ; dernier close 5.375)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 48% · rebond 69% · **stop −4.5%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.67% · baisse 56% (gap-down >1% 43% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −0.98% (p90 −2.72%) · haut méd +1.12% · range méd 2.52%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −3.85%) · haut méd +1.35% · range méd 3.48%
- Excursion ouverture 30min (n=160) : bas méd −1.77% (p90 −4.62%) · haut méd +1.54% · range méd 3.91%
- Excursion ouverture 60min (n=160) : bas méd −2.14% (p90 −5.17%) · haut méd +1.72% · range méd 4.47%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 5.38 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 73% · séance 82% (127/159) · gap 52% · délai 0.0min · rebond 56% (74/127) (MFE +1.31%)
   - −1.0% : fill 30min 66% · séance 80% (121/159) · gap 43% · délai 0.0min · rebond 59% (71/121) (MFE +1.48%)
   - −1.5% : fill 30min 63% · séance 77% (115/159) · gap 36% · délai 0.0min · rebond 60% (75/115) (MFE +1.52%)
   - −2.0% : fill 30min 57% · séance 69% (104/159) · gap 30% · délai 0.0min · rebond 59% (64/104) (MFE +1.33%)
   - −3.0% : fill 30min 47% · séance 57% (88/159) · gap 16% · délai 2.0min · rebond 73% (64/88) (MFE +1.9%)
   - −4.0% : fill 30min 34% · séance 48% (77/159) · gap 8% · délai 5.0min · rebond 69% (54/77) (MFE +2.53%)
   - −5.0% : fill 30min 21% · séance 37% (62/159) · gap 4% · délai 25.1min · rebond 62% (42/62) (MFE +1.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.21%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.8% (p90 −2.4%) → stop au-delà de −1.8% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.94% (p90 −2.68%) → stop au-delà de −2.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1042 jambes) : jambe baissière méd −1.27% (p90 −3.04%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 97% (80/83) · rebond 53% (45/80)
      · −2.0% : fill 92% (75/83) · rebond 62% (50/75)
      · −3.0% : fill 88% (70/83) · rebond 76% (53/70)
      · −4.0% : fill 76% (61/83) · rebond 73% (45/61)
      · −5.0% : fill 58% (49/83) · rebond 62% (35/49)
   - **flat** (11 séances) :
      · −1.0% : fill 98% (10/11) · rebond 75% (6/10)
      · −2.0% : fill 40% (6/11) · rebond 39% (2/6)
      · −3.0% : fill 40% (6/11) · rebond 50% (3/6)
      · −4.0% : fill 40% (6/11) · rebond 62% (4/6)
      · −5.0% : fill 30% (4/11) · rebond 78% (3/4)
   - **gap-up** (65 séances) :
      · −1.0% : fill 54% (31/65) · rebond 70% (20/31)
      · −2.0% : fill 42% (23/65) · rebond 52% (12/23)
      · −3.0% : fill 17% (12/65) · rebond 61% (8/12)
      · −4.0% : fill 12% (10/65) · rebond 41% (5/10)
      · −5.0% : fill 9% (9/65) · rebond 49% (4/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 69% si les 15 1res min sont vertes (73 cas) · 25% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 87% si début vert vs 10% si rouge (base 44% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 222min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **87%** · continue >prix actuel 58% ; creux résiduel méd -1.53% (q20 -2.47%) → **SL/trailing à −2.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.0% / q75 +3.35% → **scale +2.0% / runner +3.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **10%** (continue à baisser 67%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.64%** (au-delà de la MAE q10 -4.64%), cible rebond +1.44% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.47% .. +3.81%] · haut q95 +5.65% · bas q05 -5.19%
   - 60min (n=160) : retour [-4.95% .. +5.39%] · haut q95 +6.06% · bas q05 -5.78%
   - 2h (n=160) : retour [-6.22% .. +5.43%] · haut q95 +7.7% · bas q05 -7.56%
   - 4h (n=160) : retour [-7.11% .. +6.73%] · haut q95 +8.03% · bas q05 -7.87%
   - 6h (n=160) : retour [-7.12% .. +8.11%] · haut q95 +9.84% · bas q05 -8.91%
   - session (n=160) : retour [-6.91% .. +8.66%] · haut q95 +10.5% · bas q05 -8.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.41 · part idiosyncratique 0.59
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.9  _(survente)_
- **ADX** : 39.4  _(tendance etablie)_
- **MACD** : hist -0.077  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 69.7%
- **ATR** : 0.48 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.316  _(distribution)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 39.8  _(transition)_
- **MA** : MA20 4.71 · MA50 6.19 · MA200 9.67  _(prix < MA20)_
- **Dist MA** : MA20 -29.9% · MA50 -46.7% · MA200 -65.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (500301 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
