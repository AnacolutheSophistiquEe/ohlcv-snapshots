# MSTR

**Generated** : 2026-10-26T01:21:13.995589+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $146.01  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $146.01 (+3.8% vs entrée) · entrée $140.64 · stop $130.80 · T1 $151.28 · R/R 1.08  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 146.01 · ATR Wilder 9.79 (6.7 %)_
- **Swing** : plage **134.41 → 125.83** (-7.95 % a -13.82 % sous la cloture, 0.88 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 133.6-136.25 (A) ; 128.51-133.38 (B) ; 123.33-127.8 (A). stop INDICATIF 113.51 (-9.8 % sous le bas ; sous le support 118.4-123.01 (- 0,5 ATR)).
- **Deep** : plage **125.83 → 103.51** (-13.82 % a -29.1 % sous la cloture, 2.28 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 123.33-127.8 (A) ; 118.4-123.01 (A) ; 113.2-117.85 (B) ; 100.05-104.78 (B). stop INDICATIF 84.32 (-18.55 % sous le bas ; sous le support 89.21-91.67 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.47 ATR sous le plus haut 20 s., RSI(2) 46.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 133.6-136.25 (A, -6.68 %) ; 128.51-133.38 (B, -8.65 %) ; 123.33-127.8 (A, -12.47 %) ; 118.4-123.01 (A, -15.75 %) ; 113.2-117.85 (B, -19.28 %) ; 100.05-104.78 (B, -28.24 %)
- Resistances reelles au-dessus : 150.77-155.61 (A, 3.26 %) ; 156.01-156.11 (B, 6.85 %) ; 162.93-166.01 (A, 11.59 %) ; 168.96-173.47 (A, 15.72 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.77 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.42 %)** : le gap seul le franchit 0.478 % des séances (6 fois sur 1254).
   - exécution **2.893 pt plus bas** dans le cas TYPIQUE (médiane), 16.555 au p90, **16.952 au pire**
   - perte réelle **17.215 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 10.42 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0325 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.428 % | p01 -7.774 % | pire -27.372 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4161** [0.3446 ; 0.4904] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4093** [0.3584 ; 0.4617] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3884** [0.3381 ; 0.4405] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.4 pt), deep (25.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.01 %** | CVaR **-9.07 %** | vol 4.94 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.24 % contre 5.27 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.76 % si l'on extrapolait par √5 _(rapport 0.957 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3625** (β de hausse 1.8246, asymétrie 1.2948) vs IWM — 606 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 133.2967 sur grid_snapped (0.99 ATR, 8.707 %) — p(stop avant cible) 0.4927 [0.44 ; 0.55], R/R 3.334, perte reelle 8.885 % (gap inclus), CVaR 10.309 %, EV 0.8134 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3093 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.23 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.183 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 20.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.99 ATR (stop 10.231 %) — p(stop avant cible) 0.4073 [0.36 ; 0.46], R/R 2.856, perte reelle 10.372 % (gap inclus), EV 0.8611 % — **REFUSE**
      - refuse : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.99 ATR du spot — compartiment <1, mesure a 47.8 % de casse (IC clusterise [0.449 ; 0.507] sur 1237 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ swing_based a 1.46 ATR (stop 13.394 %) — p(stop avant cible) 0.295 [0.25 ; 0.34], R/R 2.182, perte reelle 13.576 % (gap inclus), EV 0.9509 % — **REFUSE**
      - refuse : cible atteinte seulement 10.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.47 % > budget 12.23 %
   - 🟢 support a 3.01 ATR (stop 23.826 %) — p(stop avant cible) 0.0932 [0.07 ; 0.13], R/R 1.224, perte reelle 24.202 % (gap inclus), EV 0.4087 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.53 % > budget 12.23 %
   - 🟢 support a 4.25 ATR (stop 32.202 %) — p(stop avant cible) 0.0258 [0.01 ; 0.05], R/R 0.907, perte reelle 32.674 % (gap inclus), EV 0.4532 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.82 % > budget 12.23 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.686 %) — p(stop avant cible) 0.9247 [0.89 ; 0.95], R/R 17.021, perte reelle 1.74 % (gap inclus), EV -0.3957 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 17.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.925, borne haute 0.949 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 2.4 % x 29.62 % + P(rien) 5.1 % x 9.84 % ne couvrent pas P(stop) 92.5 % x 1.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.371 %) — p(stop avant cible) 0.8171 [0.77 ; 0.86], R/R 8.459, perte reelle 3.502 % (gap inclus), EV -0.1467 % — **REFUSE**
      - refuse : cible atteinte seulement 4.8 % du temps (< 15 %) meme a 10 seances : le R/R de 8.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.817, borne haute 0.855 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 4.8 % x 29.62 % + P(rien) 13.5 % x 9.66 % ne couvrent pas P(stop) 81.7 % x 3.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.99 ATR (stop 8.707 %) — p(stop avant cible) 0.4927 [0.44 ; 0.55], R/R 3.334, perte reelle 8.885 % (gap inclus), EV 0.8134 % — **REFUSE**
      - refuse : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ grid_snapped a 1.46 ATR (stop 11.871 %) — p(stop avant cible) 0.3471 [0.30 ; 0.40], R/R 2.478, perte reelle 11.954 % (gap inclus), EV 0.98 % — **REFUSE**
      - refuse : cible atteinte seulement 10.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.45 % > budget 12.23 %
   - ⚪ atr_grid a 2.25 ATR (stop 15.17 %) — p(stop avant cible) 0.2499 [0.21 ; 0.30], R/R 1.918, perte reelle 15.441 % (gap inclus), EV 0.6927 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.52 % > budget 12.23 %
   - ⚪ atr_grid a 2.5 ATR (stop 16.855 %) — p(stop avant cible) 0.2024 [0.16 ; 0.25], R/R 1.734, perte reelle 17.081 % (gap inclus), EV 0.5973 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.77 % > budget 12.23 %
   - ⚪ atr_grid a 2.75 ATR (stop 18.541 %) — p(stop avant cible) 0.1799 [0.14 ; 0.22], R/R 1.576, perte reelle 18.793 % (gap inclus), EV 0.432 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.45 % > budget 12.23 %
   - 🟢 grid_snapped a 3.01 ATR (stop 22.302 %) — p(stop avant cible) 0.1157 [0.09 ; 0.15], R/R 1.302, perte reelle 22.747 % (gap inclus), EV 0.3729 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.33 % > budget 12.23 %
   - ⚪ atr_grid a 4.0 ATR (stop 26.969 %) — p(stop avant cible) 0.0573 [0.04 ; 0.09], R/R 1.079, perte reelle 27.454 % (gap inclus), EV 0.415 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.53 % > budget 12.23 %
   - 🟢 grid_snapped a 4.25 ATR (stop 30.678 %) — p(stop avant cible) 0.0311 [0.02 ; 0.05], R/R 0.951, perte reelle 31.151 % (gap inclus), EV 0.4789 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.22 % > budget 12.23 %
   - ⚪ atr_grid a 5.0 ATR (stop 33.711 %) — p(stop avant cible) 0.0182 [0.01 ; 0.04], R/R 0.867, perte reelle 34.184 % (gap inclus), EV 0.4888 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.33 % > budget 12.23 %
   - ⚪ atr_grid a 5.5 ATR (stop 37.082 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.78, perte reelle 37.968 % (gap inclus), EV 0.596 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.05 % > budget 12.23 %
   - ⚪ atr_grid a 6.0 ATR (stop 40.453 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.722, perte reelle 41.017 % (gap inclus), EV 0.6355 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.33 % > budget 12.23 %
   - ⚪ atr_grid a 6.5 ATR (stop 43.824 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.674, perte reelle 43.917 % (gap inclus), EV 0.6483 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.10 % > budget 12.23 %
   - ⚪ atr_grid a 7.0 ATR (stop 47.195 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.617, perte reelle 47.981 % (gap inclus), EV 0.6461 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.10 % > budget 12.23 %
   - ⚪ atr_grid a 7.5 ATR (stop 50.566 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.586, perte reelle 50.566 % (gap inclus), EV 0.6452 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.10 % > budget 12.23 %
   - ⚪ atr_grid a 8.0 ATR (stop 53.938 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.537, perte reelle 55.147 % (gap inclus), EV 0.6448 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.10 % > budget 12.23 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 146.01, ATR14 9.8443 (6.742 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.392 ATR = 2.643 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.337 % | 145.5178 | 94.06 % | 96.58 % | 97.08 % | 97.78 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.674 % | 145.0256 | 88.33 % | 92.15 % | 93.65 % | 94.95 % | 96.65 % | 97.23 % |
| 0.15 ATR | 1.011 % | 144.5334 | 81.59 % | 87.31 % | 90.02 % | 92.02 % | 94.31 % | 95.49 % |
| 0.2 ATR | 1.348 % | 144.0411 | 73.94 % | 81.97 % | 85.28 % | 88.59 % | 91.78 % | 93.44 % |
| 0.25 ATR | 1.686 % | 143.5489 | 68.01 % | 78.25 % | 82.46 % | 86.46 % | 89.34 % | 91.69 % |
| 0.35 ATR | 2.36 % | 142.5645 | 54.73 % | 68.88 % | 75.6 % | 81.21 % | 85.89 % | 89.03 % |
| 0.5 ATR | 3.371 % | 141.0879 | 37.93 % | 55.29 % | 63.61 % | 71.62 % | 78.68 % | 84.1 % |
| 0.75 ATR | 5.057 % | 138.6268 | 19.42 % | 37.87 % | 47.38 % | 58.48 % | 68.32 % | 76.21 % |
| 1.0 ATR | 6.742 % | 136.1657 | 9.56 % | 25.48 % | 35.28 % | 46.57 % | 59.09 % | 68.82 % |
| 1.25 ATR | 8.428 % | 133.7046 | 4.12 % | 14.7 % | 25.0 % | 35.76 % | 50.05 % | 61.44 % |
| 1.5 ATR | 10.113 % | 131.2436 | 2.11 % | 8.66 % | 17.34 % | 28.89 % | 42.94 % | 55.69 % |
| 2.0 ATR | 13.484 % | 126.3214 | 0.2 % | 3.12 % | 7.46 % | 16.06 % | 30.66 % | 45.74 % |
| 2.5 ATR | 16.855 % | 121.3993 | 0.1 % | 0.91 % | 2.42 % | 8.48 % | 20.91 % | 36.31 % |
| 3.0 ATR | 20.227 % | 116.4771 | 0.1 % | 0.5 % | 1.01 % | 4.34 % | 14.11 % | 26.77 % |
| 4.0 ATR | 26.969 % | 106.6329 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 5.58 % | 16.82 % |
| 6.0 ATR | 40.453 % | 86.9443 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.41 % | 3.9 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.58 ATR | 0.65 ATR | 0.85 ATR | 1.01 ATR | 1.13 ATR | 1.45 ATR | 1.83 ATR |
| **3 s.** | 0.36 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.25 ATR | 1.41 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.45 ATR | 0.93 ATR | 1.04 ATR | 1.35 ATR | 1.65 ATR | 1.85 ATR | 2.40 ATR | 2.92 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.43 ATR | 1.91 ATR | 2.29 ATR | 2.57 ATR | 3.48 ATR | 4.22 ATR |
| **20 s.** | 0.79 ATR | 1.79 ATR | 2.04 ATR | 2.67 ATR | 3.18 ATR | 3.68 ATR | 5.06 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.437–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.371 %, prix 141.088), p(touche) 37.93 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.648–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.057 %, prix 138.6263), p(touche) 37.87 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.799–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.742 %, prix 136.166), p(touche) 35.28 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.036–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.428 %, prix 133.7043), p(touche) 35.76 % (en stress 94.95 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.428–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.113 %, prix 131.244), p(touche) 42.94 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.039–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.855 %, prix 121.4), p(touche) 36.31 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.043 | EV/share : $-0.425 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 15 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 52.1 | bear 26.6 | side 21.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 261.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.669% → cible +5.372% / stop −2.686%, p_fill 64%, n_eff≈70.2) : P(cible|rempli) **16%** · **EV/risk +0.054** (×p_fill ; si rempli +0.23% du capital)
  - **swing** (entrée dip −3.678% → cible +7.566% / stop −7.0%, p_fill 48%, n_eff≈56.3) : P(cible|rempli) **44%** · **EV/risk +0.030** (×p_fill ; si rempli +0.44% du capital)
  - **deep** (entrée dip −5.687% → cible +20.967% / stop −10.723%, p_fill 50%, n_eff≈56.6) : P(cible|rempli) **13%** · **EV/risk -0.024** (×p_fill ; si rempli -0.51% du capital)
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

**Factor** : R² 0.87 · part idiosyncratique 0.13
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.9  _(momentum baissier)_
- **ADX** : 22.6  _(pas de tendance nette)_
- **MACD** : hist -1.872  _(pas de croisement recent)_
- **BB** : %B 0.32 · largeur 21.1%
- **ATR** : 9.84 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.163  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 51.8  _(transition)_
- **MA** : MA20 151.69 · MA50 139.7 · MA200 135.26  _(prix < MA20)_
- **Dist MA** : MA20 -3.7% · MA50 +4.5% · MA200 +8.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (791287 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
