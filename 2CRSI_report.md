# AL2SI

**Generated** : 2026-11-25T01:12:34.785745+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 13.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €14.48  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)  
> ↳ spot €14.48 (+2.3% vs entrée) · entrée €14.16 · stop €13.03 · T1 €16.50 · R/R 2.07  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-24 : 14.48 · ATR Wilder 2.03 (13.99 %)_
- **Swing** : plage **12.17 → 10.67** (-15.96 % a -26.34 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 11.76-12.4 (A) ; 10.52-11.36 (A). stop INDICATIF 8.29 (-22.3 % sous le bas ; sous le support 9.3-10.1 (- 0,5 ATR)).
- **Deep** : plage **10.67 → 6.74** (-26.34 % a -53.46 % sous la cloture, 1.94 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 10.52-11.36 (A) ; 9.3-10.1 (A) ; 7.85-8.83 (A) ; 6.35-7.32 (A). stop INDICATIF 3.05 (-54.7 % sous le bas ; sous le support 4.07-6.09 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.96 ATR sous le plus haut 20 s., RSI(2) 27.7. Limite **13.47** (seance suivante), stop catastrophe 5.37, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 13.0-13.24 (B, -8.56 %) ; 11.76-12.4 (A, -14.36 %) ; 10.52-11.36 (A, -21.55 %) ; 9.3-10.1 (A, -30.25 %) ; 7.85-8.83 (A, -39.02 %) ; 6.35-7.32 (A, -49.45 %)
- Resistances reelles au-dessus : 16.1-16.65 (A, 11.19 %) ; 19.75-20.1 (A, 36.4 %) ; 20.8-21.05 (B, 43.65 %) ; 22.6-23.55 (A, 56.08 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.75 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.53 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **10.739 pt plus bas** dans le cas TYPIQUE (médiane), 30.262 au p90, **37.937 au pire**
   - perte réelle **31.149 %** en moyenne _(tirée par la queue)_, jusqu'à **53.467 %** — au lieu des 15.53 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0732 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.519 % | p01 -7.775 % | pire -53.467 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0826** [0.0484 ; 0.1306] _(largeur 8.2 pt, n_eff 173.1)_
   - swing : **0.2845** [0.2389 ; 0.3337] _(largeur 9.5 pt, n_eff 345.8)_
   - deep : **0.2409** [0.1981 ; 0.288] _(largeur 9.0 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (26.3 pt), deep (26.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-15.03 %** | vol 7.07 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 5.05 % contre 8.40 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -15.78 % vs -14.48 % si l'on extrapolait par √5 _(rapport 1.089 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2177** (β de hausse 0.9825, asymétrie 1.2394) vs FCHI — 622 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.022× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 14.0939 sur atr_grid (0.25 ATR, 2.666 %) — p(stop avant cible) 0.8467 [0.81 ; 0.88], R/R 15.056, perte reelle 3.419 % (gap inclus), CVaR 15.411 %, EV 0.556 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.6893 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 15.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.847, borne haute 0.882 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 15.41 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.83 ATR (stop 13.405 %) — p(stop avant cible) 0.3269 [0.28 ; 0.38], R/R 2.818, perte reelle 18.272 % (gap inclus), EV 1.5772 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.70 % > budget 12.00 %
      - ⚠ support DETECTE a 0.83 ATR du spot — compartiment <1, mesure a 49.2 % de casse (IC clusterise [0.458 ; 0.523] sur 1200 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 1.55 ATR (stop 21.14 %) — p(stop avant cible) 0.1773 [0.14 ; 0.22], R/R 1.844, perte reelle 27.921 % (gap inclus), EV 1.5449 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.54 % > budget 12.00 %
   - 🟢 support a 2.09 ATR (stop 26.802 %) — p(stop avant cible) 0.126 [0.09 ; 0.16], R/R 1.588, perte reelle 32.412 % (gap inclus), EV 1.7356 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.54 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 2.666 %) — p(stop avant cible) 0.8467 [0.81 ; 0.88], R/R 15.056, perte reelle 3.419 % (gap inclus), EV 0.556 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 15.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.847, borne haute 0.882 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 15.41 % > budget 12.00 %
   - ⚪ atr_grid a 0.5 ATR (stop 5.332 %) — p(stop avant cible) 0.7299 [0.68 ; 0.77], R/R 7.197, perte reelle 7.153 % (gap inclus), EV -0.1252 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.730, borne haute 0.775 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 29.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 4.0 % x 51.48 % + P(rien) 23.0 % x 13.23 % ne couvrent pas P(stop) 73.0 % x 7.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.83 ATR (stop 12.039 %) — p(stop avant cible) 0.3596 [0.31 ; 0.41], R/R 3.175, perte reelle 16.216 % (gap inclus), EV 1.7363 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 33.47 % > budget 12.00 %
   - 🟢 grid_snapped a 1.55 ATR (stop 19.774 %) — p(stop avant cible) 0.1993 [0.16 ; 0.24], R/R 1.94, perte reelle 26.538 % (gap inclus), EV 1.443 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.54 % > budget 12.00 %
   - 🟢 grid_snapped a 2.09 ATR (stop 25.437 %) — p(stop avant cible) 0.1361 [0.10 ; 0.18], R/R 1.642, perte reelle 31.353 % (gap inclus), EV 1.7337 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.54 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 29.329 %) — p(stop avant cible) 0.1186 [0.09 ; 0.16], R/R 1.339, perte reelle 38.455 % (gap inclus), EV 1.1239 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.60 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 31.995 %) — p(stop avant cible) 0.1124 [0.08 ; 0.15], R/R 1.152, perte reelle 44.701 % (gap inclus), EV 0.5438 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.18 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 37.327 %) — p(stop avant cible) 0.0936 [0.07 ; 0.13], R/R 0.992, perte reelle 51.906 % (gap inclus), EV 0.5441 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 60.70 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 42.66 %) — p(stop avant cible) 0.0765 [0.05 ; 0.11], R/R 0.929, perte reelle 55.405 % (gap inclus), EV 0.8667 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 60.70 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 47.992 %) — p(stop avant cible) 0.0734 [0.05 ; 0.10], R/R 0.9, perte reelle 57.191 % (gap inclus), EV 0.7754 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 61.42 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 53.325 %) — p(stop avant cible) 0.0649 [0.04 ; 0.09], R/R 0.827, perte reelle 62.251 % (gap inclus), EV 0.7287 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 63.05 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 58.657 %) — p(stop avant cible) 0.0649 [0.04 ; 0.09], R/R 0.819, perte reelle 62.826 % (gap inclus), EV 0.6914 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 63.29 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 63.99 %) — p(stop avant cible) 0.0326 [0.02 ; 0.06], R/R 0.801, perte reelle 64.292 % (gap inclus), EV 1.4084 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.74 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 69.322 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.743, perte reelle 69.322 % (gap inclus), EV 2.094 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 74.655 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.69, perte reelle 74.655 % (gap inclus), EV 2.094 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 79.987 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.644, perte reelle 79.987 % (gap inclus), EV 2.094 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.71 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 85.32 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.603, perte reelle 85.32 % (gap inclus), EV 2.094 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.71 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 14.48, ATR14 1.5443 (10.665 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.397 ATR = 4.234 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.533 % | 14.4028 | 87.55 % | 90.97 % | 93.12 % | 94.69 % | 95.75 % | 97.2 % |
| 0.1 ATR | 1.066 % | 14.3256 | 82.75 % | 87.24 % | 90.28 % | 92.22 % | 94.16 % | 96.3 % |
| 0.15 ATR | 1.6 % | 14.2484 | 78.43 % | 83.61 % | 87.33 % | 89.07 % | 92.28 % | 95.2 % |
| 0.2 ATR | 2.133 % | 14.1711 | 72.45 % | 79.29 % | 83.4 % | 85.93 % | 89.91 % | 93.01 % |
| 0.25 ATR | 2.666 % | 14.0939 | 66.27 % | 74.68 % | 79.37 % | 82.78 % | 87.73 % | 91.41 % |
| 0.35 ATR | 3.733 % | 13.9395 | 54.41 % | 65.26 % | 71.02 % | 75.89 % | 82.89 % | 87.91 % |
| 0.5 ATR | 5.332 % | 13.7079 | 40.29 % | 53.48 % | 61.98 % | 69.09 % | 78.44 % | 85.51 % |
| 0.75 ATR | 7.999 % | 13.3218 | 22.45 % | 37.59 % | 47.15 % | 55.81 % | 67.75 % | 77.12 % |
| 1.0 ATR | 10.665 % | 12.9357 | 12.55 % | 24.73 % | 33.6 % | 44.19 % | 57.47 % | 68.93 % |
| 1.25 ATR | 13.331 % | 12.5496 | 7.35 % | 17.76 % | 24.75 % | 36.52 % | 50.64 % | 62.64 % |
| 1.5 ATR | 15.997 % | 12.1636 | 3.63 % | 11.48 % | 17.58 % | 28.94 % | 43.42 % | 56.34 % |
| 2.0 ATR | 21.33 % | 11.3914 | 0.88 % | 5.4 % | 9.92 % | 17.13 % | 31.85 % | 45.05 % |
| 2.5 ATR | 26.662 % | 10.6193 | 0.1 % | 2.36 % | 4.91 % | 10.14 % | 21.76 % | 35.06 % |
| 3.0 ATR | 31.995 % | 9.8471 | 0.1 % | 1.18 % | 2.65 % | 6.99 % | 15.43 % | 27.17 % |
| 4.0 ATR | 42.66 % | 8.3029 | 0.0 % | 0.79 % | 1.47 % | 3.05 % | 8.8 % | 18.08 % |
| 6.0 ATR | 63.99 % | 5.2143 | 0.0 % | 0.0 % | 0.29 % | 0.79 % | 2.97 % | 9.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.60 ATR | 0.71 ATR | 0.81 ATR | 1.12 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.63 ATR | 0.84 ATR | 0.99 ATR | 1.17 ATR | 1.62 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.24 ATR | 1.42 ATR | 2.00 ATR | 2.49 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 0.98 ATR | 1.37 ATR | 1.67 ATR | 1.88 ATR | 2.52 ATR | 3.50 ATR |
| **10 s.** | 0.58 ATR | 1.27 ATR | 1.45 ATR | 1.95 ATR | 2.34 ATR | 2.64 ATR | 3.82 ATR | 5.30 ATR |
| **20 s.** | 0.81 ATR | 1.78 ATR | 2.00 ATR | 2.63 ATR | 3.24 ATR | 3.79 ATR | 5.90 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.45–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (5.332 %, prix 13.7079), p(touche) 40.29 % (en stress 82.35 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (82.6 % des re-echantillons)
- **2 seance(s)** : plage utile VIDE (borne basse 0.633 ATR au-dessus du haut de la grille, 0.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.79 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.983–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (10.665 %, prix 12.9357), p(touche) 44.19 % (en stress 96.08 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.445–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (15.997 %, prix 12.1636), p(touche) 43.42 % (en stress 96.08 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.003 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 16.6 | bear 68.7 | side 14.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.207% → cible +16.494% / stop −8.0%, p_fill 64%, n_eff≈67.8) : P(cible|rempli) **2%** · **EV/risk -0.042** (×p_fill ; si rempli -0.52% du capital)
  - **swing** (entrée dip −4.865% → cible +19.742% / stop −11.21%, p_fill 44%, n_eff≈51.9) : P(cible|rempli) **10%** · **EV/risk -0.075** (×p_fill ; si rempli -1.89% du capital)
  - **deep** (entrée dip −7.513% → cible +23.175% / stop −17.297%, p_fill 45%, n_eff≈51.3) : P(cible|rempli) **12%** · **EV/risk -0.079** (×p_fill ; si rempli -3.02% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→74% · +2.0%→66% · +3.0%→50% · +5.0%→34% · +8.0%→17%
- Range intraday médian 6.93% (p90 16.1%) · excursion haute méd. +2.93% / basse méd. −3.31%
- Profil de vol intra : ouverture 4.806% vs midi 1.518% vs clôture 1.661% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑1%/↓0% ; spike-down 74% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. 0.151% ; recovery-V 25%
- **σ réalisé intraday** 4.419% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 71% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 26.6325 (VA 26.2575–26.7325 ; dernier close 26.53)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 91% · **stop −3.21%** sous le fill (sous le bruit) · cible +2.26% · R/R 0.7 (high win-rate)
- Gaps overnight (n=158) : méd. -0.0% · baisse 51% (gap-down >1% 16% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −3.16%) · haut méd +0.82% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.92%) · haut méd +1.23% · range méd 2.91%
- Excursion ouverture 30min (n=160) : bas méd −1.42% (p90 −4.38%) · haut méd +1.57% · range méd 3.4%
- Excursion ouverture 60min (n=160) : bas méd −1.64% (p90 −5.26%) · haut méd +2.01% · range méd 4.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.62 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 81% (125/158) · gap 30% · délai 0.1min · rebond 61% (81/125) (MFE +1.75%)
   - −1.0% : fill 30min 56% · séance 76% (120/158) · gap 16% · délai 0.4min · rebond 61% (79/120) (MFE +1.71%)
   - −1.5% : fill 30min 50% · séance 72% (107/158) · gap 8% · délai 2.4min · rebond 63% (68/107) (MFE +1.74%)
   - −2.0% : fill 30min 42% · séance 66% (98/158) · gap 6% · délai 7.8min · rebond 59% (60/98) (MFE +1.61%)
   - −3.0% : fill 30min 26% · séance 51% (79/158) · gap 3% · délai 31.2min · rebond 59% (53/79) (MFE +1.59%)
   - −4.0% : fill 30min 16% · séance 39% (65/158) · gap 2% · délai 55.8min · rebond 71% (49/65) (MFE +1.67%)
   - −5.0% : fill 30min 11% · séance 28% (50/158) · gap 2% · délai 48.7min · rebond 91% (46/50) (MFE +2.26%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.9%) → stop au-delà de −1.95% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.91%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.34% (p90 −3.18%) → stop au-delà de −2.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1398 jambes) : jambe baissière méd −1.21% (p90 −2.94%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 95% (51/53) · rebond 58% (30/51)
      · −2.0% : fill 87% (46/53) · rebond 59% (26/46)
      · −3.0% : fill 76% (41/53) · rebond 59% (28/41)
      · −4.0% : fill 58% (34/53) · rebond 61% (23/34)
      · −5.0% : fill 44% (27/53) · rebond 92% (24/27)
   - **flat** (34 séances) :
      · −1.0% : fill 72% (25/34) · rebond 66% (17/25)
      · −2.0% : fill 54% (19/34) · rebond 49% (11/19)
      · −3.0% : fill 40% (15/34) · rebond 60% (9/15)
      · −4.0% : fill 37% (14/34) · rebond 77% (11/14)
      · −5.0% : fill 30% (11/34) · rebond 80% (10/11)
   - **gap-up** (71 séances) :
      · −1.0% : fill 61% (44/71) · rebond 63% (32/44)
      · −2.0% : fill 52% (33/71) · rebond 65% (23/33)
      · −3.0% : fill 34% (23/71) · rebond 59% (16/23)
      · −4.0% : fill 23% (17/71) · rebond 88% (15/17)
      · −5.0% : fill 13% (12/71) · rebond 100% (12/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 56% si les 15 1res min sont vertes (77 cas) · 29% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:03** → P(séance verte=clôture>ouverture) 76% si début vert vs 15% si rouge (base 42% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -2.0% (q20 -4.42%) → **SL/trailing à −4.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.14% / q75 +3.25% → **scale +2.14% / runner +3.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **15%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.15%** (au-delà de la MAE q10 -4.15%), cible rebond +1.5% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.12% .. +5.57%] · haut q95 +6.82% · bas q05 -5.16%
   - 60min (n=160) : retour [-4.85% .. +7.25%] · haut q95 +8.2% · bas q05 -6.05%
   - 2h (n=160) : retour [-4.79% .. +9.19%] · haut q95 +9.95% · bas q05 -6.15%
   - 4h (n=160) : retour [-5.98% .. +9.6%] · haut q95 +9.98% · bas q05 -7.39%
   - 6h (n=160) : retour [-5.66% .. +10.41%] · haut q95 +12.17% · bas q05 -8.1%
   - session (n=160) : retour [-7.13% .. +9.93%] · haut q95 +12.72% · bas q05 -8.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 4.85%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.23 · part idiosyncratique 0.77
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.6  _(momentum baissier)_
- **ADX** : 20.7  _(pas de tendance nette)_
- **MACD** : hist -0.036  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 82.5%
- **ATR** : 1.54 (27.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.013  _(neutre)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 52.8  _(transition)_
- **MA** : MA20 17.81 · MA50 23.72 · MA200 29.91  _(prix < MA20)_
- **Dist MA** : MA20 -18.7% · MA50 -39.0% · MA200 -51.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (514626 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
