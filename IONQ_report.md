# IONQ

**Generated** : 2026-11-09T01:24:51.443506+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 7.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $32.62  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $32.62 (+2.0% vs entrée) · entrée $31.98 · stop $31.24 · T1 $33.33 · R/R 1.82  
> ↳ ¼-Kelly 0.017 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.32% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 140 % hors [0,100] (R² max 0.91). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-06 : 32.62 · ATR Wilder 2.78 (8.53 %)_
- **Swing** : plage **29.17 → 26.99** (-10.56 % a -17.26 % sous la cloture, 0.78 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 27.83-28.32 (B). stop INDICATIF 24.11 (-10.68 % sous le bas ; sous le support 25.5-26.33 (- 0,5 ATR)).
- **Deep** : plage **26.99 → 22.2** (-17.26 % a -31.93 % sous la cloture, 1.72 ATR) — touchee 48 % → 15 % du temps en 20 seances ; supports reels dans la plage : 25.5-26.33 (A) ; 22.27-23.49 (B). stop INDICATIF 19.22 (-13.45 % sous le bas ; sous le support 20.61-21.5 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.22 ATR sous le plus haut 20 s., RSI(2) 77.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 29.94-31.33 (B, -3.95 %) ; 27.83-28.32 (B, -13.18 %) ; 25.5-26.33 (A, -19.28 %) ; 22.27-23.49 (B, -28.0 %) ; 20.61-21.5 (B, -34.09 %) ; 17.88-18.81 (A, -42.34 %)
- Resistances reelles au-dessus : 34.77-36.03 (A, 6.59 %) ; 36.57-37.28 (A, 12.11 %) ; 38.0-38.46 (A, 16.49 %) ; 39.76-40.84 (A, 21.9 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.33 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.4 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1254).
   - exécution **8.459 pt plus bas** dans le cas TYPIQUE (médiane), 8.459 au p90, **8.459 au pire**
   - perte réelle **21.859 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 13.4 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0067 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.148 % | p01 -6.63 % | pire -21.859 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5575** [0.4831 ; 0.63] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3984** [0.3478 ; 0.4507] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.4651** [0.413 ; 0.5178] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : deep (25.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.61 %** | CVaR **-10.19 %** | vol 6.2 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 10.03 % contre 5.68 % aujourd'hui, rapport 1.76)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.92 % vs -20.01 % si l'on extrapolait par √5 _(rapport 0.896 ; < 1 = le √5 surestime)_
- **β de baisse : 2.1823** (β de hausse 1.9959, asymétrie 1.0934) vs IWM — 605 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 29.2536 sur support (1.06 ATR, 10.32 %) — p(stop avant cible) 0.5609 [0.51 ; 0.61], R/R 2.962, perte reelle 10.403 % (gap inclus), CVaR 11.256 %, EV -0.1936 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3437 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.561, borne haute 0.613 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.06 ATR (stop 10.32 %) — p(stop avant cible) 0.5609 [0.51 ; 0.61], R/R 2.962, perte reelle 10.403 % (gap inclus), EV -0.1936 % — **REFUSE**
      - refuse : cible atteinte seulement 11.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.561, borne haute 0.613 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 11.7 % x 30.81 % + P(rien) 32.2 % x 6.29 % ne couvrent pas P(stop) 56.1 % x 10.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.72 ATR (stop 22.889 %) — p(stop avant cible) 0.1503 [0.12 ; 0.19], R/R 1.334, perte reelle 23.092 % (gap inclus), EV -0.4281 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 13.1 % x 30.81 % + P(rien) 71.8 % x -1.40 % ne couvrent pas P(stop) 15.0 % x 23.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.894 %) — p(stop avant cible) 0.9094 [0.88 ; 0.94], R/R 15.924, perte reelle 1.935 % (gap inclus), EV 0.2671 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 15.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.909, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.788 %) — p(stop avant cible) 0.8272 [0.78 ; 0.86], R/R 7.875, perte reelle 3.913 % (gap inclus), EV 0.0811 % — **REFUSE**
      - refuse : cible atteinte seulement 7.8 % du temps (< 15 %) meme a 10 seances : le R/R de 7.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.827, borne haute 0.864 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 5.681 %) — p(stop avant cible) 0.7678 [0.72 ; 0.81], R/R 5.343, perte reelle 5.767 % (gap inclus), EV -0.1857 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.768, borne haute 0.810 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 10.0 % x 30.81 % + P(rien) 13.2 % x 8.71 % ne couvrent pas P(stop) 76.8 % x 5.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.5 ATR (stop 11.363 %) — p(stop avant cible) 0.5109 [0.46 ; 0.56], R/R 2.684, perte reelle 11.478 % (gap inclus), EV -0.3566 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.511, borne haute 0.563 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 11.8 % x 30.81 % + P(rien) 37.1 % x 5.06 % ne couvrent pas P(stop) 51.1 % x 11.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 13.257 %) — p(stop avant cible) 0.4126 [0.36 ; 0.47], R/R 2.309, perte reelle 13.343 % (gap inclus), EV -0.3128 % — **REFUSE**
      - refuse : cible atteinte seulement 12.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 12.2 % x 30.81 % + P(rien) 46.6 % x 3.10 % ne couvrent pas P(stop) 41.3 % x 13.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 15.151 %) — p(stop avant cible) 0.3426 [0.29 ; 0.39], R/R 2.018, perte reelle 15.272 % (gap inclus), EV -0.5872 % — **REFUSE**
      - refuse : cible atteinte seulement 12.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 12.3 % x 30.81 % + P(rien) 53.5 % x 1.61 % ne couvrent pas P(stop) 34.3 % x 15.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 17.044 %) — p(stop avant cible) 0.279 [0.23 ; 0.33], R/R 1.801, perte reelle 17.108 % (gap inclus), EV -0.4139 % — **REFUSE**
      - refuse : cible atteinte seulement 13.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 13.0 % x 30.81 % + P(rien) 59.1 % x 0.60 % ne couvrent pas P(stop) 27.9 % x 17.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 26.514 %) — p(stop avant cible) 0.1033 [0.07 ; 0.14], R/R 1.158, perte reelle 26.611 % (gap inclus), EV -0.5586 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 13.1 % x 30.81 % + P(rien) 76.5 % x -2.42 % ne couvrent pas P(stop) 10.3 % x 26.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 30.301 %) — p(stop avant cible) 0.057 [0.04 ; 0.09], R/R 1.016, perte reelle 30.337 % (gap inclus), EV -0.6853 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 13.1 % x 30.81 % + P(rien) 81.2 % x -3.70 % ne couvrent pas P(stop) 5.7 % x 30.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 34.089 %) — p(stop avant cible) 0.0207 [0.01 ; 0.04], R/R 0.903, perte reelle 34.127 % (gap inclus), EV -0.6036 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.16 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 13.1 % x 30.81 % + P(rien) 84.8 % x -4.65 % ne couvrent pas P(stop) 2.1 % x 34.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 37.877 %) — p(stop avant cible) 0.0098 [0.00 ; 0.02], R/R 0.811, perte reelle 38.003 % (gap inclus), EV -0.5667 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 13.1 % x 30.81 % + P(rien) 85.9 % x -4.94 % ne couvrent pas P(stop) 1.0 % x 38.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 41.664 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.74, perte reelle 41.664 % (gap inclus), EV -0.5455 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 13.1 % x 30.81 % + P(rien) 86.5 % x -5.13 % ne couvrent pas P(stop) 0.4 % x 41.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 45.452 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.678, perte reelle 45.452 % (gap inclus), EV -0.5257 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 13.1 % x 30.81 % + P(rien) 86.8 % x -5.22 % ne couvrent pas P(stop) 0.1 % x 45.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 49.24 %) — p(stop avant cible) 0.0004 [0.00 ; 0.01], R/R 0.626, perte reelle 49.24 % (gap inclus), EV -0.5076 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 13.1 % x 30.81 % + P(rien) 86.8 % x -5.22 % ne couvrent pas P(stop) 0.0 % x 49.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 53.027 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.581, perte reelle 53.027 % (gap inclus), EV -0.4964 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 13.1 % x 30.81 % + P(rien) 86.9 % x -5.23 % ne couvrent pas P(stop) 0.0 % x 53.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 56.815 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.542, perte reelle 56.815 % (gap inclus), EV -0.4964 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 13.1 % x 30.81 % + P(rien) 86.9 % x -5.23 % ne couvrent pas P(stop) 0.0 % x 56.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 60.603 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.508, perte reelle 60.603 % (gap inclus), EV -0.4964 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 13.1 % x 30.81 % + P(rien) 86.9 % x -5.23 % ne couvrent pas P(stop) 0.0 % x 60.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 32.62, ATR14 2.4711 (7.575 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.379 ATR = 2.871 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.379 % | 32.4964 | 93.86 % | 95.47 % | 96.27 % | 97.68 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.758 % | 32.3729 | 86.12 % | 91.24 % | 92.34 % | 94.75 % | 95.84 % | 96.82 % |
| 0.15 ATR | 1.136 % | 32.2493 | 78.77 % | 86.4 % | 88.41 % | 91.62 % | 93.6 % | 95.59 % |
| 0.2 ATR | 1.515 % | 32.1258 | 71.13 % | 80.66 % | 84.27 % | 88.38 % | 90.86 % | 93.44 % |
| 0.25 ATR | 1.894 % | 32.0022 | 64.99 % | 76.33 % | 80.75 % | 85.86 % | 88.73 % | 91.9 % |
| 0.35 ATR | 2.651 % | 31.7551 | 52.82 % | 67.27 % | 74.19 % | 79.39 % | 84.06 % | 88.31 % |
| 0.5 ATR | 3.788 % | 31.3845 | 38.03 % | 54.38 % | 62.0 % | 70.91 % | 78.58 % | 84.41 % |
| 0.75 ATR | 5.681 % | 30.7667 | 22.23 % | 39.27 % | 48.39 % | 58.79 % | 69.34 % | 76.82 % |
| 1.0 ATR | 7.575 % | 30.1489 | 9.96 % | 24.67 % | 34.68 % | 45.86 % | 58.38 % | 68.21 % |
| 1.25 ATR | 9.469 % | 29.5312 | 3.92 % | 14.3 % | 23.89 % | 34.65 % | 50.36 % | 61.85 % |
| 1.5 ATR | 11.363 % | 28.9134 | 1.21 % | 7.05 % | 15.73 % | 25.25 % | 41.12 % | 56.21 % |
| 2.0 ATR | 15.151 % | 27.6779 | 0.1 % | 1.91 % | 5.04 % | 14.24 % | 28.43 % | 45.54 % |
| 2.5 ATR | 18.938 % | 26.4423 | 0.0 % | 0.2 % | 1.31 % | 6.06 % | 18.58 % | 35.08 % |
| 3.0 ATR | 22.726 % | 25.2068 | 0.0 % | 0.1 % | 0.4 % | 2.83 % | 11.98 % | 26.77 % |
| 4.0 ATR | 30.301 % | 22.7357 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 3.45 % | 12.1 % |
| 6.0 ATR | 45.452 % | 17.7936 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.21 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.66 ATR | 0.86 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.22 ATR | 1.37 ATR | 1.77 ATR | 2.00 ATR |
| **5 s.** | 0.43 ATR | 0.92 ATR | 1.02 ATR | 1.29 ATR | 1.51 ATR | 1.74 ATR | 2.26 ATR | 2.66 ATR |
| **10 s.** | 0.60 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.17 ATR | 2.43 ATR | 3.23 ATR | 3.82 ATR |
| **20 s.** | 0.80 ATR | 1.79 ATR | 2.03 ATR | 2.62 ATR | 3.12 ATR | 3.46 ATR | 4.39 ATR | 5.32 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.429 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.655–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.681 %, prix 30.7669), p(touche) 39.27 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.812–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.575 %, prix 30.149), p(touche) 34.68 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.019–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.469 %, prix 29.5312), p(touche) 34.65 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.395–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.363 %, prix 28.9134), p(touche) 41.12 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.026–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (18.938 %, prix 26.4424), p(touche) 35.08 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (74.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.051 | EV/share : $0.038 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 — | T3 —
- Kelly (position) : f* 0.066 | ¼-Kelly 0.017 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 62.0 | bear 31.2 | side 6.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.957% → cible +4.212% / stop −2.318%, p_fill 56%, n_eff≈62.0) : P(cible|rempli) **10%** · **EV/risk -0.156** (×p_fill ; si rempli -0.65% du capital)
  - **swing** (entrée dip −4.308% → cible +19.003% / stop −9.502%, p_fill 53%, n_eff≈62.2) : P(cible|rempli) **12%** · **EV/risk -0.092** (×p_fill ; si rempli -1.65% du capital)
  - **deep** (entrée dip −6.668% → cible +22.001% / stop −12.174%, p_fill 50%, n_eff≈56.9) : P(cible|rempli) **18%** · **EV/risk -0.130** (×p_fill ; si rempli -3.17% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.38 · part idiosyncratique 0.62
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.2  _(neutre)_
- **ADX** : 33.8  _(tendance etablie)_
- **MACD** : hist 0.119  _(bullish_recent)_
- **BB** : %B 0.63 · largeur 28.1%
- **ATR** : 2.47 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.019  _(neutre)_
- **Vol ratio** : 1.73  _(volume au-dessus de la moyenne)_
- **Choppiness** : 53.7  _(transition)_
- **MA** : MA20 31.47 · MA50 36.93 · MA200 41.54  _(prix > MA20)_
- **Dist MA** : MA20 +3.6% · MA50 -11.7% · MA200 -21.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (713684 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
