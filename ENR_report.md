# ENR

**Generated** : 2026-10-09T21:45:15.621019+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €145.36  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (5 séance(s) de retard, drapeau lu sur first_passage_by_horizon); usable=false (intervalle le plus large 26.8 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €145.36 (+2.6% vs entrée) · entrée €141.73 · stop €130.39 · T1 €144.13 · R/R 0.21  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-09 : 145.36 · ATR Wilder 4.99 (3.43 %)_
- **Swing** : plage **139.81 → 135.62** (-3.82 % a -6.7 % sous la cloture, 0.84 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 137.46-139.16 (A) ; 133.85-135.72 (A). stop INDICATIF 128.4 (-5.32 % sous le bas ; sous le support 130.89-133.3 (- 0,5 ATR)).
- **Deep** : plage **135.62 → 128.63** (-6.7 % a -11.51 % sous la cloture, 1.4 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 133.85-135.72 (A) ; 130.89-133.3 (A). stop INDICATIF 120.33 (-6.45 % sous le bas ; sous le support 122.83-124.32 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.13 ATR sous le plus haut 20 s., RSI(2) 67.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 143.38-143.38 (C, -1.36 %) ; 137.46-139.16 (A, -4.27 %) ; 133.85-135.72 (A, -6.63 %) ; 130.89-133.3 (A, -8.3 %) ; 122.83-124.32 (A, -14.47 %) ; 113.47-114.51 (A, -21.22 %)
- Resistances reelles au-dessus : 150.58-151.76 (A, 3.59 %) ; 156.62-158.85 (A, 7.75 %) ; 159.46-161.46 (A, 9.7 %) ; 163.86-165.86 (A, 12.73 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.59 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.8 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **7.37 pt plus bas** dans le cas TYPIQUE (médiane), 23.04 au p90, **26.957 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 8.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0307 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.33 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.007** [0.0009 ; 0.0289] _(largeur 2.8 pt, n_eff 173.1)_
   - swing : **0.5091** [0.4565 ; 0.5615] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4735** [0.4213 ; 0.5262] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 41.8 observations effectives », dont la borne haute a 95 % vaut environ 7.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (26.8 pt), swing (35.9 pt), deep (34.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.63 %** | CVaR **-6.59 %** | vol 3.19 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.98 % contre 2.93 % aujourd'hui, rapport 2.04)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3498** (β de hausse 1.0878, asymétrie 1.2409) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.334× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 132.1639 sur atr_grid (2.75 ATR, 9.078 %) — p(stop avant cible) 0.3047 [0.26 ; 0.35], R/R 3.125, perte reelle 9.352 % (gap inclus), CVaR 10.748 %, EV -0.1684 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.966 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 22 des 22 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 38.2 % de la queue et il ne reste que -1251.71 EUR a partager. Prix du risque -0.354 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.952 %) — p(stop avant cible) 0.6002 [0.55 ; 0.65], R/R 5.72, perte reelle 5.109 % (gap inclus), EV -0.3488 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.600, borne haute 0.651 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 0.5 % x 29.22 % + P(rien) 39.5 % x 6.51 % ne couvrent pas P(stop) 60.0 % x 5.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.49 ATR (stop 6.817 %) — p(stop avant cible) 0.4684 [0.42 ; 0.52], R/R 4.138, perte reelle 7.062 % (gap inclus), EV -0.539 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.5 % x 29.22 % + P(rien) 52.7 % x 4.97 % ne couvrent pas P(stop) 46.8 % x 7.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 3.13 ATR (stop 12.219 %) — p(stop avant cible) 0.1275 [0.10 ; 0.17], R/R 2.275, perte reelle 12.843 % (gap inclus), EV 0.4414 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.81 % > budget 12.00 %
   - 🟢 support a 6.65 ATR (stop 23.833 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 1.098, perte reelle 26.625 % (gap inclus), EV 1.1204 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.76 % > budget 12.00 %
   - 🟢 support a 10.7 ATR (stop 37.225 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.785, perte reelle 37.236 % (gap inclus), EV 1.1851 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.95 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.825 %) — p(stop avant cible) 0.9332 [0.90 ; 0.96], R/R 33.376, perte reelle 0.876 % (gap inclus), EV -0.1505 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 33.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.933, borne haute 0.956 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.1 % x 29.22 % + P(rien) 6.5 % x 9.57 % ne couvrent pas P(stop) 93.3 % x 0.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.651 %) — p(stop avant cible) 0.8604 [0.82 ; 0.89], R/R 17.021, perte reelle 1.717 % (gap inclus), EV -0.1883 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 17.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.860, borne haute 0.894 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.3 % x 29.22 % + P(rien) 13.7 % x 8.84 % ne couvrent pas P(stop) 86.0 % x 1.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.476 %) — p(stop avant cible) 0.7869 [0.74 ; 0.83], R/R 11.346, perte reelle 2.576 % (gap inclus), EV -0.2407 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 11.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.787, borne haute 0.828 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 0.4 % x 29.22 % + P(rien) 20.9 % x 7.97 % ne couvrent pas P(stop) 78.7 % x 2.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.301 %) — p(stop avant cible) 0.7117 [0.66 ; 0.76], R/R 8.495, perte reelle 3.44 % (gap inclus), EV -0.2009 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 8.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.712, borne haute 0.757 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.4 % x 29.22 % + P(rien) 28.4 % x 7.48 % ne couvrent pas P(stop) 71.2 % x 3.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.49 ATR (stop 5.916 %) — p(stop avant cible) 0.5171 [0.46 ; 0.57], R/R 4.782, perte reelle 6.111 % (gap inclus), EV -0.3526 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.517, borne haute 0.569 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 0.5 % x 29.22 % + P(rien) 47.8 % x 5.56 % ne couvrent pas P(stop) 51.7 % x 6.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 7.428 %) — p(stop avant cible) 0.4122 [0.36 ; 0.46], R/R 3.824, perte reelle 7.643 % (gap inclus), EV -0.3286 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.5 % x 29.22 % + P(rien) 58.3 % x 4.59 % ne couvrent pas P(stop) 41.2 % x 7.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 8.253 %) — p(stop avant cible) 0.3651 [0.32 ; 0.42], R/R 3.432, perte reelle 8.515 % (gap inclus), EV -0.3314 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.5 % x 29.22 % + P(rien) 63.0 % x 4.17 % ne couvrent pas P(stop) 36.5 % x 8.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 9.078 %) — p(stop avant cible) 0.3047 [0.26 ; 0.35], R/R 3.125, perte reelle 9.352 % (gap inclus), EV -0.1684 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.5 % x 29.22 % + P(rien) 69.0 % x 3.67 % ne couvrent pas P(stop) 30.5 % x 9.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 3.13 ATR (stop 11.317 %) — p(stop avant cible) 0.1757 [0.14 ; 0.22], R/R 2.476, perte reelle 11.805 % (gap inclus), EV 0.2007 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.03 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 13.205 %) — p(stop avant cible) 0.0889 [0.06 ; 0.12], R/R 2.039, perte reelle 14.333 % (gap inclus), EV 0.6586 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.21 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 14.855 %) — p(stop avant cible) 0.0642 [0.04 ; 0.09], R/R 1.831, perte reelle 15.96 % (gap inclus), EV 0.7828 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.27 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.506 %) — p(stop avant cible) 0.0312 [0.02 ; 0.05], R/R 1.612, perte reelle 18.124 % (gap inclus), EV 0.9732 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.94 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 18.156 %) — p(stop avant cible) 0.0248 [0.01 ; 0.05], R/R 1.506, perte reelle 19.409 % (gap inclus), EV 1.0069 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.74 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 19.807 %) — p(stop avant cible) 0.0146 [0.01 ; 0.03], R/R 1.381, perte reelle 21.154 % (gap inclus), EV 1.0701 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.22 % > budget 12.00 %
   - 🟢 grid_snapped a 6.65 ATR (stop 22.932 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 1.112, perte reelle 26.283 % (gap inclus), EV 1.1222 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.73 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.759 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 1.069, perte reelle 27.339 % (gap inclus), EV 1.1382 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.62 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 26.409 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 1.029, perte reelle 28.406 % (gap inclus), EV 1.1536 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.48 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 145.36, ATR14 4.7986 (3.301 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.212 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.165 % | 145.1201 | 91.52 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.33 % | 144.8801 | 83.73 % | 88.15 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.495 % | 144.6402 | 76.33 % | 82.23 % | 85.87 % | 88.61 % | 91.14 % | 93.37 % |
| 0.2 ATR | 0.66 % | 144.4003 | 70.41 % | 78.97 % | 83.0 % | 86.44 % | 89.35 % | 91.96 % |
| 0.25 ATR | 0.825 % | 144.1604 | 63.91 % | 74.63 % | 79.35 % | 83.27 % | 87.26 % | 90.55 % |
| 0.35 ATR | 1.155 % | 143.6805 | 51.78 % | 64.76 % | 70.26 % | 75.74 % | 81.89 % | 86.43 % |
| 0.5 ATR | 1.651 % | 142.9607 | 36.39 % | 51.73 % | 59.39 % | 66.24 % | 74.23 % | 80.3 % |
| 0.75 ATR | 2.476 % | 141.7611 | 19.53 % | 35.64 % | 44.96 % | 54.06 % | 65.07 % | 73.47 % |
| 1.0 ATR | 3.301 % | 140.5614 | 10.95 % | 25.37 % | 33.99 % | 43.66 % | 56.42 % | 65.23 % |
| 1.25 ATR | 4.126 % | 139.3618 | 6.02 % | 17.08 % | 24.7 % | 35.25 % | 47.86 % | 57.69 % |
| 1.5 ATR | 4.952 % | 138.1621 | 2.76 % | 10.86 % | 17.59 % | 27.43 % | 40.6 % | 51.36 % |
| 2.0 ATR | 6.602 % | 135.7629 | 0.79 % | 3.95 % | 8.5 % | 15.94 % | 27.76 % | 40.1 % |
| 2.5 ATR | 8.253 % | 133.3636 | 0.3 % | 1.97 % | 3.95 % | 9.21 % | 19.1 % | 30.35 % |
| 3.0 ATR | 9.903 % | 130.9643 | 0.1 % | 0.79 % | 1.88 % | 4.85 % | 12.14 % | 22.51 % |
| 4.0 ATR | 13.205 % | 126.1657 | 0.1 % | 0.39 % | 1.09 % | 2.28 % | 6.27 % | 12.46 % |
| 6.0 ATR | 19.807 % | 116.5686 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 1.05 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.60 ATR | 0.81 ATR | 1.01 ATR | 1.16 ATR | 1.56 ATR | 1.92 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.03 ATR | 1.24 ATR | 1.42 ATR | 1.92 ATR | 2.38 ATR |
| **5 s.** | 0.36 ATR | 0.85 ATR | 0.97 ATR | 1.32 ATR | 1.61 ATR | 1.82 ATR | 2.44 ATR | 2.98 ATR |
| **10 s.** | 0.48 ATR | 1.19 ATR | 1.35 ATR | 1.80 ATR | 2.16 ATR | 2.45 ATR | 3.37 ATR | 4.62 ATR |
| **20 s.** | 0.69 ATR | 1.56 ATR | 1.78 ATR | 2.36 ATR | 2.84 ATR | 3.25 ATR | 4.69 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.605–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.476 %, prix 141.7609), p(touche) 35.64 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.749–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.476 %, prix 141.7609), p(touche) 44.96 % (en stress 96.08 %)  ✅ optimum identifie (87.0 % des re-echantillons)
- **5 seance(s)** : plage utile 0.968–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.301 %, prix 140.5617), p(touche) 43.66 % (en stress 99.01 %)  ✅ optimum identifie (89.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.348–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.952 %, prix 138.1618), p(touche) 40.6 % (en stress 100.0 %)  ✅ optimum identifie (92.6 % des re-echantillons)
- **20 seance(s)** : plage utile 1.782–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.602 %, prix 135.7633), p(touche) 40.1 % (en stress 99.0 %)  ✅ optimum identifie (87.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 10.9 | side 84.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 145.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.5% → cible +1.693% / stop −8.0%, p_fill 35%, n_eff≈41.8) : P(cible|rempli) **29%** · **EV/risk -0.003** (×p_fill ; si rempli -0.06% du capital)
  - **swing** (entrée dip −5.499% → cible +3.906% / stop −3.493%, p_fill 23%, n_eff≈27.3) : P(cible|rempli) **51%** · **EV/risk +0.029** (×p_fill ; si rempli +0.44% du capital)
  - **deep** (entrée dip −8.498% → cible +5.704% / stop −5.412%, p_fill 17%, n_eff≈20.4) : P(cible|rempli) **78%** · **EV/risk +0.099** (×p_fill ; si rempli +3.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→77% · +1.0%→62% · +2.0%→38% · +3.0%→18% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.7% (p90 6.11%) · excursion haute méd. +1.52% / basse méd. −1.74%
- Profil de vol intra : ouverture 1.958% vs midi 0.866% vs clôture 1.062% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. -0.357% ; recovery-V 20%
- **σ réalisé intraday** 2.187% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 72% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 146.1558 (VA 145.4312–146.3972 ; dernier close 145.44)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 49% · rebond 59% · **stop −3.83%** sous le fill (sous le bruit) · cible +1.48% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 33% (gap-down >1% 15% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.53% (p90 −1.67%) · haut méd +0.44% · range méd 1.12%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.17%) · haut méd +0.59% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.23%) · haut méd +0.62% · range méd 1.68%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.44%) · haut méd +0.73% · range méd 1.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 145.42 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 69% (116/159) · gap 24% · délai 0.5min · rebond 58% (62/116) (MFE +1.2%)
   - −1.0% : fill 30min 38% · séance 64% (108/159) · gap 15% · délai 10.3min · rebond 61% (62/108) (MFE +1.36%)
   - −1.5% : fill 30min 25% · séance 49% (88/159) · gap 11% · délai 22.9min · rebond 59% (50/88) (MFE +1.48%)
   - −2.0% : fill 30min 17% · séance 40% (73/159) · gap 8% · délai 62.1min · rebond 54% (44/73) (MFE +1.08%)
   - −3.0% : fill 30min 9% · séance 22% (46/159) · gap 2% · délai 189.8min · rebond 44% (26/46) (MFE +0.86%)
   - −4.0% : fill 30min 6% · séance 14% (33/159) · gap 1% · délai 76.7min · rebond 58% (22/33) (MFE +1.12%)
   - −5.0% : fill 30min 2% · séance 11% (24/159) · gap 0% · délai 388.5min · rebond 43% (12/24) (MFE +0.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.72%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.33% (p90 −1.32%) → stop au-delà de −0.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −0.95%) → stop au-delà de −0.7% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=521 jambes) : jambe baissière méd −1.02% (p90 −2.33%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 98% (52/53) · rebond 55% (28/52)
      · −2.0% : fill 75% (39/53) · rebond 44% (20/39)
      · −3.0% : fill 45% (27/53) · rebond 33% (14/27)
      · −4.0% : fill 37% (22/53) · rebond 60% (16/22)
      · −5.0% : fill 31% (18/53) · rebond 49% (11/18)
   - **flat** (17 séances) :
      · −1.0% : fill 78% (14/17) · rebond 65% (10/14)
      · −2.0% : fill 44% (9/17) · rebond 67% (6/9)
      · −3.0% : fill 27% (6/17) · rebond 46% (3/6)
      · −4.0% : fill 9% (4/17) · rebond 52% (2/4)
      · −5.0% : fill 7% (3/17) · rebond 0% (0/3)
   - **gap-up** (89 séances) :
      · −1.0% : fill 43% (42/89) · rebond 66% (24/42)
      · −2.0% : fill 21% (25/89) · rebond 65% (18/25)
      · −3.0% : fill 8% (13/89) · rebond 72% (9/13)
      · −4.0% : fill 4% (7/89) · rebond 47% (4/7)
      · −5.0% : fill 2% (3/89) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 66% si les 15 1res min sont vertes (75 cas) · 24% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:29** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 219min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **73%** · continue >prix actuel 54% ; creux résiduel méd -1.07% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.24% / q75 +2.25% → **scale +1.24% / runner +2.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.65%** (au-delà de la MAE q10 -3.65%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.93% .. +1.69%] · haut q95 +2.36% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.46% .. +1.94%] · haut q95 +2.55% · bas q05 -2.86%
   - 2h (n=160) : retour [-2.78% .. +2.36%] · haut q95 +2.76% · bas q05 -3.56%
   - 4h (n=160) : retour [-3.15% .. +2.63%] · haut q95 +3.22% · bas q05 -3.93%
   - 6h (n=160) : retour [-3.69% .. +3.35%] · haut q95 +4.15% · bas q05 -4.56%
   - session (n=160) : retour [-4.9% .. +3.08%] · haut q95 +4.77% · bas q05 -6.18%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.56 · part idiosyncratique 0.44
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.7  _(neutre)_
- **ADX** : 8.2  _(pas de tendance nette)_
- **MACD** : hist 0.547  _(pas de croisement recent)_
- **BB** : %B 0.7 · largeur 11.2%
- **ATR** : 4.8 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.118  _(distribution)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 65.8  _(marche en range (choppy))_
- **MA** : MA20 142.23 · MA50 147.45 · MA200 153.92  _(prix > MA20)_
- **Dist MA** : MA20 +2.2% · MA50 -1.4% · MA200 -5.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (950725 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
