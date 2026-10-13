# EVT

**Generated** : 2026-10-13T21:42:06.807003+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €2.44  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €2.44 (+6.6% vs entrée) · entrée €2.29 · stop €2.11 · T1 €2.37 · R/R 0.44  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-13 : 2.44 · ATR Wilder 0.151 (6.18 %)_
- **Swing** : plage **2.24 → 2.1** (-8.16 % a -14.03 % sous la cloture, 0.95 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 1.95 (-7.18 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **2.1 → 1.47** (-14.03 % a -39.92 % sous la cloture, 4.19 ATR) — touchee 48 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 1.32 (-10.28 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.61 ATR sous le plus haut 20 s., RSI(2) 0.5. Limite **2.37** (seance suivante), stop catastrophe 1.76, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Resistances reelles au-dessus : 2.71-2.77 (B, 10.88 %) ; 3.1-3.14 (A, 26.76 %) ; 3.18-3.24 (B, 29.95 %) ; 3.37-3.41 (A, 38.05 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (18.57 %)** : le gap seul le franchit 0.157 % des séances (2 fois sur 1274).
   - exécution **8.442 pt plus bas** dans le cas TYPIQUE (médiane), 12.763 au p90, **13.843 au pire**
   - perte réelle **27.012 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 18.57 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0133 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0271** [0.0101 ; 0.0597] _(largeur 5.0 pt, n_eff 173.1)_
   - swing : **0.2956** [0.2494 ; 0.3452] _(largeur 9.6 pt, n_eff 345.8)_
   - deep : **0.2833** [0.2378 ; 0.3325] _(largeur 9.5 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-5.0 %** | CVaR **-10.03 %** | vol 3.64 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.93 % contre 3.58 % aujourd'hui, rapport 0.54)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.04 % vs -11.16 % si l'on extrapolait par √5 _(rapport 1.169 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1145** (β de hausse 0.9374, asymétrie 1.1889) vs GDAXI — 599 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 2.3305 sur atr_grid (0.75 ATR, 4.643 %) — p(stop avant cible) 0.644 [0.59 ; 0.69], R/R 7.181, perte reelle 5.172 % (gap inclus), CVaR 10.892 %, EV -0.7999 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2442 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 7.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.644, borne haute 0.693 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.284 %) — p(stop avant cible) 0.3467 [0.30 ; 0.40], R/R 3.392, perte reelle 10.949 % (gap inclus), EV -1.6697 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.67 %) : P(cible) 0.4 % x 37.14 % + P(rien) 65.0 % x 3.07 % ne couvrent pas P(stop) 34.7 % x 10.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.548 %) — p(stop avant cible) 0.8653 [0.83 ; 0.90], R/R 20.255, perte reelle 1.833 % (gap inclus), EV -0.3753 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 20.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.865, borne haute 0.898 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 0.2 % x 37.14 % + P(rien) 13.3 % x 8.63 % ne couvrent pas P(stop) 86.5 % x 1.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.095 %) — p(stop avant cible) 0.7428 [0.69 ; 0.79], R/R 10.599, perte reelle 3.504 % (gap inclus), EV -0.5967 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 10.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.743, borne haute 0.787 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 0.2 % x 37.14 % + P(rien) 25.5 % x 7.56 % ne couvrent pas P(stop) 74.3 % x 3.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.643 %) — p(stop avant cible) 0.644 [0.59 ; 0.69], R/R 7.181, perte reelle 5.172 % (gap inclus), EV -0.7999 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 7.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.644, borne haute 0.693 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.80 %) : P(cible) 0.2 % x 37.14 % + P(rien) 35.4 % x 6.90 % ne couvrent pas P(stop) 64.4 % x 5.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 6.19 %) — p(stop avant cible) 0.5308 [0.48 ; 0.58], R/R 5.179, perte reelle 7.171 % (gap inclus), EV -1.1435 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.531, borne haute 0.583 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 15.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 0.4 % x 37.14 % + P(rien) 46.6 % x 5.44 % ne couvrent pas P(stop) 53.1 % x 7.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 7.738 %) — p(stop avant cible) 0.4213 [0.37 ; 0.47], R/R 3.997, perte reelle 9.291 % (gap inclus), EV -1.5142 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.51 %) : P(cible) 0.4 % x 37.14 % + P(rien) 57.5 % x 3.95 % ne couvrent pas P(stop) 42.1 % x 9.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 10.833 %) — p(stop avant cible) 0.3042 [0.26 ; 0.35], R/R 2.978, perte reelle 12.472 % (gap inclus), EV -1.8792 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.88 %) : P(cible) 0.4 % x 37.14 % + P(rien) 69.2 % x 2.58 % ne couvrent pas P(stop) 30.4 % x 12.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 12.38 %) — p(stop avant cible) 0.2359 [0.19 ; 0.28], R/R 2.609, perte reelle 14.233 % (gap inclus), EV -1.9833 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.98 %) : P(cible) 0.4 % x 37.14 % + P(rien) 76.1 % x 1.64 % ne couvrent pas P(stop) 23.6 % x 14.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 13.928 %) — p(stop avant cible) 0.1699 [0.13 ; 0.21], R/R 2.309, perte reelle 16.081 % (gap inclus), EV -1.9424 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 0.4 % x 37.14 % + P(rien) 82.7 % x 0.80 % ne couvrent pas P(stop) 17.0 % x 16.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 15.475 %) — p(stop avant cible) 0.1316 [0.10 ; 0.17], R/R 2.069, perte reelle 17.951 % (gap inclus), EV -1.9513 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.95 %) : P(cible) 0.4 % x 37.14 % + P(rien) 86.5 % x 0.33 % ne couvrent pas P(stop) 13.2 % x 17.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 17.023 %) — p(stop avant cible) 0.1134 [0.08 ; 0.15], R/R 1.912, perte reelle 19.422 % (gap inclus), EV -1.9747 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.97 %) : P(cible) 0.4 % x 37.14 % + P(rien) 88.3 % x 0.11 % ne couvrent pas P(stop) 11.3 % x 19.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 18.57 %) — p(stop avant cible) 0.0937 [0.07 ; 0.13], R/R 1.784, perte reelle 20.817 % (gap inclus), EV -1.9271 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 0.4 % x 37.14 % + P(rien) 90.3 % x -0.12 % ne couvrent pas P(stop) 9.4 % x 20.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 21.665 %) — p(stop avant cible) 0.0869 [0.06 ; 0.12], R/R 1.631, perte reelle 22.765 % (gap inclus), EV -2.0444 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.04 %) : P(cible) 0.4 % x 37.14 % + P(rien) 91.0 % x -0.22 % ne couvrent pas P(stop) 8.7 % x 22.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 24.76 %) — p(stop avant cible) 0.073 [0.05 ; 0.10], R/R 1.478, perte reelle 25.13 % (gap inclus), EV -2.1549 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.15 %) : P(cible) 0.4 % x 37.14 % + P(rien) 92.3 % x -0.49 % ne couvrent pas P(stop) 7.3 % x 25.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 27.855 %) — p(stop avant cible) 0.0541 [0.03 ; 0.08], R/R 1.323, perte reelle 28.08 % (gap inclus), EV -2.2912 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.29 %) : P(cible) 0.4 % x 37.14 % + P(rien) 94.2 % x -0.96 % ne couvrent pas P(stop) 5.4 % x 28.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 30.95 %) — p(stop avant cible) 0.0405 [0.02 ; 0.07], R/R 1.194, perte reelle 31.103 % (gap inclus), EV -2.373 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.37 %) : P(cible) 0.4 % x 37.14 % + P(rien) 95.6 % x -1.30 % ne couvrent pas P(stop) 4.0 % x 31.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 34.045 %) — p(stop avant cible) 0.0405 [0.02 ; 0.07], R/R 1.09, perte reelle 34.08 % (gap inclus), EV -2.4936 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.49 %) : P(cible) 0.4 % x 37.14 % + P(rien) 95.6 % x -1.30 % ne couvrent pas P(stop) 4.0 % x 34.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 37.141 %) — p(stop avant cible) 0.0187 [0.01 ; 0.04], R/R 1.0, perte reelle 37.141 % (gap inclus), EV -2.4341 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.43 %) : P(cible) 0.4 % x 37.14 % + P(rien) 97.8 % x -1.91 % ne couvrent pas P(stop) 1.9 % x 37.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 40.236 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.923, perte reelle 40.236 % (gap inclus), EV -2.3521 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.35 %) : P(cible) 0.4 % x 37.14 % + P(rien) 99.5 % x -2.44 % ne couvrent pas P(stop) 0.1 % x 40.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 43.331 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.857, perte reelle 43.331 % (gap inclus), EV -2.347 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.35 %) : P(cible) 0.4 % x 37.14 % + P(rien) 99.7 % x -2.49 % ne couvrent pas P(stop) 0.0 % x 43.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 46.426 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.8, perte reelle 46.426 % (gap inclus), EV -2.347 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.35 %) : P(cible) 0.4 % x 37.14 % + P(rien) 99.7 % x -2.49 % ne couvrent pas P(stop) 0.0 % x 46.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 49.521 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.75, perte reelle 49.521 % (gap inclus), EV -2.347 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.35 %) : P(cible) 0.4 % x 37.14 % + P(rien) 99.7 % x -2.49 % ne couvrent pas P(stop) 0.0 % x 49.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 2.444, ATR14 0.1513 (6.19 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.368 ATR = 2.278 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.31 % | 2.4364 | 88.95 % | 91.71 % | 93.58 % | 95.54 % | 97.31 % | 98.29 % |
| 0.1 ATR | 0.619 % | 2.4289 | 81.26 % | 86.67 % | 89.62 % | 92.67 % | 95.62 % | 97.19 % |
| 0.15 ATR | 0.929 % | 2.4213 | 75.05 % | 82.82 % | 86.56 % | 89.9 % | 93.83 % | 96.08 % |
| 0.2 ATR | 1.238 % | 2.4137 | 68.84 % | 78.87 % | 83.3 % | 87.13 % | 91.84 % | 94.77 % |
| 0.25 ATR | 1.548 % | 2.4062 | 63.21 % | 75.62 % | 80.24 % | 84.75 % | 89.95 % | 93.57 % |
| 0.35 ATR | 2.167 % | 2.3911 | 51.97 % | 67.52 % | 73.81 % | 79.9 % | 86.07 % | 91.56 % |
| 0.5 ATR | 3.095 % | 2.3684 | 35.7 % | 55.08 % | 62.94 % | 70.99 % | 80.2 % | 88.34 % |
| 0.75 ATR | 4.643 % | 2.3305 | 19.23 % | 37.81 % | 47.53 % | 59.5 % | 71.74 % | 82.11 % |
| 1.0 ATR | 6.19 % | 2.2927 | 10.16 % | 25.07 % | 35.97 % | 47.52 % | 62.29 % | 75.68 % |
| 1.25 ATR | 7.738 % | 2.2549 | 4.83 % | 17.28 % | 27.37 % | 39.5 % | 55.72 % | 70.55 % |
| 1.5 ATR | 9.285 % | 2.2171 | 3.06 % | 11.35 % | 19.66 % | 31.49 % | 48.56 % | 65.43 % |
| 2.0 ATR | 12.38 % | 2.1414 | 1.38 % | 5.03 % | 9.49 % | 19.41 % | 35.12 % | 53.67 % |
| 2.5 ATR | 15.475 % | 2.0658 | 0.49 % | 2.76 % | 5.73 % | 12.18 % | 27.76 % | 45.93 % |
| 3.0 ATR | 18.57 % | 1.9901 | 0.39 % | 1.68 % | 3.75 % | 8.61 % | 20.9 % | 39.1 % |
| 4.0 ATR | 24.76 % | 1.8389 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 11.74 % | 25.23 % |
| 6.0 ATR | 37.141 % | 1.5363 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.16 ATR | 1.61 ATR | 2.01 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.33 ATR | 1.49 ATR | 1.98 ATR | 2.68 ATR |
| **5 s.** | 0.43 ATR | 0.95 ATR | 1.08 ATR | 1.45 ATR | 1.77 ATR | 1.98 ATR | 2.81 ATR | 3.81 ATR |
| **10 s.** | 0.65 ATR | 1.45 ATR | 1.63 ATR | 2.14 ATR | 2.70 ATR | 3.10 ATR | 4.53 ATR | hors grille |
| **20 s.** | 1.03 ATR | 2.24 ATR | 2.57 ATR | 3.44 ATR | 4.04 ATR | 4.91 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.414–0.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (61.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.643 %, prix 2.3305), p(touche) 37.81 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (70.9 % des re-echantillons)
- **3 seance(s)** : plage utile 0.805–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.19 %, prix 2.2927), p(touche) 35.97 % (en stress 96.08 %)  ✅ optimum identifie (68.9 % des re-echantillons)
- **5 seance(s)** : plage utile 1.079–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.738 %, prix 2.2549), p(touche) 39.5 % (en stress 94.06 %)  ✅ optimum identifie (79.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.632–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.38 %, prix 2.1414), p(touche) 35.12 % (en stress 97.03 %)  ✅ optimum identifie (78.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.568–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (18.57 %, prix 1.9901), p(touche) 39.1 % (en stress 98.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (84.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.027 | EV/share : €-0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 61.1 | bear 5.0 | side 34.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→65% · +2.0%→42% · +3.0%→23% · +5.0%→10% · +8.0%→2%
- Range intraday médian 3.96% (p90 6.52%) · excursion haute méd. +1.57% / basse méd. −1.88%
- Profil de vol intra : ouverture 2.571% vs midi 1.19% vs clôture 1.188% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 60% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.152)_ ; drift intra méd. -0.511% ; recovery-V 19%
- **σ réalisé intraday** 3.126% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 72% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 2.9518 (VA 2.9403–2.9711 ; dernier close 2.918)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 25% · rebond 70% · **stop −1.87%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.81 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 37% (gap-down >1% 7% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −2.18%) · haut méd +0.41% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.66%) · haut méd +0.54% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −3.17%) · haut méd +0.67% · range méd 2.04%
- Excursion ouverture 60min (n=160) : bas méd −1.06% (p90 −3.37%) · haut méd +0.84% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 81% (129/159) · gap 20% · délai 0.4min · rebond 64% (86/129) (MFE +1.48%)
   - −1.0% : fill 30min 38% · séance 67% (111/159) · gap 7% · délai 9.3min · rebond 62% (74/111) (MFE +1.42%)
   - −1.5% : fill 30min 26% · séance 55% (92/159) · gap 3% · délai 31.6min · rebond 60% (58/92) (MFE +1.25%)
   - −2.0% : fill 30min 16% · séance 46% (77/159) · gap 3% · délai 67.4min · rebond 54% (43/77) (MFE +1.17%)
   - −3.0% : fill 30min 7% · séance 25% (45/159) · gap 2% · délai 86.4min · rebond 70% (32/45) (MFE +1.52%)
   - −4.0% : fill 30min 3% · séance 10% (24/159) · gap 1% · délai 359.9min · rebond 38% (13/24) (MFE +0.64%)
   - −5.0% : fill 30min 2% · séance 4% (13/159) · gap 1% · délai 33.7min · rebond 33% (7/13) (MFE +0.67%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −2.16%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.23% (p90 −1.65%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.06% (p90 −1.83%) → stop au-delà de −1.24% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=811 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~9.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 74% (46/55) · rebond 63% (31/46)
      · −2.0% : fill 52% (35/55) · rebond 49% (19/35)
      · −3.0% : fill 26% (22/55) · rebond 62% (15/22)
      · −4.0% : fill 15% (15/55) · rebond 34% (8/15)
      · −5.0% : fill 10% (10/55) · rebond 33% (5/10)
   - **flat** (30 séances) :
      · −1.0% : fill 74% (23/30) · rebond 58% (14/23)
      · −2.0% : fill 50% (17/30) · rebond 49% (8/17)
      · −3.0% : fill 29% (10/30) · rebond 83% (8/10)
      · −4.0% : fill 10% (4/30) · rebond 14% (1/4)
      · −5.0% : fill 6% (2/30) · rebond 23% (1/2)
   - **gap-up** (74 séances) :
      · −1.0% : fill 61% (42/74) · rebond 64% (29/42)
      · −2.0% : fill 41% (25/74) · rebond 60% (16/25)
      · −3.0% : fill 22% (13/74) · rebond 68% (9/13)
      · −4.0% : fill 8% (5/74) · rebond 55% (4/5)
      · −5.0% : fill 0% (1/74) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 60% si les 15 1res min sont vertes (75 cas) · 27% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **12min** → P(séance verte=clôture>ouverture) 58% si début vert vs 28% si rouge (base 43% · écart 30 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **58%** · continue >prix actuel 38% ; creux résiduel méd -1.71% (q20 -2.8%) → **SL/trailing à −2.8%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.68% / q75 +2.35% → **scale +1.68% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **28%** (continue à baisser 59%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.09%** (au-delà de la MAE q10 -4.09%), cible rebond +1.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.83% .. +3.3%] · haut q95 +3.68% · bas q05 -3.73%
   - 60min (n=160) : retour [-3.03% .. +4.12%] · haut q95 +4.72% · bas q05 -3.81%
   - 2h (n=160) : retour [-3.2% .. +3.32%] · haut q95 +5.18% · bas q05 -4.3%
   - 4h (n=160) : retour [-3.24% .. +4.34%] · haut q95 +5.21% · bas q05 -4.31%
   - 6h (n=160) : retour [-3.57% .. +5.54%] · haut q95 +5.95% · bas q05 -4.33%
   - session (n=160) : retour [-4.49% .. +4.05%] · haut q95 +6.33% · bas q05 -5.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.08 · part idiosyncratique 0.92
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.3  _(momentum baissier)_
- **ADX** : 23.6  _(pas de tendance nette)_
- **MACD** : hist -0.027  _(bearish_recent)_
- **BB** : %B -0.12 · largeur 22.5%
- **ATR** : 0.15 (17.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.36  _(distribution)_
- **Vol ratio** : 1.32  _(volume normal)_
- **Choppiness** : 40.2  _(transition)_
- **MA** : MA20 2.84 · MA50 3.12 · MA200 4.59  _(prix < MA20)_
- **Dist MA** : MA20 -13.8% · MA50 -21.7% · MA200 -46.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (945474 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
