# SAF

**Generated** : 2026-10-16T21:45:11.275187+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €317.00  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 42/125 fenêtres (p_fill pondéré 32 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €317.00 (+1.7% vs entrée) · entrée €311.81 · stop €286.86 · T1 €315.80 · R/R 0.16  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

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

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-16 : 317.0 · ATR Wilder 7.58 (2.39 %)_
- **Swing** : plage **307.99 → 302.74** (-2.84 % a -4.5 % sous la cloture, 0.69 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 306.9-310.61 (A) ; 300.92-303.89 (B). stop INDICATIF 291.59 (-3.68 % sous le bas ; sous le support 295.38-302.1 (- 0,5 ATR)).
- **Deep** : plage **302.74 → 287.3** (-4.5 % a -9.37 % sous la cloture, 2.04 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 300.92-303.89 (B) ; 295.38-302.1 (B) ; 289.55-291.92 (B). stop INDICATIF 277.16 (-3.53 % sous le bas ; sous le support 280.94-287.1 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.13 ATR sous le plus haut 20 s., RSI(2) 67.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 310.9-312.29 (C, -1.49 %) ; 306.9-310.61 (A, -2.02 %) ; 300.92-303.89 (B, -4.14 %) ; 295.38-302.1 (B, -4.7 %) ; 289.55-291.92 (B, -7.91 %) ; 280.94-287.1 (B, -9.43 %)
- Resistances reelles au-dessus : 326.14-329.2 (A, 2.88 %) ; 337.5-340.7 (A, 6.47 %) ; 344.03-346.9 (B, 8.53 %) ; 353.5-354.5 (A, 11.51 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (6.12 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **3.866 pt plus bas** dans le cas TYPIQUE (médiane), 3.866 au p90, **3.866 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 6.12 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.003 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.377 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0** [0.0 ; 0.0144] _(largeur 1.4 pt, n_eff 173.1)_
   - swing : **0.4244** [0.3731 ; 0.4769] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3822** [0.3321 ; 0.4342] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 35.2 observations effectives », dont la borne haute a 95 % vaut environ 8.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.4 pt), swing (44.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.21 %** | CVaR **-4.01 %** | vol 2.09 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.11 % contre 1.95 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3854** (β de hausse 1.3537, asymétrie 1.0234) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 305.0321 sur atr_based (1.5 ATR, 3.775 %) — p(stop avant cible) 0.4113 [0.36 ; 0.46], R/R 3.605, perte reelle 3.873 % (gap inclus), CVaR 4.57 %, EV 0.7492 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.7293 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.775 %) — p(stop avant cible) 0.4113 [0.36 ; 0.46], R/R 3.605, perte reelle 3.873 % (gap inclus), EV 0.7492 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ swing_based a 1.47 ATR (stop 5.404 %) — p(stop avant cible) 0.2724 [0.23 ; 0.32], R/R 2.549, perte reelle 5.478 % (gap inclus), EV 0.8206 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 2.7 ATR (stop 8.516 %) — p(stop avant cible) 0.112 [0.08 ; 0.15], R/R 1.602, perte reelle 8.715 % (gap inclus), EV 0.6673 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 7.18 ATR (stop 19.795 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.674, perte reelle 20.702 % (gap inclus), EV 0.6113 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.25 ATR (stop 0.629 %) — p(stop avant cible) 0.8871 [0.85 ; 0.92], R/R 21.24, perte reelle 0.657 % (gap inclus), EV 0.1884 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 21.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.887, borne haute 0.917 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.258 %) — p(stop avant cible) 0.767 [0.72 ; 0.81], R/R 10.571, perte reelle 1.321 % (gap inclus), EV 0.3676 % — **REFUSE**
      - refuse : cible atteinte seulement 3.6 % du temps (< 15 %) meme a 10 seances : le R/R de 10.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.767, borne haute 0.809 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 1.888 %) — p(stop avant cible) 0.6749 [0.62 ; 0.72], R/R 7.125, perte reelle 1.959 % (gap inclus), EV 0.4592 % — **REFUSE**
      - refuse : cible atteinte seulement 3.7 % du temps (< 15 %) meme a 10 seances : le R/R de 7.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.675, borne haute 0.723 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 2.517 %) — p(stop avant cible) 0.5865 [0.53 ; 0.64], R/R 5.338, perte reelle 2.615 % (gap inclus), EV 0.5936 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.587, borne haute 0.637 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 1.47 ATR (stop 4.445 %) — p(stop avant cible) 0.3544 [0.31 ; 0.41], R/R 3.083, perte reelle 4.529 % (gap inclus), EV 0.7031 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 5.034 %) — p(stop avant cible) 0.2992 [0.25 ; 0.35], R/R 2.74, perte reelle 5.094 % (gap inclus), EV 0.8386 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.7 ATR (stop 7.557 %) — p(stop avant cible) 0.1561 [0.12 ; 0.20], R/R 1.818, perte reelle 7.677 % (gap inclus), EV 0.7071 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 10.068 %) — p(stop avant cible) 0.0693 [0.05 ; 0.10], R/R 1.358, perte reelle 10.283 % (gap inclus), EV 0.6243 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 11.326 %) — p(stop avant cible) 0.0518 [0.03 ; 0.08], R/R 1.198, perte reelle 11.656 % (gap inclus), EV 0.6054 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 12.585 %) — p(stop avant cible) 0.0362 [0.02 ; 0.06], R/R 1.045, perte reelle 13.366 % (gap inclus), EV 0.6004 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.18 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 13.843 %) — p(stop avant cible) 0.0253 [0.01 ; 0.05], R/R 0.935, perte reelle 14.927 % (gap inclus), EV 0.5735 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.71 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 15.101 %) — p(stop avant cible) 0.0111 [0.00 ; 0.03], R/R 0.81, perte reelle 17.237 % (gap inclus), EV 0.5907 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.36 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 16.36 %) — p(stop avant cible) 0.0057 [0.00 ; 0.02], R/R 0.717, perte reelle 19.476 % (gap inclus), EV 0.6005 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.16 % > budget 12.00 %
   - 🟢 grid_snapped a 7.18 ATR (stop 18.836 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 0.684, perte reelle 20.422 % (gap inclus), EV 0.6106 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 8.0 ATR (stop 20.135 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.67, perte reelle 20.835 % (gap inclus), EV 0.6107 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 317.0, ATR14 7.9786 (2.517 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 0.868 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.126 % | 316.6011 | 89.41 % | 92.64 % | 93.81 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.252 % | 316.2021 | 81.57 % | 87.24 % | 89.19 % | 91.34 % | 93.37 % | 94.81 % |
| 0.15 ATR | 0.378 % | 315.8032 | 75.39 % | 83.61 % | 86.44 % | 88.88 % | 91.39 % | 92.91 % |
| 0.2 ATR | 0.503 % | 315.4043 | 68.43 % | 78.41 % | 82.91 % | 85.53 % | 89.02 % | 91.21 % |
| 0.25 ATR | 0.629 % | 315.0054 | 61.27 % | 73.8 % | 79.17 % | 83.46 % | 87.73 % | 90.31 % |
| 0.35 ATR | 0.881 % | 314.2075 | 49.41 % | 63.59 % | 69.94 % | 77.17 % | 82.79 % | 87.31 % |
| 0.5 ATR | 1.258 % | 313.0107 | 35.29 % | 51.91 % | 59.23 % | 68.6 % | 76.06 % | 81.82 % |
| 0.75 ATR | 1.888 % | 311.0161 | 20.78 % | 35.53 % | 42.93 % | 53.25 % | 63.4 % | 71.43 % |
| 1.0 ATR | 2.517 % | 309.0214 | 10.0 % | 23.95 % | 32.81 % | 42.62 % | 54.3 % | 62.64 % |
| 1.25 ATR | 3.146 % | 307.0268 | 4.41 % | 15.41 % | 23.97 % | 33.46 % | 46.79 % | 55.84 % |
| 1.5 ATR | 3.775 % | 305.0321 | 2.25 % | 10.11 % | 16.6 % | 25.2 % | 38.58 % | 47.85 % |
| 2.0 ATR | 5.034 % | 301.0429 | 0.98 % | 4.51 % | 7.66 % | 15.65 % | 27.4 % | 37.96 % |
| 2.5 ATR | 6.292 % | 297.0536 | 0.2 % | 1.47 % | 3.73 % | 8.86 % | 18.79 % | 28.87 % |
| 3.0 ATR | 7.551 % | 293.0643 | 0.0 % | 0.88 % | 2.16 % | 5.81 % | 12.56 % | 22.48 % |
| 4.0 ATR | 10.068 % | 285.0857 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 4.55 % | 10.89 % |
| 6.0 ATR | 15.101 % | 269.1286 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.77 ATR | 1.00 ATR | 1.22 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.81 ATR | 0.98 ATR | 1.12 ATR | 1.51 ATR | 1.96 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.72 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.87 ATR | 2.34 ATR |
| **5 s.** | 0.39 ATR | 0.83 ATR | 0.94 ATR | 1.26 ATR | 1.51 ATR | 1.77 ATR | 2.42 ATR | 3.17 ATR |
| **10 s.** | 0.52 ATR | 1.14 ATR | 1.30 ATR | 1.75 ATR | 2.14 ATR | 2.43 ATR | 3.32 ATR | 3.94 ATR |
| **20 s.** | 0.66 ATR | 1.43 ATR | 1.64 ATR | 2.27 ATR | 2.80 ATR | 3.21 ATR | 4.23 ATR | 5.49 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.397–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.605–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.888 %, prix 311.015), p(touche) 35.53 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.718–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.888 %, prix 311.015), p(touche) 42.93 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.944–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.517 %, prix 309.0211), p(touche) 42.62 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.305–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.775 %, prix 305.0333), p(touche) 38.58 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.644–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.034 %, prix 301.0422), p(touche) 37.96 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.048 | EV/share : €-1.188 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 14 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.5 | bear 17.6 | side 72.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.641% → cible +1.279% / stop −8.0%, p_fill 32%, n_eff≈35.2) : P(cible|rempli) **30%** · **EV/risk -0.006** (×p_fill ; si rempli -0.15% du capital)
  - **swing** (entrée dip −3.603% → cible +2.919% / stop −2.611%, p_fill 13%, n_eff≈17.2) : P(cible|rempli) **49%** · **EV/risk +0.028** (×p_fill ; si rempli +0.56% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=13, n_eff=12))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→50% · +2.0%→24% · +3.0%→8% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.49% (p90 4.07%) · excursion haute méd. +0.98% / basse méd. −0.99%
- Profil de vol intra : ouverture 1.488% vs midi 0.546% vs clôture 0.685% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 40% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.099 ; mean-reverting — autocorr -0.058)_ ; drift intra méd. -0.278% ; recovery-V 20%
- **σ réalisé intraday** 1.556% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 68% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 332.2313 (VA 330.9188–333.8062 ; dernier close 330.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 23% · rebond 30% · **stop −1.38%** sous le fill (sous le bruit) · cible +0.71% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.28% · baisse 36% (gap-down >1% 1% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.37% (p90 −1.37%) · haut méd +0.21% · range méd 0.8%
- Excursion ouverture 15min (n=160) : bas méd −0.37% (p90 −1.58%) · haut méd +0.37% · range méd 1.02%
- Excursion ouverture 30min (n=160) : bas méd −0.45% (p90 −1.67%) · haut méd +0.52% · range méd 1.11%
- Excursion ouverture 60min (n=160) : bas méd −0.61% (p90 −1.81%) · haut méd +0.57% · range méd 1.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 330.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 59% (92/159) · gap 8% · délai 1.0min · rebond 36% (35/92) (MFE +0.77%)
   - −1.0% : fill 30min 24% · séance 47% (74/159) · gap 1% · délai 30.6min · rebond 47% (36/74) (MFE +0.87%)
   - −1.5% : fill 30min 9% · séance 28% (46/159) · gap 0% · délai 80.2min · rebond 28% (18/46) (MFE +0.62%)
   - −2.0% : fill 30min 3% · séance 23% (38/159) · gap 0% · délai 218.5min · rebond 30% (14/38) (MFE +0.71%)
   - −3.0% : fill 30min 1% · séance 9% (16/159) · gap 0% · délai 398.1min · rebond 20% (6/16) (MFE +0.54%)
   - −4.0% : fill 30min 0% · séance 1% (4/159) · gap 0% · délai 282.8min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.64% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.23% (p90 −0.66%) → stop au-delà de −0.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.08% (p90 −0.99%) → stop au-delà de −0.67% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=198 jambes) : jambe baissière méd −1.05% (p90 −2.41%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (23 séances) :
      · −1.0% : fill 83% (19/23) · rebond 30% (6/19)
      · −2.0% : fill 53% (13/23) · rebond 24% (5/13)
      · −3.0% : fill 21% (6/23) · rebond 18% (2/6)
      · −4.0% : fill 5% (2/23) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/23) · rebond 0% (0/0)
   - **flat** (45 séances) :
      · −1.0% : fill 52% (24/45) · rebond 48% (13/24)
      · −2.0% : fill 29% (11/45) · rebond 23% (2/11)
      · −3.0% : fill 11% (4/45) · rebond 19% (1/4)
      · −4.0% : fill 0% (0/45) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/45) · rebond 0% (0/0)
   - **gap-up** (91 séances) :
      · −1.0% : fill 32% (31/91) · rebond 60% (17/31)
      · −2.0% : fill 9% (14/91) · rebond 56% (7/14)
      · −3.0% : fill 4% (6/91) · rebond 27% (3/6)
      · −4.0% : fill 1% (2/91) · rebond 38% (1/2)
      · −5.0% : fill 0% (1/91) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 66% si les 15 1res min sont vertes (75 cas) · 27% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 79% si début vert vs 20% si rouge (base 46% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 34min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **79%** · continue >prix actuel 60% ; creux résiduel méd -0.73% (q20 -1.22%) → **SL/trailing à −1.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.0% / q75 +1.41% → **scale +1.0% / runner +1.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **20%** (continue à baisser 59%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.24%** (au-delà de la MAE q10 -2.24%), cible rebond +0.86% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.49% .. +1.27%] · haut q95 +1.76% · bas q05 -1.94%
   - 60min (n=160) : retour [-1.63% .. +1.69%] · haut q95 +1.9% · bas q05 -1.98%
   - 2h (n=160) : retour [-1.79% .. +1.94%] · haut q95 +2.35% · bas q05 -2.39%
   - 4h (n=160) : retour [-1.87% .. +1.93%] · haut q95 +2.53% · bas q05 -2.72%
   - 6h (n=160) : retour [-2.06% .. +2.31%] · haut q95 +2.78% · bas q05 -2.78%
   - session (n=160) : retour [-2.86% .. +2.04%] · haut q95 +2.99% · bas q05 -3.47%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.47 · part idiosyncratique 0.54
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 34.0  _(momentum baissier)_
- **ADX** : 21.2  _(pas de tendance nette)_
- **MACD** : hist -0.77  _(pas de croisement recent)_
- **BB** : %B 0.25 · largeur 10.8%
- **ATR** : 7.98 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.125  _(distribution)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 45.3  _(transition)_
- **MA** : MA20 325.73 · MA50 334.44 · MA200 316.26  _(prix < MA20)_
- **Dist MA** : MA20 -2.7% · MA50 -5.2% · MA200 +0.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (804281 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
