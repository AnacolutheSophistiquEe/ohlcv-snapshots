# RHM

**Generated** : 2026-10-23T21:39:10.689489+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €1019.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)  
> ↳ spot €1019.00 (+4.0% vs entrée) · entrée €979.63 · stop €940.32 · T1 €1041.07 · R/R 1.56  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 173 % hors [0,100] (R² max 0.61). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 1019.0 · ATR Wilder 37.27 (3.66 %)_
- **Swing** : plage **966.48 → 936.14** (-5.15 % a -8.13 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 953.59-953.59 (C) ; 928.8-940.0 (A). stop INDICATIF 874.47 (-6.59 % sous le bas ; sous le support 893.11-919.11 (- 0,5 ATR)).
- **Deep** : plage **936.14 → 846.75** (-8.13 % a -16.9 % sous la cloture, 2.4 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 928.8-940.0 (A) ; 893.11-919.11 (A). stop INDICATIF 801.18 (-5.38 % sous le bas ; sous le support 819.81-846.61 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.08 ATR sous le plus haut 20 s., RSI(2) 33.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 976.0-987.1 (B, -3.13 %) ; 953.59-953.59 (C, -6.42 %) ; 928.8-940.0 (A, -7.75 %) ; 893.11-919.11 (A, -9.8 %) ; 819.81-846.61 (B, -16.92 %) ; 677.76-695.89 (A, -31.71 %)
- Resistances reelles au-dessus : 1045.0-1055.06 (A, 2.55 %) ; 1096.6-1105.6 (A, 7.62 %) ; 1120.6-1134.6 (B, 9.97 %) ; 1146.0-1158.6 (A, 12.46 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.72 %)** : le gap seul le franchit 0.157 % des séances (2 fois sur 1274).
   - exécution **7.421 pt plus bas** dans le cas TYPIQUE (médiane), 13.252 au p90, **14.709 au pire**
   - perte réelle **15.141 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 7.72 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0116 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3404** [0.2729 ; 0.4132] _(largeur 14.0 pt, n_eff 173.1)_
   - swing : **0.4956** [0.4431 ; 0.5482] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.5039** [0.4514 ; 0.5564] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (26.5 pt), swing (30.0 pt), deep (31.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.55 %** | CVaR **-6.3 %** | vol 2.79 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 1.78 % contre 2.97 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.83 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.871 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5283** (β de hausse 0.5653, asymétrie 0.9346) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.143× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 931.6943 sur grid_snapped (1.92 ATR, 8.568 %) — p(stop avant cible) 0.3676 [0.32 ; 0.42], R/R 3.009, perte reelle 9.05 % (gap inclus), CVaR 11.973 %, EV -0.9215 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.944 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.787 %) — p(stop avant cible) 0.5531 [0.50 ; 0.60], R/R 4.423, perte reelle 6.157 % (gap inclus), EV -0.7854 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.553, borne haute 0.605 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.79 %) : P(cible) 0.7 % x 27.23 % + P(rien) 44.0 % x 5.50 % ne couvrent pas P(stop) 55.3 % x 6.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 1.92 ATR (stop 9.667 %) — p(stop avant cible) 0.28 [0.23 ; 0.33], R/R 2.688, perte reelle 10.13 % (gap inclus), EV -0.8611 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 0.9 % x 27.23 % + P(rien) 71.1 % x 2.42 % ne couvrent pas P(stop) 28.0 % x 10.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.8 ATR (stop 13.052 %) — p(stop avant cible) 0.1552 [0.12 ; 0.20], R/R 1.995, perte reelle 13.65 % (gap inclus), EV -0.9725 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 0.9 % x 27.23 % + P(rien) 83.5 % x 1.07 % ne couvrent pas P(stop) 15.5 % x 13.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 0.965 %) — p(stop avant cible) 0.9283 [0.90 ; 0.95], R/R 26.584, perte reelle 1.024 % (gap inclus), EV -0.1521 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 26.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.928, borne haute 0.952 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.2 % x 27.23 % + P(rien) 7.0 % x 10.68 % ne couvrent pas P(stop) 92.8 % x 1.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.929 %) — p(stop avant cible) 0.8612 [0.82 ; 0.89], R/R 13.58, perte reelle 2.005 % (gap inclus), EV -0.2254 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 13.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.861, borne haute 0.895 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.3 % x 27.23 % + P(rien) 13.6 % x 10.46 % ne couvrent pas P(stop) 86.1 % x 2.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.894 %) — p(stop avant cible) 0.7761 [0.73 ; 0.82], R/R 8.777, perte reelle 3.103 % (gap inclus), EV -0.4953 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 8.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.776, borne haute 0.818 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 0.4 % x 27.23 % + P(rien) 21.9 % x 8.16 % ne couvrent pas P(stop) 77.6 % x 3.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.858 %) — p(stop avant cible) 0.6944 [0.64 ; 0.74], R/R 6.672, perte reelle 4.082 % (gap inclus), EV -0.5282 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.694, borne haute 0.741 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.4 % x 27.23 % + P(rien) 30.1 % x 7.25 % ne couvrent pas P(stop) 69.4 % x 4.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 4.823 %) — p(stop avant cible) 0.6213 [0.57 ; 0.67], R/R 5.323, perte reelle 5.116 % (gap inclus), EV -0.5797 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.621, borne haute 0.671 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 0.5 % x 27.23 % + P(rien) 37.4 % x 6.59 % ne couvrent pas P(stop) 62.1 % x 5.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.92 ATR (stop 8.568 %) — p(stop avant cible) 0.3676 [0.32 ; 0.42], R/R 3.009, perte reelle 9.05 % (gap inclus), EV -0.9215 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 0.8 % x 27.23 % + P(rien) 62.4 % x 3.49 % ne couvrent pas P(stop) 36.8 % x 9.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 2.8 ATR (stop 11.952 %) — p(stop avant cible) 0.1841 [0.15 ; 0.23], R/R 2.186, perte reelle 12.457 % (gap inclus), EV -0.8766 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 0.9 % x 27.23 % + P(rien) 80.7 % x 1.44 % ne couvrent pas P(stop) 18.4 % x 12.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 15.432 %) — p(stop avant cible) 0.1107 [0.08 ; 0.15], R/R 1.698, perte reelle 16.034 % (gap inclus), EV -0.9848 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 0.9 % x 27.23 % + P(rien) 88.0 % x 0.61 % ne couvrent pas P(stop) 11.1 % x 16.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 17.362 %) — p(stop avant cible) 0.0727 [0.05 ; 0.10], R/R 1.514, perte reelle 17.989 % (gap inclus), EV -0.9637 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 0.9 % x 27.23 % + P(rien) 91.8 % x 0.10 % ne couvrent pas P(stop) 7.3 % x 17.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 19.291 %) — p(stop avant cible) 0.0478 [0.03 ; 0.07], R/R 1.364, perte reelle 19.965 % (gap inclus), EV -0.9471 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 0.9 % x 27.23 % + P(rien) 94.3 % x -0.26 % ne couvrent pas P(stop) 4.8 % x 19.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 21.22 %) — p(stop avant cible) 0.0331 [0.02 ; 0.06], R/R 1.245, perte reelle 21.872 % (gap inclus), EV -0.9428 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 0.9 % x 27.23 % + P(rien) 95.8 % x -0.50 % ne couvrent pas P(stop) 3.3 % x 21.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 23.149 %) — p(stop avant cible) 0.0121 [0.00 ; 0.03], R/R 1.128, perte reelle 24.149 % (gap inclus), EV -0.7673 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.77 %) : P(cible) 0.9 % x 27.23 % + P(rien) 97.9 % x -0.75 % ne couvrent pas P(stop) 1.2 % x 24.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 25.078 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 1.056, perte reelle 25.792 % (gap inclus), EV -0.7469 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 0.9 % x 27.23 % + P(rien) 98.5 % x -0.87 % ne couvrent pas P(stop) 0.5 % x 25.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 27.007 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 1.008, perte reelle 27.007 % (gap inclus), EV -0.7066 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 0.9 % x 27.23 % + P(rien) 98.6 % x -0.86 % ne couvrent pas P(stop) 0.4 % x 27.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 28.936 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.941, perte reelle 28.936 % (gap inclus), EV -0.7149 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 0.9 % x 27.23 % + P(rien) 98.6 % x -0.86 % ne couvrent pas P(stop) 0.4 % x 28.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 30.865 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.882, perte reelle 30.865 % (gap inclus), EV -0.6257 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 0.9 % x 27.23 % + P(rien) 98.9 % x -0.85 % ne couvrent pas P(stop) 0.1 % x 30.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1019.0, ATR14 39.3143 (3.858 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.392 ATR = 1.512 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.193 % | 1017.0343 | 89.64 % | 92.4 % | 93.58 % | 94.75 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.386 % | 1015.0686 | 83.73 % | 88.25 % | 90.12 % | 91.68 % | 95.42 % | 96.48 % |
| 0.15 ATR | 0.579 % | 1013.1029 | 76.53 % | 83.12 % | 85.97 % | 88.42 % | 93.13 % | 94.97 % |
| 0.2 ATR | 0.772 % | 1011.1371 | 69.82 % | 78.58 % | 81.72 % | 85.25 % | 91.04 % | 93.37 % |
| 0.25 ATR | 0.965 % | 1009.1714 | 62.33 % | 72.85 % | 76.68 % | 81.09 % | 88.56 % | 91.56 % |
| 0.35 ATR | 1.35 % | 1005.24 | 53.65 % | 65.75 % | 71.05 % | 76.63 % | 85.97 % | 89.45 % |
| 0.5 ATR | 1.929 % | 999.3429 | 40.63 % | 55.08 % | 61.66 % | 69.21 % | 80.5 % | 84.22 % |
| 0.75 ATR | 2.894 % | 989.5143 | 23.57 % | 39.29 % | 47.53 % | 57.82 % | 70.95 % | 77.89 % |
| 1.0 ATR | 3.858 % | 979.6857 | 13.21 % | 26.95 % | 36.76 % | 48.71 % | 63.08 % | 71.56 % |
| 1.25 ATR | 4.823 % | 969.8572 | 7.59 % | 18.26 % | 26.78 % | 39.8 % | 55.12 % | 65.43 % |
| 1.5 ATR | 5.787 % | 960.0286 | 3.94 % | 13.23 % | 20.85 % | 32.08 % | 46.77 % | 58.59 % |
| 2.0 ATR | 7.716 % | 940.3715 | 1.78 % | 7.11 % | 12.35 % | 21.29 % | 35.02 % | 48.94 % |
| 2.5 ATR | 9.645 % | 920.7143 | 0.49 % | 3.36 % | 6.42 % | 12.57 % | 25.17 % | 39.3 % |
| 3.0 ATR | 11.574 % | 901.0572 | 0.1 % | 1.38 % | 3.85 % | 7.72 % | 17.41 % | 32.86 % |
| 4.0 ATR | 15.432 % | 861.7429 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.66 % | 20.6 % |
| 6.0 ATR | 23.149 % | 783.1144 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.84 ATR | 1.14 ATR | 1.43 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.88 ATR | 1.06 ATR | 1.20 ATR | 1.76 ATR | 2.28 ATR |
| **3 s.** | 0.28 ATR | 0.71 ATR | 0.81 ATR | 1.09 ATR | 1.32 ATR | 1.55 ATR | 2.20 ATR | 2.78 ATR |
| **5 s.** | 0.38 ATR | 0.96 ATR | 1.10 ATR | 1.47 ATR | 1.83 ATR | 2.07 ATR | 2.77 ATR | 3.61 ATR |
| **10 s.** | 0.64 ATR | 1.40 ATR | 1.57 ATR | 2.10 ATR | 2.51 ATR | 2.83 ATR | 3.85 ATR | 4.93 ATR |
| **20 s.** | 0.86 ATR | 1.95 ATR | 2.20 ATR | 2.99 ATR | 3.64 ATR | 4.07 ATR | 5.24 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.45–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.66–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.894 %, prix 989.5101), p(touche) 39.29 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.809–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.858 %, prix 979.687), p(touche) 36.76 % (en stress 95.1 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.104–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.823 %, prix 969.8536), p(touche) 39.8 % (en stress 98.02 %)  ✅ optimum identifie (83.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.575–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.716 %, prix 940.374), p(touche) 35.02 % (en stress 96.04 %)  ✅ optimum identifie (97.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.204–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.645 %, prix 920.7174), p(touche) 39.3 % (en stress 98.0 %)  ✅ optimum identifie (97.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.065 | EV/share : €-2.551 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 11 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 84.0 | bear 5.0 | side 11.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.755% → cible +1.964% / stop −2.0%, p_fill 49%, n_eff≈51.8) : P(cible|rempli) **20%** · **EV/risk -0.124** (×p_fill ; si rempli -0.51% du capital)
  - **swing** (entrée dip −3.862% → cible +6.272% / stop −4.013%, p_fill 34%, n_eff≈39.3) : P(cible|rempli) **15%** · **EV/risk -0.095** (×p_fill ; si rempli -1.12% du capital)
  - **deep** (entrée dip −5.973% → cible +8.653% / stop −6.155%, p_fill 32%, n_eff≈36.5) : P(cible|rempli) **10%** · **EV/risk -0.122** (×p_fill ; si rempli -2.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→42% · +3.0%→25% · +5.0%→3% · +8.0%→1%
- Range intraday médian 3.8% (p90 6.51%) · excursion haute méd. +1.53% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.349% vs midi 0.894% vs clôture 1.023% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 7% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. -0.537% ; recovery-V 10%
- **σ réalisé intraday** 2.314% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 64% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 954.8875 (VA 951.8125–962.2675 ; dernier close 959.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 24% · rebond 48% · **stop −2.11%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.4% · baisse 30% (gap-down >1% 7% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.74%) · haut méd +0.44% · range méd 1.28%
- Excursion ouverture 15min (n=160) : bas méd −0.86% (p90 −2.06%) · haut méd +0.6% · range méd 1.7%
- Excursion ouverture 30min (n=160) : bas méd −0.94% (p90 −2.14%) · haut méd +0.75% · range méd 1.9%
- Excursion ouverture 60min (n=160) : bas méd −0.96% (p90 −2.41%) · haut méd +0.82% · range méd 2.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 956.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 74% (109/159) · gap 17% · délai 1.1min · rebond 51% (57/109) (MFE +1.03%)
   - −1.0% : fill 30min 40% · séance 65% (97/159) · gap 7% · délai 9.5min · rebond 60% (57/97) (MFE +1.23%)
   - −1.5% : fill 30min 25% · séance 53% (79/159) · gap 5% · délai 33.3min · rebond 55% (45/79) (MFE +1.15%)
   - −2.0% : fill 30min 16% · séance 43% (66/159) · gap 2% · délai 76.1min · rebond 56% (39/66) (MFE +1.22%)
   - −3.0% : fill 30min 6% · séance 24% (37/159) · gap 2% · délai 141.3min · rebond 48% (19/37) (MFE +0.99%)
   - −4.0% : fill 30min 2% · séance 11% (21/159) · gap 1% · délai 149.9min · rebond 65% (12/21) (MFE +1.74%)
   - −5.0% : fill 30min 0% · séance 5% (11/159) · gap 0% · délai 307.4min · rebond 92% (10/11) (MFE +2.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −1.32%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.62%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.68%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=561 jambes) : jambe baissière méd −1.02% (p90 −2.36%) · ~7.7 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (31 séances) :
      · −1.0% : fill 97% (30/31) · rebond 65% (20/30)
      · −2.0% : fill 70% (25/31) · rebond 46% (15/25)
      · −3.0% : fill 48% (14/31) · rebond 33% (7/14)
      · −4.0% : fill 38% (11/31) · rebond 65% (7/11)
      · −5.0% : fill 15% (6/31) · rebond 100% (6/6)
   - **flat** (27 séances) :
      · −1.0% : fill 86% (21/27) · rebond 66% (15/21)
      · −2.0% : fill 52% (12/27) · rebond 75% (9/12)
      · −3.0% : fill 27% (6/27) · rebond 67% (3/6)
      · −4.0% : fill 4% (2/27) · rebond 62% (1/2)
      · −5.0% : fill 4% (2/27) · rebond 62% (1/2)
   - **gap-up** (101 séances) :
      · −1.0% : fill 45% (46/101) · rebond 50% (22/46)
      · −2.0% : fill 28% (29/101) · rebond 49% (15/29)
      · −3.0% : fill 15% (17/101) · rebond 50% (9/17)
      · −4.0% : fill 5% (8/101) · rebond 66% (4/8)
      · −5.0% : fill 1% (3/101) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 49% si les 15 1res min sont vertes (73 cas) · 28% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 58% si début vert vs 20% si rouge (base 38% · écart 38 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **58%** · continue >prix actuel 45% ; creux résiduel méd -1.43% (q20 -2.65%) → **SL/trailing à −2.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.37% / q75 +2.51% → **scale +1.37% / runner +2.51%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **20%** (continue à baisser 61%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.38%** (au-delà de la MAE q10 -3.38%), cible rebond +1.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.57% .. +2.77%] · haut q95 +3.12% · bas q05 -2.92%
   - 60min (n=160) : retour [-2.47% .. +2.88%] · haut q95 +3.76% · bas q05 -3.36%
   - 2h (n=160) : retour [-3.19% .. +2.58%] · haut q95 +4.0% · bas q05 -3.76%
   - 4h (n=160) : retour [-3.2% .. +2.65%] · haut q95 +4.43% · bas q05 -4.1%
   - 6h (n=160) : retour [-3.5% .. +3.02%] · haut q95 +4.52% · bas q05 -4.31%
   - session (n=160) : retour [-4.02% .. +3.3%] · haut q95 +4.58% · bas q05 -4.8%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.27 · part idiosyncratique 0.73
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.2  _(momentum haussier)_
- **ADX** : 28.3  _(tendance etablie)_
- **MACD** : hist 9.774  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 18.9%
- **ATR** : 39.31 (15.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.047  _(neutre)_
- **Vol ratio** : 0.54  _(volume atone)_
- **Choppiness** : 40.8  _(transition)_
- **MA** : MA20 985.11 · MA50 1037.58 · MA200 1283.97  _(prix > MA20)_
- **Dist MA** : MA20 +3.4% · MA50 -1.8% · MA200 -20.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (809051 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
