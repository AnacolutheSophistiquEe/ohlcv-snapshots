# CEG

**Generated** : 2026-10-09T00:30:26.182983+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $284.92  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $284.92 (+11.3% vs entrée) · entrée $255.96 · stop $241.48 · T1 $283.67 · R/R 1.91  
> ↳ ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -8.2 % ≠ (strike 275.0 − spot 284.92)/spot = -3.5 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.100 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-08 : 284.92 · ATR Wilder 14.1 (4.95 %)_
- **Swing** : plage **266.01 → 255.58** (-6.64 % a -10.3 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 263.92-280.16 (B) ; 255.71-260.27 (A). stop INDICATIF 240.15 (-6.04 % sous le bas ; sous le support 247.2-250.55 (- 0,5 ATR)).
- **Deep** : plage **255.58 → 229.26** (-10.3 % a -19.54 % sous la cloture, 1.87 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 247.2-250.55 (A) ; 240.14-246.18 (A) ; 232.79-236.2 (A) ; 224.73-229.28 (A). stop INDICATIF 209.08 (-8.8 % sous le bas ; sous le support 216.13-228.28 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.76 ATR sous le plus haut 20 s., RSI(2) 38.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 263.92-280.16 (B, -1.67 %) ; 255.71-260.27 (A, -8.65 %) ; 247.2-250.55 (A, -12.06 %) ; 240.14-246.18 (A, -13.6 %) ; 232.79-236.2 (A, -17.1 %) ; 224.73-229.28 (A, -19.53 %)
- Resistances reelles au-dessus : 291.53-294.09 (A, 2.32 %) ; 299.33-305.8 (A, 5.06 %) ; 306.91-309.97 (A, 7.72 %) ; 317.52-322.17 (A, 11.44 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.03 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (15.24 %)** : le gap seul le franchit 0.084 % des séances (1 fois sur 1184).
   - exécution **0.584 pt plus bas** dans le cas TYPIQUE (médiane), 0.584 au p90, **0.584 au pire**
   - perte réelle **15.824 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 15.24 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0005 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.853 % | p01 -4.433 % | pire -15.824 % _(sur 1184 séances)_
- **P(stop avant cible)** _(source : daily, 1185 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0095** [0.0017 ; 0.0332] _(largeur 3.1 pt, n_eff 173.1)_
   - swing : **0.3571** [0.3079 ; 0.4086] _(largeur 10.1 pt, n_eff 345.5)_
   - deep : **0.324** [0.2763 ; 0.3747] _(largeur 9.8 pt, n_eff 345.5)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.86 %** | CVaR **-7.41 %** | vol 3.19 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 5.30 % contre 2.95 % aujourd'hui, rapport 1.80)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.95 % vs -9.62 % si l'on extrapolait par √5 _(rapport 1.034 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1719** (β de hausse 1.1845, asymétrie 0.9894) vs SPY — 547 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 281.3004 sur atr_grid (0.25 ATR, 1.27 %) — p(stop avant cible) 0.8934 [0.86 ; 0.92], R/R 22.74, perte reelle 1.367 % (gap inclus), CVaR 2.898 %, EV -0.2403 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.6508 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 22.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.893, borne haute 0.923 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.114 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.1 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 1.35 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.622 %) — p(stop avant cible) 0.3771 [0.33 ; 0.43], R/R 3.982, perte reelle 7.806 % (gap inclus), EV -0.191 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 9.01 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.9 % x 31.08 % + P(rien) 61.4 % x 4.02 % ne couvrent pas P(stop) 37.7 % x 7.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 2.81 ATR (stop 16.643 %) — p(stop avant cible) 0.0574 [0.04 ; 0.09], R/R 1.861, perte reelle 16.698 % (gap inclus), EV -0.1288 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.71 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 1.0 % x 31.08 % + P(rien) 93.3 % x 0.57 % ne couvrent pas P(stop) 5.7 % x 16.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.27 %) — p(stop avant cible) 0.8934 [0.86 ; 0.92], R/R 22.74, perte reelle 1.367 % (gap inclus), EV -0.2403 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 22.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.893, borne haute 0.923 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 0.4 % x 31.08 % + P(rien) 10.3 % x 8.34 % ne couvrent pas P(stop) 89.3 % x 1.37 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.541 %) — p(stop avant cible) 0.7561 [0.71 ; 0.80], R/R 11.512, perte reelle 2.7 % (gap inclus), EV 0.0418 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 11.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.756, borne haute 0.799 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 4.70 % > budget 3.00 %
   - ⚪ atr_grid a 0.75 ATR (stop 3.811 %) — p(stop avant cible) 0.6538 [0.60 ; 0.70], R/R 7.76, perte reelle 4.005 % (gap inclus), EV -0.1376 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 7.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.654, borne haute 0.703 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.04 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.9 % x 31.08 % + P(rien) 33.7 % x 6.51 % ne couvrent pas P(stop) 65.4 % x 4.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 5.082 %) — p(stop avant cible) 0.5723 [0.52 ; 0.62], R/R 5.926, perte reelle 5.244 % (gap inclus), EV -0.3632 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.572, borne haute 0.624 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.94 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.9 % x 31.08 % + P(rien) 41.9 % x 5.62 % ne couvrent pas P(stop) 57.2 % x 5.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 6.352 %) — p(stop avant cible) 0.4692 [0.42 ; 0.52], R/R 4.743, perte reelle 6.553 % (gap inclus), EV -0.2278 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 8.24 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.9 % x 31.08 % + P(rien) 52.2 % x 4.91 % ne couvrent pas P(stop) 46.9 % x 6.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 8.893 %) — p(stop avant cible) 0.3308 [0.28 ; 0.38], R/R 3.446, perte reelle 9.018 % (gap inclus), EV -0.3423 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 9.72 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 0.9 % x 31.08 % + P(rien) 66.0 % x 3.57 % ne couvrent pas P(stop) 33.1 % x 9.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 10.163 %) — p(stop avant cible) 0.2751 [0.23 ; 0.32], R/R 3.026, perte reelle 10.27 % (gap inclus), EV -0.2988 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 10.75 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 0.9 % x 31.08 % + P(rien) 71.6 % x 3.13 % ne couvrent pas P(stop) 27.5 % x 10.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 11.434 %) — p(stop avant cible) 0.2285 [0.19 ; 0.27], R/R 2.694, perte reelle 11.537 % (gap inclus), EV -0.3207 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.91 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 1.0 % x 31.08 % + P(rien) 76.2 % x 2.64 % ne couvrent pas P(stop) 22.9 % x 11.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 12.704 %) — p(stop avant cible) 0.1922 [0.15 ; 0.24], R/R 2.428, perte reelle 12.801 % (gap inclus), EV -0.3625 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.08 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 1.0 % x 31.08 % + P(rien) 79.8 % x 2.25 % ne couvrent pas P(stop) 19.2 % x 12.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 2.81 ATR (stop 15.78 %) — p(stop avant cible) 0.0863 [0.06 ; 0.12], R/R 1.964, perte reelle 15.822 % (gap inclus), EV -0.1726 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.85 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 1.0 % x 31.08 % + P(rien) 90.4 % x 0.99 % ne couvrent pas P(stop) 8.6 % x 15.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 17.786 %) — p(stop avant cible) 0.0451 [0.03 ; 0.07], R/R 1.73, perte reelle 17.97 % (gap inclus), EV -0.1373 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.82 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 1.0 % x 31.08 % + P(rien) 94.5 % x 0.39 % ne couvrent pas P(stop) 4.5 % x 17.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 20.327 %) — p(stop avant cible) 0.0178 [0.01 ; 0.04], R/R 1.522, perte reelle 20.42 % (gap inclus), EV -0.0477 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.94 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 1.0 % x 31.08 % + P(rien) 97.3 % x 0.01 % ne couvrent pas P(stop) 1.8 % x 20.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 22.867 %) — p(stop avant cible) 0.0089 [0.00 ; 0.02], R/R 1.354, perte reelle 22.949 % (gap inclus), EV 0.0037 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.51 % > budget 3.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 25.408 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 1.223, perte reelle 25.408 % (gap inclus), EV 0.0173 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.60 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.949 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 1.11, perte reelle 27.991 % (gap inclus), EV 0.0139 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.73 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 30.49 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.019, perte reelle 30.49 % (gap inclus), EV 0.0293 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.43 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 33.031 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.941, perte reelle 33.031 % (gap inclus), EV 0.0269 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.43 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 35.571 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.874, perte reelle 35.571 % (gap inclus), EV 0.0278 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.43 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 38.112 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.815, perte reelle 38.112 % (gap inclus), EV 0.0278 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.43 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 40.653 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.765, perte reelle 40.653 % (gap inclus), EV 0.0278 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.43 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 284.92, ATR14 14.4786 (5.082 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.389 ATR = 1.977 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.254 % | 284.1961 | 91.56 % | 94.58 % | 95.55 % | 96.63 % | 97.6 % | 98.01 % |
| 0.1 ATR | 0.508 % | 283.4722 | 85.5 % | 90.47 % | 92.41 % | 94.02 % | 95.63 % | 96.8 % |
| 0.15 ATR | 0.762 % | 282.7482 | 79.11 % | 86.24 % | 88.5 % | 90.54 % | 93.77 % | 95.47 % |
| 0.2 ATR | 1.016 % | 282.0243 | 72.08 % | 80.82 % | 84.06 % | 86.74 % | 91.37 % | 94.14 % |
| 0.25 ATR | 1.27 % | 281.3004 | 65.26 % | 75.3 % | 79.28 % | 83.04 % | 88.63 % | 92.15 % |
| 0.35 ATR | 1.779 % | 279.8525 | 53.9 % | 65.87 % | 71.48 % | 76.74 % | 84.15 % | 88.62 % |
| 0.5 ATR | 2.541 % | 277.6807 | 38.74 % | 52.76 % | 59.44 % | 66.2 % | 76.94 % | 82.87 % |
| 0.75 ATR | 3.811 % | 274.0611 | 20.24 % | 36.51 % | 45.01 % | 53.26 % | 66.56 % | 75.91 % |
| 1.0 ATR | 5.082 % | 270.4414 | 11.26 % | 24.05 % | 33.19 % | 43.37 % | 57.49 % | 69.61 % |
| 1.25 ATR | 6.352 % | 266.8218 | 5.84 % | 16.14 % | 24.3 % | 35.54 % | 51.26 % | 63.54 % |
| 1.5 ATR | 7.622 % | 263.2022 | 2.81 % | 10.73 % | 17.46 % | 29.02 % | 44.26 % | 57.68 % |
| 2.0 ATR | 10.163 % | 255.9629 | 0.87 % | 4.33 % | 9.22 % | 17.83 % | 31.37 % | 46.52 % |
| 2.5 ATR | 12.704 % | 248.7236 | 0.43 % | 2.28 % | 4.77 % | 10.98 % | 21.2 % | 36.57 % |
| 3.0 ATR | 15.245 % | 241.4843 | 0.0 % | 1.08 % | 2.82 % | 6.96 % | 15.63 % | 28.73 % |
| 4.0 ATR | 20.327 % | 227.0057 | 0.0 % | 0.22 % | 0.87 % | 2.72 % | 7.1 % | 14.25 % |
| 6.0 ATR | 30.49 % | 198.0486 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.77 % | 2.76 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.06 ATR | 1.32 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.56 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.00 ATR | 1.23 ATR | 1.41 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.38 ATR | 0.83 ATR | 0.96 ATR | 1.35 ATR | 1.68 ATR | 1.90 ATR | 2.62 ATR | 3.46 ATR |
| **10 s.** | 0.55 ATR | 1.29 ATR | 1.47 ATR | 1.94 ATR | 2.31 ATR | 2.61 ATR | 3.66 ATR | 4.66 ATR |
| **20 s.** | 0.79 ATR | 1.84 ATR | 2.08 ATR | 2.73 ATR | 3.26 ATR | 3.60 ATR | 4.74 ATR | 5.61 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.438–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.541 %, prix 277.6802), p(touche) 38.74 % (en stress 81.72 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.619–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.811 %, prix 274.0617), p(touche) 36.51 % (en stress 88.17 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.75–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.811 %, prix 274.0617), p(touche) 45.01 % (en stress 97.85 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.959–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.082 %, prix 270.4404), p(touche) 43.37 % (en stress 96.74 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.474–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.622 %, prix 263.2034), p(touche) 44.26 % (en stress 98.91 %)  ✅ optimum identifie (69.6 % des re-echantillons)
- **20 seance(s)** : plage utile 2.076–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (12.704 %, prix 248.7238), p(touche) 36.57 % (en stress 95.6 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (87.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.01 | EV/share : $0.141 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 2 % | T3 0 %
- Kelly (position) : f* 0.012 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 15.4 | bear 48.2 | side 36.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 254.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→61% · +2.0%→33% · +3.0%→18% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.35% (p90 5.52%) · excursion haute méd. +1.42% / basse méd. −1.56%
- Profil de vol intra : ouverture 2.454% vs midi 0.669% vs clôture 0.758% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑1%/↓0% ; spike-down 51% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr 0.022)_ ; drift intra méd. -0.452% ; recovery-V 16%
- **σ réalisé intraday** 2.399% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 68% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 254.8755 (VA 253.3035–256.4475 ; dernier close 257.55)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 37% · rebond 57% · **stop −2.7%** sous le fill (sous le bruit) · cible +1.1% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 38% (gap-down >1% 10% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −1.58%) · haut méd +0.77% · range méd 1.41%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.27%) · haut méd +0.93% · range méd 1.85%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.61%) · haut méd +1.01% · range méd 2.12%
- Excursion ouverture 60min (n=160) : bas méd −1.14% (p90 −3.48%) · haut méd +1.13% · range méd 2.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 257.49 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 66% (103/159) · gap 26% · délai 1.3min · rebond 43% (50/103) (MFE +0.8%)
   - −1.0% : fill 30min 38% · séance 53% (87/159) · gap 10% · délai 2.5min · rebond 43% (40/87) (MFE +0.95%)
   - −1.5% : fill 30min 32% · séance 45% (72/159) · gap 6% · délai 10.5min · rebond 52% (36/72) (MFE +1.02%)
   - −2.0% : fill 30min 25% · séance 37% (59/159) · gap 3% · délai 21.2min · rebond 57% (33/59) (MFE +1.1%)
   - −3.0% : fill 30min 9% · séance 18% (32/159) · gap 2% · délai 31.6min · rebond 45% (14/32) (MFE +0.78%)
   - −4.0% : fill 30min 6% · séance 9% (18/159) · gap 1% · délai 9.3min · rebond 42% (10/18) (MFE +0.76%)
   - −5.0% : fill 30min 4% · séance 6% (11/159) · gap 0% · délai 17.8min · rebond 70% (8/11) (MFE +1.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −1.1%) → stop au-delà de −0.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.32% (p90 −1.17%) → stop au-delà de −0.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −2.23%) → stop au-delà de −1.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.08% (p90 −2.55%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 91% (40/43) · rebond 45% (21/40)
      · −2.0% : fill 80% (33/43) · rebond 57% (18/33)
      · −3.0% : fill 36% (18/43) · rebond 29% (6/18)
      · −4.0% : fill 28% (14/43) · rebond 39% (7/14)
      · −5.0% : fill 20% (10/43) · rebond 69% (7/10)
   - **flat** (27 séances) :
      · −1.0% : fill 47% (18/27) · rebond 11% (4/18)
      · −2.0% : fill 30% (11/27) · rebond 47% (6/11)
      · −3.0% : fill 13% (6/27) · rebond 24% (2/6)
      · −4.0% : fill 5% (3/27) · rebond 43% (2/3)
      · −5.0% : fill 1% (1/27) · rebond 100% (1/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 34% (29/89) · rebond 52% (15/29)
      · −2.0% : fill 16% (15/89) · rebond 61% (9/15)
      · −3.0% : fill 9% (8/89) · rebond 88% (6/8)
      · −4.0% : fill 1% (1/89) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/89) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 59% si les 15 1res min sont vertes (86 cas) · 30% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 85% si début vert vs 8% si rouge (base 44% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **85%** · continue >prix actuel 57% ; creux résiduel méd -0.88% (q20 -1.57%) → **SL/trailing à −1.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.8% / q75 +1.26% → **scale +0.8% / runner +1.26%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **8%** (continue à baisser 66%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.22%** (au-delà de la MAE q10 -2.22%), cible rebond +0.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.58% .. +2.04%] · haut q95 +3.04% · bas q05 -4.75%
   - 60min (n=160) : retour [-3.48% .. +2.54%] · haut q95 +3.33% · bas q05 -4.99%
   - 2h (n=160) : retour [-3.71% .. +2.98%] · haut q95 +3.95% · bas q05 -5.37%
   - 4h (n=160) : retour [-3.72% .. +3.29%] · haut q95 +4.1% · bas q05 -5.37%
   - 6h (n=160) : retour [-3.86% .. +3.44%] · haut q95 +4.48% · bas q05 -5.37%
   - session (n=160) : retour [-3.61% .. +3.56%] · haut q95 +4.53% · bas q05 -5.47%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 4.4% / strong 2.5%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 16% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.07% (p75 1.89% / p90 2.36%) · ~1.0 replis/séance, durée méd 144.56 min. P(nouveau plus-haut après repli) :
   - −0.5% → **69%** (reprise méd 24.3 min, n=22)
   - −1.0% → **69%** (reprise méd 179.47 min, n=11)
   - −1.5% → **48%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.36%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +3.62% (q75 +4.82% / q95 +6.2%), MFE méd +4.65% / q90 +5.84%
   - Échelle scale-out : +4.65% (33%) / +5.3% (33%) / +5.84% (34%)
- **DÉSARMER** : repli > **−2.36%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.84% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.48%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.49 · part idiosyncratique 0.51
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 65.8  _(momentum haussier)_
- **ADX** : 22.8  _(pas de tendance nette)_
- **MACD** : hist 3.805  _(bullish_recent)_
- **BB** : %B 0.82 · largeur 20.5%
- **ATR** : 14.48 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.102  _(distribution)_
- **Vol ratio** : 1.36  _(volume normal)_
- **Choppiness** : 44.5  _(transition)_
- **MA** : MA20 267.43 · MA50 273.17 · MA200 285.74  _(prix > MA20)_
- **Dist MA** : MA20 +6.5% · MA50 +4.3% · MA200 -0.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (868577 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
