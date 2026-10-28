# HOOD

**Generated** : 2026-10-28T01:31:50.235664+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $94.56  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $94.56 (+0.3% vs entrée) · entrée $94.24 · stop $91.41 · T1 $96.83 · R/R 0.92  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +7.7 % ≠ (strike 100.0 − spot 94.56)/spot = +5.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-27 : 94.56 · ATR Wilder 5.35 (5.66 %)_
- **Swing** : plage **88.59 → 84.03** (-6.31 % a -11.13 % sous la cloture, 0.85 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 79.26 (-5.68 % sous le bas ; sous le support 81.93-83.68 (- 0,5 ATR)).
- **Deep** : plage **84.03 → 74.23** (-11.13 % a -21.5 % sous la cloture, 1.83 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 81.93-83.68 (A) ; 77.8-79.57 (A) ; 72.79-74.59 (A). stop INDICATIF 67.26 (-9.4 % sous le bas ; sous le support 69.93-72.25 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.41 ATR sous le plus haut 20 s., RSI(2) 47.2. Limite **91.89** (seance suivante), stop catastrophe 70.49, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 88.6-90.7 (B, -4.08 %) ; 81.93-83.68 (A, -11.51 %) ; 77.8-79.57 (A, -15.85 %) ; 72.79-74.59 (A, -21.12 %) ; 69.93-72.25 (A, -23.59 %) ; 66.91-69.22 (A, -26.8 %)
- Resistances reelles au-dessus : 98.75-100.88 (A, 4.43 %) ; 101.71-102.1 (B, 7.56 %) ; 104.45-106.31 (A, 10.46 %) ; 108.81-111.46 (A, 15.07 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.26 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.24 %)** : le gap seul le franchit 1.197 % des séances (15 fois sur 1253).
   - exécution **2.785 pt plus bas** dans le cas TYPIQUE (médiane), 6.997 au p90, **11.545 au pire**
   - perte réelle **9.829 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 6.24 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.043 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.437 % | p01 -6.769 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2911** [0.2273 ; 0.3618] _(largeur 13.5 pt, n_eff 173.1)_
   - swing : **0.5277** [0.475 ; 0.5799] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4788** [0.4265 ; 0.5315] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-6.03 %** | CVaR **-8.94 %** | vol 4.3 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.47 % contre 4.42 % aujourd'hui, rapport 0.56)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.4 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.003 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7704** (β de hausse 1.6283, asymétrie 1.0873) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.437× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 86.7777 sur atr_based (1.5 ATR, 8.23 %) — p(stop avant cible) 0.505 [0.45 ; 0.56], R/R 3.331, perte reelle 8.679 % (gap inclus), CVaR 11.549 %, EV 0.6652 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6803 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.505, borne haute 0.557 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.21 ATR (stop 3.549 %) — p(stop avant cible) 0.7604 [0.71 ; 0.80], R/R 7.699, perte reelle 3.755 % (gap inclus), EV 0.3092 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.760, borne haute 0.803 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 support a 0.6 ATR (stop 5.708 %) — p(stop avant cible) 0.6448 [0.59 ; 0.69], R/R 4.817, perte reelle 6.001 % (gap inclus), EV 0.3412 % — **REFUSE**
      - refuse : cible atteinte seulement 4.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.645, borne haute 0.694 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.24 ATR du spot — compartiment <1, mesure a 49.7 % de casse (IC clusterise [0.467 ; 0.529] sur 1189 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 8.23 %) — p(stop avant cible) 0.505 [0.45 ; 0.56], R/R 3.331, perte reelle 8.679 % (gap inclus), EV 0.6652 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.505, borne haute 0.557 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🟢 support a 3.01 ATR (stop 18.938 %) — p(stop avant cible) 0.0868 [0.06 ; 0.12], R/R 1.501, perte reelle 19.255 % (gap inclus), EV 1.6018 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.49 % > budget 12.00 %
   - 🟢 support a 4.88 ATR (stop 29.206 %) — p(stop avant cible) 0.0201 [0.01 ; 0.04], R/R 0.98, perte reelle 29.507 % (gap inclus), EV 1.6593 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.99 % > budget 12.00 %
   - ⚪ grid_snapped a 0.21 ATR (stop 2.787 %) — p(stop avant cible) 0.7999 [0.76 ; 0.84], R/R 9.665, perte reelle 2.991 % (gap inclus), EV 0.2856 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 9.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.800, borne haute 0.840 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 grid_snapped a 0.6 ATR (stop 4.945 %) — p(stop avant cible) 0.6798 [0.63 ; 0.73], R/R 5.55, perte reelle 5.209 % (gap inclus), EV 0.2657 % — **REFUSE**
      - refuse : cible atteinte seulement 3.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.680, borne haute 0.727 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 6.858 %) — p(stop avant cible) 0.5863 [0.53 ; 0.64], R/R 4.01, perte reelle 7.21 % (gap inclus), EV 0.4473 % — **REFUSE**
      - refuse : cible atteinte seulement 4.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.586, borne haute 0.637 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.75 ATR (stop 9.602 %) — p(stop avant cible) 0.4344 [0.38 ; 0.49], R/R 2.873, perte reelle 10.064 % (gap inclus), EV 0.9263 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.07 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 10.973 %) — p(stop avant cible) 0.3608 [0.31 ; 0.41], R/R 2.517, perte reelle 11.488 % (gap inclus), EV 1.0121 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.60 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 12.345 %) — p(stop avant cible) 0.2921 [0.25 ; 0.34], R/R 2.23, perte reelle 12.963 % (gap inclus), EV 1.2385 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.91 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 13.717 %) — p(stop avant cible) 0.2424 [0.20 ; 0.29], R/R 2.022, perte reelle 14.298 % (gap inclus), EV 1.1508 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.47 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.088 %) — p(stop avant cible) 0.2017 [0.16 ; 0.25], R/R 1.859, perte reelle 15.551 % (gap inclus), EV 1.2393 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.95 % > budget 12.00 %
   - 🟢 grid_snapped a 3.01 ATR (stop 18.175 %) — p(stop avant cible) 0.1026 [0.07 ; 0.14], R/R 1.557, perte reelle 18.569 % (gap inclus), EV 1.5141 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.98 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 21.947 %) — p(stop avant cible) 0.0545 [0.03 ; 0.08], R/R 1.297, perte reelle 22.289 % (gap inclus), EV 1.6295 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.32 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 24.69 %) — p(stop avant cible) 0.0298 [0.02 ; 0.05], R/R 1.144, perte reelle 25.267 % (gap inclus), EV 1.655 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.99 % > budget 12.00 %
   - 🟢 grid_snapped a 4.88 ATR (stop 28.444 %) — p(stop avant cible) 0.0218 [0.01 ; 0.04], R/R 1.003, perte reelle 28.81 % (gap inclus), EV 1.6423 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.04 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 30.177 %) — p(stop avant cible) 0.0201 [0.01 ; 0.04], R/R 0.952, perte reelle 30.373 % (gap inclus), EV 1.6402 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.33 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 32.92 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 0.872, perte reelle 33.172 % (gap inclus), EV 1.7267 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.99 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 35.663 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.793, perte reelle 36.469 % (gap inclus), EV 1.7719 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.11 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 38.407 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.753, perte reelle 38.407 % (gap inclus), EV 1.7801 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.99 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.15 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.703, perte reelle 41.15 % (gap inclus), EV 1.7874 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.82 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 43.894 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.659, perte reelle 43.894 % (gap inclus), EV 1.7874 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.82 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 94.56, ATR14 5.1882 (5.487 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.373 ATR = 2.047 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.274 % | 94.3006 | 93.15 % | 95.26 % | 96.17 % | 96.66 % | 97.15 % | 98.05 % |
| 0.1 ATR | 0.549 % | 94.0412 | 85.5 % | 90.62 % | 92.33 % | 93.93 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.823 % | 93.7818 | 77.84 % | 85.58 % | 88.29 % | 90.7 % | 92.68 % | 95.07 % |
| 0.2 ATR | 1.097 % | 93.5224 | 71.5 % | 80.34 % | 84.16 % | 87.46 % | 90.45 % | 93.22 % |
| 0.25 ATR | 1.372 % | 93.2629 | 64.55 % | 74.6 % | 79.52 % | 83.92 % | 87.8 % | 90.86 % |
| 0.35 ATR | 1.92 % | 92.7441 | 52.37 % | 65.62 % | 72.25 % | 78.16 % | 83.64 % | 87.89 % |
| 0.5 ATR | 2.743 % | 91.9659 | 36.86 % | 53.63 % | 61.35 % | 68.96 % | 76.63 % | 82.14 % |
| 0.75 ATR | 4.115 % | 90.6688 | 19.34 % | 36.09 % | 46.01 % | 55.92 % | 65.75 % | 72.9 % |
| 1.0 ATR | 5.487 % | 89.3718 | 9.26 % | 23.19 % | 33.1 % | 44.19 % | 55.18 % | 65.3 % |
| 1.25 ATR | 6.858 % | 88.0747 | 4.83 % | 14.62 % | 22.6 % | 33.87 % | 47.46 % | 58.73 % |
| 1.5 ATR | 8.23 % | 86.7777 | 2.42 % | 9.88 % | 16.35 % | 27.0 % | 40.55 % | 52.87 % |
| 2.0 ATR | 10.973 % | 84.1836 | 0.4 % | 3.73 % | 7.16 % | 15.27 % | 29.88 % | 43.02 % |
| 2.5 ATR | 13.717 % | 81.5895 | 0.0 % | 1.41 % | 3.73 % | 8.09 % | 21.54 % | 33.88 % |
| 3.0 ATR | 16.46 % | 78.9954 | 0.0 % | 0.5 % | 2.12 % | 4.85 % | 14.84 % | 25.87 % |
| 4.0 ATR | 21.947 % | 73.8071 | 0.0 % | 0.3 % | 0.61 % | 1.82 % | 6.0 % | 14.27 % |
| 6.0 ATR | 32.92 % | 63.4307 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.77 ATR | 1.00 ATR | 1.19 ATR | 1.35 ATR | 1.84 ATR | 2.31 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.98 ATR | 1.28 ATR | 1.58 ATR | 1.80 ATR | 2.37 ATR | 2.98 ATR |
| **10 s.** | 0.54 ATR | 1.17 ATR | 1.34 ATR | 1.85 ATR | 2.29 ATR | 2.62 ATR | 3.55 ATR | 4.43 ATR |
| **20 s.** | 0.69 ATR | 1.65 ATR | 1.90 ATR | 2.56 ATR | 3.08 ATR | 3.51 ATR | 4.88 ATR | 5.92 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.421–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.623–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.115 %, prix 90.6689), p(touche) 36.09 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.77–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.487 %, prix 89.3715), p(touche) 33.1 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.983–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.487 %, prix 89.3715), p(touche) 44.19 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.339–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.23 %, prix 86.7777), p(touche) 40.55 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.899–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (13.717 %, prix 81.5892), p(touche) 33.88 % (en stress 92.86 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (64.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.01 | EV/share : $-0.028 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.5 | bear 85.0 | side 6.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 85.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.34% → cible +2.753% / stop −3.0%, p_fill 91%, n_eff≈97.7) : P(cible|rempli) **26%** · **EV/risk -0.111** (×p_fill ; si rempli -0.37% du capital)
  - **swing** (entrée dip −0.753% → cible +8.383% / stop −5.528%, p_fill 88%, n_eff≈101.9) : P(cible|rempli) **25%** · **EV/risk -0.181** (×p_fill ; si rempli -1.14% du capital)
  - **deep** (entrée dip −1.14% → cible +8.803% / stop −8.325%, p_fill 89%, n_eff≈98.3) : P(cible|rempli) **46%** · **EV/risk -0.053** (×p_fill ; si rempli -0.50% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→79% · +2.0%→52% · +3.0%→34% · +5.0%→18% · +8.0%→6%
- Range intraday médian 4.75% (p90 8.94%) · excursion haute méd. +2.07% / basse méd. −2.15%
- Profil de vol intra : ouverture 3.568% vs midi 0.948% vs clôture 1.079% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 21% · trend ↑0%/↓1% ; spike-down 68% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.057)_ ; drift intra méd. -0.413% ; recovery-V 19%
- **σ réalisé intraday** 3.025% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 60% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 96.1559 (VA 95.5739–96.6651 ; dernier close 95.07)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 27% · rebond 71% · **stop −3.99%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. -0.16% · baisse 53% (gap-down >1% 34% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.34%) · haut méd +0.88% · range méd 2.06%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −2.96%) · haut méd +1.23% · range méd 2.63%
- Excursion ouverture 30min (n=160) : bas méd −1.41% (p90 −3.35%) · haut méd +1.36% · range méd 3.2%
- Excursion ouverture 60min (n=160) : bas méd −1.78% (p90 −3.71%) · haut méd +1.53% · range méd 3.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 95.07 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (122/159) · gap 41% · délai 0.0min · rebond 60% (70/122) (MFE +1.4%)
   - −1.0% : fill 30min 58% · séance 70% (107/159) · gap 34% · délai 0.0min · rebond 65% (66/107) (MFE +1.62%)
   - −1.5% : fill 30min 46% · séance 62% (97/159) · gap 25% · délai 1.1min · rebond 55% (54/97) (MFE +1.31%)
   - −2.0% : fill 30min 36% · séance 50% (84/159) · gap 19% · délai 1.6min · rebond 63% (55/84) (MFE +1.3%)
   - −3.0% : fill 30min 24% · séance 35% (61/159) · gap 10% · délai 7.4min · rebond 74% (44/61) (MFE +1.88%)
   - −4.0% : fill 30min 15% · séance 27% (45/159) · gap 3% · délai 11.1min · rebond 71% (32/45) (MFE +2.53%)
   - −5.0% : fill 30min 7% · séance 17% (28/159) · gap 1% · délai 55.8min · rebond 47% (18/28) (MFE +1.02%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.47%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.3%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.41%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=725 jambes) : jambe baissière méd −1.14% (p90 −2.78%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 91% (68/72) · rebond 57% (36/68)
      · −2.0% : fill 73% (58/72) · rebond 64% (37/58)
      · −3.0% : fill 59% (47/72) · rebond 82% (35/47)
      · −4.0% : fill 47% (36/72) · rebond 78% (28/36)
      · −5.0% : fill 31% (24/72) · rebond 47% (15/24)
   - **flat** (17 séances) :
      · −1.0% : fill 72% (11/17) · rebond 79% (8/11)
      · −2.0% : fill 38% (8/17) · rebond 55% (5/8)
      · −3.0% : fill 15% (3/17) · rebond 0% (0/3)
      · −4.0% : fill 15% (3/17) · rebond 0% (0/3)
      · −5.0% : fill 13% (2/17) · rebond 15% (1/2)
   - **gap-up** (70 séances) :
      · −1.0% : fill 45% (28/70) · rebond 78% (22/28)
      · −2.0% : fill 29% (18/70) · rebond 63% (13/18)
      · −3.0% : fill 13% (11/70) · rebond 56% (9/11)
      · −4.0% : fill 7% (6/70) · rebond 63% (4/6)
      · −5.0% : fill 2% (2/70) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 58% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **53min** → P(séance verte=clôture>ouverture) 65% si début vert vs 18% si rouge (base 42% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **65%** · continue >prix actuel 43% ; creux résiduel méd -1.45% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +2.53% → **scale +1.32% / runner +2.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **18%** (continue à baisser 63%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.8%** (au-delà de la MAE q10 -3.8%), cible rebond +1.47% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.48% .. +3.77%] · haut q95 +4.35% · bas q05 -4.82%
   - 60min (n=160) : retour [-3.67% .. +4.97%] · haut q95 +5.48% · bas q05 -4.85%
   - 2h (n=160) : retour [-4.63% .. +4.96%] · haut q95 +6.62% · bas q05 -5.1%
   - 4h (n=160) : retour [-4.82% .. +5.74%] · haut q95 +7.31% · bas q05 -6.0%
   - 6h (n=160) : retour [-5.77% .. +6.28%] · haut q95 +7.31% · bas q05 -7.11%
   - session (n=160) : retour [-5.56% .. +6.85%] · haut q95 +7.46% · bas q05 -7.12%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.88% (p75 1.28% / p90 2.57%) · ~3.72 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=50)
   - −1.0% → **68%** (reprise méd 26.42 min, n=21)
   - −1.5% → **64%** (reprise méd 29.02 min, n=10)
   - −2.0% → **53%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.57%** (p90, défaut prudent ; serré/agressif −1.28%) ; extension open→close méd +6.81% (q75 +7.91% / q95 +11.09%), MFE méd +7.28% / q90 +11.48%
   - Échelle scale-out : +7.28% (33%) / +8.78% (33%) / +11.48% (34%)
- **DÉSARMER** : repli > **−2.57%** depuis le plus-haut = décay → P(retournement) **39%** (préavis méd 256.98 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.48% : P(retournement après) 0% (mèche méd 3.29%)
- **CONTEXTE** : la dernière heure tient les gains 79% du temps (retour médian dernière heure +0.47%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.71 · part idiosyncratique 0.29
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.2  _(momentum baissier)_
- **ADX** : 21.8  _(pas de tendance nette)_
- **MACD** : hist -1.344  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 27.4%
- **ATR** : 5.19 (40.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.327  _(distribution)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 48.2  _(transition)_
- **MA** : MA20 104.37 · MA50 108.78 · MA200 93.04  _(prix < MA20)_
- **Dist MA** : MA20 -9.4% · MA50 -13.1% · MA200 +1.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (787393 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
