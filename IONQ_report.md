# IONQ

**Generated** : 2026-11-16T01:25:53.622888+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 7.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $28.88  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (15 séance(s) de retard, drapeau lu sur first_passage_by_horizon); usable=false (intervalle le plus large 29.7 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $28.88 (+7.1% vs entrée) · entrée $26.97 · stop $24.04 · T1 $31.52 · R/R 1.55  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-13 : 28.88 · ATR Wilder 2.78 (9.64 %)_
- **Swing** : plage **25.39 → 23.19** (-12.08 % a -19.69 % sous la cloture, 0.79 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 24.92-25.92 (A) ; 22.27-23.49 (B). stop INDICATIF 19.22 (-17.14 % sous le bas ; sous le support 20.61-21.5 (- 0,5 ATR)).
- **Deep** : plage **23.19 → 18.37** (-19.69 % a -36.38 % sous la cloture, 1.73 ATR) — touchee 48 % → 15 % du temps en 20 seances ; supports reels dans la plage : 22.27-23.49 (B) ; 20.61-21.5 (B) ; 17.88-18.81 (A). stop INDICATIF 15.59 (-15.16 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (2.68 ATR sous le plus haut 20 s., RSI(2) 8.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 24.92-25.92 (A, -10.24 %) ; 22.27-23.49 (B, -18.68 %) ; 20.61-21.5 (B, -25.55 %) ; 17.88-18.81 (A, -34.87 %) ; 13.38-14.15 (A, -51.0 %) ; 11.69-12.73 (B, -55.92 %)
- Resistances reelles au-dessus : 29.94-31.33 (A, 3.67 %) ; 31.81-31.85 (A, 10.15 %) ; 33.29-34.18 (A, 15.27 %) ; 34.77-36.03 (A, 20.39 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.33 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (16.76 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1254).
   - exécution **5.099 pt plus bas** dans le cas TYPIQUE (médiane), 5.099 au p90, **5.099 au pire**
   - perte réelle **21.859 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 16.76 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0041 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.148 % | p01 -6.503 % | pire -21.859 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4412** [0.3687 ; 0.5156] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3436** [0.295 ; 0.3948] _(largeur 10.0 pt, n_eff 345.7)_
   - deep : **0.2918** [0.2458 ; 0.3413] _(largeur 9.6 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (28.4 pt), swing (29.7 pt), deep (31.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.61 %** | CVaR **-10.11 %** | vol 6.11 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 10.32 % contre 5.60 % aujourd'hui, rapport 1.84)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.92 % vs -20.01 % si l'on extrapolait par √5 _(rapport 0.896 ; < 1 = le √5 surestime)_
- **β de baisse : 2.1584** (β de hausse 2.0107, asymétrie 1.0735) vs IWM — 605 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 25.9519 sur atr_grid (1.0 ATR, 10.139 %) — p(stop avant cible) 0.5835 [0.53 ; 0.63], R/R 3.11, perte reelle 10.225 % (gap inclus), CVaR 11.144 %, EV -0.4342 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4311 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 10.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.584, borne haute 0.635 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.35 ATR (stop 17.014 %) — p(stop avant cible) 0.2938 [0.25 ; 0.34], R/R 1.863, perte reelle 17.066 % (gap inclus), EV -0.6785 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 11.8 % x 31.80 % + P(rien) 58.8 % x 0.99 % ne couvrent pas P(stop) 29.4 % x 17.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 2.535 %) — p(stop avant cible) 0.8734 [0.84 ; 0.91], R/R 11.971, perte reelle 2.657 % (gap inclus), EV 0.357 % — **REFUSE**
      - refuse : cible atteinte seulement 6.2 % du temps (< 15 %) meme a 10 seances : le R/R de 11.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.873, borne haute 0.905 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 5.069 %) — p(stop avant cible) 0.7918 [0.75 ; 0.83], R/R 6.12, perte reelle 5.196 % (gap inclus), EV -0.3259 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.792, borne haute 0.832 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 8.2 % x 31.80 % + P(rien) 12.6 % x 9.30 % ne couvrent pas P(stop) 79.2 % x 5.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 7.604 %) — p(stop avant cible) 0.688 [0.64 ; 0.74], R/R 4.118, perte reelle 7.724 % (gap inclus), EV -0.1521 % — **REFUSE**
      - refuse : cible atteinte seulement 10.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.688, borne haute 0.735 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 10.3 % x 31.80 % + P(rien) 20.9 % x 9.05 % ne couvrent pas P(stop) 68.8 % x 7.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 10.139 %) — p(stop avant cible) 0.5835 [0.53 ; 0.63], R/R 3.11, perte reelle 10.225 % (gap inclus), EV -0.4342 % — **REFUSE**
      - refuse : cible atteinte seulement 10.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.584, borne haute 0.635 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 10.8 % x 31.80 % + P(rien) 30.8 % x 6.77 % ne couvrent pas P(stop) 58.4 % x 10.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 20.278 %) — p(stop avant cible) 0.2124 [0.17 ; 0.26], R/R 1.559, perte reelle 20.405 % (gap inclus), EV -0.4301 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 11.9 % x 31.80 % + P(rien) 66.8 % x 0.18 % ne couvrent pas P(stop) 21.2 % x 20.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 22.813 %) — p(stop avant cible) 0.1525 [0.12 ; 0.19], R/R 1.382, perte reelle 23.021 % (gap inclus), EV -0.2968 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 11.9 % x 31.80 % + P(rien) 72.8 % x -0.80 % ne couvrent pas P(stop) 15.2 % x 23.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 25.347 %) — p(stop avant cible) 0.1054 [0.08 ; 0.14], R/R 1.251, perte reelle 25.429 % (gap inclus), EV -0.1894 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 11.9 % x 31.80 % + P(rien) 77.5 % x -1.68 % ne couvrent pas P(stop) 10.5 % x 25.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 27.882 %) — p(stop avant cible) 0.085 [0.06 ; 0.12], R/R 1.138, perte reelle 27.936 % (gap inclus), EV -0.3383 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 11.9 % x 31.80 % + P(rien) 79.6 % x -2.21 % ne couvrent pas P(stop) 8.5 % x 27.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 30.417 %) — p(stop avant cible) 0.054 [0.03 ; 0.08], R/R 1.045, perte reelle 30.448 % (gap inclus), EV -0.3699 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 11.9 % x 31.80 % + P(rien) 82.7 % x -3.05 % ne couvrent pas P(stop) 5.4 % x 30.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 35.486 %) — p(stop avant cible) 0.0121 [0.00 ; 0.03], R/R 0.893, perte reelle 35.611 % (gap inclus), EV -0.2589 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 11.9 % x 31.80 % + P(rien) 86.9 % x -4.17 % ne couvrent pas P(stop) 1.2 % x 35.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 40.556 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 0.784, perte reelle 40.556 % (gap inclus), EV -0.2475 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 11.9 % x 31.80 % + P(rien) 87.6 % x -4.40 % ne couvrent pas P(stop) 0.4 % x 40.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 45.625 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.697, perte reelle 45.631 % (gap inclus), EV -0.2314 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 11.9 % x 31.80 % + P(rien) 88.0 % x -4.53 % ne couvrent pas P(stop) 0.1 % x 45.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 50.695 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.627, perte reelle 50.695 % (gap inclus), EV -0.2017 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 11.9 % x 31.80 % + P(rien) 88.1 % x -4.54 % ne couvrent pas P(stop) 0.0 % x 50.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 55.764 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.57, perte reelle 55.764 % (gap inclus), EV -0.2017 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 11.9 % x 31.80 % + P(rien) 88.1 % x -4.54 % ne couvrent pas P(stop) 0.0 % x 55.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 60.834 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.523, perte reelle 60.834 % (gap inclus), EV -0.2017 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 11.9 % x 31.80 % + P(rien) 88.1 % x -4.54 % ne couvrent pas P(stop) 0.0 % x 60.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 65.903 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.483, perte reelle 65.903 % (gap inclus), EV -0.2017 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 11.9 % x 31.80 % + P(rien) 88.1 % x -4.54 % ne couvrent pas P(stop) 0.0 % x 65.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 70.973 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.448, perte reelle 70.973 % (gap inclus), EV -0.2017 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 11.9 % x 31.80 % + P(rien) 88.1 % x -4.54 % ne couvrent pas P(stop) 0.0 % x 70.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 76.042 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.418, perte reelle 76.042 % (gap inclus), EV -0.2017 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 11.9 % x 31.80 % + P(rien) 88.1 % x -4.54 % ne couvrent pas P(stop) 0.0 % x 76.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 81.112 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.392, perte reelle 81.112 % (gap inclus), EV -0.2017 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 11.9 % x 31.80 % + P(rien) 88.1 % x -4.54 % ne couvrent pas P(stop) 0.0 % x 81.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 28.88, ATR14 2.9281 (10.139 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.379 ATR = 3.843 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.507 % | 28.7336 | 93.86 % | 95.47 % | 96.27 % | 97.68 % | 98.17 % | 98.67 % |
| 0.1 ATR | 1.014 % | 28.5872 | 86.12 % | 91.24 % | 92.34 % | 94.75 % | 95.84 % | 96.82 % |
| 0.15 ATR | 1.521 % | 28.4408 | 78.87 % | 86.4 % | 88.41 % | 91.62 % | 93.6 % | 95.59 % |
| 0.2 ATR | 2.028 % | 28.2944 | 71.03 % | 80.46 % | 84.17 % | 88.28 % | 90.86 % | 93.44 % |
| 0.25 ATR | 2.535 % | 28.148 | 64.99 % | 76.23 % | 80.75 % | 85.76 % | 88.73 % | 91.9 % |
| 0.35 ATR | 3.549 % | 27.8551 | 52.82 % | 67.27 % | 74.19 % | 79.49 % | 84.06 % | 88.31 % |
| 0.5 ATR | 5.069 % | 27.4159 | 38.13 % | 54.48 % | 62.2 % | 71.21 % | 78.58 % | 84.41 % |
| 0.75 ATR | 7.604 % | 26.6839 | 22.23 % | 39.48 % | 48.69 % | 59.19 % | 69.44 % | 76.82 % |
| 1.0 ATR | 10.139 % | 25.9519 | 9.96 % | 24.87 % | 34.98 % | 46.26 % | 58.58 % | 68.21 % |
| 1.25 ATR | 12.674 % | 25.2198 | 3.92 % | 14.5 % | 24.19 % | 35.05 % | 50.56 % | 61.85 % |
| 1.5 ATR | 15.208 % | 24.4878 | 1.21 % | 7.25 % | 15.93 % | 25.66 % | 41.52 % | 56.21 % |
| 2.0 ATR | 20.278 % | 23.0237 | 0.1 % | 1.91 % | 5.14 % | 14.44 % | 28.93 % | 45.54 % |
| 2.5 ATR | 25.347 % | 21.5596 | 0.0 % | 0.2 % | 1.31 % | 6.06 % | 18.88 % | 34.97 % |
| 3.0 ATR | 30.417 % | 20.0956 | 0.0 % | 0.1 % | 0.4 % | 2.83 % | 12.08 % | 26.87 % |
| 4.0 ATR | 40.556 % | 17.1674 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 3.45 % | 12.21 % |
| 6.0 ATR | 60.834 % | 11.3111 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.21 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.66 ATR | 0.86 ATR | 1.00 ATR | 1.12 ATR | 1.41 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.73 ATR | 0.82 ATR | 1.05 ATR | 1.23 ATR | 1.38 ATR | 1.77 ATR | 2.02 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.03 ATR | 1.30 ATR | 1.53 ATR | 1.75 ATR | 2.27 ATR | 2.66 ATR |
| **10 s.** | 0.60 ATR | 1.26 ATR | 1.40 ATR | 1.84 ATR | 2.20 ATR | 2.44 ATR | 3.24 ATR | 3.82 ATR |
| **20 s.** | 0.80 ATR | 1.79 ATR | 2.03 ATR | 2.62 ATR | 3.13 ATR | 3.47 ATR | 4.41 ATR | 5.33 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.43 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (60.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.658–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (7.604 %, prix 26.684), p(touche) 39.48 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.817–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (10.139 %, prix 25.9519), p(touche) 34.98 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.028–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (12.674 %, prix 25.2197), p(touche) 35.05 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.404–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (15.208 %, prix 24.4879), p(touche) 41.52 % (en stress 97.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.026 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (73.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.116 | EV/share : $-0.339 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 5 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 28.4 | bear 49.0 | side 22.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.013% → cible +6.283% / stop −3.141%, p_fill 41%, n_eff≈45.1) : P(cible|rempli) **7%** · **EV/risk -0.116** (×p_fill ; si rempli -0.89% du capital)
  - **swing** (entrée dip −6.621% → cible +16.871% / stop −10.858%, p_fill 35%, n_eff≈41.1) : P(cible|rempli) **18%** · **EV/risk -0.013** (×p_fill ; si rempli -0.39% du capital)
  - **deep** (entrée dip −10.231% → cible +21.575% / stop −16.943%, p_fill 31%, n_eff≈35.5) : P(cible|rempli) **10%** · **EV/risk -0.087** (×p_fill ; si rempli -4.74% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→77% · +2.0%→62% · +3.0%→52% · +5.0%→26% · +8.0%→12%
- Range intraday médian 6.97% (p90 11.38%) · excursion haute méd. +3.18% / basse méd. −2.5%
- Profil de vol intra : ouverture 4.647% vs midi 1.288% vs clôture 1.495% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 25% · trend ↑0%/↓0% ; spike-down 64% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.142 ; neutre — autocorr -0.018)_ ; drift intra méd. -0.489% ; recovery-V 23%
- **σ réalisé intraday** 3.806% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 60% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 31.1144 (VA 30.5681–31.2294 ; dernier close 31.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 66% · **stop −5.21%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.25 (high win-rate)
- Gaps overnight (n=159) : méd. -0.24% · baisse 53% (gap-down >1% 38% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −1.04% (p90 −2.65%) · haut méd +0.99% · range méd 2.55%
- Excursion ouverture 15min (n=160) : bas méd −1.23% (p90 −3.55%) · haut méd +1.33% · range méd 3.12%
- Excursion ouverture 30min (n=160) : bas méd −1.67% (p90 −4.61%) · haut méd +1.77% · range méd 3.97%
- Excursion ouverture 60min (n=160) : bas méd −1.74% (p90 −5.6%) · haut méd +1.78% · range méd 4.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 31.27 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 78% (126/159) · gap 47% · délai 0.0min · rebond 55% (80/126) (MFE +1.5%)
   - −1.0% : fill 30min 67% · séance 74% (119/159) · gap 38% · délai 0.0min · rebond 64% (83/119) (MFE +1.62%)
   - −1.5% : fill 30min 60% · séance 69% (112/159) · gap 34% · délai 0.0min · rebond 65% (76/112) (MFE +1.95%)
   - −2.0% : fill 30min 51% · séance 59% (100/159) · gap 25% · délai 0.0min · rebond 67% (68/100) (MFE +1.87%)
   - −3.0% : fill 30min 39% · séance 48% (82/159) · gap 12% · délai 2.9min · rebond 63% (57/82) (MFE +2.28%)
   - −4.0% : fill 30min 26% · séance 38% (63/159) · gap 6% · délai 9.0min · rebond 62% (44/63) (MFE +1.9%)
   - −5.0% : fill 30min 13% · séance 26% (47/159) · gap 1% · délai 31.4min · rebond 66% (35/47) (MFE +1.3%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −2.44%) → stop au-delà de −1.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −2.35%) → stop au-delà de −1.58% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −1.85%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1013 jambes) : jambe baissière méd −1.23% (p90 −2.88%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (79 séances) :
      · −1.0% : fill 100% (79/79) · rebond 62% (54/79)
      · −2.0% : fill 87% (71/79) · rebond 68% (50/71)
      · −3.0% : fill 73% (59/79) · rebond 63% (40/59)
      · −4.0% : fill 60% (45/79) · rebond 58% (29/45)
      · −5.0% : fill 39% (33/79) · rebond 61% (22/33)
   - **flat** (16 séances) :
      · −1.0% : fill 67% (11/16) · rebond 88% (10/11)
      · −2.0% : fill 51% (9/16) · rebond 92% (7/9)
      · −3.0% : fill 37% (6/16) · rebond 78% (5/6)
      · −4.0% : fill 19% (4/16) · rebond 57% (3/4)
      · −5.0% : fill 14% (3/16) · rebond 100% (3/3)
   - **gap-up** (64 séances) :
      · −1.0% : fill 44% (29/64) · rebond 58% (19/29)
      · −2.0% : fill 25% (20/64) · rebond 52% (11/20)
      · −3.0% : fill 20% (17/64) · rebond 57% (12/17)
      · −4.0% : fill 15% (14/64) · rebond 88% (12/14)
      · −5.0% : fill 14% (11/64) · rebond 72% (10/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 56% si les 15 1res min sont vertes (90 cas) · 27% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 68% si début vert vs 16% si rouge (base 43% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **68%** · continue >prix actuel 42% ; creux résiduel méd -1.91% (q20 -3.16%) → **SL/trailing à −3.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +2.85% → **scale +1.5% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **16%** (continue à baisser 55%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.1%** (au-delà de la MAE q10 -4.1%), cible rebond +1.66% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.02% .. +5.03%] · haut q95 +5.67% · bas q05 -5.45%
   - 60min (n=160) : retour [-5.78% .. +5.37%] · haut q95 +6.95% · bas q05 -6.77%
   - 2h (n=160) : retour [-6.38% .. +6.14%] · haut q95 +7.8% · bas q05 -7.08%
   - 4h (n=160) : retour [-6.7% .. +6.96%] · haut q95 +8.6% · bas q05 -7.66%
   - 6h (n=160) : retour [-6.45% .. +7.44%] · haut q95 +9.93% · bas q05 -7.51%
   - session (n=160) : retour [-6.41% .. +8.2%] · haut q95 +9.95% · bas q05 -7.51%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **39%**. Lecture précoce 30 min : signature présente → 13% vs absente 6% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 2.14% / p90 2.83%) · ~4.0 replis/séance, durée méd 55.01 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 29.17 min, n=54)
   - −1.0% → **82%** (reprise méd 31.37 min, n=38)
   - −1.5% → **76%** (reprise méd 44.94 min, n=20)
   - −2.0% → **68%** (reprise méd 38.95 min, n=14)
   - −3.0% → **74%** (reprise méd 175.76 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.83%** (p90, défaut prudent ; serré/agressif −2.14%) ; extension open→close méd +8.26% (q75 +11.05% / q95 +12.73%), MFE méd +10.06% / q90 +12.75%
   - Échelle scale-out : +10.06% (33%) / +12.25% (33%) / +12.75% (34%)
- **DÉSARMER** : repli > **−2.83%** depuis le plus-haut = décay → P(retournement) **16%** (préavis méd 167.77 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.75% : P(retournement après) 0% (mèche méd 2.07%)
- **CONTEXTE** : la dernière heure tient les gains 76% du temps (retour médian dernière heure +0.3%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.39 · part idiosyncratique 0.61
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 46.6  _(neutre)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist 0.361  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 28.0%
- **ATR** : 2.93 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.075  _(accumulation)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 48.4  _(transition)_
- **MA** : MA20 31.28 · MA50 36.35 · MA200 41.23  _(prix < MA20)_
- **Dist MA** : MA20 -7.7% · MA50 -20.5% · MA200 -30.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (713533 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
