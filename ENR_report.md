# ENR

**Generated** : 2026-11-03T01:07:34.683770+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €130.42  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)  
> ↳ spot €130.42 (+1.2% vs entrée) · entrée €128.90 · stop €125.49 · T1 €135.70 · R/R 1.99  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-02 : 130.42 · ATR Wilder 6.13 (4.7 %)_
- **Swing** : plage **123.08 → 118.03** (-5.62 % a -9.5 % sous la cloture, 0.82 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 122.83-124.46 (B). stop INDICATIF 113.77 (-3.61 % sous le bas ; sous le support 116.84-117.65 (- 0,5 ATR)).
- **Deep** : plage **118.03 → 109.01** (-9.5 % a -16.41 % sous la cloture, 1.47 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 116.84-117.65 (A) ; 113.47-114.51 (A) ; 109.88-110.08 (C). stop INDICATIF 100.14 (-8.14 % sous le bas ; sous le support 103.21-104.4 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.36 ATR sous le plus haut 20 s., RSI(2) 52.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 122.83-124.46 (B, -4.57 %) ; 116.84-117.65 (A, -9.79 %) ; 113.47-114.51 (A, -12.2 %) ; 109.88-110.08 (C, -15.6 %) ; 103.21-104.4 (B, -19.95 %) ; 98.56-100.32 (A, -23.08 %)
- Resistances reelles au-dessus : 135.7-138.68 (A, 4.05 %) ; 139.16-140.18 (A, 6.7 %) ; 143.38-146.08 (B, 9.94 %) ; 146.98-148.4 (B, 12.7 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.75 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.87 %)** : le gap seul le franchit 0.314 % des séances (4 fois sur 1274).
   - exécution **7.033 pt plus bas** dans le cas TYPIQUE (médiane), 22.011 au p90, **27.887 au pire**
   - perte réelle **18.578 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 7.87 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0336 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.382 % | p01 -5.39 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2904** [0.2267 ; 0.3611] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.398** [0.3474 ; 0.4503] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.381** [0.331 ; 0.433] _(largeur 10.2 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.83 %** | CVaR **-6.77 %** | vol 3.21 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 6.12 % contre 3.07 % aujourd'hui, rapport 1.99)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.88 % vs -9.98 % si l'on extrapolait par √5 _(rapport 0.89 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3424** (β de hausse 1.1031, asymétrie 1.2169) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.299× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 122.2473 sur grid_snapped (0.88 ATR, 6.266 %) — p(stop avant cible) 0.5242 [0.47 ; 0.58], R/R 6.486, perte reelle 6.713 % (gap inclus), CVaR 10.606 %, EV -0.9762 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0442 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.524, borne haute 0.577 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.88 ATR (stop 7.109 %) — p(stop avant cible) 0.469 [0.42 ; 0.52], R/R 5.559, perte reelle 7.833 % (gap inclus), EV -1.0712 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.87 % > budget 12.00 %
      - ⚠ support DETECTE a 0.88 ATR du spot — compartiment <1, mesure a 46.6 % de casse (IC clusterise [0.432 ; 0.500] sur 1220 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 0.1 % x 43.54 % + P(rien) 53.0 % x 4.86 % ne couvrent pas P(stop) 46.9 % x 7.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 2.3 ATR (stop 14.629 %) — p(stop avant cible) 0.09 [0.06 ; 0.12], R/R 2.828, perte reelle 15.399 % (gap inclus), EV 0.1165 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.02 % > budget 12.00 %
   - 🟢 support a 4.42 ATR (stop 25.853 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 1.544, perte reelle 28.195 % (gap inclus), EV 0.5156 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.74 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.324 %) — p(stop avant cible) 0.9087 [0.87 ; 0.94], R/R 31.278, perte reelle 1.392 % (gap inclus), EV -0.3802 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 31.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.909, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 0.0 % x 43.54 % + P(rien) 9.1 % x 9.69 % ne couvrent pas P(stop) 90.9 % x 1.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.649 %) — p(stop avant cible) 0.7867 [0.74 ; 0.83], R/R 15.762, perte reelle 2.762 % (gap inclus), EV -0.4289 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 15.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.787, borne haute 0.827 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 0.1 % x 43.54 % + P(rien) 21.3 % x 8.08 % ne couvrent pas P(stop) 78.7 % x 2.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 grid_snapped a 0.88 ATR (stop 6.266 %) — p(stop avant cible) 0.5242 [0.47 ; 0.58], R/R 6.486, perte reelle 6.713 % (gap inclus), EV -0.9762 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.524, borne haute 0.577 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 0.1 % x 43.54 % + P(rien) 47.5 % x 5.30 % ne couvrent pas P(stop) 52.4 % x 6.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.5 ATR (stop 7.946 %) — p(stop avant cible) 0.4094 [0.36 ; 0.46], R/R 4.973, perte reelle 8.755 % (gap inclus), EV -0.958 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 0.1 % x 43.54 % + P(rien) 59.0 % x 4.41 % ne couvrent pas P(stop) 40.9 % x 8.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 9.27 %) — p(stop avant cible) 0.3346 [0.29 ; 0.39], R/R 4.349, perte reelle 10.012 % (gap inclus), EV -0.8484 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 0.1 % x 43.54 % + P(rien) 66.5 % x 3.72 % ne couvrent pas P(stop) 33.5 % x 10.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 10.594 %) — p(stop avant cible) 0.2622 [0.22 ; 0.31], R/R 3.869, perte reelle 11.255 % (gap inclus), EV -0.6832 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 0.1 % x 43.54 % + P(rien) 73.7 % x 3.04 % ne couvrent pas P(stop) 26.2 % x 11.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 grid_snapped a 2.3 ATR (stop 13.787 %) — p(stop avant cible) 0.1169 [0.09 ; 0.15], R/R 2.983, perte reelle 14.594 % (gap inclus), EV -0.0674 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 0.1 % x 43.54 % + P(rien) 88.2 % x 1.83 % ne couvrent pas P(stop) 11.7 % x 14.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+43.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 15.892 %) — p(stop avant cible) 0.0521 [0.03 ; 0.08], R/R 2.576, perte reelle 16.901 % (gap inclus), EV 0.292 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.94 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 18.54 %) — p(stop avant cible) 0.0395 [0.02 ; 0.06], R/R 2.271, perte reelle 19.174 % (gap inclus), EV 0.3079 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.02 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 21.189 %) — p(stop avant cible) 0.0064 [0.00 ; 0.02], R/R 1.77, perte reelle 24.605 % (gap inclus), EV 0.4574 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.17 % > budget 12.00 %
   - 🟢 grid_snapped a 4.42 ATR (stop 25.01 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 1.562, perte reelle 27.874 % (gap inclus), EV 0.5167 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.72 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 29.134 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 1.438, perte reelle 30.282 % (gap inclus), EV 0.5299 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.47 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 31.783 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.317, perte reelle 33.07 % (gap inclus), EV 0.5433 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.23 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 34.432 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.249, perte reelle 34.857 % (gap inclus), EV 0.5413 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.27 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 37.08 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 1.174, perte reelle 37.103 % (gap inclus), EV 0.5419 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.28 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 39.729 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 1.096, perte reelle 39.729 % (gap inclus), EV 0.5379 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.30 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 42.377 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 1.027, perte reelle 42.377 % (gap inclus), EV 0.5437 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.19 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 130.42, ATR14 6.9086 (5.297 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.37 ATR = 1.96 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.265 % | 130.0746 | 91.42 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.53 % | 129.7291 | 83.63 % | 88.15 % | 90.51 % | 92.57 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.795 % | 129.3837 | 76.23 % | 82.23 % | 85.77 % | 88.61 % | 91.24 % | 93.37 % |
| 0.2 ATR | 1.059 % | 129.0383 | 70.32 % | 78.87 % | 82.81 % | 86.53 % | 89.45 % | 91.96 % |
| 0.25 ATR | 1.324 % | 128.6929 | 63.61 % | 74.43 % | 79.05 % | 83.27 % | 87.46 % | 90.65 % |
| 0.35 ATR | 1.854 % | 128.002 | 52.07 % | 64.96 % | 70.36 % | 76.04 % | 82.39 % | 86.83 % |
| 0.5 ATR | 2.649 % | 126.9657 | 36.69 % | 52.02 % | 59.58 % | 66.73 % | 74.83 % | 80.8 % |
| 0.75 ATR | 3.973 % | 125.2386 | 19.72 % | 36.03 % | 45.36 % | 54.75 % | 65.77 % | 74.07 % |
| 1.0 ATR | 5.297 % | 123.5114 | 11.14 % | 25.86 % | 34.78 % | 44.85 % | 57.61 % | 66.33 % |
| 1.25 ATR | 6.621 % | 121.7843 | 6.11 % | 17.37 % | 25.2 % | 36.04 % | 48.96 % | 58.79 % |
| 1.5 ATR | 7.946 % | 120.0571 | 2.96 % | 11.25 % | 18.18 % | 28.32 % | 41.89 % | 52.56 % |
| 2.0 ATR | 10.594 % | 116.6029 | 0.79 % | 4.24 % | 8.99 % | 16.83 % | 28.86 % | 41.31 % |
| 2.5 ATR | 13.243 % | 113.1486 | 0.3 % | 2.07 % | 4.25 % | 10.0 % | 20.2 % | 31.56 % |
| 3.0 ATR | 15.892 % | 109.6943 | 0.1 % | 0.89 % | 2.08 % | 5.35 % | 13.23 % | 23.72 % |
| 4.0 ATR | 21.189 % | 102.7857 | 0.1 % | 0.39 % | 1.19 % | 2.48 % | 7.06 % | 13.27 % |
| 6.0 ATR | 31.783 % | 88.9686 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.43 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.34 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.02 ATR | 1.17 ATR | 1.59 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.05 ATR | 1.26 ATR | 1.44 ATR | 1.95 ATR | 2.42 ATR |
| **5 s.** | 0.37 ATR | 0.87 ATR | 1.00 ATR | 1.35 ATR | 1.64 ATR | 1.86 ATR | 2.50 ATR | 3.12 ATR |
| **10 s.** | 0.50 ATR | 1.22 ATR | 1.39 ATR | 1.84 ATR | 2.22 ATR | 2.51 ATR | 3.52 ATR | 4.85 ATR |
| **20 s.** | 0.71 ATR | 1.61 ATR | 1.84 ATR | 2.43 ATR | 2.92 ATR | 3.36 ATR | 4.83 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.419–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.61–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.973 %, prix 125.2384), p(touche) 36.03 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.759–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.297 %, prix 123.5117), p(touche) 34.78 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (85.6 % des re-echantillons)
- **5 seance(s)** : plage utile 0.996–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.297 %, prix 123.5117), p(touche) 44.85 % (en stress 99.01 %)  ✅ optimum identifie (90.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.39–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.946 %, prix 120.0568), p(touche) 41.89 % (en stress 100.0 %)  ✅ optimum identifie (92.8 % des re-echantillons)
- **20 seance(s)** : plage utile 1.836–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.594 %, prix 116.6033), p(touche) 41.31 % (en stress 99.0 %)  ✅ optimum identifie (90.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 56.9 | bear 36.3 | side 6.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.172% → cible +5.277% / stop −2.639%, p_fill 69%, n_eff≈72.0) : P(cible|rempli) **1%** · **EV/risk -0.168** (×p_fill ; si rempli -0.64% du capital)
  - **swing** (entrée dip −2.573% → cible +6.793% / stop −5.437%, p_fill 53%, n_eff≈63.3) : P(cible|rempli) **18%** · **EV/risk -0.074** (×p_fill ; si rempli -0.76% du capital)
  - **deep** (entrée dip −3.974% → cible +8.354% / stop −8.275%, p_fill 59%, n_eff≈67.5) : P(cible|rempli) **27%** · **EV/risk -0.040** (×p_fill ; si rempli -0.56% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→34% · +3.0%→15% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.62% (p90 6.06%) · excursion haute méd. +1.37% / basse méd. −1.89%
- Profil de vol intra : ouverture 1.961% vs midi 0.824% vs clôture 1.048% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 61% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. -0.864% ; recovery-V 25%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 83% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 121.5065 (VA 120.2185–123.5995 ; dernier close 118.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 18% · rebond 57% · **stop −4.86%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.22 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 38% (gap-down >1% 20% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.49% (p90 −1.69%) · haut méd +0.49% · range méd 1.14%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.05%) · haut méd +0.58% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.19%) · haut méd +0.62% · range méd 1.69%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.35%) · haut méd +0.68% · range méd 1.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 118.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 70% (115/159) · gap 30% · délai 0.2min · rebond 48% (59/115) (MFE +0.88%)
   - −1.0% : fill 30min 40% · séance 66% (107/159) · gap 20% · délai 8.6min · rebond 51% (59/107) (MFE +1.04%)
   - −1.5% : fill 30min 29% · séance 53% (88/159) · gap 13% · délai 12.6min · rebond 55% (48/88) (MFE +1.28%)
   - −2.0% : fill 30min 23% · séance 44% (73/159) · gap 9% · délai 20.7min · rebond 50% (41/73) (MFE +1.0%)
   - −3.0% : fill 30min 10% · séance 29% (48/159) · gap 3% · délai 251.6min · rebond 40% (24/48) (MFE +0.66%)
   - −4.0% : fill 30min 6% · séance 18% (32/159) · gap 2% · délai 200.1min · rebond 57% (20/32) (MFE +1.05%)
   - −5.0% : fill 30min 4% · séance 13% (24/159) · gap 0% · délai 397.7min · rebond 38% (11/24) (MFE +0.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.17%) → stop au-delà de −1.55% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.63%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.66%) → stop au-delà de −0.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=526 jambes) : jambe baissière méd −1.04% (p90 −2.31%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (53/54) · rebond 41% (26/53)
      · −2.0% : fill 84% (41/54) · rebond 49% (20/41)
      · −3.0% : fill 59% (30/54) · rebond 40% (14/30)
      · −4.0% : fill 39% (22/54) · rebond 75% (16/22)
      · −5.0% : fill 30% (18/54) · rebond 47% (10/18)
   - **flat** (18 séances) :
      · −1.0% : fill 59% (13/18) · rebond 64% (9/13)
      · −2.0% : fill 33% (8/18) · rebond 68% (6/8)
      · −3.0% : fill 20% (5/18) · rebond 48% (3/5)
      · −4.0% : fill 6% (3/18) · rebond 59% (2/3)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 46% (41/87) · rebond 61% (24/41)
      · −2.0% : fill 23% (24/87) · rebond 46% (15/24)
      · −3.0% : fill 13% (13/87) · rebond 36% (7/13)
      · −4.0% : fill 9% (7/87) · rebond 11% (2/7)
      · −5.0% : fill 5% (4/87) · rebond 12% (1/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 61% si les 15 1res min sont vertes (71 cas) · 30% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 43% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **72%** · continue >prix actuel 56% ; creux résiduel méd -1.18% (q20 -2.25%) → **SL/trailing à −2.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.1% → **scale +1.08% / runner +2.1%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **21%** (continue à baisser 57%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.96%** (au-delà de la MAE q10 -4.96%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.97% .. +1.62%] · haut q95 +2.08% · bas q05 -2.65%
   - 60min (n=160) : retour [-2.5% .. +1.42%] · haut q95 +2.41% · bas q05 -3.07%
   - 2h (n=160) : retour [-2.53% .. +2.22%] · haut q95 +2.56% · bas q05 -3.58%
   - 4h (n=160) : retour [-2.61% .. +2.42%] · haut q95 +3.02% · bas q05 -4.04%
   - 6h (n=160) : retour [-3.22% .. +3.06%] · haut q95 +3.68% · bas q05 -4.31%
   - session (n=160) : retour [-5.78% .. +2.83%] · haut q95 +4.66% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.37%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.67 · part idiosyncratique 0.33
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.5  _(momentum baissier)_
- **ADX** : 19.5  _(pas de tendance nette)_
- **MACD** : hist 0.181  _(bullish_recent)_
- **BB** : %B 0.38 · largeur 24.9%
- **ATR** : 6.91 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.124  _(accumulation)_
- **Vol ratio** : 0.41  _(volume atone)_
- **Choppiness** : 46.5  _(transition)_
- **MA** : MA20 134.4 · MA50 140.05 · MA200 154.28  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 -6.9% · MA200 -15.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (745860 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
