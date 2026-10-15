# ENR

**Generated** : 2026-10-15T00:07:39.196608+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €135.70  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (8 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €135.70 (+2.0% vs entrée) · entrée €133.02 · stop €127.85 · T1 €138.80 · R/R 1.12  
> ↳ ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 135.7 · ATR Wilder 5.19 (3.82 %)_
- **Swing** : plage **129.96 → 125.59** (-4.23 % a -7.45 % sous la cloture, 0.84 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 120.23 (-4.27 % sous le bas ; sous le support 122.83-124.32 (- 0,5 ATR)).
- **Deep** : plage **125.59 → 118.33** (-7.45 % a -12.8 % sous la cloture, 1.4 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 122.83-124.32 (A). stop INDICATIF 110.87 (-6.3 % sous le bas ; sous le support 113.47-114.51 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.95 ATR sous le plus haut 20 s., RSI(2) 7.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 130.89-133.3 (A, -1.77 %) ; 122.83-124.32 (A, -8.39 %) ; 113.47-114.51 (A, -15.61 %) ; 109.88-110.08 (C, -18.88 %) ; 103.21-104.4 (B, -23.06 %) ; 98.56-100.32 (A, -26.07 %)
- Resistances reelles au-dessus : 137.46-139.16 (A, 1.3 %) ; 146.08-148.06 (A, 7.65 %) ; 150.58-151.76 (A, 10.97 %) ; 156.62-158.85 (A, 15.42 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.59 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.78 %)** : le gap seul le franchit 0.706 % des séances (9 fois sur 1274).
   - exécution **1.286 pt plus bas** dans le cas TYPIQUE (médiane), 14.307 au p90, **29.977 au pire**
   - perte réelle **11.87 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 5.78 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.043 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.33 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0068** [0.0009 ; 0.0285] _(largeur 2.8 pt, n_eff 173.1)_
   - swing : **0.4722** [0.42 ; 0.5249] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4403** [0.3887 ; 0.4929] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 76.8 observations effectives », dont la borne haute a 95 % vaut environ 3.9 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.65 %** | CVaR **-6.6 %** | vol 3.2 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.97 % contre 2.92 % aujourd'hui, rapport 2.04)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.76 % si l'on extrapolait par √5 _(rapport 0.903 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3422** (β de hausse 1.0908, asymétrie 1.2305) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.319× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 121.4864 sur atr_grid (2.75 ATR, 10.474 %) — p(stop avant cible) 0.227 [0.19 ; 0.27], R/R 3.559, perte reelle 10.772 % (gap inclus), CVaR 11.827 %, EV 0.0102 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9953 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 27.9 % de la queue et il ne reste que 13.84 EUR a partager. Prix du risque 0.004 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.04 ATR (stop 6.401 %) — p(stop avant cible) 0.4866 [0.43 ; 0.54], R/R 5.771, perte reelle 6.644 % (gap inclus), EV -0.4331 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 0.1 % x 38.34 % + P(rien) 51.3 % x 5.41 % ne couvrent pas P(stop) 48.7 % x 6.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+38.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 support a 4.3 ATR (stop 18.815 %) — p(stop avant cible) 0.022 [0.01 ; 0.04], R/R 1.923, perte reelle 19.938 % (gap inclus), EV 1.0273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.52 % > budget 12.00 %
      - ⚠ support DETECTE a 0.94 ATR du spot — compartiment <1, mesure a 47.1 % de casse (IC clusterise [0.439 ; 0.504] sur 1187 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🔴 support a 8.07 ATR (stop 33.16 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.129, perte reelle 33.967 % (gap inclus), EV 1.1942 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.86 % > budget 12.00 %
      - ⚠ support DETECTE a 7.42 ATR du spot — compartiment >=6, mesure a 58.0 % de casse (IC clusterise [0.419 ; 0.723] sur 50 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 0.952 %) — p(stop avant cible) 0.9205 [0.89 ; 0.95], R/R 38.204, perte reelle 1.004 % (gap inclus), EV -0.1501 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 38.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.920, borne haute 0.946 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.0 % x 38.34 % + P(rien) 8.0 % x 9.73 % ne couvrent pas P(stop) 92.0 % x 1.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+38.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 1.904 %) — p(stop avant cible) 0.8401 [0.80 ; 0.88], R/R 19.105, perte reelle 2.007 % (gap inclus), EV -0.312 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 19.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.840, borne haute 0.876 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 0.0 % x 38.34 % + P(rien) 16.0 % x 8.59 % ne couvrent pas P(stop) 84.0 % x 2.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+38.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 2.857 %) — p(stop avant cible) 0.7596 [0.71 ; 0.80], R/R 12.818, perte reelle 2.991 % (gap inclus), EV -0.2805 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 12.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.760, borne haute 0.802 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 0.1 % x 38.34 % + P(rien) 24.0 % x 8.19 % ne couvrent pas P(stop) 76.0 % x 2.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+38.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 1.04 ATR (stop 5.114 %) — p(stop avant cible) 0.586 [0.53 ; 0.64], R/R 7.254, perte reelle 5.285 % (gap inclus), EV -0.4065 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.586, borne haute 0.637 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 0.1 % x 38.34 % + P(rien) 41.3 % x 6.45 % ne couvrent pas P(stop) 58.6 % x 5.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+38.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.5 ATR (stop 5.713 %) — p(stop avant cible) 0.5249 [0.47 ; 0.58], R/R 6.475, perte reelle 5.921 % (gap inclus), EV -0.3376 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.525, borne haute 0.577 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 0.1 % x 38.34 % + P(rien) 47.4 % x 5.78 % ne couvrent pas P(stop) 52.5 % x 5.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+38.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 7.618 %) — p(stop avant cible) 0.4 [0.35 ; 0.45], R/R 4.904, perte reelle 7.819 % (gap inclus), EV -0.3081 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 0.1 % x 38.34 % + P(rien) 59.9 % x 4.66 % ne couvrent pas P(stop) 40.0 % x 7.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+38.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 8.57 %) — p(stop avant cible) 0.3225 [0.27 ; 0.37], R/R 4.338, perte reelle 8.838 % (gap inclus), EV -0.1673 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.1 % x 38.34 % + P(rien) 67.7 % x 3.92 % ne couvrent pas P(stop) 32.2 % x 8.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+38.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 9.522 %) — p(stop avant cible) 0.2765 [0.23 ; 0.33], R/R 3.92, perte reelle 9.781 % (gap inclus), EV -0.0833 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.1 % x 38.34 % + P(rien) 72.3 % x 3.59 % ne couvrent pas P(stop) 27.7 % x 9.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+38.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 10.474 %) — p(stop avant cible) 0.227 [0.19 ; 0.27], R/R 3.559, perte reelle 10.772 % (gap inclus), EV 0.0102 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 3.0 ATR (stop 11.426 %) — p(stop avant cible) 0.1681 [0.13 ; 0.21], R/R 3.212, perte reelle 11.938 % (gap inclus), EV 0.2588 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.15 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 13.331 %) — p(stop avant cible) 0.0869 [0.06 ; 0.12], R/R 2.659, perte reelle 14.418 % (gap inclus), EV 0.6727 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.22 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 15.235 %) — p(stop avant cible) 0.0494 [0.03 ; 0.08], R/R 2.323, perte reelle 16.505 % (gap inclus), EV 0.8767 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.47 % > budget 12.00 %
   - 🔴 grid_snapped a 4.3 ATR (stop 17.527 %) — p(stop avant cible) 0.0279 [0.01 ; 0.05], R/R 2.054, perte reelle 18.671 % (gap inclus), EV 1.0005 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.81 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.949 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 1.563, perte reelle 24.525 % (gap inclus), EV 1.1036 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.89 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.853 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 1.46, perte reelle 26.261 % (gap inclus), EV 1.1327 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.66 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.757 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 1.402, perte reelle 27.338 % (gap inclus), EV 1.1485 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.55 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.662 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.328, perte reelle 28.883 % (gap inclus), EV 1.1754 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.23 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.566 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.292, perte reelle 29.684 % (gap inclus), EV 1.1729 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.28 % > budget 12.00 %
   - 🔴 grid_snapped a 8.07 ATR (stop 31.873 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.157, perte reelle 33.129 % (gap inclus), EV 1.1952 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.84 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 135.7, ATR14 5.1686 (3.809 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.398 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.19 % | 135.4416 | 91.42 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.381 % | 135.1831 | 83.73 % | 88.25 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.571 % | 134.9247 | 76.43 % | 82.33 % | 85.87 % | 88.61 % | 91.14 % | 93.27 % |
| 0.2 ATR | 0.762 % | 134.6663 | 70.41 % | 78.97 % | 82.91 % | 86.53 % | 89.35 % | 91.86 % |
| 0.25 ATR | 0.952 % | 134.4079 | 63.91 % | 74.63 % | 79.25 % | 83.37 % | 87.36 % | 90.55 % |
| 0.35 ATR | 1.333 % | 133.891 | 51.78 % | 64.76 % | 70.16 % | 75.84 % | 81.99 % | 86.43 % |
| 0.5 ATR | 1.904 % | 133.1157 | 36.49 % | 51.83 % | 59.39 % | 66.44 % | 74.33 % | 80.3 % |
| 0.75 ATR | 2.857 % | 131.8236 | 19.53 % | 35.64 % | 44.96 % | 54.26 % | 65.07 % | 73.47 % |
| 1.0 ATR | 3.809 % | 130.5314 | 10.95 % | 25.37 % | 34.09 % | 43.96 % | 56.52 % | 65.33 % |
| 1.25 ATR | 4.761 % | 129.2393 | 6.02 % | 17.08 % | 24.7 % | 35.35 % | 47.86 % | 57.79 % |
| 1.5 ATR | 5.713 % | 127.9471 | 2.76 % | 10.86 % | 17.59 % | 27.43 % | 40.6 % | 51.36 % |
| 2.0 ATR | 7.618 % | 125.3629 | 0.79 % | 3.95 % | 8.5 % | 15.94 % | 27.76 % | 40.1 % |
| 2.5 ATR | 9.522 % | 122.7786 | 0.3 % | 1.97 % | 3.95 % | 9.21 % | 19.1 % | 30.35 % |
| 3.0 ATR | 11.426 % | 120.1943 | 0.1 % | 0.79 % | 1.88 % | 4.85 % | 12.14 % | 22.51 % |
| 4.0 ATR | 15.235 % | 115.0257 | 0.1 % | 0.39 % | 1.09 % | 2.28 % | 6.27 % | 12.46 % |
| 6.0 ATR | 22.853 % | 104.6886 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 1.05 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.60 ATR | 0.81 ATR | 1.01 ATR | 1.16 ATR | 1.56 ATR | 1.92 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.03 ATR | 1.24 ATR | 1.42 ATR | 1.92 ATR | 2.38 ATR |
| **5 s.** | 0.36 ATR | 0.85 ATR | 0.97 ATR | 1.32 ATR | 1.61 ATR | 1.82 ATR | 2.44 ATR | 2.98 ATR |
| **10 s.** | 0.49 ATR | 1.19 ATR | 1.35 ATR | 1.80 ATR | 2.16 ATR | 2.45 ATR | 3.37 ATR | 4.62 ATR |
| **20 s.** | 0.69 ATR | 1.56 ATR | 1.78 ATR | 2.36 ATR | 2.84 ATR | 3.25 ATR | 4.69 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.417–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.605–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.857 %, prix 131.823), p(touche) 35.64 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.749–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.857 %, prix 131.823), p(touche) 44.96 % (en stress 96.08 %)  ✅ optimum identifie (84.4 % des re-echantillons)
- **5 seance(s)** : plage utile 0.975–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.809 %, prix 130.5312), p(touche) 43.96 % (en stress 99.01 %)  ✅ optimum identifie (89.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.348–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.713 %, prix 127.9475), p(touche) 40.6 % (en stress 100.0 %)  ✅ optimum identifie (92.0 % des re-echantillons)
- **20 seance(s)** : plage utile 1.782–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.618 %, prix 125.3624), p(touche) 40.1 % (en stress 99.0 %)  ✅ optimum identifie (87.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.003 | EV/share : €0.015 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 16 % | T3 4 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 18.9 | side 76.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.902% → cible +1.922% / stop −8.0%, p_fill 73%, n_eff≈76.8) : P(cible|rempli) **26%** · **EV/risk -0.045** (×p_fill ; si rempli -0.50% du capital)
  - **swing** (entrée dip −1.971% → cible +4.344% / stop −3.886%, p_fill 66%, n_eff≈78.1) : P(cible|rempli) **26%** · **EV/risk -0.233** (×p_fill ; si rempli -1.36% du capital)
  - **deep** (entrée dip −3.047% → cible +6.212% / stop −5.893%, p_fill 66%, n_eff≈73.8) : P(cible|rempli) **37%** · **EV/risk -0.117** (×p_fill ; si rempli -1.05% du capital)
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
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.59 · part idiosyncratique 0.41
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 41.0  _(momentum baissier)_
- **ADX** : 9.0  _(pas de tendance nette)_
- **MACD** : hist -0.194  _(bearish_recent)_
- **BB** : %B -0.22 · largeur 7.5%
- **ATR** : 5.17 (29.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.139  _(distribution)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 58.5  _(transition)_
- **MA** : MA20 143.37 · MA50 146.97 · MA200 154.24  _(prix < MA20)_
- **Dist MA** : MA20 -5.3% · MA50 -7.7% · MA200 -12.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (895134 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
