# MSTR

**Generated** : 2026-10-28T01:23:03.346354+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · $141.36  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $141.36 (+2.6% vs entrée) · entrée $137.82 · stop $128.37 · T1 $151.32 · R/R 1.43  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +3.0 % ≠ (strike 144.0 − spot 141.36)/spot = +1.9 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -42 % hors [0,100] (R² max 0.79). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-27 : 141.36 · ATR Wilder 9.26 (6.55 %)_
- **Swing** : plage **130.31 → 122.21** (-7.82 % a -13.55 % sous la cloture, 0.87 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 127.8-128.51 (C) ; 123.01-126.59 (A). stop INDICATIF 113.22 (-7.35 % sous le bas ; sous le support 117.85-121.38 (- 0,5 ATR)).
- **Deep** : plage **122.21 → 101.17** (-13.55 % a -28.43 % sous la cloture, 2.27 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 117.85-121.38 (A) ; 113.2-116.4 (B) ; 104.78-105.5 (C) ; 100.05-104.6 (B). stop INDICATIF 84.58 (-16.4 % sous le bas ; sous le support 89.21-91.67 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.11 ATR sous le plus haut 20 s., RSI(2) 37.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 132.55-136.25 (A, -3.61 %) ; 127.8-128.51 (C, -9.09 %) ; 123.01-126.59 (A, -10.45 %) ; 117.85-121.38 (A, -14.13 %) ; 113.2-116.4 (B, -17.66 %) ; 104.78-105.5 (C, -25.37 %)
- Resistances reelles au-dessus : 144.2-147.37 (A, 2.01 %) ; 149.54-153.9 (A, 5.79 %) ; 154.69-156.11 (A, 9.43 %) ; 162.93-166.01 (A, 15.26 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.77 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.19 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **4.123 pt plus bas** dans le cas TYPIQUE (médiane), 17.785 au p90, **18.182 au pire**
   - perte réelle **17.215 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 9.19 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0384 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.43 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2682** [0.2064 ; 0.3376] _(largeur 13.1 pt, n_eff 173.1)_
   - swing : **0.4356** [0.384 ; 0.4882] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3839** [0.3338 ; 0.436] _(largeur 10.2 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.01 %** | CVaR **-9.07 %** | vol 4.94 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.22 % contre 5.28 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.77 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3646** (β de hausse 1.8371, asymétrie 1.2871) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 127.1839 sur atr_grid (1.5 ATR, 10.028 %) — p(stop avant cible) 0.4313 [0.38 ; 0.48], R/R 3.348, perte reelle 10.146 % (gap inclus), CVaR 11.042 %, EV 0.4859 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.656 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **11.16 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.155 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 21.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.82 ATR (stop 8.425 %) — p(stop avant cible) 0.5078 [0.46 ; 0.56], R/R 3.923, perte reelle 8.658 % (gap inclus), EV 0.5521 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.508, borne haute 0.560 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.68 ATR du spot — compartiment <1, mesure a 49.7 % de casse (IC clusterise [0.467 ; 0.529] sur 1189 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 2.64 ATR (stop 20.592 %) — p(stop avant cible) 0.1362 [0.10 ; 0.18], R/R 1.621, perte reelle 20.952 % (gap inclus), EV 0.186 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.57 % > budget 11.16 %
   - 🟢 support a 3.94 ATR (stop 29.244 %) — p(stop avant cible) 0.0445 [0.03 ; 0.07], R/R 1.143, perte reelle 29.723 % (gap inclus), EV 0.1532 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.39 % > budget 11.16 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.671 %) — p(stop avant cible) 0.9267 [0.90 ; 0.95], R/R 19.604, perte reelle 1.733 % (gap inclus), EV -0.4312 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 19.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.927, borne haute 0.951 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 1.6 % x 33.97 % + P(rien) 5.7 % x 10.89 % ne couvrent pas P(stop) 92.7 % x 1.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.343 %) — p(stop avant cible) 0.8199 [0.78 ; 0.86], R/R 9.778, perte reelle 3.474 % (gap inclus), EV -0.17 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 9.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.820, borne haute 0.858 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 3.2 % x 33.97 % + P(rien) 14.8 % x 10.71 % ne couvrent pas P(stop) 82.0 % x 3.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.82 ATR (stop 7.495 %) — p(stop avant cible) 0.5608 [0.51 ; 0.61], R/R 4.405, perte reelle 7.711 % (gap inclus), EV 0.5546 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.561, borne haute 0.612 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.5 ATR (stop 10.028 %) — p(stop avant cible) 0.4313 [0.38 ; 0.48], R/R 3.348, perte reelle 10.146 % (gap inclus), EV 0.4859 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.75 ATR (stop 11.7 %) — p(stop avant cible) 0.3594 [0.31 ; 0.41], R/R 2.88, perte reelle 11.795 % (gap inclus), EV 0.7044 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.38 % > budget 11.16 %
   - ⚪ atr_grid a 2.0 ATR (stop 13.371 %) — p(stop avant cible) 0.2938 [0.25 ; 0.34], R/R 2.506, perte reelle 13.554 % (gap inclus), EV 0.6894 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.45 % > budget 11.16 %
   - ⚪ atr_grid a 2.25 ATR (stop 15.043 %) — p(stop avant cible) 0.2479 [0.20 ; 0.30], R/R 2.216, perte reelle 15.327 % (gap inclus), EV 0.4941 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.45 % > budget 11.16 %
   - 🟢 grid_snapped a 2.64 ATR (stop 19.663 %) — p(stop avant cible) 0.1434 [0.11 ; 0.18], R/R 1.703, perte reelle 19.95 % (gap inclus), EV 0.2262 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.49 % > budget 11.16 %
   - ⚪ atr_grid a 3.5 ATR (stop 23.399 %) — p(stop avant cible) 0.0962 [0.07 ; 0.13], R/R 1.429, perte reelle 23.773 % (gap inclus), EV 0.1933 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.12 % > budget 11.16 %
   - 🟢 grid_snapped a 3.94 ATR (stop 28.314 %) — p(stop avant cible) 0.0514 [0.03 ; 0.08], R/R 1.181, perte reelle 28.763 % (gap inclus), EV 0.1436 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.78 % > budget 11.16 %
   - ⚪ atr_grid a 4.5 ATR (stop 30.085 %) — p(stop avant cible) 0.0377 [0.02 ; 0.06], R/R 1.113, perte reelle 30.524 % (gap inclus), EV 0.2064 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.49 % > budget 11.16 %
   - ⚪ atr_grid a 5.0 ATR (stop 33.428 %) — p(stop avant cible) 0.0216 [0.01 ; 0.04], R/R 1.004, perte reelle 33.847 % (gap inclus), EV 0.24 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.85 % > budget 11.16 %
   - ⚪ atr_grid a 5.5 ATR (stop 36.771 %) — p(stop avant cible) 0.0057 [0.00 ; 0.02], R/R 0.897, perte reelle 37.862 % (gap inclus), EV 0.3726 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.05 % > budget 11.16 %
   - ⚪ atr_grid a 6.0 ATR (stop 40.113 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.831, perte reelle 40.858 % (gap inclus), EV 0.4137 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.27 % > budget 11.16 %
   - ⚪ atr_grid a 6.5 ATR (stop 43.456 %) — p(stop avant cible) 0.0004 [0.00 ; 0.01], R/R 0.781, perte reelle 43.516 % (gap inclus), EV 0.4205 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.13 % > budget 11.16 %
   - ⚪ atr_grid a 7.0 ATR (stop 46.799 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.72, perte reelle 47.17 % (gap inclus), EV 0.4251 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.04 % > budget 11.16 %
   - ⚪ atr_grid a 7.5 ATR (stop 50.142 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.677, perte reelle 50.179 % (gap inclus), EV 0.4241 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.05 % > budget 11.16 %
   - ⚪ atr_grid a 8.0 ATR (stop 53.485 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.63, perte reelle 53.88 % (gap inclus), EV 0.4234 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.05 % > budget 11.16 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 141.36, ATR14 9.4507 (6.686 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.391 ATR = 2.614 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.334 % | 140.8875 | 93.96 % | 96.57 % | 97.07 % | 97.67 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.669 % | 140.4149 | 88.22 % | 92.14 % | 93.64 % | 94.84 % | 96.65 % | 97.23 % |
| 0.15 ATR | 1.003 % | 139.9424 | 81.47 % | 87.3 % | 90.01 % | 91.91 % | 94.31 % | 95.48 % |
| 0.2 ATR | 1.337 % | 139.4699 | 73.82 % | 81.85 % | 85.27 % | 88.47 % | 91.77 % | 93.43 % |
| 0.25 ATR | 1.671 % | 138.9973 | 67.88 % | 78.12 % | 82.44 % | 86.35 % | 89.33 % | 91.68 % |
| 0.35 ATR | 2.34 % | 138.0523 | 54.58 % | 68.75 % | 75.48 % | 81.09 % | 85.87 % | 89.01 % |
| 0.5 ATR | 3.343 % | 136.6346 | 37.66 % | 55.14 % | 63.47 % | 71.49 % | 78.66 % | 84.09 % |
| 0.75 ATR | 5.014 % | 134.272 | 19.34 % | 37.7 % | 47.23 % | 58.24 % | 68.29 % | 76.18 % |
| 1.0 ATR | 6.686 % | 131.9093 | 9.47 % | 25.3 % | 35.02 % | 46.31 % | 59.04 % | 68.79 % |
| 1.25 ATR | 8.357 % | 129.5466 | 4.03 % | 14.52 % | 24.72 % | 35.49 % | 50.0 % | 61.4 % |
| 1.5 ATR | 10.028 % | 127.1839 | 2.01 % | 8.47 % | 17.05 % | 28.61 % | 42.89 % | 55.65 % |
| 2.0 ATR | 13.371 % | 122.4586 | 0.1 % | 2.92 % | 7.16 % | 15.77 % | 30.59 % | 45.69 % |
| 2.5 ATR | 16.714 % | 117.7332 | 0.1 % | 0.71 % | 2.12 % | 8.19 % | 20.63 % | 36.24 % |
| 3.0 ATR | 20.057 % | 113.0079 | 0.1 % | 0.3 % | 0.71 % | 4.04 % | 13.82 % | 26.59 % |
| 4.0 ATR | 26.742 % | 103.5571 | 0.0 % | 0.0 % | 0.2 % | 0.61 % | 5.39 % | 16.63 % |
| 6.0 ATR | 40.113 % | 84.6557 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.41 % | 3.9 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.43 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.01 ATR | 1.12 ATR | 1.44 ATR | 1.81 ATR |
| **3 s.** | 0.36 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.24 ATR | 1.40 ATR | 1.86 ATR | 2.21 ATR |
| **5 s.** | 0.45 ATR | 0.92 ATR | 1.03 ATR | 1.34 ATR | 1.64 ATR | 1.83 ATR | 2.38 ATR | 2.88 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.43 ATR | 1.90 ATR | 2.28 ATR | 2.55 ATR | 3.45 ATR | 4.16 ATR |
| **20 s.** | 0.79 ATR | 1.78 ATR | 2.04 ATR | 2.67 ATR | 3.16 ATR | 3.66 ATR | 5.04 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.435–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.343 %, prix 136.6343), p(touche) 37.66 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.014 %, prix 134.2722), p(touche) 37.7 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.796–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.686 %, prix 131.9087), p(touche) 35.02 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.03–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.357 %, prix 129.5465), p(touche) 35.49 % (en stress 94.95 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.426–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.028 %, prix 127.1844), p(touche) 42.89 % (en stress 100.0 %)  ✅ optimum identifie (60.6 % des re-echantillons)
- **20 seance(s)** : plage utile 2.037–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.714 %, prix 117.7331), p(touche) 36.24 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : $-0.122 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 11 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 52.4 | bear 22.4 | side 25.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 254.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.14% → cible +3.381% / stop −3.5%, p_fill 75%, n_eff≈81.5) : P(cible|rempli) **31%** · **EV/risk -0.003** (×p_fill ; si rempli -0.01% du capital)
  - **swing** (entrée dip −2.504% → cible +9.796% / stop −6.857%, p_fill 68%, n_eff≈79.5) : P(cible|rempli) **31%** · **EV/risk +0.012** (×p_fill ; si rempli +0.12% du capital)
  - **deep** (entrée dip −3.872% → cible +11.356% / stop −10.432%, p_fill 64%, n_eff≈72.0) : P(cible|rempli) **42%** · **EV/risk -0.012** (×p_fill ; si rempli -0.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→58% · +3.0%→40% · +5.0%→19% · +8.0%→10%
- Range intraday médian 5.35% (p90 9.82%) · excursion haute méd. +2.51% / basse méd. −2.26%
- Profil de vol intra : ouverture 3.268% vs midi 1.123% vs clôture 1.265% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 17% · trend ↑2%/↓0% ; spike-down 69% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. 0.468% ; recovery-V 35%
- **σ réalisé intraday** 3.406% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 59% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 148.5395 (VA 146.6095–150.0835 ; dernier close 146.04)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 73% · **stop −3.89%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 38% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.78% (p90 −1.81%) · haut méd +0.88% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.68%) · haut méd +1.24% · range méd 2.55%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.06%) · haut méd +1.47% · range méd 2.95%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −3.47%) · haut méd +1.83% · range méd 3.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 146.01 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 76% (121/159) · gap 46% · délai 0.0min · rebond 44% (57/121) (MFE +0.7%)
   - −1.0% : fill 30min 55% · séance 67% (112/159) · gap 38% · délai 0.0min · rebond 48% (59/112) (MFE +0.91%)
   - −1.5% : fill 30min 45% · séance 61% (103/159) · gap 31% · délai 0.0min · rebond 53% (57/103) (MFE +1.16%)
   - −2.0% : fill 30min 38% · séance 54% (91/159) · gap 25% · délai 0.0min · rebond 60% (54/91) (MFE +1.25%)
   - −3.0% : fill 30min 28% · séance 41% (71/159) · gap 17% · délai 0.7min · rebond 52% (38/71) (MFE +1.5%)
   - −4.0% : fill 30min 21% · séance 32% (56/159) · gap 6% · délai 3.2min · rebond 72% (37/56) (MFE +1.65%)
   - −5.0% : fill 30min 17% · séance 25% (41/159) · gap 4% · délai 12.9min · rebond 73% (29/41) (MFE +2.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.65% (p90 −2.12%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.8% (p90 −2.19%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −2.14%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=888 jambes) : jambe baissière méd −1.12% (p90 −2.6%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 97% (74/75) · rebond 49% (34/74)
      · −2.0% : fill 86% (66/75) · rebond 58% (37/66)
      · −3.0% : fill 71% (57/75) · rebond 49% (30/57)
      · −4.0% : fill 60% (48/75) · rebond 72% (32/48)
      · −5.0% : fill 49% (37/75) · rebond 74% (27/37)
   - **flat** (18 séances) :
      · −1.0% : fill 74% (14/18) · rebond 55% (10/14)
      · −2.0% : fill 46% (9/18) · rebond 54% (5/9)
      · −3.0% : fill 38% (7/18) · rebond 71% (4/7)
      · −4.0% : fill 17% (4/18) · rebond 80% (3/4)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 30% (24/66) · rebond 41% (15/24)
      · −2.0% : fill 19% (16/66) · rebond 70% (12/16)
      · −3.0% : fill 7% (7/66) · rebond 67% (4/7)
      · −4.0% : fill 3% (4/66) · rebond 58% (2/4)
      · −5.0% : fill 2% (2/66) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 56% si les 15 1res min sont vertes (88 cas) · 32% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 71% si début vert vs 7% si rouge (base 46% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=90) : tient le vert **71%** · continue >prix actuel 43% ; creux résiduel méd -1.55% (q20 -2.88%) → **SL/trailing à −2.88%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +2.85% → **scale +1.62% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **7%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.18%** (au-delà de la MAE q10 -5.18%), cible rebond +1.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.82% .. +3.69%] · haut q95 +3.94% · bas q05 -3.62%
   - 60min (n=160) : retour [-3.45% .. +5.63%] · haut q95 +6.12% · bas q05 -4.56%
   - 2h (n=160) : retour [-4.42% .. +7.83%] · haut q95 +8.96% · bas q05 -5.49%
   - 4h (n=160) : retour [-5.2% .. +8.2%] · haut q95 +10.02% · bas q05 -6.02%
   - 6h (n=160) : retour [-5.31% .. +8.86%] · haut q95 +10.13% · bas q05 -6.26%
   - session (n=160) : retour [-5.14% .. +8.51%] · haut q95 +10.13% · bas q05 -6.52%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0.6% / strong 6.9%) · base = 12 séances trend-up (n_eff 8.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **47%**. Lecture précoce 30 min : signature présente → 17% vs absente 6% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.9% (p75 1.29% / p90 2.02%) · ~4.0 replis/séance, durée méd 30.47 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 20.0 min, n=46)
   - −1.0% → **74%** (reprise méd 17.06 min, n=20)
   - −1.5% → **58%** (reprise méd 13.97 min, n=11)
   - −2.0% → **46%** (reprise méd 31.23 min, n=8)
   - −3.0% → **38%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.02%** (p90, défaut prudent ; serré/agressif −1.29%) ; extension open→close méd +8.69% (q75 +10.68% / q95 +13.17%), MFE méd +10.02% / q90 +13.15%
   - Échelle scale-out : +10.02% (33%) / +12.77% (33%) / +13.15% (34%)
- **DÉSARMER** : repli > **−2.02%** depuis le plus-haut = décay → P(retournement) **81%** (préavis méd 157.2 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.15% : P(retournement après) 0% (mèche méd 0.05%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.81%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.88 · part idiosyncratique 0.12
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.7  _(momentum baissier)_
- **ADX** : 19.9  _(pas de tendance nette)_
- **MACD** : hist -1.938  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 22.7%
- **ATR** : 9.45 (42.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.128  _(distribution)_
- **Vol ratio** : 0.46  _(volume atone)_
- **Choppiness** : 63.4  _(marche en range (choppy))_
- **MA** : MA20 150.16 · MA50 141.51 · MA200 135.04  _(prix < MA20)_
- **Dist MA** : MA20 -5.9% · MA50 -0.1% · MA200 +4.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (790852 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
