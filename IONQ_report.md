# IONQ

**Generated** : 2026-10-26T01:24:38.744196+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $31.27  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $31.27 (+1.0% vs entrée) · entrée $30.97 · stop $30.23 · T1 $32.21 · R/R 1.68  
> ↳ P(T1 av. stop) 18 % _(réel 5 s)_ · EV/risk -0.103 _(réel 5 s)_ (GBM 0.048) · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.4% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 31.27 · ATR Wilder 2.45 (7.84 %)_
- **Swing** : plage **28.25 → 26.37** (-9.67 % a -15.66 % sous la cloture, 0.76 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 27.83-28.32 (B). stop INDICATIF 24.27 (-7.96 % sous le bas ; sous le support 25.5-26.33 (- 0,5 ATR)).
- **Deep** : plage **26.37 → 22.26** (-15.66 % a -28.81 % sous la cloture, 1.68 ATR) — touchee 47 % → 15 % du temps en 20 seances ; supports reels dans la plage : 25.5-26.33 (A) ; 22.27-23.49 (B). stop INDICATIF 19.38 (-12.92 % sous le bas ; sous le support 20.61-21.5 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.78 ATR sous le plus haut 20 s., RSI(2) 39.3. Limite **30.04** (seance suivante), stop catastrophe 20.23, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 27.83-28.32 (B, -9.43 %) ; 25.5-26.33 (A, -15.8 %) ; 22.27-23.49 (B, -24.9 %) ; 20.61-21.5 (B, -31.24 %) ; 17.88-18.81 (A, -39.85 %) ; 13.38-14.15 (A, -54.75 %)
- Resistances reelles au-dessus : 33.29-34.18 (A, 6.46 %) ; 34.77-35.93 (A, 11.19 %) ; 36.03-37.25 (A, 15.22 %) ; 37.28-38.46 (A, 19.22 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.25 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.04 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1254).
   - exécution **1.653 pt plus bas** dans le cas TYPIQUE (médiane), 8.845 au p90, **11.819 au pire**
   - perte réelle **13.966 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 10.04 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0125 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.108 % | p01 -6.63 % | pire -21.859 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5264** [0.4521 ; 0.5998] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4769** [0.4246 ; 0.5296] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4557** [0.4038 ; 0.5084] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.84 %** | CVaR **-10.52 %** | vol 6.13 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 10.04 % contre 5.51 % aujourd'hui, rapport 1.82)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.92 % vs -19.94 % si l'on extrapolait par √5 _(rapport 0.899 ; < 1 = le √5 surestime)_
- **β de baisse : 2.1997** (β de hausse 2.0083, asymétrie 1.0953) vs IWM — 606 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 28.1745 sur atr_grid (1.25 ATR, 9.899 %) — p(stop avant cible) 0.5819 [0.53 ; 0.63], R/R 2.763, perte reelle 9.967 % (gap inclus), CVaR 10.686 %, EV 0.1713 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.23 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.582, borne haute 0.633 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.52 ATR (stop 7.063 %) — p(stop avant cible) 0.6902 [0.64 ; 0.74], R/R 3.83, perte reelle 7.188 % (gap inclus), EV 0.3485 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.690, borne haute 0.737 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.49 ATR du spot — compartiment <1, mesure a 47.8 % de casse (IC clusterise [0.449 ; 0.507] sur 1237 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 11.879 %) — p(stop avant cible) 0.4848 [0.43 ; 0.54], R/R 2.298, perte reelle 11.98 % (gap inclus), EV -0.0207 % — **REFUSE**
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 16.5 % x 27.53 % + P(rien) 35.0 % x 3.57 % ne couvrent pas P(stop) 48.5 % x 11.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.17 ATR (stop 20.175 %) — p(stop avant cible) 0.2134 [0.17 ; 0.26], R/R 1.357, perte reelle 20.297 % (gap inclus), EV -0.1007 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 17.8 % x 27.53 % + P(rien) 60.8 % x -1.12 % ne couvrent pas P(stop) 21.3 % x 20.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.98 %) — p(stop avant cible) 0.8973 [0.86 ; 0.93], R/R 13.636, perte reelle 2.019 % (gap inclus), EV 0.2396 % — **REFUSE**
      - refuse : cible atteinte seulement 6.1 % du temps (< 15 %) meme a 10 seances : le R/R de 13.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.897, borne haute 0.926 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 9.899 %) — p(stop avant cible) 0.5819 [0.53 ; 0.63], R/R 2.763, perte reelle 9.967 % (gap inclus), EV 0.1713 % — **REFUSE**
      - refuse : p_stop_first 0.582, borne haute 0.633 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 13.859 %) — p(stop avant cible) 0.3973 [0.35 ; 0.45], R/R 1.971, perte reelle 13.966 % (gap inclus), EV -0.1649 % — **REFUSE**
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 16.9 % x 27.53 % + P(rien) 43.4 % x 1.71 % ne couvrent pas P(stop) 39.7 % x 13.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 21.779 %) — p(stop avant cible) 0.1889 [0.15 ; 0.23], R/R 1.25, perte reelle 22.033 % (gap inclus), EV -0.1586 % — **REFUSE**
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 17.9 % x 27.53 % + P(rien) 63.2 % x -1.46 % ne couvrent pas P(stop) 18.9 % x 22.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 23.759 %) — p(stop avant cible) 0.1379 [0.10 ; 0.18], R/R 1.149, perte reelle 23.955 % (gap inclus), EV -0.1069 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 17.9 % x 27.53 % + P(rien) 68.3 % x -2.53 % ne couvrent pas P(stop) 13.8 % x 23.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 27.718 %) — p(stop avant cible) 0.0924 [0.07 ; 0.13], R/R 0.991, perte reelle 27.777 % (gap inclus), EV -0.3351 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 17.9 % x 27.53 % + P(rien) 72.9 % x -3.70 % ne couvrent pas P(stop) 9.2 % x 27.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 31.678 %) — p(stop avant cible) 0.0396 [0.02 ; 0.06], R/R 0.867, perte reelle 31.775 % (gap inclus), EV -0.3689 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 17.9 % x 27.53 % + P(rien) 78.1 % x -5.17 % ne couvrent pas P(stop) 4.0 % x 31.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 35.638 %) — p(stop avant cible) 0.0127 [0.00 ; 0.03], R/R 0.77, perte reelle 35.755 % (gap inclus), EV -0.2576 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 17.9 % x 27.53 % + P(rien) 80.8 % x -5.85 % ne couvrent pas P(stop) 1.3 % x 35.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 39.598 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.695, perte reelle 39.618 % (gap inclus), EV -0.2595 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 17.9 % x 27.53 % + P(rien) 81.5 % x -6.07 % ne couvrent pas P(stop) 0.6 % x 39.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 43.557 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.632, perte reelle 43.557 % (gap inclus), EV -0.2286 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 17.9 % x 27.53 % + P(rien) 82.0 % x -6.21 % ne couvrent pas P(stop) 0.1 % x 43.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 47.517 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.579, perte reelle 47.517 % (gap inclus), EV -0.2129 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 17.9 % x 27.53 % + P(rien) 82.1 % x -6.23 % ne couvrent pas P(stop) 0.1 % x 47.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 51.477 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.535, perte reelle 51.477 % (gap inclus), EV -0.1983 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 17.9 % x 27.53 % + P(rien) 82.1 % x -6.24 % ne couvrent pas P(stop) 0.0 % x 51.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 55.437 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.497, perte reelle 55.437 % (gap inclus), EV -0.1983 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 17.9 % x 27.53 % + P(rien) 82.1 % x -6.24 % ne couvrent pas P(stop) 0.0 % x 55.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 59.396 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.464, perte reelle 59.396 % (gap inclus), EV -0.1983 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 17.9 % x 27.53 % + P(rien) 82.1 % x -6.24 % ne couvrent pas P(stop) 0.0 % x 59.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 63.356 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.435, perte reelle 63.356 % (gap inclus), EV -0.1983 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 17.9 % x 27.53 % + P(rien) 82.1 % x -6.24 % ne couvrent pas P(stop) 0.0 % x 63.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 31.27, ATR14 2.4764 (7.92 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.38 ATR = 3.009 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.396 % | 31.1462 | 93.86 % | 95.47 % | 96.17 % | 97.58 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.792 % | 31.0224 | 86.22 % | 91.24 % | 92.34 % | 94.65 % | 95.84 % | 96.82 % |
| 0.15 ATR | 1.188 % | 30.8985 | 78.87 % | 86.4 % | 88.41 % | 91.62 % | 93.6 % | 95.59 % |
| 0.2 ATR | 1.584 % | 30.7747 | 71.23 % | 80.66 % | 84.27 % | 88.38 % | 90.86 % | 93.44 % |
| 0.25 ATR | 1.98 % | 30.6509 | 65.19 % | 76.54 % | 80.75 % | 85.86 % | 88.83 % | 91.9 % |
| 0.35 ATR | 2.772 % | 30.4033 | 53.02 % | 67.47 % | 74.19 % | 79.39 % | 84.16 % | 88.31 % |
| 0.5 ATR | 3.96 % | 30.0318 | 38.03 % | 54.58 % | 62.3 % | 71.11 % | 78.68 % | 84.41 % |
| 0.75 ATR | 5.94 % | 29.4127 | 22.43 % | 39.48 % | 48.59 % | 58.99 % | 69.34 % | 76.82 % |
| 1.0 ATR | 7.92 % | 28.7936 | 10.16 % | 24.97 % | 35.08 % | 46.26 % | 58.38 % | 68.21 % |
| 1.25 ATR | 9.899 % | 28.1745 | 3.82 % | 14.4 % | 24.19 % | 34.95 % | 50.56 % | 61.85 % |
| 1.5 ATR | 11.879 % | 27.5554 | 1.11 % | 7.15 % | 15.83 % | 25.66 % | 41.52 % | 56.21 % |
| 2.0 ATR | 15.839 % | 26.3171 | 0.1 % | 1.91 % | 5.24 % | 14.44 % | 28.53 % | 45.33 % |
| 2.5 ATR | 19.799 % | 25.0789 | 0.0 % | 0.2 % | 1.31 % | 6.06 % | 18.58 % | 34.56 % |
| 3.0 ATR | 23.759 % | 23.8407 | 0.0 % | 0.1 % | 0.4 % | 2.83 % | 11.88 % | 26.26 % |
| 4.0 ATR | 31.678 % | 21.3643 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 3.45 % | 11.08 % |
| 6.0 ATR | 47.517 % | 16.4114 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.01 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.58 ATR | 0.66 ATR | 0.86 ATR | 1.00 ATR | 1.12 ATR | 1.40 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.82 ATR | 1.05 ATR | 1.23 ATR | 1.38 ATR | 1.77 ATR | 2.03 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.03 ATR | 1.30 ATR | 1.53 ATR | 1.75 ATR | 2.27 ATR | 2.66 ATR |
| **10 s.** | 0.60 ATR | 1.26 ATR | 1.40 ATR | 1.83 ATR | 2.18 ATR | 2.43 ATR | 3.22 ATR | 3.82 ATR |
| **20 s.** | 0.80 ATR | 1.78 ATR | 2.02 ATR | 2.59 ATR | 3.08 ATR | 3.41 ATR | 4.22 ATR | 5.25 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.43–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.659–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.94 %, prix 29.4126), p(touche) 39.48 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.816–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.92 %, prix 28.7934), p(touche) 35.08 % (en stress 92.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.028–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.899 %, prix 28.1746), p(touche) 34.95 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.404–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.879 %, prix 27.5554), p(touche) 41.52 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.015–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (69.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.048 | EV/share : $0.035 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 — | T3 —
- Kelly (position) : f* 0.066 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.6 | bear 67.7 | side 21.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.964% → cible +3.998% / stop −2.399%, p_fill 75%, n_eff≈81.6) : P(cible|rempli) **18%** · **EV/risk -0.103** (×p_fill ; si rempli -0.33% du capital)
  - **swing** (entrée dip −2.12% → cible +12.207% / stop −8.091%, p_fill 75%, n_eff≈88.4) : P(cible|rempli) **23%** · **EV/risk -0.123** (×p_fill ; si rempli -1.33% du capital)
  - **deep** (entrée dip −3.281% → cible +13.55% / stop −12.282%, p_fill 75%, n_eff≈84.8) : P(cible|rempli) **27%** · **EV/risk -0.235** (×p_fill ; si rempli -3.85% du capital)
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.51 · part idiosyncratique 0.49
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.8  _(survente)_
- **ADX** : 29.0  _(tendance etablie)_
- **MACD** : hist -0.738  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 59.1%
- **ATR** : 2.48 (12.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.357  _(distribution)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 30.8  _(marche directionnel)_
- **MA** : MA20 37.59 · MA50 39.48 · MA200 42.5  _(prix < MA20)_
- **Dist MA** : MA20 -16.8% · MA50 -20.8% · MA200 -26.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (774842 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
