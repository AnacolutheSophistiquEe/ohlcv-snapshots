# HOOD

**Generated** : 2026-10-26T01:29:18.686976+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $95.07  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-27 — HOOD earnings (J-1 sess · earnings)  
> ↳ spot $95.07 (+1.0% vs entrée) · entrée $94.09 · stop $88.79 · T1 $101.70 · R/R 1.44  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk -0.177 _(réel 5 s)_ (GBM -0.099) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -26 % hors [0,100] (R² max 0.39). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 95.07 · ATR Wilder 5.62 (5.91 %)_
- **Swing** : plage **88.8 → 84.01** (-6.59 % a -11.63 % sous la cloture, 0.85 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 88.6-90.7 (B). stop INDICATIF 79.12 (-5.82 % sous le bas ; sous le support 81.93-83.68 (- 0,5 ATR)).
- **Deep** : plage **84.01 → 73.8** (-11.63 % a -22.38 % sous la cloture, 1.82 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 81.93-83.68 (A) ; 77.8-79.57 (A) ; 72.79-74.59 (A). stop INDICATIF 67.12 (-9.05 % sous le bas ; sous le support 69.93-72.25 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.06 ATR sous le plus haut 20 s., RSI(2) 20.7. Limite **92.26** (seance suivante), stop catastrophe 69.78, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 91.44-93.36 (A, -1.8 %) ; 88.6-90.7 (B, -4.6 %) ; 81.93-83.68 (A, -11.98 %) ; 77.8-79.57 (A, -16.3 %) ; 72.79-74.59 (A, -21.54 %) ; 69.93-72.25 (A, -24.0 %)
- Resistances reelles au-dessus : 98.75-100.88 (A, 3.87 %) ; 101.71-104.45 (A, 6.98 %) ; 105.11-106.31 (B, 10.56 %) ; 108.81-111.46 (A, 14.45 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.34 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.61 %)** : le gap seul le franchit 1.196 % des séances (15 fois sur 1254).
   - exécution **2.463 pt plus bas** dans le cas TYPIQUE (médiane), 6.627 au p90, **11.175 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 6.61 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0405 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.456 % | p01 -7.299 % | pire -17.785 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.298** [0.2336 ; 0.3691] _(largeur 13.5 pt, n_eff 173.1)_
   - swing : **0.5186** [0.466 ; 0.5709] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4723** [0.4201 ; 0.525] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-6.03 %** | CVaR **-8.94 %** | vol 4.29 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.52 % contre 4.42 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.4 % vs -14.49 % si l'on extrapolait par √5 _(rapport 0.994 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7837** (β de hausse 1.6185, asymétrie 1.1021) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.433× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 87.1065 sur atr_based (1.5 ATR, 8.376 %) — p(stop avant cible) 0.4962 [0.44 ; 0.55], R/R 3.204, perte reelle 8.796 % (gap inclus), CVaR 11.68 %, EV 0.7491 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6267 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.3 ATR (stop 4.634 %) — p(stop avant cible) 0.6886 [0.64 ; 0.74], R/R 5.812, perte reelle 4.849 % (gap inclus), EV 0.4663 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.689, borne haute 0.736 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 support a 0.68 ATR (stop 6.756 %) — p(stop avant cible) 0.5887 [0.54 ; 0.64], R/R 3.985, perte reelle 7.071 % (gap inclus), EV 0.5069 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.589, borne haute 0.640 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.33 ATR du spot — compartiment <1, mesure a 47.8 % de casse (IC clusterise [0.449 ; 0.507] sur 1237 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 8.376 %) — p(stop avant cible) 0.4962 [0.44 ; 0.55], R/R 3.204, perte reelle 8.796 % (gap inclus), EV 0.7491 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - 🟢 support a 3.04 ATR (stop 19.914 %) — p(stop avant cible) 0.0719 [0.05 ; 0.10], R/R 1.391, perte reelle 20.266 % (gap inclus), EV 1.7929 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.42 % > budget 12.00 %
   - 🟢 support a 4.87 ATR (stop 30.128 %) — p(stop avant cible) 0.0203 [0.01 ; 0.04], R/R 0.929, perte reelle 30.329 % (gap inclus), EV 1.8255 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.39 % > budget 12.00 %
   - ⚪ grid_snapped a 0.3 ATR (stop 3.372 %) — p(stop avant cible) 0.7633 [0.72 ; 0.81], R/R 7.851, perte reelle 3.589 % (gap inclus), EV 0.4059 % — **REFUSE**
      - refuse : cible atteinte seulement 3.5 % du temps (< 15 %) meme a 10 seances : le R/R de 7.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.763, borne haute 0.806 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 grid_snapped a 0.68 ATR (stop 5.494 %) — p(stop avant cible) 0.6485 [0.60 ; 0.70], R/R 4.848, perte reelle 5.813 % (gap inclus), EV 0.4578 % — **REFUSE**
      - refuse : cible atteinte seulement 4.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.648, borne haute 0.697 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.75 ATR (stop 9.773 %) — p(stop avant cible) 0.4152 [0.36 ; 0.47], R/R 2.753, perte reelle 10.237 % (gap inclus), EV 1.1629 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.25 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 11.169 %) — p(stop avant cible) 0.3426 [0.29 ; 0.39], R/R 2.409, perte reelle 11.696 % (gap inclus), EV 1.245 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.68 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 12.565 %) — p(stop avant cible) 0.2803 [0.23 ; 0.33], R/R 2.13, perte reelle 13.229 % (gap inclus), EV 1.3867 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.21 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 13.961 %) — p(stop avant cible) 0.2299 [0.19 ; 0.28], R/R 1.938, perte reelle 14.542 % (gap inclus), EV 1.3905 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.59 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.357 %) — p(stop avant cible) 0.1929 [0.15 ; 0.24], R/R 1.778, perte reelle 15.849 % (gap inclus), EV 1.4226 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 12.00 %
   - 🟢 grid_snapped a 3.04 ATR (stop 18.652 %) — p(stop avant cible) 0.0951 [0.07 ; 0.13], R/R 1.483, perte reelle 18.999 % (gap inclus), EV 1.7066 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.31 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.337 %) — p(stop avant cible) 0.0516 [0.03 ; 0.08], R/R 1.241, perte reelle 22.703 % (gap inclus), EV 1.8145 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.71 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 25.129 %) — p(stop avant cible) 0.0301 [0.02 ; 0.05], R/R 1.099, perte reelle 25.645 % (gap inclus), EV 1.8284 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.28 % > budget 12.00 %
   - 🟢 grid_snapped a 4.87 ATR (stop 28.866 %) — p(stop avant cible) 0.0215 [0.01 ; 0.04], R/R 0.965, perte reelle 29.191 % (gap inclus), EV 1.8236 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.17 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.506 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 0.832, perte reelle 33.855 % (gap inclus), EV 1.9435 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.45 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 36.298 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.769, perte reelle 36.639 % (gap inclus), EV 1.9573 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.17 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 39.09 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.721, perte reelle 39.09 % (gap inclus), EV 1.965 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.06 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.882 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.673, perte reelle 41.882 % (gap inclus), EV 1.9727 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.87 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.674 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.631, perte reelle 44.674 % (gap inclus), EV 1.9727 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.87 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 95.07, ATR14 5.309 (5.584 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.375 ATR = 2.094 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.279 % | 94.8045 | 93.16 % | 95.27 % | 96.17 % | 96.67 % | 97.16 % | 98.05 % |
| 0.1 ATR | 0.558 % | 94.5391 | 85.51 % | 90.63 % | 92.34 % | 93.94 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.838 % | 94.2736 | 77.87 % | 85.6 % | 88.31 % | 90.71 % | 92.69 % | 95.08 % |
| 0.2 ATR | 1.117 % | 94.0082 | 71.53 % | 80.36 % | 84.17 % | 87.47 % | 90.46 % | 93.23 % |
| 0.25 ATR | 1.396 % | 93.7427 | 64.59 % | 74.62 % | 79.54 % | 83.94 % | 87.82 % | 90.87 % |
| 0.35 ATR | 1.955 % | 93.2118 | 52.52 % | 65.66 % | 72.28 % | 78.18 % | 83.65 % | 87.9 % |
| 0.5 ATR | 2.792 % | 92.4155 | 37.12 % | 53.68 % | 61.39 % | 68.99 % | 76.65 % | 82.15 % |
| 0.75 ATR | 4.188 % | 91.0883 | 19.62 % | 36.25 % | 46.07 % | 56.06 % | 65.79 % | 72.92 % |
| 1.0 ATR | 5.584 % | 89.761 | 9.36 % | 23.36 % | 33.17 % | 44.44 % | 55.23 % | 65.33 % |
| 1.25 ATR | 6.98 % | 88.4338 | 4.93 % | 14.8 % | 22.88 % | 34.14 % | 47.51 % | 58.77 % |
| 1.5 ATR | 8.376 % | 87.1065 | 2.52 % | 10.07 % | 16.63 % | 27.27 % | 40.61 % | 52.92 % |
| 2.0 ATR | 11.169 % | 84.452 | 0.5 % | 3.93 % | 7.46 % | 15.56 % | 29.95 % | 43.08 % |
| 2.5 ATR | 13.961 % | 81.7975 | 0.1 % | 1.61 % | 4.03 % | 8.38 % | 21.62 % | 33.95 % |
| 3.0 ATR | 16.753 % | 79.143 | 0.0 % | 0.7 % | 2.42 % | 5.15 % | 15.03 % | 25.95 % |
| 4.0 ATR | 22.337 % | 73.834 | 0.0 % | 0.4 % | 0.91 % | 2.12 % | 6.29 % | 14.46 % |
| 6.0 ATR | 33.506 % | 63.216 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.25 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.97 ATR | 1.10 ATR | 1.51 ATR | 1.91 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.77 ATR | 1.00 ATR | 1.20 ATR | 1.36 ATR | 1.86 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.99 ATR | 1.29 ATR | 1.60 ATR | 1.81 ATR | 2.39 ATR | 3.05 ATR |
| **10 s.** | 0.54 ATR | 1.17 ATR | 1.34 ATR | 1.86 ATR | 2.30 ATR | 2.62 ATR | 3.58 ATR | 4.52 ATR |
| **20 s.** | 0.69 ATR | 1.65 ATR | 1.90 ATR | 2.56 ATR | 3.08 ATR | 3.52 ATR | 4.91 ATR | 5.92 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.423–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.792 %, prix 92.4156), p(touche) 37.12 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.188 %, prix 91.0885), p(touche) 36.25 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.771–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.584 %, prix 89.7613), p(touche) 33.17 % (en stress 92.0 %)  ✅ optimum identifie (60.0 % des re-echantillons)
- **5 seance(s)** : plage utile 0.988–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.584 %, prix 89.7613), p(touche) 44.44 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.341–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.376 %, prix 87.1069), p(touche) 40.61 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.902–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (13.961 %, prix 81.7973), p(touche) 33.95 % (en stress 93.88 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (63.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.099 | EV/share : $-0.527 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 16 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 7.4 | bear 80.1 | side 12.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 85.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.464% → cible +2.805% / stop −3.0%, p_fill 86%, n_eff≈92.3) : P(cible|rempli) **25%** · **EV/risk -0.102** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −1.026% → cible +8.086% / stop −5.642%, p_fill 85%, n_eff≈98.0) : P(cible|rempli) **27%** · **EV/risk -0.177** (×p_fill ; si rempli -1.18% du capital)
  - **deep** (entrée dip −1.583% → cible +8.701% / stop −8.511%, p_fill 86%, n_eff≈95.5) : P(cible|rempli) **49%** · **EV/risk +0.023** (×p_fill ; si rempli +0.23% du capital)
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.73 · part idiosyncratique 0.27
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-27 — HOOD earnings (J-1 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-27 — HOOD earnings (J-1 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-27 — HOOD earnings (J-1 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 27.7  _(survente)_
- **ADX** : 19.7  _(pas de tendance nette)_
- **MACD** : hist -1.505  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 26.2%
- **ATR** : 5.31 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.342  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 46.6  _(transition)_
- **MA** : MA20 106.64 · MA50 108.87 · MA200 93.25  _(prix < MA20)_
- **Dist MA** : MA20 -10.8% · MA50 -12.7% · MA200 +1.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (784475 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
