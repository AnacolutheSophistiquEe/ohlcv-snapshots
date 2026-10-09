# SRT3

**Generated** : 2026-10-09T21:41:59.375827+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €253.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €253.00 (+4.7% vs entrée) · entrée €241.59 · stop €231.24 · T1 €262.29 · R/R 2.0  
> ↳ ¼-Kelly 0.014 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-09 : 253.0 · ATR Wilder 9.31 (3.68 %)_
- **Swing** : plage **240.59 → 233.02** (-4.9 % a -7.9 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 238.58-242.86 (B) ; 233.21-236.68 (B). stop INDICATIF 223.56 (-4.06 % sous le bas ; sous le support 228.21-232.82 (- 0,5 ATR)).
- **Deep** : plage **233.02 → 213.84** (-7.9 % a -15.48 % sous la cloture, 2.06 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 228.21-232.82 (A) ; 223.23-227.65 (A) ; 218.31-222.78 (B) ; 213.07-217.7 (A). stop INDICATIF 203.33 (-4.92 % sous le bas ; sous le support 207.98-212.57 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.03 ATR sous le plus haut 20 s., RSI(2) 51.9 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 243.56-247.91 (B, -2.01 %) ; 238.58-242.86 (B, -4.01 %) ; 233.21-236.68 (B, -6.45 %) ; 228.21-232.82 (A, -7.98 %) ; 223.23-227.65 (A, -10.02 %) ; 218.31-222.78 (B, -11.94 %)
- Resistances reelles au-dessus : 259.9-264.1 (A, 2.73 %) ; 266.78-270.86 (A, 5.45 %) ; 271.9-275.96 (A, 7.47 %) ; 288.55-290.03 (A, 14.05 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.6 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **1.372 pt plus bas** dans le cas TYPIQUE (médiane), 4.759 au p90, **5.605 au pire**
   - perte réelle **11.278 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 8.6 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0063 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.607 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1987** [0.1445 ; 0.2628] _(largeur 11.8 pt, n_eff 173.1)_
   - swing : **0.3877** [0.3375 ; 0.4398] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3584** [0.3092 ; 0.41] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (28.9 pt), swing (44.8 pt), deep (46.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.11 %** | CVaR **-6.59 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.98 % vs -9.16 % si l'on extrapolait par √5 _(rapport 1.089 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0899** (β de hausse 1.1756, asymétrie 0.9271) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.328× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 242.9214 sur atr_grid (1.0 ATR, 3.984 %) — p(stop avant cible) 0.5585 [0.51 ; 0.61], R/R 3.062, perte reelle 4.108 % (gap inclus), CVaR 5.303 %, EV 0.3848 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3762 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.558, borne haute 0.610 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.975 %) — p(stop avant cible) 0.3851 [0.33 ; 0.44], R/R 2.064, perte reelle 6.096 % (gap inclus), EV 0.6668 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 2.16 ATR (stop 10.882 %) — p(stop avant cible) 0.1473 [0.11 ; 0.19], R/R 1.15, perte reelle 10.943 % (gap inclus), EV 0.6502 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 2.86 ATR (stop 13.672 %) — p(stop avant cible) 0.0652 [0.04 ; 0.09], R/R 0.911, perte reelle 13.81 % (gap inclus), EV 0.7774 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.85 % > budget 12.00 %
   - 🟢 support a 5.48 ATR (stop 24.094 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 0.491, perte reelle 25.615 % (gap inclus), EV 0.9493 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.06 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.996 %) — p(stop avant cible) 0.8885 [0.85 ; 0.92], R/R 12.255, perte reelle 1.027 % (gap inclus), EV 0.0044 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 12.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.888, borne haute 0.918 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.992 %) — p(stop avant cible) 0.7744 [0.73 ; 0.82], R/R 6.174, perte reelle 2.037 % (gap inclus), EV -0.056 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.774, borne haute 0.816 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 6.7 % x 12.58 % + P(rien) 15.8 % x 4.27 % ne couvrent pas P(stop) 77.4 % x 2.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.988 %) — p(stop avant cible) 0.6593 [0.61 ; 0.71], R/R 4.08, perte reelle 3.084 % (gap inclus), EV 0.2435 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.659, borne haute 0.708 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 3.984 %) — p(stop avant cible) 0.5585 [0.51 ; 0.61], R/R 3.062, perte reelle 4.108 % (gap inclus), EV 0.3848 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.558, borne haute 0.610 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 4.98 %) — p(stop avant cible) 0.4848 [0.43 ; 0.54], R/R 2.482, perte reelle 5.068 % (gap inclus), EV 0.4196 % — **REFUSE**
      - refuse : cible atteinte seulement 11.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 6.971 %) — p(stop avant cible) 0.342 [0.29 ; 0.39], R/R 1.784, perte reelle 7.052 % (gap inclus), EV 0.5975 % — **REFUSE**
      - refuse : cible atteinte seulement 11.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.16 ATR (stop 9.794 %) — p(stop avant cible) 0.1807 [0.14 ; 0.22], R/R 1.272, perte reelle 9.89 % (gap inclus), EV 0.6924 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.86 ATR (stop 12.585 %) — p(stop avant cible) 0.0885 [0.06 ; 0.12], R/R 0.993, perte reelle 12.664 % (gap inclus), EV 0.7362 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.72 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 15.934 %) — p(stop avant cible) 0.025 [0.01 ; 0.05], R/R 0.759, perte reelle 16.569 % (gap inclus), EV 0.8641 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.26 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 17.926 %) — p(stop avant cible) 0.0125 [0.00 ; 0.03], R/R 0.665, perte reelle 18.93 % (gap inclus), EV 0.9109 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.65 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 19.918 %) — p(stop avant cible) 0.0098 [0.00 ; 0.02], R/R 0.616, perte reelle 20.425 % (gap inclus), EV 0.9119 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.65 % > budget 12.00 %
   - 🟢 grid_snapped a 5.48 ATR (stop 23.006 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 0.523, perte reelle 24.067 % (gap inclus), EV 0.935 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.37 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 25.894 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.47, perte reelle 26.76 % (gap inclus), EV 0.9532 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.98 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 27.885 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.451, perte reelle 27.885 % (gap inclus), EV 0.953 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.01 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 29.877 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.421, perte reelle 29.877 % (gap inclus), EV 0.9587 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.87 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 31.869 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.395, perte reelle 31.869 % (gap inclus), EV 0.9585 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.87 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 253.0, ATR14 10.0786 (3.984 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 1.522 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.199 % | 252.4961 | 88.95 % | 92.69 % | 94.27 % | 96.04 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.398 % | 251.9921 | 82.54 % | 88.35 % | 90.81 % | 93.47 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.598 % | 251.4882 | 74.95 % | 83.51 % | 86.76 % | 90.3 % | 93.33 % | 94.97 % |
| 0.2 ATR | 0.797 % | 250.9843 | 68.44 % | 78.68 % | 82.81 % | 87.23 % | 92.04 % | 94.37 % |
| 0.25 ATR | 0.996 % | 250.4804 | 63.12 % | 75.32 % | 79.55 % | 84.85 % | 90.25 % | 93.07 % |
| 0.35 ATR | 1.394 % | 249.4725 | 53.16 % | 68.9 % | 73.72 % | 80.5 % | 86.87 % | 90.95 % |
| 0.5 ATR | 1.992 % | 247.9607 | 38.26 % | 56.37 % | 64.13 % | 73.76 % | 82.29 % | 88.24 % |
| 0.75 ATR | 2.988 % | 245.4411 | 19.23 % | 36.72 % | 47.63 % | 59.01 % | 71.94 % | 81.61 % |
| 1.0 ATR | 3.984 % | 242.9214 | 9.96 % | 24.58 % | 34.68 % | 47.72 % | 62.59 % | 74.47 % |
| 1.25 ATR | 4.98 % | 240.4018 | 4.83 % | 15.0 % | 24.6 % | 38.32 % | 52.94 % | 67.24 % |
| 1.5 ATR | 5.975 % | 237.8821 | 2.27 % | 10.07 % | 17.79 % | 30.79 % | 45.57 % | 61.21 % |
| 2.0 ATR | 7.967 % | 232.8429 | 0.69 % | 4.54 % | 8.1 % | 17.03 % | 34.23 % | 51.36 % |
| 2.5 ATR | 9.959 % | 227.8036 | 0.3 % | 1.97 % | 4.74 % | 10.59 % | 23.88 % | 41.21 % |
| 3.0 ATR | 11.951 % | 222.7643 | 0.2 % | 1.48 % | 2.96 % | 6.34 % | 17.11 % | 33.87 % |
| 4.0 ATR | 15.934 % | 212.6857 | 0.0 % | 0.69 % | 1.78 % | 3.56 % | 8.76 % | 19.9 % |
| 6.0 ATR | 23.902 % | 192.5286 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.67 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.51 ATR | 1.96 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.24 ATR | 1.42 ATR | 1.90 ATR | 2.46 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.71 ATR | 1.89 ATR | 2.57 ATR | 3.48 ATR |
| **10 s.** | 0.68 ATR | 1.35 ATR | 1.52 ATR | 2.06 ATR | 2.45 ATR | 2.79 ATR | 3.85 ATR | 5.13 ATR |
| **20 s.** | 0.98 ATR | 2.07 ATR | 2.31 ATR | 3.06 ATR | 3.63 ATR | 3.99 ATR | 5.54 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.992 %, prix 247.9602), p(touche) 38.26 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.645–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.988 %, prix 245.4404), p(touche) 36.72 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.801–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.984 %, prix 242.9205), p(touche) 34.68 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.072–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.98 %, prix 240.4006), p(touche) 38.32 % (en stress 94.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.525–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.967 %, prix 232.8435), p(touche) 34.23 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.313–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.959 %, prix 227.8037), p(touche) 41.21 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.05 | EV/share : €0.514 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 2 % | T3 0 %
- Kelly (position) : f* 0.055 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 13.7 | bear 31.3 | side 55.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 506.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.051% → cible +2.034% / stop −2.5%, p_fill 36%, n_eff≈39.9) : P(cible|rempli) **30%** · **EV/risk +0.066** (×p_fill ; si rempli +0.46% du capital)
  - **swing** (entrée dip −4.509% → cible +8.569% / stop −4.285%, p_fill 13%, n_eff≈16.5) : P(cible|rempli) **11%** · **EV/risk +0.016** (×p_fill ; si rempli +0.53% du capital)
  - **deep** (entrée dip −6.975% → cible +11.44% / stop −6.423%, p_fill 12%, n_eff≈14.7) : P(cible|rempli) **6%** · **EV/risk +0.021** (×p_fill ; si rempli +1.14% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→72% · +2.0%→44% · +3.0%→23% · +5.0%→7% · +8.0%→0%
- Range intraday médian 3.33% (p90 6.12%) · excursion haute méd. +1.77% / basse méd. −1.47%
- Profil de vol intra : ouverture 1.936% vs midi 0.828% vs clôture 0.957% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.047)_ ; drift intra méd. 0.284% ; recovery-V 26%
- **σ réalisé intraday** 2.228% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 61% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 252.4856 (VA 251.8969–253.2706 ; dernier close 252.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 46% · rebond 59% · **stop −1.74%** sous le fill (sous le bruit) · cible +1.24% · R/R 0.71 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 58% (gap-down >1% 6% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.26% (p90 −1.61%) · haut méd +0.6% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.3% (p90 −1.79%) · haut méd +0.78% · range méd 1.34%
- Excursion ouverture 30min (n=160) : bas méd −0.43% (p90 −1.9%) · haut méd +0.86% · range méd 1.52%
- Excursion ouverture 60min (n=160) : bas méd −0.49% (p90 −2.03%) · haut méd +0.91% · range méd 1.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 251.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 80% (123/159) · gap 25% · délai 0.5min · rebond 51% (67/123) (MFE +1.04%)
   - −1.0% : fill 30min 39% · séance 67% (103/159) · gap 6% · délai 7.9min · rebond 58% (60/103) (MFE +1.2%)
   - −1.5% : fill 30min 22% · séance 46% (78/159) · gap 2% · délai 38.9min · rebond 59% (45/78) (MFE +1.24%)
   - −2.0% : fill 30min 7% · séance 32% (57/159) · gap 0% · délai 236.0min · rebond 50% (29/57) (MFE +1.06%)
   - −3.0% : fill 30min 2% · séance 10% (26/159) · gap 0% · délai 183.5min · rebond 50% (12/26) (MFE +0.88%)
   - −4.0% : fill 30min 1% · séance 5% (13/159) · gap 0% · délai 55.4min · rebond 62% (8/13) (MFE +1.73%)
   - −5.0% : fill 30min 0% · séance 3% (7/159) · gap 0% · délai 141.9min · rebond 84% (6/7) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −1.59%) → stop au-delà de −1.0% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.07% (p90 −1.59%) → stop au-delà de −1.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.15% (p90 −1.99%) → stop au-delà de −1.15% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=442 jambes) : jambe baissière méd −1.02% (p90 −2.22%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 78% (49/61) · rebond 61% (30/49)
      · −2.0% : fill 37% (27/61) · rebond 47% (14/27)
      · −3.0% : fill 13% (15/61) · rebond 34% (7/15)
      · −4.0% : fill 6% (8/61) · rebond 60% (6/8)
      · −5.0% : fill 3% (4/61) · rebond 100% (4/4)
   - **flat** (40 séances) :
      · −1.0% : fill 61% (25/40) · rebond 53% (12/25)
      · −2.0% : fill 34% (16/40) · rebond 49% (7/16)
      · −3.0% : fill 6% (5/40) · rebond 34% (1/5)
      · −4.0% : fill 2% (2/40) · rebond 0% (0/2)
      · −5.0% : fill 2% (1/40) · rebond 0% (0/1)
   - **gap-up** (58 séances) :
      · −1.0% : fill 56% (29/58) · rebond 57% (18/29)
      · −2.0% : fill 22% (14/58) · rebond 59% (8/14)
      · −3.0% : fill 9% (6/58) · rebond 88% (4/6)
      · −4.0% : fill 6% (3/58) · rebond 89% (2/3)
      · −5.0% : fill 5% (2/58) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 56% si les 15 1res min sont vertes (88 cas) · 42% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 67% si début vert vs 27% si rouge (base 50% · écart 40 pts) ; prédictivité sature ensuite (plafond brut 235min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **67%** · continue >prix actuel 50% ; creux résiduel méd -1.2% (q20 -2.49%) → **SL/trailing à −2.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.95% / q75 +1.97% → **scale +0.95% / runner +1.97%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **27%** (continue à baisser 50%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.65%** (au-delà de la MAE q10 -2.65%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.07% .. +2.01%] · haut q95 +2.53% · bas q05 -2.81%
   - 60min (n=160) : retour [-2.27% .. +2.33%] · haut q95 +2.72% · bas q05 -2.84%
   - 2h (n=160) : retour [-2.12% .. +2.25%] · haut q95 +2.93% · bas q05 -2.95%
   - 4h (n=160) : retour [-2.23% .. +2.43%] · haut q95 +3.11% · bas q05 -3.15%
   - 6h (n=160) : retour [-2.48% .. +2.87%] · haut q95 +3.58% · bas q05 -3.16%
   - session (n=160) : retour [-3.0% .. +4.36%] · haut q95 +5.16% · bas q05 -3.82%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.18 · part idiosyncratique 0.82
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.1  _(neutre)_
- **ADX** : 23.8  _(pas de tendance nette)_
- **MACD** : hist -0.829  _(pas de croisement recent)_
- **BB** : %B 0.53 · largeur 14.2%
- **ATR** : 10.08 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.011  _(neutre)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 61.6  _(transition)_
- **MA** : MA20 251.96 · MA50 243.92 · MA200 233.69  _(prix > MA20)_
- **Dist MA** : MA20 +0.4% · MA50 +3.7% · MA200 +8.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (943698 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
