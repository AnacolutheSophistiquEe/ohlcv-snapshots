# SOFI

**Generated** : 2026-10-26T01:30:29.556834+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $14.61  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-27 — SOFI earnings (J-1 sess · earnings)  
> ↳ spot $14.61 (+1.2% vs entrée) · entrée $14.43 · stop $14.21 · T1 $14.75 · R/R 1.45  
> ↳ P(T1 av. stop) 21 % _(réel 5 s)_ · EV/risk -0.149 _(réel 5 s)_ · _probas brutes, non calibrées · n=0_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 14.61 · ATR Wilder 0.6466 (4.42 %)_
- **Swing** : plage **13.77 → 13.3** (-5.75 % a -8.99 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 13.75-13.9 (A) ; 13.42-13.6 (C). stop INDICATIF 12.54 (-5.75 % sous le bas ; sous le support 12.86-13.01 (- 0,5 ATR)).
- **Deep** : plage **13.3 → 12.1** (-8.99 % a -17.21 % sous la cloture, 1.86 ATR) — touchee 45 % → 15 % du temps en 20 seances ; supports reels dans la plage : 12.86-13.01 (B) ; 12.5-12.74 (A). stop INDICATIF 11.11 (-8.2 % sous le bas ; sous le support 11.43-11.65 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.79 ATR sous le plus haut 20 s., RSI(2) 30.8 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 13.75-13.9 (A, -4.89 %) ; 13.42-13.6 (C, -6.94 %) ; 12.86-13.01 (B, -10.98 %) ; 12.5-12.74 (A, -12.83 %) ; 11.43-11.65 (B, -20.29 %) ; 10.49-10.49 (C, -28.22 %)
- Resistances reelles au-dessus : 15.2-15.5 (A, 4.0 %) ; 15.53-15.65 (A, 6.26 %) ; 16.25-16.53 (A, 11.19 %) ; 16.61-16.93 (A, 13.65 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.23 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1254).
   - exécution **2.093 pt plus bas** dans le cas TYPIQUE (médiane), 2.878 au p90, **3.875 au pire**
   - perte réelle **8.985 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 7.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0126 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.517 % | pire -11.105 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5386** [0.4642 ; 0.6117] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.5291** [0.4764 ; 0.5813] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5001** [0.4476 ; 0.5526] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : deep (25.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-5.85 %** | CVaR **-7.65 %** | vol 3.41 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.16 % contre 3.21 % aujourd'hui, rapport 1.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.28 % si l'on extrapolait par √5 _(rapport 1.015 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8012** (β de hausse 1.7182, asymétrie 1.0484) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.334× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 13.5223 sur support (1.18 ATR, 7.477 %) — p(stop avant cible) 0.4935 [0.44 ; 0.55], R/R 3.915, perte reelle 7.827 % (gap inclus), CVaR 10.585 %, EV -1.2495 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.924 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.18 ATR (stop 7.477 %) — p(stop avant cible) 0.4935 [0.44 ; 0.55], R/R 3.915, perte reelle 7.827 % (gap inclus), EV -1.2495 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 1.1 % x 30.65 % + P(rien) 49.5 % x 4.57 % ne couvrent pas P(stop) 49.4 % x 7.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.098 %) — p(stop avant cible) 0.9391 [0.91 ; 0.96], R/R 26.307, perte reelle 1.165 % (gap inclus), EV -0.251 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 26.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.939, borne haute 0.961 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.5 % x 30.65 % + P(rien) 5.6 % x 12.41 % ne couvrent pas P(stop) 93.9 % x 1.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.197 %) — p(stop avant cible) 0.8865 [0.85 ; 0.92], R/R 12.798, perte reelle 2.395 % (gap inclus), EV -0.7374 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 12.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.886, borne haute 0.917 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 0.9 % x 30.65 % + P(rien) 10.5 % x 10.68 % ne couvrent pas P(stop) 88.6 % x 2.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 3.295 %) — p(stop avant cible) 0.7995 [0.75 ; 0.84], R/R 8.566, perte reelle 3.578 % (gap inclus), EV -1.0397 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.799, borne haute 0.839 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 1.0 % x 30.65 % + P(rien) 19.1 % x 7.96 % ne couvrent pas P(stop) 80.0 % x 3.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 1.18 ATR (stop 6.484 %) — p(stop avant cible) 0.5507 [0.50 ; 0.60], R/R 4.54, perte reelle 6.751 % (gap inclus), EV -1.0375 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.551, borne haute 0.603 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 1.1 % x 30.65 % + P(rien) 43.8 % x 5.32 % ne couvrent pas P(stop) 55.1 % x 6.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 8.786 %) — p(stop avant cible) 0.4142 [0.36 ; 0.47], R/R 3.326, perte reelle 9.214 % (gap inclus), EV -1.4538 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.45 %) : P(cible) 1.1 % x 30.65 % + P(rien) 57.4 % x 3.51 % ne couvrent pas P(stop) 41.4 % x 9.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 9.885 %) — p(stop avant cible) 0.3636 [0.31 ; 0.42], R/R 2.975, perte reelle 10.302 % (gap inclus), EV -1.6002 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 1.2 % x 30.65 % + P(rien) 62.5 % x 2.86 % ne couvrent pas P(stop) 36.4 % x 10.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 10.983 %) — p(stop avant cible) 0.2919 [0.25 ; 0.34], R/R 2.708, perte reelle 11.315 % (gap inclus), EV -1.4407 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.44 %) : P(cible) 1.2 % x 30.65 % + P(rien) 69.6 % x 2.16 % ne couvrent pas P(stop) 29.2 % x 11.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 12.081 %) — p(stop avant cible) 0.2316 [0.19 ; 0.28], R/R 2.48, perte reelle 12.357 % (gap inclus), EV -1.2178 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 1.2 % x 30.65 % + P(rien) 75.7 % x 1.69 % ne couvrent pas P(stop) 23.2 % x 12.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 13.18 %) — p(stop avant cible) 0.1825 [0.14 ; 0.23], R/R 2.281, perte reelle 13.436 % (gap inclus), EV -0.9605 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 1.2 % x 30.65 % + P(rien) 80.6 % x 1.40 % ne couvrent pas P(stop) 18.2 % x 13.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 15.376 %) — p(stop avant cible) 0.1036 [0.07 ; 0.14], R/R 1.978, perte reelle 15.498 % (gap inclus), EV -0.7219 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 1.2 % x 30.65 % + P(rien) 88.5 % x 0.59 % ne couvrent pas P(stop) 10.4 % x 15.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 17.573 %) — p(stop avant cible) 0.0538 [0.03 ; 0.08], R/R 1.733, perte reelle 17.688 % (gap inclus), EV -0.6174 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 1.2 % x 30.65 % + P(rien) 93.4 % x -0.03 % ne couvrent pas P(stop) 5.4 % x 17.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 19.77 %) — p(stop avant cible) 0.0414 [0.02 ; 0.07], R/R 1.548, perte reelle 19.797 % (gap inclus), EV -0.653 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 1.2 % x 30.65 % + P(rien) 94.7 % x -0.21 % ne couvrent pas P(stop) 4.1 % x 19.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 21.966 %) — p(stop avant cible) 0.0295 [0.02 ; 0.05], R/R 1.384, perte reelle 22.151 % (gap inclus), EV -0.6996 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 1.2 % x 30.65 % + P(rien) 95.9 % x -0.43 % ne couvrent pas P(stop) 2.9 % x 22.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 24.163 %) — p(stop avant cible) 0.02 [0.01 ; 0.04], R/R 1.257, perte reelle 24.38 % (gap inclus), EV -0.6817 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 1.2 % x 30.65 % + P(rien) 96.8 % x -0.57 % ne couvrent pas P(stop) 2.0 % x 24.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 26.359 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 1.148, perte reelle 26.704 % (gap inclus), EV -0.5726 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 1.2 % x 30.65 % + P(rien) 98.4 % x -0.85 % ne couvrent pas P(stop) 0.4 % x 26.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 28.556 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 1.073, perte reelle 28.574 % (gap inclus), EV -0.5662 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 1.2 % x 30.65 % + P(rien) 98.6 % x -0.87 % ne couvrent pas P(stop) 0.3 % x 28.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 30.753 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.996, perte reelle 30.755 % (gap inclus), EV -0.5708 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 1.2 % x 30.65 % + P(rien) 98.6 % x -0.87 % ne couvrent pas P(stop) 0.2 % x 30.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 32.949 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.93, perte reelle 32.949 % (gap inclus), EV -0.5628 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 1.2 % x 30.65 % + P(rien) 98.6 % x -0.87 % ne couvrent pas P(stop) 0.2 % x 32.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 35.146 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.869, perte reelle 35.273 % (gap inclus), EV -0.5597 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 1.2 % x 30.65 % + P(rien) 98.7 % x -0.89 % ne couvrent pas P(stop) 0.1 % x 35.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 14.615, ATR14 0.6421 (4.393 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.378 ATR = 1.661 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.22 % | 14.5829 | 92.86 % | 95.77 % | 97.08 % | 97.58 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.439 % | 14.5508 | 85.11 % | 89.33 % | 92.04 % | 93.33 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.659 % | 14.5187 | 78.87 % | 84.59 % | 88.0 % | 90.4 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.879 % | 14.4866 | 71.63 % | 79.36 % | 83.37 % | 86.87 % | 90.56 % | 93.33 % |
| 0.25 ATR | 1.098 % | 14.4545 | 66.3 % | 75.13 % | 80.24 % | 84.55 % | 89.34 % | 92.21 % |
| 0.35 ATR | 1.538 % | 14.3903 | 52.82 % | 65.46 % | 72.38 % | 78.79 % | 85.89 % | 89.03 % |
| 0.5 ATR | 2.197 % | 14.294 | 37.53 % | 53.27 % | 61.79 % | 69.6 % | 79.9 % | 84.92 % |
| 0.75 ATR | 3.295 % | 14.1334 | 20.42 % | 37.06 % | 46.98 % | 57.47 % | 70.56 % | 78.46 % |
| 1.0 ATR | 4.393 % | 13.9729 | 8.75 % | 24.57 % | 34.07 % | 45.35 % | 60.41 % | 69.95 % |
| 1.25 ATR | 5.492 % | 13.8124 | 4.12 % | 15.21 % | 24.29 % | 36.06 % | 51.37 % | 63.49 % |
| 1.5 ATR | 6.59 % | 13.6519 | 1.91 % | 9.47 % | 16.63 % | 27.47 % | 43.55 % | 57.23 % |
| 2.0 ATR | 8.786 % | 13.3309 | 0.6 % | 4.53 % | 8.57 % | 15.66 % | 30.05 % | 46.26 % |
| 2.5 ATR | 10.983 % | 13.0098 | 0.3 % | 1.91 % | 4.03 % | 9.8 % | 20.41 % | 36.41 % |
| 3.0 ATR | 13.18 % | 12.6888 | 0.1 % | 0.81 % | 2.82 % | 6.26 % | 14.21 % | 28.62 % |
| 4.0 ATR | 17.573 % | 12.0467 | 0.0 % | 0.3 % | 0.6 % | 2.42 % | 7.31 % | 15.28 % |
| 6.0 ATR | 26.359 % | 10.7626 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.18 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.95 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.79 ATR | 1.03 ATR | 1.23 ATR | 1.39 ATR | 1.91 ATR | 2.39 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.01 ATR | 1.34 ATR | 1.60 ATR | 1.82 ATR | 2.48 ATR | 3.33 ATR |
| **10 s.** | 0.63 ATR | 1.29 ATR | 1.45 ATR | 1.89 ATR | 2.26 ATR | 2.53 ATR | 3.61 ATR | 4.72 ATR |
| **20 s.** | 0.85 ATR | 1.83 ATR | 2.06 ATR | 2.72 ATR | 3.27 ATR | 3.65 ATR | 4.87 ATR | 5.70 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.427–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.197 %, prix 14.2939), p(touche) 37.53 % (en stress 83.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.628–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.295 %, prix 14.1334), p(touche) 37.06 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.788–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.393 %, prix 13.973), p(touche) 34.07 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.009–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.492 %, prix 13.8123), p(touche) 36.06 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.454–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.59 %, prix 13.6519), p(touche) 43.55 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.064–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.983 %, prix 13.0098), p(touche) 36.41 % (en stress 98.98 %)  ✅ optimum identifie (77.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 17.4 | bear 5.0 | side 77.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.29% → cible +2.226% / stop −1.499%, p_fill 65%, n_eff≈71.7) : P(cible|rempli) **21%** · **EV/risk -0.149** (×p_fill ; si rempli -0.34% du capital)
  - **swing** (entrée dip −2.837% → cible +6.054% / stop −4.521%, p_fill 52%, n_eff≈61.5) : P(cible|rempli) **36%** · **EV/risk +0.077** (×p_fill ; si rempli +0.67% du capital)
  - **deep** (entrée dip −4.39% → cible +7.773% / stop −6.892%, p_fill 45%, n_eff≈50.2) : P(cible|rempli) **34%** · **EV/risk -0.034** (×p_fill ; si rempli -0.52% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→65% · +2.0%→42% · +3.0%→31% · +5.0%→10% · +8.0%→2%
- Range intraday médian 4.0% (p90 6.7%) · excursion haute méd. +1.55% / basse méd. −2.04%
- Profil de vol intra : ouverture 2.79% vs midi 0.796% vs clôture 0.916% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 21% · trend ↑2%/↓0% ; spike-down 58% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.156 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.193% ; recovery-V 30%
- **σ réalisé intraday** 2.295% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 53% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 14.6352 (VA 14.5663–14.6583 ; dernier close 14.62)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 65% · **stop −2.96%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 50% (gap-down >1% 27% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.59% (p90 −1.66%) · haut méd +0.66% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.81% (p90 −2.19%) · haut méd +0.86% · range méd 2.02%
- Excursion ouverture 30min (n=160) : bas méd −1.03% (p90 −3.07%) · haut méd +0.91% · range méd 2.35%
- Excursion ouverture 60min (n=160) : bas méd −1.13% (p90 −3.56%) · haut méd +1.02% · range méd 2.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 14.615 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (121/159) · gap 37% · délai 0.0min · rebond 52% (68/121) (MFE +1.12%)
   - −1.0% : fill 30min 50% · séance 64% (103/159) · gap 27% · délai 0.9min · rebond 44% (52/103) (MFE +0.88%)
   - −1.5% : fill 30min 42% · séance 56% (92/159) · gap 22% · délai 1.2min · rebond 61% (59/92) (MFE +1.28%)
   - −2.0% : fill 30min 31% · séance 44% (71/159) · gap 10% · délai 2.8min · rebond 65% (48/71) (MFE +1.55%)
   - −3.0% : fill 30min 8% · séance 29% (49/159) · gap 1% · délai 68.9min · rebond 44% (28/49) (MFE +0.9%)
   - −4.0% : fill 30min 5% · séance 14% (27/159) · gap 1% · délai 91.2min · rebond 47% (16/27) (MFE +0.59%)
   - −5.0% : fill 30min 1% · séance 8% (13/159) · gap 1% · délai 214.3min · rebond 45% (6/13) (MFE +0.64%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −1.8%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.25% (p90 −1.74%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.22% (p90 −1.25%) → stop au-delà de −0.84% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=576 jambes) : jambe baissière méd −1.02% (p90 −2.7%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 91% (59/62) · rebond 42% (30/59)
      · −2.0% : fill 79% (51/62) · rebond 72% (35/51)
      · −3.0% : fill 50% (35/62) · rebond 45% (21/35)
      · −4.0% : fill 26% (21/62) · rebond 58% (14/21)
      · −5.0% : fill 13% (10/62) · rebond 34% (4/10)
   - **flat** (24 séances) :
      · −1.0% : fill 73% (16/24) · rebond 26% (5/16)
      · −2.0% : fill 42% (9/24) · rebond 40% (5/9)
      · −3.0% : fill 38% (8/24) · rebond 32% (3/8)
      · −4.0% : fill 19% (4/24) · rebond 15% (1/4)
      · −5.0% : fill 15% (2/24) · rebond 64% (1/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 35% (28/73) · rebond 63% (17/28)
      · −2.0% : fill 11% (11/73) · rebond 56% (8/11)
      · −3.0% : fill 6% (6/73) · rebond 60% (4/6)
      · −4.0% : fill 2% (2/73) · rebond 20% (1/2)
      · −5.0% : fill 0% (1/73) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 70% si les 15 1res min sont vertes (75 cas) · 25% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **28min** → P(séance verte=clôture>ouverture) 76% si début vert vs 18% si rouge (base 46% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 215min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **76%** · continue >prix actuel 49% ; creux résiduel méd -1.53% (q20 -2.61%) → **SL/trailing à −2.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.24% / q75 +2.49% → **scale +1.24% / runner +2.49%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **18%** (continue à baisser 64%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.81%** (au-delà de la MAE q10 -2.81%), cible rebond +1.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.87% .. +3.38%] · haut q95 +3.7% · bas q05 -3.56%
   - 60min (n=160) : retour [-3.14% .. +4.07%] · haut q95 +4.61% · bas q05 -4.01%
   - 2h (n=160) : retour [-3.61% .. +4.53%] · haut q95 +5.04% · bas q05 -4.49%
   - 4h (n=160) : retour [-3.96% .. +4.31%] · haut q95 +5.5% · bas q05 -5.12%
   - 6h (n=160) : retour [-4.61% .. +4.09%] · haut q95 +5.63% · bas q05 -5.18%
   - session (n=160) : retour [-4.53% .. +4.64%] · haut q95 +5.63% · bas q05 -5.28%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.71%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.54 · part idiosyncratique 0.46
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-27 — SOFI earnings (J-1 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-27 — SOFI earnings (J-1 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-27 — SOFI earnings (J-1 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 36.0  _(momentum baissier)_
- **ADX** : 24.2  _(pas de tendance nette)_
- **MACD** : hist 0.01  _(bullish_recent)_
- **BB** : %B 0.22 · largeur 15.4%
- **ATR** : 0.64 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.169  _(distribution)_
- **Vol ratio** : 0.86  _(volume normal)_
- **Choppiness** : 51.6  _(transition)_
- **MA** : MA20 15.28 · MA50 16.74 · MA200 18.05  _(prix < MA20)_
- **Dist MA** : MA20 -4.3% · MA50 -12.7% · MA200 -19.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (779445 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
