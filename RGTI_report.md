# RGTI

**Generated** : 2026-11-05T01:28:16.783249+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $11.23  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $11.23 (+0.4% vs entrée) · entrée $11.18 · stop $10.96 · T1 $11.55 · R/R 1.68  
> ↳ ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +3.7 % ≠ (strike 11.5 − spot 11.23)/spot = +2.4 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-04 : 11.23 · ATR Wilder 0.8045 (7.17 %)_
- **Swing** : plage **10.25 → 9.84** (-8.71 % a -12.34 % sous la cloture, 0.51 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 10.05-10.31 (A). stop INDICATIF 9.1 (-7.54 % sous le bas ; sous le support 9.5-9.74 (- 0,5 ATR)).
- **Deep** : plage **9.84 → 8.79** (-12.34 % a -21.71 % sous la cloture, 1.31 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 9.5-9.74 (C) ; 8.92-9.14 (A). stop INDICATIF 7.95 (-9.56 % sous le bas ; sous le support 8.35-8.45 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.21 ATR sous le plus haut 20 s., RSI(2) 57.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 10.05-10.31 (A, -8.15 %) ; 9.5-9.74 (C, -13.23 %) ; 8.92-9.14 (A, -18.57 %) ; 8.35-8.45 (B, -24.72 %) ; 6.86-7.03 (B, -37.42 %) ; 5.95-5.95 (C, -46.99 %)
- Resistances reelles au-dessus : 11.8-12.08 (A, 5.12 %) ; 12.34-12.59 (A, 9.93 %) ; 12.75-13.13 (A, 13.59 %) ; 13.41-13.61 (A, 19.47 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.78 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.48 %)** : le gap seul le franchit 1.117 % des séances (14 fois sur 1253).
   - exécution **3.207 pt plus bas** dans le cas TYPIQUE (médiane), 8.459 au p90, **22.733 au pire**
   - perte réelle **13.376 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 8.48 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0547 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 14 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.144 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5325** [0.4581 ; 0.6058] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5232** [0.4705 ; 0.5755] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.6104** [0.5582 ; 0.6607] _(largeur 10.2 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.71 %** | CVaR **-10.82 %** | vol 6.74 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 17.76 % contre 6.11 % aujourd'hui, rapport 2.91)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8317** (β de hausse 2.0293, asymétrie 0.9026) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.454× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 10.1219 sur atr_based (1.5 ATR, 9.827 %) — p(stop avant cible) 0.6348 [0.58 ; 0.68], R/R 3.204, perte reelle 9.984 % (gap inclus), CVaR 11.688 %, EV -1.516 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6002 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.635, borne haute 0.684 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 0.16 ATR (stop 4.058 %) — p(stop avant cible) 0.828 [0.79 ; 0.86], R/R 7.722, perte reelle 4.142 % (gap inclus), EV -0.3235 % — **REFUSE**
      - refuse : cible atteinte seulement 6.4 % du temps (< 15 %) meme a 10 seances : le R/R de 7.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.828, borne haute 0.865 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 6.4 % x 31.98 % + P(rien) 10.8 % x 9.89 % ne couvrent pas P(stop) 82.8 % x 4.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 9.827 %) — p(stop avant cible) 0.6348 [0.58 ; 0.68], R/R 3.204, perte reelle 9.984 % (gap inclus), EV -1.516 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.635, borne haute 0.684 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.52 %) : P(cible) 9.7 % x 31.98 % + P(rien) 26.9 % x 6.45 % ne couvrent pas P(stop) 63.5 % x 9.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 0.16 ATR (stop 2.99 %) — p(stop avant cible) 0.869 [0.83 ; 0.90], R/R 10.413, perte reelle 3.071 % (gap inclus), EV -0.2274 % — **REFUSE**
      - refuse : cible atteinte seulement 5.4 % du temps (< 15 %) meme a 10 seances : le R/R de 10.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.869, borne haute 0.901 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 5.4 % x 31.98 % + P(rien) 7.7 % x 9.21 % ne couvrent pas P(stop) 86.9 % x 3.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.914 %) — p(stop avant cible) 0.8043 [0.76 ; 0.84], R/R 6.41, perte reelle 4.99 % (gap inclus), EV -0.6066 % — **REFUSE**
      - refuse : cible atteinte seulement 6.9 % du temps (< 15 %) meme a 10 seances : le R/R de 6.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.804, borne haute 0.844 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 6.9 % x 31.98 % + P(rien) 12.7 % x 9.54 % ne couvrent pas P(stop) 80.4 % x 4.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 6.552 %) — p(stop avant cible) 0.7324 [0.68 ; 0.78], R/R 4.77, perte reelle 6.705 % (gap inclus), EV -0.6869 % — **REFUSE**
      - refuse : cible atteinte seulement 8.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.732, borne haute 0.777 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 8.7 % x 31.98 % + P(rien) 18.1 % x 8.03 % ne couvrent pas P(stop) 73.2 % x 6.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 8.19 %) — p(stop avant cible) 0.6772 [0.63 ; 0.72], R/R 3.824, perte reelle 8.365 % (gap inclus), EV -1.1125 % — **REFUSE**
      - refuse : cible atteinte seulement 9.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.677, borne haute 0.725 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 9.4 % x 31.98 % + P(rien) 22.9 % x 6.77 % ne couvrent pas P(stop) 67.7 % x 8.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 11.465 %) — p(stop avant cible) 0.5572 [0.50 ; 0.61], R/R 2.747, perte reelle 11.642 % (gap inclus), EV -1.6419 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.557, borne haute 0.609 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.64 %) : P(cible) 10.1 % x 31.98 % + P(rien) 34.2 % x 4.72 % ne couvrent pas P(stop) 55.7 % x 11.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 13.103 %) — p(stop avant cible) 0.4686 [0.42 ; 0.52], R/R 2.409, perte reelle 13.279 % (gap inclus), EV -1.2657 % — **REFUSE**
      - refuse : cible atteinte seulement 10.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 10.5 % x 31.98 % + P(rien) 42.6 % x 3.72 % ne couvrent pas P(stop) 46.9 % x 13.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 14.741 %) — p(stop avant cible) 0.4075 [0.36 ; 0.46], R/R 2.131, perte reelle 15.008 % (gap inclus), EV -1.4488 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.45 %) : P(cible) 10.9 % x 31.98 % + P(rien) 48.3 % x 2.44 % ne couvrent pas P(stop) 40.8 % x 15.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 16.379 %) — p(stop avant cible) 0.3412 [0.29 ; 0.39], R/R 1.927, perte reelle 16.598 % (gap inclus), EV -1.2086 % — **REFUSE**
      - refuse : cible atteinte seulement 11.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 11.7 % x 31.98 % + P(rien) 54.2 % x 1.34 % ne couvrent pas P(stop) 34.1 % x 16.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 18.017 %) — p(stop avant cible) 0.2741 [0.23 ; 0.32], R/R 1.745, perte reelle 18.326 % (gap inclus), EV -1.0473 % — **REFUSE**
      - refuse : cible atteinte seulement 12.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 12.0 % x 31.98 % + P(rien) 60.6 % x 0.21 % ne couvrent pas P(stop) 27.4 % x 18.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 19.655 %) — p(stop avant cible) 0.2377 [0.20 ; 0.28], R/R 1.601, perte reelle 19.972 % (gap inclus), EV -1.0838 % — **REFUSE**
      - refuse : cible atteinte seulement 12.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.16 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 12.4 % x 31.98 % + P(rien) 63.8 % x -0.49 % ne couvrent pas P(stop) 23.8 % x 19.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 22.931 %) — p(stop avant cible) 0.1402 [0.11 ; 0.18], R/R 1.376, perte reelle 23.251 % (gap inclus), EV -0.8879 % — **REFUSE**
      - refuse : cible atteinte seulement 12.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 12.6 % x 31.98 % + P(rien) 73.4 % x -2.24 % ne couvrent pas P(stop) 14.0 % x 23.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 26.207 %) — p(stop avant cible) 0.0942 [0.07 ; 0.13], R/R 1.21, perte reelle 26.423 % (gap inclus), EV -0.7821 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 12.9 % x 31.98 % + P(rien) 77.7 % x -3.11 % ne couvrent pas P(stop) 9.4 % x 26.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 29.483 %) — p(stop avant cible) 0.0592 [0.04 ; 0.09], R/R 1.077, perte reelle 29.704 % (gap inclus), EV -0.7616 % — **REFUSE**
      - refuse : cible atteinte seulement 12.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 12.9 % x 31.98 % + P(rien) 81.1 % x -3.87 % ne couvrent pas P(stop) 5.9 % x 29.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 32.759 %) — p(stop avant cible) 0.0317 [0.02 ; 0.05], R/R 0.97, perte reelle 32.971 % (gap inclus), EV -0.6699 % — **REFUSE**
      - refuse : cible atteinte seulement 13.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 13.0 % x 31.98 % + P(rien) 83.9 % x -4.50 % ne couvrent pas P(stop) 3.2 % x 32.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 36.034 %) — p(stop avant cible) 0.021 [0.01 ; 0.04], R/R 0.882, perte reelle 36.28 % (gap inclus), EV -0.6342 % — **REFUSE**
      - refuse : cible atteinte seulement 13.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 13.0 % x 31.98 % + P(rien) 84.9 % x -4.76 % ne couvrent pas P(stop) 2.1 % x 36.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 39.31 %) — p(stop avant cible) 0.0114 [0.00 ; 0.03], R/R 0.809, perte reelle 39.514 % (gap inclus), EV -0.5999 % — **REFUSE**
      - refuse : cible atteinte seulement 13.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 13.0 % x 31.98 % + P(rien) 85.8 % x -5.03 % ne couvrent pas P(stop) 1.1 % x 39.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 42.586 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 0.751, perte reelle 42.586 % (gap inclus), EV -0.5386 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.14 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 13.1 % x 31.98 % + P(rien) 86.4 % x -5.24 % ne couvrent pas P(stop) 0.5 % x 42.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 45.862 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 0.693, perte reelle 46.146 % (gap inclus), EV -0.5486 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 13.1 % x 31.98 % + P(rien) 86.5 % x -5.25 % ne couvrent pas P(stop) 0.4 % x 46.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 49.138 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.651, perte reelle 49.138 % (gap inclus), EV -0.5487 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 13.1 % x 31.98 % + P(rien) 86.6 % x -5.32 % ne couvrent pas P(stop) 0.3 % x 49.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 52.414 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.593, perte reelle 53.953 % (gap inclus), EV -0.564 % — **REFUSE**
      - refuse : cible atteinte seulement 13.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 13.1 % x 31.98 % + P(rien) 86.6 % x -5.32 % ne couvrent pas P(stop) 0.3 % x 53.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 11.225, ATR14 0.7354 (6.552 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.406 ATR = 2.66 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.328 % | 11.1882 | 91.94 % | 94.35 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.655 % | 11.1515 | 86.1 % | 90.83 % | 92.33 % | 94.94 % | 95.93 % | 97.43 % |
| 0.15 ATR | 0.983 % | 11.1147 | 80.77 % | 87.2 % | 89.0 % | 92.11 % | 94.11 % | 96.1 % |
| 0.2 ATR | 1.31 % | 11.0779 | 73.92 % | 82.56 % | 85.37 % | 88.78 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.638 % | 11.0411 | 67.98 % | 78.43 % | 81.53 % | 85.74 % | 88.92 % | 92.51 % |
| 0.35 ATR | 2.293 % | 10.9676 | 55.39 % | 68.45 % | 73.76 % | 79.47 % | 84.55 % | 89.63 % |
| 0.5 ATR | 3.276 % | 10.8573 | 40.99 % | 56.96 % | 64.78 % | 71.79 % | 79.27 % | 85.32 % |
| 0.75 ATR | 4.914 % | 10.6734 | 21.55 % | 39.11 % | 50.15 % | 59.15 % | 71.14 % | 79.06 % |
| 1.0 ATR | 6.552 % | 10.4896 | 9.37 % | 23.99 % | 33.7 % | 46.92 % | 62.3 % | 72.59 % |
| 1.25 ATR | 8.19 % | 10.3057 | 4.03 % | 14.52 % | 23.71 % | 37.11 % | 53.15 % | 65.2 % |
| 1.5 ATR | 9.828 % | 10.1219 | 1.71 % | 7.16 % | 13.62 % | 25.38 % | 43.29 % | 57.19 % |
| 2.0 ATR | 13.103 % | 9.7541 | 0.3 % | 1.61 % | 4.14 % | 10.72 % | 25.3 % | 41.07 % |
| 2.5 ATR | 16.379 % | 9.3864 | 0.0 % | 0.2 % | 1.01 % | 4.25 % | 14.43 % | 28.75 % |
| 3.0 ATR | 19.655 % | 9.0187 | 0.0 % | 0.1 % | 0.3 % | 1.42 % | 7.22 % | 17.15 % |
| 4.0 ATR | 26.207 % | 8.2833 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.63 % | 4.52 % |
| 6.0 ATR | 39.31 % | 6.8124 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.78 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.33 ATR | 0.75 ATR | 0.83 ATR | 1.02 ATR | 1.22 ATR | 1.34 ATR | 1.69 ATR | 1.96 ATR |
| **5 s.** | 0.44 ATR | 0.94 ATR | 1.05 ATR | 1.34 ATR | 1.51 ATR | 1.68 ATR | 2.06 ATR | 2.44 ATR |
| **10 s.** | 0.63 ATR | 1.33 ATR | 1.46 ATR | 1.79 ATR | 2.01 ATR | 2.24 ATR | 2.81 ATR | 3.40 ATR |
| **20 s.** | 0.91 ATR | 1.72 ATR | 1.88 ATR | 2.33 ATR | 2.66 ATR | 2.88 ATR | 3.57 ATR | 3.96 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.458–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.276 %, prix 10.8573), p(touche) 40.99 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (62.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.668–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.914 %, prix 10.6734), p(touche) 39.11 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.828–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.552 %, prix 10.4895), p(touche) 33.7 % (en stress 88.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.049–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.19 %, prix 10.3057), p(touche) 37.11 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.457–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.828 %, prix 10.1218), p(touche) 43.29 % (en stress 95.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (72.6 % des re-echantillons)
- **20 seance(s)** : plage utile 1.878–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.103 %, prix 9.7542), p(touche) 41.07 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.03 | EV/share : $0.007 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 — | T3 —
- Kelly (position) : f* 0.042 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 80.1 | bear 5.0 | side 14.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.408% → cible +3.289% / stop −2.0%, p_fill 87%, n_eff≈93.9) : P(cible|rempli) **22%** · **EV/risk -0.145** (×p_fill ; si rempli -0.33% du capital)
  - **swing** (entrée dip −0.852% → cible +15.387% / stop −7.693%, p_fill 90%, n_eff≈104.6) : P(cible|rempli) **13%** · **EV/risk -0.244** (×p_fill ; si rempli -2.09% du capital)
  - **deep** (entrée dip −1.242% → cible +15.841% / stop −9.952%, p_fill 93%, n_eff≈104.1) : P(cible|rempli) **19%** · **EV/risk -0.391** (×p_fill ; si rempli -4.19% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.49 · part idiosyncratique 0.51
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.9  _(momentum baissier)_
- **ADX** : 32.8  _(tendance etablie)_
- **MACD** : hist 0.021  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 30.9%
- **ATR** : 0.74 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.122  _(distribution)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 62.1  _(marche en range (choppy))_
- **MA** : MA20 12.06 · MA50 14.18 · MA200 16.96  _(prix < MA20)_
- **Dist MA** : MA20 -6.9% · MA50 -20.8% · MA200 -33.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (753988 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
