# MSTR

**Generated** : 2026-11-23T01:22:20.447857+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 1/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $77.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $77.80 (+12.2% vs entrée) · entrée $69.34 · stop $66.80 · T1 $73.57 · R/R 1.67  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 514 % hors [0,100] (R² max 0.79). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-20 : 77.8 · ATR Wilder 8.69 (11.17 %)_
- **Swing** : plage **66.79 → 59.07** (-14.16 % a -24.07 % sous la cloture, 0.89 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 58.85-61.41 (C). stop INDICATIF 44.39 (-24.86 % sous le bas ; sous le support 48.73-52.79 (- 0,5 ATR)).
- **Deep** : plage **59.07 → 39.29** (-24.07 % a -49.5 % sous la cloture, 2.28 ATR) — touchee 47 % → 15 % du temps en 20 seances ; supports reels dans la plage : 58.85-61.41 (C) ; 48.73-52.79 (A) ; 43.87-46.75 (B). stop INDICATIF 30.6 (-22.11 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 7.86 ATR sous le plus haut 20 s., RSI(2) 0.1. Limite **73.46** (seance suivante), stop catastrophe 38.71, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 58.85-61.41 (C, -21.06 %) ; 48.73-52.79 (A, -32.15 %) ; 43.87-46.75 (B, -39.91 %)
- Resistances reelles au-dessus : 80.68-81.81 (A, 3.7 %) ; 89.21-91.67 (A, 14.67 %) ; 100.05-104.17 (A, 28.6 %) ; 104.6-105.5 (A, 34.45 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=11.01 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (31.14 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1254).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 31.14 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.584 % | p01 -7.774 % | pire -27.372 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2628** [0.2015 ; 0.3319] _(largeur 13.0 pt, n_eff 173.1)_
   - swing : **0.2213** [0.18 ; 0.2673] _(largeur 8.7 pt, n_eff 345.7)_
   - deep : **0.1952** [0.1561 ; 0.2394] _(largeur 8.3 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.56 %** | CVaR **-9.41 %** | vol 5.06 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.31 % contre 5.41 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.49 % vs -18.25 % si l'on extrapolait par √5 _(rapport 0.958 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3909** (β de hausse 1.8255, asymétrie 1.3097) vs IWM — 605 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 69.3386 sur atr_grid (1.0 ATR, 10.876 %) — p(stop avant cible) 0.4196 [0.37 ; 0.47], R/R 2.833, perte reelle 11.081 % (gap inclus), CVaR 12.569 %, EV -0.1583 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6397 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.57 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 16.314 %) — p(stop avant cible) 0.2237 [0.18 ; 0.27], R/R 1.885, perte reelle 16.651 % (gap inclus), EV -0.5592 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 7.0 % x 31.39 % + P(rien) 70.6 % x 1.35 % ne couvrent pas P(stop) 22.4 % x 16.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 2.719 %) — p(stop avant cible) 0.8791 [0.84 ; 0.91], R/R 10.897, perte reelle 2.881 % (gap inclus), EV -0.8315 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 10.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.879, borne haute 0.910 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 2.9 % x 31.39 % + P(rien) 9.2 % x 8.73 % ne couvrent pas P(stop) 87.9 % x 2.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 5.438 %) — p(stop avant cible) 0.7131 [0.66 ; 0.76], R/R 5.528, perte reelle 5.679 % (gap inclus), EV -0.3623 % — **REFUSE**
      - refuse : cible atteinte seulement 6.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.713, borne haute 0.759 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 6.2 % x 31.39 % + P(rien) 22.5 % x 7.78 % ne couvrent pas P(stop) 71.3 % x 5.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 8.157 %) — p(stop avant cible) 0.5597 [0.51 ; 0.61], R/R 3.725, perte reelle 8.428 % (gap inclus), EV -0.1691 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.560, borne haute 0.611 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 6.8 % x 31.39 % + P(rien) 37.2 % x 6.46 % ne couvrent pas P(stop) 56.0 % x 8.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 10.876 %) — p(stop avant cible) 0.4196 [0.37 ; 0.47], R/R 2.833, perte reelle 11.081 % (gap inclus), EV -0.1583 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 7.0 % x 31.39 % + P(rien) 51.1 % x 4.52 % ne couvrent pas P(stop) 42.0 % x 11.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 13.595 %) — p(stop avant cible) 0.3183 [0.27 ; 0.37], R/R 2.271, perte reelle 13.823 % (gap inclus), EV -0.3432 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 7.0 % x 31.39 % + P(rien) 61.1 % x 3.03 % ne couvrent pas P(stop) 31.8 % x 13.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 19.033 %) — p(stop avant cible) 0.1634 [0.13 ; 0.21], R/R 1.621, perte reelle 19.369 % (gap inclus), EV -0.7496 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 7.1 % x 31.39 % + P(rien) 76.6 % x 0.25 % ne couvrent pas P(stop) 16.3 % x 19.37 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 21.752 %) — p(stop avant cible) 0.1298 [0.10 ; 0.17], R/R 1.416, perte reelle 22.165 % (gap inclus), EV -0.8499 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 7.1 % x 31.39 % + P(rien) 79.9 % x -0.24 % ne couvrent pas P(stop) 13.0 % x 22.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 24.471 %) — p(stop avant cible) 0.0922 [0.07 ; 0.13], R/R 1.264, perte reelle 24.845 % (gap inclus), EV -0.9119 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.16 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 7.1 % x 31.39 % + P(rien) 83.7 % x -1.01 % ne couvrent pas P(stop) 9.2 % x 24.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 27.19 %) — p(stop avant cible) 0.0653 [0.04 ; 0.10], R/R 1.139, perte reelle 27.553 % (gap inclus), EV -0.9412 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 7.1 % x 31.39 % + P(rien) 86.4 % x -1.58 % ne couvrent pas P(stop) 6.5 % x 27.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 29.909 %) — p(stop avant cible) 0.0455 [0.03 ; 0.07], R/R 1.038, perte reelle 30.257 % (gap inclus), EV -0.9647 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 7.1 % x 31.39 % + P(rien) 88.4 % x -2.05 % ne couvrent pas P(stop) 4.5 % x 30.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 32.628 %) — p(stop avant cible) 0.0343 [0.02 ; 0.06], R/R 0.954, perte reelle 32.908 % (gap inclus), EV -0.9819 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 7.1 % x 31.39 % + P(rien) 89.5 % x -2.32 % ne couvrent pas P(stop) 3.4 % x 32.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 38.066 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 0.816, perte reelle 38.473 % (gap inclus), EV -0.858 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 7.1 % x 31.39 % + P(rien) 92.5 % x -3.14 % ne couvrent pas P(stop) 0.4 % x 38.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 43.503 %) — p(stop avant cible) 0.0003 [0.00 ; 0.01], R/R 0.721, perte reelle 43.558 % (gap inclus), EV -0.8195 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 7.1 % x 31.39 % + P(rien) 92.9 % x -3.26 % ne couvrent pas P(stop) 0.0 % x 43.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 48.941 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.639, perte reelle 49.147 % (gap inclus), EV -0.8191 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 7.1 % x 31.39 % + P(rien) 92.9 % x -3.27 % ne couvrent pas P(stop) 0.0 % x 49.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 54.379 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.567, perte reelle 55.398 % (gap inclus), EV -0.8202 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 7.1 % x 31.39 % + P(rien) 92.9 % x -3.27 % ne couvrent pas P(stop) 0.0 % x 55.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 59.817 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.523, perte reelle 60.055 % (gap inclus), EV -0.8153 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 7.1 % x 31.39 % + P(rien) 92.9 % x -3.27 % ne couvrent pas P(stop) 0.0 % x 60.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 65.255 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.481, perte reelle 65.255 % (gap inclus), EV -0.817 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 7.1 % x 31.39 % + P(rien) 92.9 % x -3.27 % ne couvrent pas P(stop) 0.0 % x 65.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 70.693 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.444, perte reelle 70.693 % (gap inclus), EV -0.8174 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 7.1 % x 31.39 % + P(rien) 92.9 % x -3.27 % ne couvrent pas P(stop) 0.0 % x 70.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 76.131 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.412, perte reelle 76.131 % (gap inclus), EV -0.8174 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 7.1 % x 31.39 % + P(rien) 92.9 % x -3.27 % ne couvrent pas P(stop) 0.0 % x 76.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 81.569 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.385, perte reelle 81.569 % (gap inclus), EV -0.8174 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 7.1 % x 31.39 % + P(rien) 92.9 % x -3.27 % ne couvrent pas P(stop) 0.0 % x 81.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 87.007 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.361, perte reelle 87.007 % (gap inclus), EV -0.8174 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 7.1 % x 31.39 % + P(rien) 92.9 % x -3.27 % ne couvrent pas P(stop) 0.0 % x 87.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 77.8, ATR14 8.4614 (10.876 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.391 ATR = 4.252 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.544 % | 77.3769 | 93.96 % | 96.48 % | 97.08 % | 97.68 % | 98.17 % | 98.67 % |
| 0.1 ATR | 1.088 % | 76.9539 | 88.23 % | 92.04 % | 93.75 % | 94.95 % | 96.75 % | 97.33 % |
| 0.15 ATR | 1.631 % | 76.5308 | 81.59 % | 87.51 % | 90.22 % | 92.12 % | 94.52 % | 95.59 % |
| 0.2 ATR | 2.175 % | 76.1077 | 74.04 % | 82.18 % | 85.58 % | 88.79 % | 92.08 % | 93.64 % |
| 0.25 ATR | 2.719 % | 75.6846 | 67.71 % | 78.45 % | 82.76 % | 86.67 % | 89.64 % | 91.9 % |
| 0.35 ATR | 3.807 % | 74.8385 | 54.63 % | 69.28 % | 75.91 % | 81.62 % | 86.29 % | 89.23 % |
| 0.5 ATR | 5.438 % | 73.5693 | 37.63 % | 55.59 % | 64.01 % | 72.32 % | 79.29 % | 84.51 % |
| 0.75 ATR | 8.157 % | 71.4539 | 19.52 % | 38.27 % | 48.19 % | 59.49 % | 69.54 % | 77.03 % |
| 1.0 ATR | 10.876 % | 69.3386 | 9.56 % | 25.78 % | 35.79 % | 47.27 % | 60.41 % | 69.95 % |
| 1.25 ATR | 13.595 % | 67.2232 | 4.12 % | 14.9 % | 25.5 % | 36.57 % | 51.27 % | 62.56 % |
| 1.5 ATR | 16.314 % | 65.1079 | 2.11 % | 8.66 % | 17.64 % | 29.8 % | 44.26 % | 56.92 % |
| 2.0 ATR | 21.752 % | 60.8771 | 0.1 % | 2.92 % | 7.16 % | 16.26 % | 31.57 % | 47.08 % |
| 2.5 ATR | 27.19 % | 56.6464 | 0.1 % | 0.7 % | 2.12 % | 8.48 % | 21.02 % | 37.54 % |
| 3.0 ATR | 32.628 % | 52.4157 | 0.1 % | 0.3 % | 0.71 % | 4.14 % | 14.11 % | 27.79 % |
| 4.0 ATR | 43.503 % | 43.9543 | 0.0 % | 0.0 % | 0.2 % | 0.61 % | 5.69 % | 16.92 % |
| 6.0 ATR | 65.255 % | 27.0314 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.41 % | 3.9 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.43 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.29 ATR | 0.58 ATR | 0.65 ATR | 0.85 ATR | 1.02 ATR | 1.13 ATR | 1.45 ATR | 1.82 ATR |
| **3 s.** | 0.36 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.27 ATR | 1.43 ATR | 1.86 ATR | 2.21 ATR |
| **5 s.** | 0.46 ATR | 0.94 ATR | 1.05 ATR | 1.38 ATR | 1.68 ATR | 1.86 ATR | 2.40 ATR | 2.90 ATR |
| **10 s.** | 0.61 ATR | 1.29 ATR | 1.47 ATR | 1.94 ATR | 2.31 ATR | 2.57 ATR | 3.49 ATR | 4.26 ATR |
| **20 s.** | 0.82 ATR | 1.85 ATR | 2.11 ATR | 2.73 ATR | 3.26 ATR | 3.72 ATR | 5.06 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.435–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (5.438 %, prix 73.5692), p(touche) 37.63 % (en stress 85.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.653–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (8.157 %, prix 71.4539), p(touche) 38.27 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.814–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (10.876 %, prix 69.3385), p(touche) 35.79 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.053–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (13.595 %, prix 67.2231), p(touche) 36.57 % (en stress 95.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.474–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (16.314 %, prix 65.1077), p(touche) 44.26 % (en stress 100.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (63.6 % des re-echantillons)
- **20 seance(s)** : plage utile VIDE (borne basse 2.109 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 79.5 | side 15.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→58% · +3.0%→40% · +5.0%→19% · +8.0%→10%
- Range intraday médian 5.35% (p90 9.82%) · excursion haute méd. +2.51% / basse méd. −2.26%
- Profil de vol intra : ouverture 3.268% vs midi 1.123% vs clôture 1.265% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 17% · trend ↑2%/↓0% ; spike-down 69% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. 0.468% ; recovery-V 35%
- **σ réalisé intraday** 3.406% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 59% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 148.5395 (VA 146.6095–150.0835 ; dernier close 146.04)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 73% · **stop −3.89%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 38% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.78% (p90 −1.81%) · haut méd +0.88% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.68%) · haut méd +1.24% · range méd 2.55%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.06%) · haut méd +1.47% · range méd 2.95%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −3.47%) · haut méd +1.83% · range méd 3.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 146.01 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 76% (121/159) · gap 46% · délai 0.0min · rebond 44% (57/121) (MFE +0.7%)
   - −1.0% : fill 30min 55% · séance 67% (112/159) · gap 38% · délai 0.0min · rebond 48% (59/112) (MFE +0.91%)
   - −1.5% : fill 30min 45% · séance 61% (103/159) · gap 31% · délai 0.0min · rebond 53% (57/103) (MFE +1.16%)
   - −2.0% : fill 30min 38% · séance 54% (91/159) · gap 25% · délai 0.0min · rebond 60% (54/91) (MFE +1.25%)
   - −3.0% : fill 30min 28% · séance 41% (71/159) · gap 17% · délai 0.7min · rebond 52% (38/71) (MFE +1.5%)
   - −4.0% : fill 30min 21% · séance 32% (56/159) · gap 6% · délai 3.2min · rebond 72% (37/56) (MFE +1.65%)
   - −5.0% : fill 30min 17% · séance 25% (41/159) · gap 4% · délai 12.9min · rebond 73% (29/41) (MFE +2.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.65% (p90 −2.12%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.8% (p90 −2.19%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −2.14%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=888 jambes) : jambe baissière méd −1.12% (p90 −2.6%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 97% (74/75) · rebond 49% (34/74)
      · −2.0% : fill 86% (66/75) · rebond 58% (37/66)
      · −3.0% : fill 71% (57/75) · rebond 49% (30/57)
      · −4.0% : fill 60% (48/75) · rebond 72% (32/48)
      · −5.0% : fill 49% (37/75) · rebond 74% (27/37)
   - **flat** (18 séances) :
      · −1.0% : fill 74% (14/18) · rebond 55% (10/14)
      · −2.0% : fill 46% (9/18) · rebond 54% (5/9)
      · −3.0% : fill 38% (7/18) · rebond 71% (4/7)
      · −4.0% : fill 17% (4/18) · rebond 80% (3/4)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 30% (24/66) · rebond 41% (15/24)
      · −2.0% : fill 19% (16/66) · rebond 70% (12/16)
      · −3.0% : fill 7% (7/66) · rebond 67% (4/7)
      · −4.0% : fill 3% (4/66) · rebond 58% (2/4)
      · −5.0% : fill 2% (2/66) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 56% si les 15 1res min sont vertes (88 cas) · 32% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 71% si début vert vs 7% si rouge (base 46% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=90) : tient le vert **71%** · continue >prix actuel 43% ; creux résiduel méd -1.55% (q20 -2.88%) → **SL/trailing à −2.88%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +2.85% → **scale +1.62% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **7%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.18%** (au-delà de la MAE q10 -5.18%), cible rebond +1.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.82% .. +3.69%] · haut q95 +3.94% · bas q05 -3.62%
   - 60min (n=160) : retour [-3.45% .. +5.63%] · haut q95 +6.12% · bas q05 -4.56%
   - 2h (n=160) : retour [-4.42% .. +7.83%] · haut q95 +8.96% · bas q05 -5.49%
   - 4h (n=160) : retour [-5.2% .. +8.2%] · haut q95 +10.02% · bas q05 -6.02%
   - 6h (n=160) : retour [-5.31% .. +8.86%] · haut q95 +10.13% · bas q05 -6.26%
   - session (n=160) : retour [-5.14% .. +8.51%] · haut q95 +10.13% · bas q05 -6.52%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0.6% / strong 6.9%) · base = 12 séances trend-up (n_eff 8.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **47%**. Lecture précoce 30 min : signature présente → 17% vs absente 6% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.9% (p75 1.29% / p90 2.02%) · ~4.0 replis/séance, durée méd 30.47 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 20.0 min, n=46)
   - −1.0% → **74%** (reprise méd 17.06 min, n=20)
   - −1.5% → **58%** (reprise méd 13.97 min, n=11)
   - −2.0% → **46%** (reprise méd 31.23 min, n=8)
   - −3.0% → **38%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.02%** (p90, défaut prudent ; serré/agressif −1.29%) ; extension open→close méd +8.69% (q75 +10.68% / q95 +13.17%), MFE méd +10.02% / q90 +13.15%
   - Échelle scale-out : +10.02% (33%) / +12.77% (33%) / +13.15% (34%)
- **DÉSARMER** : repli > **−2.02%** depuis le plus-haut = décay → P(retournement) **81%** (préavis méd 157.2 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.15% : P(retournement après) 0% (mèche méd 0.05%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.81%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.83 · part idiosyncratique 0.17
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 16.5  _(survente)_
- **ADX** : 30.4  _(tendance etablie)_
- **MACD** : hist -4.816  _(pas de croisement recent)_
- **BB** : %B -0.03 · largeur 67.5%
- **ATR** : 8.46 (25.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.272  _(distribution)_
- **Vol ratio** : 1.86  _(volume au-dessus de la moyenne)_
- **Choppiness** : 20.8  _(marche directionnel)_
- **MA** : MA20 120.72 · MA50 138.91 · MA200 131.76  _(prix < MA20)_
- **Dist MA** : MA20 -35.6% · MA50 -44.0% · MA200 -41.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (694816 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
