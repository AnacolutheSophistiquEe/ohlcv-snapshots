# SMR

**Generated** : 2026-11-19T01:30:05.954117+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 6.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $3.91  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 1/125 fenêtres (p_fill pondéré 0 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $3.91 (+14.7% vs entrée) · entrée $3.41 · stop $3.26 · T1 $3.66 · R/R 1.67  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +34.5 % ≠ (strike 5.5 − spot 3.91)/spot = +40.7 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-18 : 3.91 · ATR Wilder 0.4753 (12.16 %)_
- **Swing** : plage **3.34 → 3.03** (-14.46 % a -22.45 % sous la cloture, 0.66 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 3.18-3.22 (B). stop INDICATIF 2.57 (-15.17 % sous le bas ; sous le support 2.81-2.93 (- 0,5 ATR)).
- **Deep** : plage **3.03 → 2.25** (-22.45 % a -42.58 % sous la cloture, 1.66 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 2.81-2.93 (B) ; 2.45-2.55 (B). stop INDICATIF 1.64 (-26.85 % sous le bas ; sous le support 1.88-1.88 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.63 ATR sous le plus haut 20 s., RSI(2) 1.4. Limite **3.67** (seance suivante), stop catastrophe 1.77, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 3.48-3.5 (C, -10.49 %) ; 3.18-3.22 (B, -17.65 %) ; 2.81-2.93 (B, -25.06 %) ; 2.45-2.55 (B, -34.76 %) ; 1.88-1.88 (C, -51.92 %)
- Resistances reelles au-dessus : 4.61-4.69 (C, 17.9 %) ; 5.2-5.3 (B, 32.99 %) ; 5.5-5.58 (B, 40.66 %) ; 6.35-6.36 (B, 62.4 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.09 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (34.49 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1185).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 34.49 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.615 % | p01 -7.0 % | pire -30.323 % _(sur 1185 séances)_
- **P(stop avant cible)** _(source : daily, 1186 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3616** [0.2928 ; 0.435] _(largeur 14.2 pt, n_eff 173.1)_
   - swing : **0.3518** [0.3028 ; 0.4032] _(largeur 10.0 pt, n_eff 345.5)_
   - deep : **0.3523** [0.3033 ; 0.4037] _(largeur 10.0 pt, n_eff 345.5)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-9.4 %** | CVaR **-12.07 %** | vol 6.84 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 11.01 % contre 5.79 % aujourd'hui, rapport 1.90)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.45 % vs -18.74 % si l'on extrapolait par √5 _(rapport 1.038 ; < 1 = le √5 surestime)_
- **β de baisse : 1.664** (β de hausse 1.4097, asymétrie 1.1804) vs IWM — 565 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.795× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 3.6602 sur atr_grid (0.5 ATR, 6.389 %) — p(stop avant cible) 0.7594 [0.71 ; 0.80], R/R 2.626, perte reelle 6.59 % (gap inclus), CVaR 8.839 %, EV -1.7037 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5832 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.759, borne haute 0.802 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 19.169 %) — p(stop avant cible) 0.2939 [0.25 ; 0.34], R/R 0.89, perte reelle 19.434 % (gap inclus), EV -2.8043 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.80 %) : P(cible) 27.2 % x 17.30 % + P(rien) 43.4 % x -4.16 % ne couvrent pas P(stop) 29.4 % x 19.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 3.195 %) — p(stop avant cible) 0.8736 [0.84 ; 0.91], R/R 5.273, perte reelle 3.282 % (gap inclus), EV -0.9181 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.874, borne haute 0.905 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 11.0 % x 17.30 % + P(rien) 1.6 % x 2.77 % ne couvrent pas P(stop) 87.4 % x 3.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 6.389 %) — p(stop avant cible) 0.7594 [0.71 ; 0.80], R/R 2.626, perte reelle 6.59 % (gap inclus), EV -1.7037 % — **REFUSE**
      - refuse : p_stop_first 0.759, borne haute 0.802 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.70 %) : P(cible) 18.5 % x 17.30 % + P(rien) 5.6 % x 1.90 % ne couvrent pas P(stop) 75.9 % x 6.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 9.584 %) — p(stop avant cible) 0.6233 [0.57 ; 0.67], R/R 1.785, perte reelle 9.695 % (gap inclus), EV -2.0835 % — **REFUSE**
      - refuse : p_stop_first 0.623, borne haute 0.673 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 23.1 % x 17.30 % + P(rien) 14.6 % x -0.22 % ne couvrent pas P(stop) 62.3 % x 9.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 12.779 %) — p(stop avant cible) 0.5222 [0.47 ; 0.57], R/R 1.342, perte reelle 12.891 % (gap inclus), EV -2.4417 % — **REFUSE**
      - refuse : p_stop_first 0.522, borne haute 0.575 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.44 %) : P(cible) 25.9 % x 17.30 % + P(rien) 21.9 % x -0.85 % ne couvrent pas P(stop) 52.2 % x 12.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 15.973 %) — p(stop avant cible) 0.4077 [0.36 ; 0.46], R/R 1.074, perte reelle 16.108 % (gap inclus), EV -2.7082 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.71 %) : P(cible) 27.0 % x 17.30 % + P(rien) 32.2 % x -2.54 % ne couvrent pas P(stop) 40.8 % x 16.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 22.363 %) — p(stop avant cible) 0.2002 [0.16 ; 0.24], R/R 0.767, perte reelle 22.547 % (gap inclus), EV -2.743 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.74 %) : P(cible) 27.4 % x 17.30 % + P(rien) 52.6 % x -5.63 % ne couvrent pas P(stop) 20.0 % x 22.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 25.557 %) — p(stop avant cible) 0.1325 [0.10 ; 0.17], R/R 0.672, perte reelle 25.756 % (gap inclus), EV -2.5802 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.58 %) : P(cible) 27.4 % x 17.30 % + P(rien) 59.4 % x -6.57 % ne couvrent pas P(stop) 13.2 % x 25.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 28.752 %) — p(stop avant cible) 0.0838 [0.06 ; 0.12], R/R 0.595, perte reelle 29.077 % (gap inclus), EV -2.5897 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.59 %) : P(cible) 27.4 % x 17.30 % + P(rien) 64.2 % x -7.61 % ne couvrent pas P(stop) 8.4 % x 29.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 31.946 %) — p(stop avant cible) 0.0385 [0.02 ; 0.06], R/R 0.539, perte reelle 32.091 % (gap inclus), EV -2.5267 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.53 %) : P(cible) 27.4 % x 17.30 % + P(rien) 68.8 % x -8.77 % ne couvrent pas P(stop) 3.9 % x 32.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 35.141 %) — p(stop avant cible) 0.0222 [0.01 ; 0.04], R/R 0.492, perte reelle 35.206 % (gap inclus), EV -2.474 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.47 %) : P(cible) 27.4 % x 17.30 % + P(rien) 70.4 % x -9.14 % ne couvrent pas P(stop) 2.2 % x 35.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 38.336 %) — p(stop avant cible) 0.0163 [0.01 ; 0.03], R/R 0.451, perte reelle 38.349 % (gap inclus), EV -2.5173 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.52 %) : P(cible) 27.4 % x 17.30 % + P(rien) 71.0 % x -9.34 % ne couvrent pas P(stop) 1.6 % x 38.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 44.725 %) — p(stop avant cible) 0.009 [0.00 ; 0.02], R/R 0.387, perte reelle 44.725 % (gap inclus), EV -2.5126 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 27.4 % x 17.30 % + P(rien) 71.7 % x -9.55 % ne couvrent pas P(stop) 0.9 % x 44.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 51.114 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.339, perte reelle 51.114 % (gap inclus), EV -2.5112 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 27.4 % x 17.30 % + P(rien) 72.6 % x -9.98 % ne couvrent pas P(stop) 0.0 % x 51.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 57.504 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.301, perte reelle 57.504 % (gap inclus), EV -2.5102 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 27.4 % x 17.30 % + P(rien) 72.6 % x -9.98 % ne couvrent pas P(stop) 0.0 % x 57.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 63.893 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.271, perte reelle 63.893 % (gap inclus), EV -2.5102 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 27.4 % x 17.30 % + P(rien) 72.6 % x -9.98 % ne couvrent pas P(stop) 0.0 % x 63.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 70.282 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.246, perte reelle 70.282 % (gap inclus), EV -2.5102 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 27.4 % x 17.30 % + P(rien) 72.6 % x -9.98 % ne couvrent pas P(stop) 0.0 % x 70.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 76.672 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.226, perte reelle 76.672 % (gap inclus), EV -2.5102 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 27.4 % x 17.30 % + P(rien) 72.6 % x -9.98 % ne couvrent pas P(stop) 0.0 % x 76.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 83.061 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.208, perte reelle 83.061 % (gap inclus), EV -2.5102 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 27.4 % x 17.30 % + P(rien) 72.6 % x -9.98 % ne couvrent pas P(stop) 0.0 % x 83.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 89.45 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.193, perte reelle 89.45 % (gap inclus), EV -2.5102 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 27.4 % x 17.30 % + P(rien) 72.6 % x -9.98 % ne couvrent pas P(stop) 0.0 % x 89.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 95.839 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.181, perte reelle 95.839 % (gap inclus), EV -2.5102 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 27.4 % x 17.30 % + P(rien) 72.6 % x -9.98 % ne couvrent pas P(stop) 0.0 % x 95.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.91, ATR14 0.4996 (12.779 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.426 ATR = 5.444 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.639 % | 3.885 | 92.76 % | 95.24 % | 96.42 % | 97.18 % | 98.03 % | 98.45 % |
| 0.1 ATR | 1.278 % | 3.86 | 87.03 % | 91.56 % | 93.5 % | 94.9 % | 96.4 % | 97.57 % |
| 0.15 ATR | 1.917 % | 3.8351 | 80.86 % | 87.12 % | 89.82 % | 91.97 % | 94.21 % | 96.25 % |
| 0.2 ATR | 2.556 % | 3.8101 | 75.14 % | 82.79 % | 86.57 % | 89.47 % | 92.69 % | 95.25 % |
| 0.25 ATR | 3.195 % | 3.7851 | 69.95 % | 79.65 % | 83.97 % | 87.19 % | 91.05 % | 94.15 % |
| 0.35 ATR | 4.473 % | 3.7351 | 58.27 % | 72.29 % | 77.57 % | 82.95 % | 88.1 % | 91.83 % |
| 0.5 ATR | 6.389 % | 3.6602 | 41.95 % | 59.09 % | 67.28 % | 74.38 % | 83.73 % | 88.96 % |
| 0.75 ATR | 9.584 % | 3.5353 | 20.54 % | 37.77 % | 47.89 % | 60.26 % | 73.14 % | 81.79 % |
| 1.0 ATR | 12.779 % | 3.4104 | 11.14 % | 26.08 % | 36.19 % | 50.05 % | 65.39 % | 76.16 % |
| 1.25 ATR | 15.973 % | 3.2854 | 4.65 % | 16.23 % | 25.79 % | 39.09 % | 55.9 % | 69.98 % |
| 1.5 ATR | 19.168 % | 3.1605 | 2.27 % | 9.96 % | 16.9 % | 29.1 % | 46.83 % | 63.47 % |
| 2.0 ATR | 25.557 % | 2.9107 | 0.32 % | 3.25 % | 6.93 % | 15.42 % | 32.42 % | 50.66 % |
| 2.5 ATR | 31.946 % | 2.6609 | 0.11 % | 1.41 % | 3.25 % | 7.82 % | 21.62 % | 39.96 % |
| 3.0 ATR | 38.336 % | 2.4111 | 0.11 % | 0.54 % | 1.84 % | 4.23 % | 12.77 % | 30.35 % |
| 4.0 ATR | 51.114 % | 1.9114 | 0.0 % | 0.22 % | 0.33 % | 1.19 % | 5.24 % | 15.34 % |
| 6.0 ATR | 76.672 % | 0.9121 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.33 % | 1.77 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.60 ATR | 0.70 ATR | 0.76 ATR | 1.04 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.61 ATR | 0.67 ATR | 0.85 ATR | 1.03 ATR | 1.15 ATR | 1.50 ATR | 1.87 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.08 ATR | 1.27 ATR | 1.41 ATR | 1.85 ATR | 2.26 ATR |
| **5 s.** | 0.49 ATR | 1.00 ATR | 1.11 ATR | 1.40 ATR | 1.65 ATR | 1.83 ATR | 2.36 ATR | 2.89 ATR |
| **10 s.** | 0.71 ATR | 1.41 ATR | 1.56 ATR | 1.98 ATR | 2.34 ATR | 2.59 ATR | 3.37 ATR | 4.10 ATR |
| **20 s.** | 1.05 ATR | 2.03 ATR | 2.26 ATR | 2.86 ATR | 3.36 ATR | 3.69 ATR | 4.79 ATR | 5.52 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.472 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.665–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (9.584 %, prix 3.5353), p(touche) 37.77 % (en stress 89.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (77.0 % des re-echantillons)
- **3 seance(s)** : plage utile 0.812–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (12.779 %, prix 3.4103), p(touche) 36.19 % (en stress 91.4 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.6 % des re-echantillons)
- **5 seance(s)** : plage utile 1.115–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (15.973 %, prix 3.2855), p(touche) 39.09 % (en stress 95.7 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.563 ATR au-dessus du haut de la grille, 1.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.264 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 81.8 | side 13.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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

**Factor** : R² 0.35 · part idiosyncratique 0.65
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 26.1  _(survente)_
- **ADX** : 34.6  _(tendance etablie)_
- **MACD** : hist -0.035  _(bearish_recent)_
- **BB** : %B -0.03 · largeur 44.2%
- **ATR** : 0.5 (13.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.151  _(distribution)_
- **Vol ratio** : 1.09  _(volume normal)_
- **Choppiness** : 48.8  _(transition)_
- **MA** : MA20 5.09 · MA50 6.63 · MA200 9.93  _(prix < MA20)_
- **Dist MA** : MA20 -23.2% · MA50 -41.0% · MA200 -60.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (681402 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
