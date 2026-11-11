# IONQ

**Generated** : 2026-11-11T01:24:25.621814+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 7.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $34.98  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)  
> ↳ spot $34.98 (+2.1% vs entrée) · entrée $34.25 · stop $32.82 · T1 $37.12 · R/R 2.01  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -9.4 % ≠ (strike 32.0 − spot 34.98)/spot = -8.5 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-10 : 34.98 · ATR Wilder 2.81 (8.05 %)_
- **Swing** : plage **31.49 → 29.27** (-9.98 % a -16.32 % sous la cloture, 0.79 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 29.94-31.33 (B). stop INDICATIF 26.42 (-9.73 % sous le bas ; sous le support 27.83-28.32 (- 0,5 ATR)).
- **Deep** : plage **29.27 → 24.37** (-16.32 % a -30.33 % sous la cloture, 1.74 ATR) — touchee 48 % → 15 % du temps en 20 seances ; supports reels dans la plage : 27.83-28.32 (B) ; 24.92-25.92 (A). stop INDICATIF 20.86 (-14.4 % sous le bas ; sous le support 22.27-23.49 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.49 ATR sous le plus haut 20 s., RSI(2) 78.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 31.81-31.85 (B, -8.95 %) ; 29.94-31.33 (B, -10.43 %) ; 27.83-28.32 (B, -19.04 %) ; 24.92-25.92 (A, -25.89 %) ; 22.27-23.49 (B, -32.86 %) ; 20.61-21.5 (B, -38.54 %)
- Resistances reelles au-dessus : 36.57-37.28 (A, 4.55 %) ; 38.0-38.46 (A, 8.63 %) ; 39.76-40.84 (A, 13.68 %) ; 41.29-41.9 (A, 18.04 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.26 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.23 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **9.629 pt plus bas** dans le cas TYPIQUE (médiane), 9.629 au p90, **9.629 au pire**
   - perte réelle **21.859 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 12.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0077 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.111 % | p01 -6.504 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3426** [0.275 ; 0.4154] _(largeur 14.0 pt, n_eff 173.1)_
   - swing : **0.476** [0.4237 ; 0.5287] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4493** [0.3975 ; 0.502] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : deep (26.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.53 %** | CVaR **-10.08 %** | vol 6.19 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 10.05 % contre 5.68 % aujourd'hui, rapport 1.77)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.92 % vs -19.94 % si l'on extrapolait par √5 _(rapport 0.899 ; < 1 = le √5 surestime)_
- **β de baisse : 2.1599** (β de hausse 2.0023, asymétrie 1.0787) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 31.0397 sur sr_based (1.19 ATR, 11.264 %) — p(stop avant cible) 0.5204 [0.47 ; 0.57], R/R 2.426, perte reelle 11.364 % (gap inclus), CVaR 12.302 %, EV -0.4808 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2577 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.520, borne haute 0.573 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.30 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.19 ATR (stop 11.264 %) — p(stop avant cible) 0.5204 [0.47 ; 0.57], R/R 2.426, perte reelle 11.364 % (gap inclus), EV -0.4808 % — **REFUSE**
      - refuse : p_stop_first 0.520, borne haute 0.573 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 15.3 % x 27.57 % + P(rien) 32.6 % x 3.69 % ne couvrent pas P(stop) 52.0 % x 11.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 1.86 ATR (stop 16.446 %) — p(stop avant cible) 0.298 [0.25 ; 0.35], R/R 1.668, perte reelle 16.533 % (gap inclus), EV -0.7551 % — **REFUSE**
      - refuse : R/R 1.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 16.2 % x 27.57 % + P(rien) 54.0 % x -0.55 % ne couvrent pas P(stop) 29.8 % x 16.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.4 ATR (stop 28.167 %) — p(stop avant cible) 0.0808 [0.06 ; 0.11], R/R 0.977, perte reelle 28.219 % (gap inclus), EV -0.5953 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 16.7 % x 27.57 % + P(rien) 75.2 % x -3.88 % ne couvrent pas P(stop) 8.1 % x 28.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 3.96 ATR (stop 32.484 %) — p(stop avant cible) 0.0285 [0.01 ; 0.05], R/R 0.847, perte reelle 32.554 % (gap inclus), EV -0.6208 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 16.7 % x 27.57 % + P(rien) 80.5 % x -5.34 % ne couvrent pas P(stop) 2.9 % x 32.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.913 %) — p(stop avant cible) 0.9104 [0.88 ; 0.94], R/R 14.01, perte reelle 1.968 % (gap inclus), EV 0.1183 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 14.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.910, borne haute 0.937 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.825 %) — p(stop avant cible) 0.8291 [0.79 ; 0.87], R/R 6.979, perte reelle 3.95 % (gap inclus), EV -0.0577 % — **REFUSE**
      - refuse : cible atteinte seulement 9.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.829, borne haute 0.866 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 9.5 % x 27.57 % + P(rien) 7.6 % x 7.91 % ne couvrent pas P(stop) 82.9 % x 3.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 5.738 %) — p(stop avant cible) 0.7675 [0.72 ; 0.81], R/R 4.733, perte reelle 5.826 % (gap inclus), EV -0.3433 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.767, borne haute 0.810 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 11.9 % x 27.57 % + P(rien) 11.3 % x 7.39 % ne couvrent pas P(stop) 76.8 % x 5.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 19.125 %) — p(stop avant cible) 0.2389 [0.20 ; 0.29], R/R 1.429, perte reelle 19.288 % (gap inclus), EV -0.6987 % — **REFUSE**
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 16.6 % x 27.57 % + P(rien) 59.5 % x -1.12 % ne couvrent pas P(stop) 23.9 % x 19.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 21.038 %) — p(stop avant cible) 0.1917 [0.15 ; 0.24], R/R 1.301, perte reelle 21.189 % (gap inclus), EV -0.3621 % — **REFUSE**
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 16.7 % x 27.57 % + P(rien) 64.1 % x -1.41 % ne couvrent pas P(stop) 19.2 % x 21.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 22.95 %) — p(stop avant cible) 0.1482 [0.11 ; 0.19], R/R 1.191, perte reelle 23.144 % (gap inclus), EV -0.403 % — **REFUSE**
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 16.7 % x 27.57 % + P(rien) 68.5 % x -2.30 % ne couvrent pas P(stop) 14.8 % x 23.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 34.425 %) — p(stop avant cible) 0.02 [0.01 ; 0.04], R/R 0.8, perte reelle 34.455 % (gap inclus), EV -0.5706 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 16.7 % x 27.57 % + P(rien) 81.3 % x -5.51 % ne couvrent pas P(stop) 2.0 % x 34.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 38.25 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 0.719, perte reelle 38.365 % (gap inclus), EV -0.5096 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 16.7 % x 27.57 % + P(rien) 82.6 % x -5.85 % ne couvrent pas P(stop) 0.7 % x 38.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 42.075 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.655, perte reelle 42.075 % (gap inclus), EV -0.4854 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 16.7 % x 27.57 % + P(rien) 83.2 % x -6.05 % ne couvrent pas P(stop) 0.1 % x 42.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 45.901 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.601, perte reelle 45.904 % (gap inclus), EV -0.49 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 16.7 % x 27.57 % + P(rien) 83.2 % x -6.07 % ne couvrent pas P(stop) 0.1 % x 45.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 49.726 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.554, perte reelle 49.726 % (gap inclus), EV -0.4596 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 16.7 % x 27.57 % + P(rien) 83.3 % x -6.08 % ne couvrent pas P(stop) 0.0 % x 49.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 53.551 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.515, perte reelle 53.551 % (gap inclus), EV -0.4596 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 16.7 % x 27.57 % + P(rien) 83.3 % x -6.08 % ne couvrent pas P(stop) 0.0 % x 53.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 57.376 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.481, perte reelle 57.376 % (gap inclus), EV -0.4596 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 16.7 % x 27.57 % + P(rien) 83.3 % x -6.08 % ne couvrent pas P(stop) 0.0 % x 57.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 61.201 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.45, perte reelle 61.201 % (gap inclus), EV -0.4596 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 16.7 % x 27.57 % + P(rien) 83.3 % x -6.08 % ne couvrent pas P(stop) 0.0 % x 61.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 34.98, ATR14 2.676 (7.65 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.377 ATR = 2.884 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.383 % | 34.8462 | 93.86 % | 95.46 % | 96.27 % | 97.67 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.765 % | 34.7124 | 86.1 % | 91.23 % | 92.33 % | 94.74 % | 95.83 % | 96.82 % |
| 0.15 ATR | 1.148 % | 34.5786 | 78.75 % | 86.39 % | 88.4 % | 91.61 % | 93.6 % | 95.59 % |
| 0.2 ATR | 1.53 % | 34.4448 | 71.0 % | 80.54 % | 84.26 % | 88.37 % | 90.85 % | 93.43 % |
| 0.25 ATR | 1.913 % | 34.311 | 64.85 % | 76.21 % | 80.73 % | 85.84 % | 88.72 % | 91.89 % |
| 0.35 ATR | 2.678 % | 34.0434 | 52.67 % | 67.24 % | 74.27 % | 79.47 % | 84.04 % | 88.3 % |
| 0.5 ATR | 3.825 % | 33.642 | 37.97 % | 54.44 % | 62.16 % | 71.08 % | 78.56 % | 84.39 % |
| 0.75 ATR | 5.738 % | 32.973 | 22.26 % | 39.42 % | 48.64 % | 59.05 % | 69.41 % | 76.8 % |
| 1.0 ATR | 7.65 % | 32.304 | 9.97 % | 24.8 % | 34.91 % | 46.11 % | 58.54 % | 68.17 % |
| 1.25 ATR | 9.563 % | 31.635 | 3.93 % | 14.42 % | 24.12 % | 34.88 % | 50.51 % | 61.81 % |
| 1.5 ATR | 11.475 % | 30.966 | 1.21 % | 7.16 % | 15.94 % | 25.48 % | 41.36 % | 56.16 % |
| 2.0 ATR | 15.3 % | 29.628 | 0.1 % | 1.92 % | 5.15 % | 14.36 % | 28.66 % | 45.48 % |
| 2.5 ATR | 19.125 % | 28.29 | 0.0 % | 0.2 % | 1.31 % | 6.07 % | 18.7 % | 35.01 % |
| 3.0 ATR | 22.95 % | 26.952 | 0.0 % | 0.1 % | 0.4 % | 2.83 % | 11.99 % | 26.9 % |
| 4.0 ATR | 30.6 % | 24.276 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 3.46 % | 12.32 % |
| 6.0 ATR | 45.901 % | 18.924 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.21 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.66 ATR | 0.86 ATR | 1.00 ATR | 1.12 ATR | 1.40 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.82 ATR | 1.04 ATR | 1.23 ATR | 1.38 ATR | 1.77 ATR | 2.02 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.02 ATR | 1.30 ATR | 1.52 ATR | 1.75 ATR | 2.26 ATR | 2.67 ATR |
| **10 s.** | 0.60 ATR | 1.26 ATR | 1.40 ATR | 1.83 ATR | 2.18 ATR | 2.44 ATR | 3.23 ATR | 3.82 ATR |
| **20 s.** | 0.80 ATR | 1.79 ATR | 2.02 ATR | 2.62 ATR | 3.13 ATR | 3.47 ATR | 4.42 ATR | 5.33 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.428 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.657–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.738 %, prix 32.9728), p(touche) 39.42 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.816–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.65 %, prix 32.304), p(touche) 34.91 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.025–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.563 %, prix 31.6349), p(touche) 34.88 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.401–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.475 %, prix 30.966), p(touche) 41.36 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.023–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (19.125 %, prix 28.2901), p(touche) 35.01 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (75.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 54.2 | bear 10.6 | side 35.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.084% → cible +8.386% / stop −4.193%, p_fill 56%, n_eff≈62.0) : P(cible|rempli) **2%** · **EV/risk -0.127** (×p_fill ; si rempli -0.96% du capital)
  - **swing** (entrée dip −4.58% → cible +11.221% / stop −8.017%, p_fill 50%, n_eff≈59.3) : P(cible|rempli) **23%** · **EV/risk -0.112** (×p_fill ; si rempli -1.78% du capital)
  - **deep** (entrée dip −7.075% → cible +14.208% / stop −12.348%, p_fill 44%, n_eff≈50.1) : P(cible|rempli) **20%** · **EV/risk -0.175** (×p_fill ; si rempli -4.85% du capital)
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
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.44 · part idiosyncratique 0.56
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.8  _(momentum haussier)_
- **ADX** : 29.2  _(tendance etablie)_
- **MACD** : hist 0.749  _(bullish_recent)_
- **BB** : %B 0.92 · largeur 27.1%
- **ATR** : 2.68 (25.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.142  _(accumulation)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 45.0  _(transition)_
- **MA** : MA20 31.44 · MA50 36.76 · MA200 41.44  _(prix > MA20)_
- **Dist MA** : MA20 +11.3% · MA50 -4.8% · MA200 -15.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (699029 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
