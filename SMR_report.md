# SMR

**Generated** : 2026-11-27T01:30:07.317204+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $3.25  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 1/125 fenêtres (p_fill pondéré 0 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $3.25 (+15.7% vs entrée) · entrée $2.81 · stop $2.68 · T1 $3.03 · R/R 1.69  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-25 : 3.25 · ATR Wilder 0.4489 (13.81 %)_
- **Swing** : plage **2.71 → 2.41** (-16.55 % a -25.82 % sous la cloture, 0.67 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 2.45-2.55 (B). stop INDICATIF 1.66 (-31.33 % sous le bas ; sous le support 1.88-1.88 (- 0,5 ATR)).
- **Deep** : plage **2.41 → 1.67** (-25.82 % a -48.74 % sous la cloture, 1.66 ATR) — touchee 45 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1.88-1.88 (C). stop INDICATIF 1.22 (-26.95 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.37 ATR sous le plus haut 20 s., RSI(2) 15.1. Limite **3.03** (seance suivante), stop catastrophe 1.23, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 2.81-2.9 (B, -10.77 %) ; 2.45-2.55 (B, -21.51 %) ; 1.88-1.88 (C, -42.15 %)
- Resistances reelles au-dessus : 3.48-3.5 (B, 7.08 %) ; 3.76-3.79 (A, 15.69 %) ; 4.61-4.69 (C, 41.85 %) ; 5.2-5.3 (B, 60.0 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.23 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (35.84 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1190).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 35.84 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.636 % | p01 -6.989 % | pire -30.323 % _(sur 1190 séances)_
- **P(stop avant cible)** _(source : daily, 1191 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3404** [0.2729 ; 0.4132] _(largeur 14.0 pt, n_eff 173.1)_
   - swing : **0.3707** [0.321 ; 0.4225] _(largeur 10.2 pt, n_eff 345.5)_
   - deep : **0.3708** [0.3211 ; 0.4226] _(largeur 10.2 pt, n_eff 345.5)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-9.52 %** | CVaR **-12.14 %** | vol 6.86 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 11.02 % contre 5.67 % aujourd'hui, rapport 1.94)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.59 % vs -18.75 % si l'on extrapolait par √5 _(rapport 1.044 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6879** (β de hausse 1.4175, asymétrie 1.1908) vs IWM — 567 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.713× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 3.0299 sur atr_grid (0.5 ATR, 6.774 %) — p(stop avant cible) 0.7682 [0.72 ; 0.81], R/R 2.623, perte reelle 6.995 % (gap inclus), CVaR 9.451 %, EV -2.185 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5991 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.768, borne haute 0.810 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 20.32 %) — p(stop avant cible) 0.2852 [0.24 ; 0.33], R/R 0.893, perte reelle 20.537 % (gap inclus), EV -3.7051 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.71 %) : P(cible) 24.0 % x 18.34 % + P(rien) 47.5 % x -4.73 % ne couvrent pas P(stop) 28.5 % x 20.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 3.387 %) — p(stop avant cible) 0.8744 [0.84 ; 0.91], R/R 5.295, perte reelle 3.465 % (gap inclus), EV -1.1483 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.874, borne haute 0.906 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 9.8 % x 18.34 % + P(rien) 2.7 % x 2.74 % ne couvrent pas P(stop) 87.4 % x 3.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 6.774 %) — p(stop avant cible) 0.7682 [0.72 ; 0.81], R/R 2.623, perte reelle 6.995 % (gap inclus), EV -2.185 % — **REFUSE**
      - refuse : p_stop_first 0.768, borne haute 0.810 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.19 %) : P(cible) 16.4 % x 18.34 % + P(rien) 6.7 % x 2.56 % ne couvrent pas P(stop) 76.8 % x 7.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 10.16 %) — p(stop avant cible) 0.6285 [0.58 ; 0.68], R/R 1.79, perte reelle 10.249 % (gap inclus), EV -2.6477 % — **REFUSE**
      - refuse : p_stop_first 0.628, borne haute 0.678 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.65 %) : P(cible) 20.7 % x 18.34 % + P(rien) 16.4 % x -0.07 % ne couvrent pas P(stop) 62.8 % x 10.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 13.547 %) — p(stop avant cible) 0.5143 [0.46 ; 0.57], R/R 1.342, perte reelle 13.672 % (gap inclus), EV -2.9922 % — **REFUSE**
      - refuse : p_stop_first 0.514, borne haute 0.567 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.99 %) : P(cible) 23.0 % x 18.34 % + P(rien) 25.6 % x -0.70 % ne couvrent pas P(stop) 51.4 % x 13.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 16.934 %) — p(stop avant cible) 0.393 [0.34 ; 0.45], R/R 1.076, perte reelle 17.045 % (gap inclus), EV -3.429 % — **REFUSE**
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.43 %) : P(cible) 23.8 % x 18.34 % + P(rien) 36.9 % x -2.96 % ne couvrent pas P(stop) 39.3 % x 17.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 23.708 %) — p(stop avant cible) 0.1904 [0.15 ; 0.23], R/R 0.767, perte reelle 23.926 % (gap inclus), EV -3.624 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.62 %) : P(cible) 24.0 % x 18.34 % + P(rien) 56.9 % x -6.11 % ne couvrent pas P(stop) 19.0 % x 23.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 27.095 %) — p(stop avant cible) 0.1122 [0.08 ; 0.15], R/R 0.669, perte reelle 27.414 % (gap inclus), EV -3.5316 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.53 %) : P(cible) 24.1 % x 18.34 % + P(rien) 64.7 % x -7.52 % ne couvrent pas P(stop) 11.2 % x 27.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 30.481 %) — p(stop avant cible) 0.0715 [0.05 ; 0.10], R/R 0.598, perte reelle 30.682 % (gap inclus), EV -3.6373 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.64 %) : P(cible) 24.1 % x 18.34 % + P(rien) 68.8 % x -8.51 % ne couvrent pas P(stop) 7.1 % x 30.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 33.868 %) — p(stop avant cible) 0.0422 [0.02 ; 0.07], R/R 0.541, perte reelle 33.911 % (gap inclus), EV -3.599 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.60 %) : P(cible) 24.1 % x 18.34 % + P(rien) 71.7 % x -9.18 % ne couvrent pas P(stop) 4.2 % x 33.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 37.255 %) — p(stop avant cible) 0.0319 [0.02 ; 0.05], R/R 0.492, perte reelle 37.269 % (gap inclus), EV -3.6785 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.68 %) : P(cible) 24.1 % x 18.34 % + P(rien) 72.8 % x -9.49 % ne couvrent pas P(stop) 3.2 % x 37.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 40.642 %) — p(stop avant cible) 0.0173 [0.01 ; 0.04], R/R 0.449, perte reelle 40.829 % (gap inclus), EV -3.6776 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.68 %) : P(cible) 24.1 % x 18.34 % + P(rien) 74.2 % x -9.95 % ne couvrent pas P(stop) 1.7 % x 40.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 47.415 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.387, perte reelle 47.415 % (gap inclus), EV -3.6739 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 24.1 % x 18.34 % + P(rien) 75.5 % x -10.44 % ne couvrent pas P(stop) 0.4 % x 47.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 54.189 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.339, perte reelle 54.189 % (gap inclus), EV -3.6688 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.16 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 24.1 % x 18.34 % + P(rien) 75.9 % x -10.64 % ne couvrent pas P(stop) 0.0 % x 54.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 60.963 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.301, perte reelle 60.963 % (gap inclus), EV -3.6685 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 24.1 % x 18.34 % + P(rien) 75.9 % x -10.64 % ne couvrent pas P(stop) 0.0 % x 60.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 67.736 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.271, perte reelle 67.736 % (gap inclus), EV -3.6685 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 24.1 % x 18.34 % + P(rien) 75.9 % x -10.64 % ne couvrent pas P(stop) 0.0 % x 67.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 74.51 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.246, perte reelle 74.51 % (gap inclus), EV -3.6685 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 24.1 % x 18.34 % + P(rien) 75.9 % x -10.64 % ne couvrent pas P(stop) 0.0 % x 74.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 81.284 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.226, perte reelle 81.284 % (gap inclus), EV -3.6685 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 24.1 % x 18.34 % + P(rien) 75.9 % x -10.64 % ne couvrent pas P(stop) 0.0 % x 81.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 88.057 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.208, perte reelle 88.057 % (gap inclus), EV -3.6685 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 24.1 % x 18.34 % + P(rien) 75.9 % x -10.64 % ne couvrent pas P(stop) 0.0 % x 88.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 94.831 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.193, perte reelle 94.831 % (gap inclus), EV -3.6685 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.67 %) : P(cible) 24.1 % x 18.34 % + P(rien) 75.9 % x -10.64 % ne couvrent pas P(stop) 0.0 % x 94.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.25, ATR14 0.4403 (13.547 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.427 ATR = 5.785 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.677 % | 3.228 | 92.8 % | 95.26 % | 96.44 % | 97.19 % | 98.05 % | 98.46 % |
| 0.1 ATR | 1.355 % | 3.206 | 87.1 % | 91.6 % | 93.53 % | 94.92 % | 96.42 % | 97.59 % |
| 0.15 ATR | 2.032 % | 3.184 | 80.97 % | 87.19 % | 89.87 % | 92.01 % | 94.25 % | 96.27 % |
| 0.2 ATR | 2.709 % | 3.1619 | 75.27 % | 82.88 % | 86.64 % | 89.52 % | 92.73 % | 95.28 % |
| 0.25 ATR | 3.387 % | 3.1399 | 70.11 % | 79.76 % | 84.05 % | 87.26 % | 91.1 % | 94.18 % |
| 0.35 ATR | 4.742 % | 3.0959 | 58.39 % | 72.44 % | 77.69 % | 83.05 % | 88.17 % | 91.88 % |
| 0.5 ATR | 6.774 % | 3.0299 | 42.04 % | 59.31 % | 67.46 % | 74.51 % | 83.82 % | 89.02 % |
| 0.75 ATR | 10.16 % | 2.9198 | 20.54 % | 38.0 % | 48.17 % | 60.48 % | 73.29 % | 81.89 % |
| 1.0 ATR | 13.547 % | 2.8097 | 11.08 % | 26.05 % | 36.42 % | 50.32 % | 65.58 % | 76.29 % |
| 1.25 ATR | 16.934 % | 2.6996 | 4.62 % | 16.25 % | 25.86 % | 39.42 % | 56.13 % | 70.14 % |
| 1.5 ATR | 20.321 % | 2.5896 | 2.26 % | 9.9 % | 16.92 % | 29.48 % | 47.12 % | 63.67 % |
| 2.0 ATR | 27.095 % | 2.3694 | 0.32 % | 3.23 % | 6.9 % | 15.66 % | 32.79 % | 50.93 % |
| 2.5 ATR | 33.868 % | 2.1493 | 0.11 % | 1.4 % | 3.23 % | 7.78 % | 21.93 % | 40.29 % |
| 3.0 ATR | 40.642 % | 1.9291 | 0.11 % | 0.54 % | 1.83 % | 4.21 % | 13.03 % | 30.63 % |
| 4.0 ATR | 54.189 % | 1.4889 | 0.0 % | 0.22 % | 0.32 % | 1.19 % | 5.43 % | 15.59 % |
| 6.0 ATR | 81.284 % | 0.6083 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.33 % | 1.76 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.60 ATR | 0.70 ATR | 0.76 ATR | 1.04 ATR | 1.24 ATR |
| **2 s.** | 0.32 ATR | 0.61 ATR | 0.67 ATR | 0.85 ATR | 1.03 ATR | 1.15 ATR | 1.50 ATR | 1.87 ATR |
| **3 s.** | 0.39 ATR | 0.73 ATR | 0.82 ATR | 1.08 ATR | 1.27 ATR | 1.41 ATR | 1.84 ATR | 2.26 ATR |
| **5 s.** | 0.49 ATR | 1.01 ATR | 1.12 ATR | 1.41 ATR | 1.66 ATR | 1.84 ATR | 2.36 ATR | 2.89 ATR |
| **10 s.** | 0.71 ATR | 1.42 ATR | 1.57 ATR | 1.99 ATR | 2.36 ATR | 2.61 ATR | 3.40 ATR | 4.17 ATR |
| **20 s.** | 1.05 ATR | 2.04 ATR | 2.28 ATR | 2.88 ATR | 3.37 ATR | 3.71 ATR | 4.81 ATR | 5.53 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.473 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.668–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (10.16 %, prix 2.9198), p(touche) 38.0 % (en stress 89.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (78.5 % des re-echantillons)
- **3 seance(s)** : plage utile VIDE (borne basse 0.817 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (60.6 % des re-echantillons)
- **5 seance(s)** : plage utile 1.122–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (16.934 %, prix 2.6996), p(touche) 39.42 % (en stress 96.77 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.574 ATR au-dessus du haut de la grille, 1.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.279 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.2 | bear 78.6 | side 16.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.42 · part idiosyncratique 0.58
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.5  _(momentum baissier)_
- **ADX** : 40.9  _(tendance tres forte)_
- **MACD** : hist -0.072  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 74.1%
- **ATR** : 0.44 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.3  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 32.3  _(marche directionnel)_
- **MA** : MA20 4.59 · MA50 6.09 · MA200 9.6  _(prix < MA20)_
- **Dist MA** : MA20 -29.1% · MA50 -46.6% · MA200 -66.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (673794 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
