# RHM

**Generated** : 2026-11-03T21:40:06.400749+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1004.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)  
> ↳ spot €1004.80 (+1.4% vs entrée) · entrée €990.46 · stop €970.65 · T1 €1010.19 · R/R 1.0  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-03 : 1004.8 · ATR Wilder 35.56 (3.54 %)_
- **Swing** : plage **954.29 → 925.55** (-5.03 % a -7.89 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 928.8-940.0 (A). stop INDICATIF 875.33 (-5.43 % sous le bas ; sous le support 893.11-919.11 (- 0,5 ATR)).
- **Deep** : plage **925.55 → 840.45** (-7.89 % a -16.36 % sous la cloture, 2.39 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 893.11-919.11 (A) ; 819.81-846.61 (B). stop INDICATIF 804.89 (-4.23 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (2.58 ATR sous le plus haut 20 s., RSI(2) 29.8 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 976.0-987.1 (B, -1.76 %) ; 928.8-940.0 (A, -6.45 %) ; 893.11-919.11 (A, -8.53 %) ; 819.81-846.61 (B, -15.74 %) ; 677.76-692.54 (B, -31.08 %) ; 617.47-627.13 (C, -37.59 %)
- Resistances reelles au-dessus : 1045.0-1060.4 (A, 4.0 %) ; 1096.6-1105.6 (A, 9.14 %) ; 1120.6-1134.6 (B, 11.52 %) ; 1146.0-1158.6 (A, 14.05 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.07 %)** : le gap seul le franchit 0.157 % des séances (2 fois sur 1274).
   - exécution **8.071 pt plus bas** dans le cas TYPIQUE (médiane), 13.902 au p90, **15.359 au pire**
   - perte réelle **15.141 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 7.07 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0127 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3272** [0.2606 ; 0.3995] _(largeur 13.9 pt, n_eff 173.1)_
   - swing : **0.4895** [0.4371 ; 0.5421] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4945** [0.442 ; 0.5471] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (28.6 pt), deep (29.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.55 %** | CVaR **-6.3 %** | vol 2.79 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 1.75 % contre 2.94 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.83 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.871 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5283** (β de hausse 0.5767, asymétrie 0.9161) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.158× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 931.6285 sur grid_snapped (1.55 ATR, 7.282 %) — p(stop avant cible) 0.4181 [0.37 ; 0.47], R/R 3.76, perte reelle 7.72 % (gap inclus), CVaR 10.815 %, EV -0.6483 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9513 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.16 ATR (stop 3.078 %) — p(stop avant cible) 0.7332 [0.68 ; 0.78], R/R 8.828, perte reelle 3.288 % (gap inclus), EV -0.3008 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 8.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.733, borne haute 0.778 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 0.4 % x 29.03 % + P(rien) 26.3 % x 7.59 % ne couvrent pas P(stop) 73.3 % x 3.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 5.893 %) — p(stop avant cible) 0.5368 [0.48 ; 0.59], R/R 4.643, perte reelle 6.252 % (gap inclus), EV -0.68 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.537, borne haute 0.589 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 0.7 % x 29.03 % + P(rien) 45.6 % x 5.43 % ne couvrent pas P(stop) 53.7 % x 6.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 1.55 ATR (stop 8.555 %) — p(stop avant cible) 0.3531 [0.30 ; 0.40], R/R 3.211, perte reelle 9.04 % (gap inclus), EV -0.7681 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.77 %) : P(cible) 0.7 % x 29.03 % + P(rien) 64.0 % x 3.46 % ne couvrent pas P(stop) 35.3 % x 9.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.43 ATR (stop 11.986 %) — p(stop avant cible) 0.1768 [0.14 ; 0.22], R/R 2.325, perte reelle 12.486 % (gap inclus), EV -0.7376 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 0.7 % x 29.03 % + P(rien) 81.6 % x 1.54 % ne couvrent pas P(stop) 17.7 % x 12.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.16 ATR (stop 1.805 %) — p(stop avant cible) 0.8483 [0.81 ; 0.88], R/R 15.399, perte reelle 1.885 % (gap inclus), EV -0.0215 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 15.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.848, borne haute 0.883 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.3 % x 29.03 % + P(rien) 14.9 % x 10.04 % ne couvrent pas P(stop) 84.8 % x 1.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.929 %) — p(stop avant cible) 0.6767 [0.63 ; 0.72], R/R 7.001, perte reelle 4.146 % (gap inclus), EV -0.419 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 7.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.677, borne haute 0.724 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 0.4 % x 29.03 % + P(rien) 31.9 % x 7.12 % ne couvrent pas P(stop) 67.7 % x 4.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 4.911 %) — p(stop avant cible) 0.606 [0.55 ; 0.66], R/R 5.536, perte reelle 5.244 % (gap inclus), EV -0.521 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.606, borne haute 0.656 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 0.4 % x 29.03 % + P(rien) 39.0 % x 6.49 % ne couvrent pas P(stop) 60.6 % x 5.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.55 ATR (stop 7.282 %) — p(stop avant cible) 0.4181 [0.37 ; 0.47], R/R 3.76, perte reelle 7.72 % (gap inclus), EV -0.6483 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 0.7 % x 29.03 % + P(rien) 57.5 % x 4.12 % ne couvrent pas P(stop) 41.8 % x 7.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 7.858 %) — p(stop avant cible) 0.3816 [0.33 ; 0.43], R/R 3.479, perte reelle 8.343 % (gap inclus), EV -0.6793 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 0.7 % x 29.03 % + P(rien) 61.1 % x 3.75 % ne couvrent pas P(stop) 38.2 % x 8.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 2.43 ATR (stop 10.713 %) — p(stop avant cible) 0.2157 [0.17 ; 0.26], R/R 2.59, perte reelle 11.207 % (gap inclus), EV -0.6945 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 0.7 % x 29.03 % + P(rien) 77.7 % x 1.94 % ne couvrent pas P(stop) 21.6 % x 11.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 13.751 %) — p(stop avant cible) 0.1281 [0.10 ; 0.17], R/R 2.015, perte reelle 14.406 % (gap inclus), EV -0.7629 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 0.7 % x 29.03 % + P(rien) 86.5 % x 1.01 % ne couvrent pas P(stop) 12.8 % x 14.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 15.716 %) — p(stop avant cible) 0.0979 [0.07 ; 0.13], R/R 1.778, perte reelle 16.321 % (gap inclus), EV -0.8308 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 0.7 % x 29.03 % + P(rien) 89.5 % x 0.62 % ne couvrent pas P(stop) 9.8 % x 16.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 17.68 %) — p(stop avant cible) 0.0677 [0.04 ; 0.10], R/R 1.588, perte reelle 18.283 % (gap inclus), EV -0.8247 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 0.7 % x 29.03 % + P(rien) 92.5 % x 0.22 % ne couvrent pas P(stop) 6.8 % x 18.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 19.645 %) — p(stop avant cible) 0.0445 [0.03 ; 0.07], R/R 1.43, perte reelle 20.299 % (gap inclus), EV -0.8147 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 0.7 % x 29.03 % + P(rien) 94.8 % x -0.13 % ne couvrent pas P(stop) 4.5 % x 20.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 21.609 %) — p(stop avant cible) 0.0283 [0.01 ; 0.05], R/R 1.304, perte reelle 22.268 % (gap inclus), EV -0.7499 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 0.7 % x 29.03 % + P(rien) 96.4 % x -0.34 % ne couvrent pas P(stop) 2.8 % x 22.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 23.574 %) — p(stop avant cible) 0.0087 [0.00 ; 0.02], R/R 1.175, perte reelle 24.706 % (gap inclus), EV -0.6074 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 0.7 % x 29.03 % + P(rien) 98.4 % x -0.61 % ne couvrent pas P(stop) 0.9 % x 24.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 25.538 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 1.118, perte reelle 25.972 % (gap inclus), EV -0.6092 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.61 %) : P(cible) 0.7 % x 29.03 % + P(rien) 98.8 % x -0.69 % ne couvrent pas P(stop) 0.5 % x 25.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 27.503 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 1.055, perte reelle 27.503 % (gap inclus), EV -0.5702 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 0.7 % x 29.03 % + P(rien) 98.9 % x -0.68 % ne couvrent pas P(stop) 0.4 % x 27.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 29.467 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 0.985, perte reelle 29.467 % (gap inclus), EV -0.5638 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 0.7 % x 29.03 % + P(rien) 98.9 % x -0.68 % ne couvrent pas P(stop) 0.4 % x 29.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 31.432 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.923, perte reelle 31.432 % (gap inclus), EV -0.4448 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 0.7 % x 29.03 % + P(rien) 99.3 % x -0.66 % ne couvrent pas P(stop) 0.0 % x 31.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1004.8, ATR14 39.4786 (3.929 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.389 ATR = 1.528 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.196 % | 1002.8261 | 89.55 % | 92.3 % | 93.58 % | 94.75 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.393 % | 1000.8521 | 83.63 % | 88.15 % | 90.12 % | 91.68 % | 95.42 % | 96.48 % |
| 0.15 ATR | 0.589 % | 998.8782 | 76.43 % | 82.92 % | 85.87 % | 88.32 % | 92.94 % | 94.97 % |
| 0.2 ATR | 0.786 % | 996.9043 | 69.72 % | 78.38 % | 81.62 % | 85.15 % | 90.85 % | 93.37 % |
| 0.25 ATR | 0.982 % | 994.9303 | 62.13 % | 72.56 % | 76.48 % | 80.99 % | 88.26 % | 91.56 % |
| 0.35 ATR | 1.375 % | 990.9825 | 53.35 % | 65.35 % | 70.85 % | 76.44 % | 85.57 % | 89.45 % |
| 0.5 ATR | 1.964 % | 985.0607 | 40.43 % | 54.69 % | 61.36 % | 69.01 % | 80.2 % | 84.32 % |
| 0.75 ATR | 2.947 % | 975.1911 | 23.47 % | 38.99 % | 47.23 % | 57.62 % | 70.65 % | 77.99 % |
| 1.0 ATR | 3.929 % | 965.3214 | 13.21 % | 26.85 % | 36.56 % | 48.51 % | 62.69 % | 71.66 % |
| 1.25 ATR | 4.911 % | 955.4518 | 7.59 % | 18.16 % | 26.48 % | 39.41 % | 54.73 % | 65.53 % |
| 1.5 ATR | 5.893 % | 945.5822 | 3.85 % | 13.13 % | 20.55 % | 31.68 % | 46.37 % | 58.39 % |
| 2.0 ATR | 7.858 % | 925.8429 | 1.78 % | 7.11 % | 12.35 % | 21.29 % | 34.93 % | 49.05 % |
| 2.5 ATR | 9.822 % | 906.1036 | 0.49 % | 3.36 % | 6.42 % | 12.57 % | 25.17 % | 39.4 % |
| 3.0 ATR | 11.787 % | 886.3643 | 0.1 % | 1.38 % | 3.85 % | 7.72 % | 17.41 % | 32.86 % |
| 4.0 ATR | 15.716 % | 846.8858 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.66 % | 20.6 % |
| 6.0 ATR | 23.574 % | 767.9287 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.83 ATR | 1.14 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.57 ATR | 0.65 ATR | 0.87 ATR | 1.05 ATR | 1.20 ATR | 1.76 ATR | 2.28 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.09 ATR | 1.31 ATR | 1.53 ATR | 2.20 ATR | 2.78 ATR |
| **5 s.** | 0.38 ATR | 0.96 ATR | 1.10 ATR | 1.46 ATR | 1.82 ATR | 2.07 ATR | 2.77 ATR | 3.61 ATR |
| **10 s.** | 0.64 ATR | 1.39 ATR | 1.56 ATR | 2.10 ATR | 2.51 ATR | 2.83 ATR | 3.85 ATR | 4.93 ATR |
| **20 s.** | 0.87 ATR | 1.95 ATR | 2.21 ATR | 2.99 ATR | 3.64 ATR | 4.07 ATR | 5.24 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.447–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.654–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.947 %, prix 975.1885), p(touche) 38.99 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.802–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.929 %, prix 965.3214), p(touche) 36.56 % (en stress 96.08 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.096–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.911 %, prix 955.4543), p(touche) 39.41 % (en stress 98.02 %)  ✅ optimum identifie (81.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.56–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.858 %, prix 925.8428), p(touche) 34.93 % (en stress 96.04 %)  ✅ optimum identifie (97.8 % des re-echantillons)
- **20 seance(s)** : plage utile 2.21–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.822 %, prix 906.1085), p(touche) 39.4 % (en stress 98.0 %)  ✅ optimum identifie (97.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.002 | EV/share : €-0.047 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 13 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.7 | bear 5.0 | side 10.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.429% → cible +1.993% / stop −2.0%, p_fill 54%, n_eff≈59.6) : P(cible|rempli) **21%** · **EV/risk -0.119** (×p_fill ; si rempli -0.44% du capital)
  - **swing** (entrée dip −3.141% → cible +6.968% / stop −4.056%, p_fill 38%, n_eff≈44.4) : P(cible|rempli) **14%** · **EV/risk -0.058** (×p_fill ; si rempli -0.62% du capital)
  - **deep** (entrée dip −4.857% → cible +8.894% / stop −6.194%, p_fill 37%, n_eff≈42.4) : P(cible|rempli) **14%** · **EV/risk -0.112** (×p_fill ; si rempli -1.86% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→43% · +3.0%→26% · +5.0%→4% · +8.0%→1%
- Range intraday médian 3.92% (p90 6.37%) · excursion haute méd. +1.54% / basse méd. −1.65%
- Profil de vol intra : ouverture 2.386% vs midi 0.887% vs clôture 1.007% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.037)_ ; drift intra méd. 0.01% ; recovery-V 14%
- **σ réalisé intraday** 2.348% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 65% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 1019.35 (VA 1013.75–1023.55 ; dernier close 1015.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 52% · rebond 59% · **stop −2.85%** sous le fill (sous le bruit) · cible +1.34% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 39% (gap-down >1% 7% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.73%) · haut méd +0.46% · range méd 1.27%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.14%) · haut méd +0.6% · range méd 1.62%
- Excursion ouverture 30min (n=160) : bas méd −0.92% (p90 −2.31%) · haut méd +0.75% · range méd 1.88%
- Excursion ouverture 60min (n=160) : bas méd −0.94% (p90 −2.38%) · haut méd +0.88% · range méd 2.09%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1019.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 75% (112/159) · gap 18% · délai 0.4min · rebond 57% (62/112) (MFE +1.08%)
   - −1.0% : fill 30min 42% · séance 64% (98/159) · gap 7% · délai 6.3min · rebond 59% (58/98) (MFE +1.26%)
   - −1.5% : fill 30min 26% · séance 52% (80/159) · gap 4% · délai 29.9min · rebond 59% (47/80) (MFE +1.34%)
   - −2.0% : fill 30min 16% · séance 40% (66/159) · gap 2% · délai 88.0min · rebond 52% (38/66) (MFE +1.2%)
   - −3.0% : fill 30min 6% · séance 25% (38/159) · gap 2% · délai 141.2min · rebond 42% (18/38) (MFE +0.97%)
   - −4.0% : fill 30min 2% · séance 12% (21/159) · gap 1% · délai 153.2min · rebond 60% (12/21) (MFE +1.73%)
   - −5.0% : fill 30min 0% · séance 5% (11/159) · gap 0% · délai 103.2min · rebond 94% (10/11) (MFE +2.81%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −1.37%) → stop au-delà de −1.11% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.44%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −1.48%) → stop au-delà de −0.96% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=544 jambes) : jambe baissière méd −0.97% (p90 −2.4%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (37 séances) :
      · −1.0% : fill 98% (36/37) · rebond 69% (25/36)
      · −2.0% : fill 65% (28/37) · rebond 46% (16/28)
      · −3.0% : fill 46% (16/37) · rebond 33% (7/16)
      · −4.0% : fill 34% (12/37) · rebond 58% (7/12)
      · −5.0% : fill 15% (6/37) · rebond 100% (6/6)
   - **flat** (29 séances) :
      · −1.0% : fill 74% (21/29) · rebond 60% (14/21)
      · −2.0% : fill 41% (11/29) · rebond 75% (8/11)
      · −3.0% : fill 21% (6/29) · rebond 67% (3/6)
      · −4.0% : fill 3% (2/29) · rebond 62% (1/2)
      · −5.0% : fill 3% (2/29) · rebond 62% (1/2)
   - **gap-up** (93 séances) :
      · −1.0% : fill 41% (41/93) · rebond 46% (19/41)
      · −2.0% : fill 27% (27/93) · rebond 44% (14/27)
      · −3.0% : fill 15% (16/93) · rebond 41% (8/16)
      · −4.0% : fill 4% (7/93) · rebond 70% (4/7)
      · −5.0% : fill 1% (3/93) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 57% si les 15 1res min sont vertes (73 cas) · 32% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **45min** → P(séance verte=clôture>ouverture) 65% si début vert vs 20% si rouge (base 43% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **65%** · continue >prix actuel 48% ; creux résiduel méd -1.21% (q20 -2.27%) → **SL/trailing à −2.27%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +2.5% → **scale +1.5% / runner +2.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **20%** (continue à baisser 58%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.6%** (au-delà de la MAE q10 -3.6%), cible rebond +1.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.04% .. +2.68%] · haut q95 +2.92% · bas q05 -2.8%
   - 60min (n=160) : retour [-2.51% .. +3.12%] · haut q95 +3.43% · bas q05 -3.45%
   - 2h (n=160) : retour [-3.37% .. +2.76%] · haut q95 +3.79% · bas q05 -3.97%
   - 4h (n=160) : retour [-3.21% .. +2.84%] · haut q95 +4.17% · bas q05 -4.74%
   - 6h (n=160) : retour [-3.6% .. +3.07%] · haut q95 +4.55% · bas q05 -5.07%
   - session (n=160) : retour [-4.05% .. +3.96%] · haut q95 +4.97% · bas q05 -5.07%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.18 · part idiosyncratique 0.82
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.4  _(neutre)_
- **ADX** : 23.3  _(pas de tendance nette)_
- **MACD** : hist 0.52  _(pas de croisement recent)_
- **BB** : %B 0.49 · largeur 17.8%
- **ATR** : 39.48 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.152  _(accumulation)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 58.3  _(transition)_
- **MA** : MA20 1007.25 · MA50 1017.47 · MA200 1254.5  _(prix < MA20)_
- **Dist MA** : MA20 -0.2% · MA50 -1.2% · MA200 -19.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (770738 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
