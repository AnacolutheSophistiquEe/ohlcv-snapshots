# SOI

**Generated** : 2026-10-30T21:49:53.015198+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €120.25  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (5 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €120.25 (+1.0% vs entrée) · entrée €119.06 · stop €109.64 · T1 €135.99 · R/R 1.8  
> ↳ ¼-Kelly 0.031 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -52 % hors [0,100] (R² max 0.47). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-30 : 120.25 · ATR Wilder 9.55 (7.95 %)_
- **Swing** : plage **105.99 → 98.47** (-11.86 % a -18.11 % sous la cloture, 0.79 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 104.8-109.55 (A) ; 97.95-102.4 (B). stop INDICATIF 86.87 (-11.78 % sous le bas ; sous le support 91.65-96.02 (- 0,5 ATR)).
- **Deep** : plage **98.47 → 67.76** (-18.11 % a -43.65 % sous la cloture, 3.21 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 97.95-102.4 (B) ; 91.65-96.02 (A) ; 84.75-89.15 (B) ; 77.85-82.4 (A) ; 72.55-72.9 (C) ; 64.2-68.5 (B). stop INDICATIF 54.16 (-20.07 % sous le bas ; sous le support 58.94-63.5 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.57 ATR sous le plus haut 20 s., RSI(2) 32.2. Limite **115.47** (seance suivante), stop catastrophe 77.25, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 110.4-114.9 (B, -4.45 %) ; 104.8-109.55 (A, -8.9 %) ; 97.95-102.4 (B, -14.84 %) ; 91.65-96.02 (A, -20.15 %) ; 84.75-89.15 (B, -25.86 %) ; 77.85-82.4 (A, -31.48 %)
- Resistances reelles au-dessus : 126.65-128.0 (A, 5.32 %) ; 132.0-136.1 (A, 9.77 %) ; 137.5-140.8 (A, 14.35 %) ; 142.9-146.0 (A, 18.84 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.22 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.83 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **4.055 pt plus bas** dans le cas TYPIQUE (médiane), 15.176 au p90, **20.464 au pire**
   - perte réelle **15.318 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 8.83 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0304 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.767 % | p01 -5.347 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4412** [0.3687 ; 0.5156] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4056** [0.3548 ; 0.458] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3853** [0.3351 ; 0.4374] _(largeur 10.2 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.66 %** | CVaR **-13.47 %** | vol 6.33 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 2.93 % contre 6.71 % aujourd'hui, rapport 0.44)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.89 % vs -11.97 % si l'on extrapolait par √5 _(rapport 1.077 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0593** (β de hausse 1.5901, asymétrie 0.6662) vs FCHI — 621 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.081× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 114.2866 sur support (0.34 ATR, 4.959 %) — p(stop avant cible) 0.6633 [0.61 ; 0.71], R/R 5.706, perte reelle 5.365 % (gap inclus), CVaR 9.658 %, EV 2.2162 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9582 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.663, borne haute 0.712 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 9.66 % > budget 6.73 %
- Budget de queue : **6.73 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.164 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 20.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.34 ATR (stop 4.959 %) — p(stop avant cible) 0.6633 [0.61 ; 0.71], R/R 5.706, perte reelle 5.365 % (gap inclus), EV 2.2162 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.663, borne haute 0.712 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 9.66 % > budget 6.73 %
      - ⚠ support DETECTE a 0.18 ATR du spot — compartiment <1, mesure a 47.3 % de casse (IC clusterise [0.442 ; 0.505] sur 1151 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 1.57 ATR (stop 14.523 %) — p(stop avant cible) 0.3306 [0.28 ; 0.38], R/R 2.036, perte reelle 15.031 % (gap inclus), EV 1.8442 % — **REFUSE**
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.63 % > budget 6.73 %
   - 🟢 support a 4.1 ATR (stop 34.348 %) — p(stop avant cible) 0.0213 [0.01 ; 0.04], R/R 0.89, perte reelle 34.407 % (gap inclus), EV 2.8745 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.01 % > budget 6.73 %
   - ⚪ atr_grid a 1.0 ATR (stop 7.835 %) — p(stop avant cible) 0.5557 [0.50 ; 0.61], R/R 3.723, perte reelle 8.223 % (gap inclus), EV 1.8162 % — **REFUSE**
      - refuse : cible atteinte seulement 13.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.556, borne haute 0.607 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 11.87 % > budget 6.73 %
   - ⚪ atr_grid a 1.25 ATR (stop 9.794 %) — p(stop avant cible) 0.4755 [0.42 ; 0.53], R/R 3.015, perte reelle 10.153 % (gap inclus), EV 2.0109 % — **REFUSE**
      - refuse : cible atteinte seulement 14.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.17 % > budget 6.73 %
   - ⚪ atr_grid a 2.0 ATR (stop 15.67 %) — p(stop avant cible) 0.284 [0.24 ; 0.33], R/R 1.903, perte reelle 16.083 % (gap inclus), EV 2.2947 % — **REFUSE**
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.02 % > budget 6.73 %
   - ⚪ atr_grid a 2.25 ATR (stop 17.628 %) — p(stop avant cible) 0.2292 [0.19 ; 0.28], R/R 1.694, perte reelle 18.073 % (gap inclus), EV 2.7353 % — **REFUSE**
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.67 % > budget 6.73 %
   - ⚪ atr_grid a 2.5 ATR (stop 19.587 %) — p(stop avant cible) 0.194 [0.15 ; 0.24], R/R 1.528, perte reelle 20.037 % (gap inclus), EV 2.8829 % — **REFUSE**
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.33 % > budget 6.73 %
   - ⚪ atr_grid a 2.75 ATR (stop 21.546 %) — p(stop avant cible) 0.1391 [0.11 ; 0.18], R/R 1.397, perte reelle 21.919 % (gap inclus), EV 2.951 % — **REFUSE**
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.58 % > budget 6.73 %
   - ⚪ atr_grid a 3.0 ATR (stop 23.505 %) — p(stop avant cible) 0.11 [0.08 ; 0.15], R/R 1.284, perte reelle 23.833 % (gap inclus), EV 2.9797 % — **REFUSE**
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.23 % > budget 6.73 %
   - ⚪ atr_grid a 3.5 ATR (stop 27.422 %) — p(stop avant cible) 0.056 [0.04 ; 0.08], R/R 1.106, perte reelle 27.672 % (gap inclus), EV 2.9297 % — **REFUSE**
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.70 % > budget 6.73 %
   - ⚪ atr_grid a 5.0 ATR (stop 39.174 %) — p(stop avant cible) 0.0089 [0.00 ; 0.02], R/R 0.781, perte reelle 39.174 % (gap inclus), EV 2.8845 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.77 % > budget 6.73 %
   - ⚪ atr_grid a 5.5 ATR (stop 43.092 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.71, perte reelle 43.092 % (gap inclus), EV 2.9385 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.71 % > budget 6.73 %
   - ⚪ atr_grid a 6.0 ATR (stop 47.009 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.651, perte reelle 47.009 % (gap inclus), EV 2.9385 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.71 % > budget 6.73 %
   - ⚪ atr_grid a 6.5 ATR (stop 50.927 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.601, perte reelle 50.927 % (gap inclus), EV 2.9385 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.71 % > budget 6.73 %
   - ⚪ atr_grid a 7.0 ATR (stop 54.844 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.558, perte reelle 54.844 % (gap inclus), EV 2.9385 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.71 % > budget 6.73 %
   - ⚪ atr_grid a 7.5 ATR (stop 58.761 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.521, perte reelle 58.761 % (gap inclus), EV 2.9385 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.71 % > budget 6.73 %
   - ⚪ atr_grid a 8.0 ATR (stop 62.679 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.488, perte reelle 62.679 % (gap inclus), EV 2.9385 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.71 % > budget 6.73 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 120.25, ATR14 9.4214 (7.835 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.357 ATR = 2.797 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.392 % | 119.7789 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.783 % | 119.3079 | 84.71 % | 89.89 % | 91.75 % | 94.29 % | 96.04 % | 97.2 % |
| 0.15 ATR | 1.175 % | 118.8368 | 77.75 % | 84.89 % | 87.52 % | 90.85 % | 93.57 % | 95.1 % |
| 0.2 ATR | 1.567 % | 118.3657 | 68.92 % | 79.59 % | 83.4 % | 87.7 % | 91.2 % | 93.11 % |
| 0.25 ATR | 1.959 % | 117.8946 | 62.45 % | 75.76 % | 79.96 % | 85.93 % | 89.81 % | 92.51 % |
| 0.35 ATR | 2.742 % | 116.9525 | 50.69 % | 67.32 % | 72.99 % | 80.81 % | 85.56 % | 89.91 % |
| 0.5 ATR | 3.917 % | 115.5393 | 35.98 % | 55.54 % | 62.67 % | 73.03 % | 80.71 % | 87.01 % |
| 0.75 ATR | 5.876 % | 113.1839 | 16.86 % | 35.23 % | 46.46 % | 58.07 % | 72.21 % | 80.22 % |
| 1.0 ATR | 7.835 % | 110.8286 | 8.04 % | 23.55 % | 33.99 % | 47.24 % | 64.09 % | 74.83 % |
| 1.25 ATR | 9.794 % | 108.4732 | 4.02 % | 15.7 % | 25.25 % | 37.5 % | 56.48 % | 69.73 % |
| 1.5 ATR | 11.752 % | 106.1179 | 2.16 % | 10.6 % | 18.47 % | 30.02 % | 48.66 % | 63.54 % |
| 2.0 ATR | 15.67 % | 101.4071 | 0.59 % | 4.51 % | 9.14 % | 18.21 % | 35.21 % | 52.95 % |
| 2.5 ATR | 19.587 % | 96.6964 | 0.29 % | 2.45 % | 5.01 % | 11.91 % | 24.43 % | 45.15 % |
| 3.0 ATR | 23.505 % | 91.9857 | 0.2 % | 0.79 % | 2.55 % | 7.28 % | 17.21 % | 37.06 % |
| 4.0 ATR | 31.339 % | 82.5643 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 10.19 % | 23.48 % |
| 6.0 ATR | 47.009 % | 63.7214 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 11.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.19 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.63 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.55 ATR | 1.96 ATR |
| **3 s.** | 0.32 ATR | 0.69 ATR | 0.78 ATR | 1.03 ATR | 1.26 ATR | 1.44 ATR | 1.95 ATR | 2.50 ATR |
| **5 s.** | 0.46 ATR | 0.94 ATR | 1.06 ATR | 1.40 ATR | 1.71 ATR | 1.92 ATR | 2.71 ATR | 3.61 ATR |
| **10 s.** | 0.67 ATR | 1.46 ATR | 1.64 ATR | 2.10 ATR | 2.47 ATR | 2.81 ATR | 4.07 ATR | 5.81 ATR |
| **20 s.** | 0.99 ATR | 2.19 ATR | 2.51 ATR | 3.30 ATR | 3.89 ATR | 4.61 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.408–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (63.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.63–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.779–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.835 %, prix 110.8284), p(touche) 33.99 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.057–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.636–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.509–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.188 | EV/share : €1.772 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 14 % | T3 9 %
- Kelly (position) : f* 0.125 | ¼-Kelly 0.031 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 12.0 | bear 5.0 | side 83.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 120.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.446% → cible +6.136% / stop −3.068%, p_fill 88%, n_eff≈94.2) : P(cible|rempli) **12%** · **EV/risk -0.231** (×p_fill ; si rempli -0.80% du capital)
  - **swing** (entrée dip −0.995% → cible +14.223% / stop −7.913%, p_fill 85%, n_eff≈99.9) : P(cible|rempli) **21%** · **EV/risk -0.144** (×p_fill ; si rempli -1.33% du capital)
  - **deep** (entrée dip −1.448% → cible +14.752% / stop −11.925%, p_fill 87%, n_eff≈98.3) : P(cible|rempli) **36%** · **EV/risk -0.104** (×p_fill ; si rempli -1.43% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→83% · +1.0%→74% · +2.0%→62% · +3.0%→46% · +5.0%→29% · +8.0%→10%
- Range intraday médian 7.0% (p90 13.76%) · excursion haute méd. +2.7% / basse méd. −3.24%
- Profil de vol intra : ouverture 4.423% vs midi 1.287% vs clôture 1.954% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑1%/↓1% ; spike-down 73% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.002)_ ; drift intra méd. -0.88% ; recovery-V 29%
- **σ réalisé intraday** 3.81% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 78% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 111.4765 (VA 109.8045–114.4025 ; dernier close 111.96)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 66% · **stop −6.95%** sous le fill (sous le bruit) · cible +2.1% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. 0.56% · baisse 40% (gap-down >1% 26% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.01% (p90 −3.1%) · haut méd +0.82% · range méd 2.14%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −3.34%) · haut méd +1.06% · range méd 2.95%
- Excursion ouverture 30min (n=160) : bas méd −1.56% (p90 −3.74%) · haut méd +1.13% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.76% (p90 −4.51%) · haut méd +1.44% · range méd 3.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 111.65 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 77% (120/159) · gap 33% · délai 0.2min · rebond 61% (78/120) (MFE +1.63%)
   - −1.0% : fill 30min 55% · séance 73% (114/159) · gap 26% · délai 0.2min · rebond 63% (76/114) (MFE +1.69%)
   - −1.5% : fill 30min 48% · séance 65% (104/159) · gap 21% · délai 1.3min · rebond 58% (72/104) (MFE +1.84%)
   - −2.0% : fill 30min 44% · séance 62% (98/159) · gap 18% · délai 4.5min · rebond 66% (72/98) (MFE +1.89%)
   - −3.0% : fill 30min 30% · séance 47% (80/159) · gap 9% · délai 8.9min · rebond 73% (66/80) (MFE +1.88%)
   - −4.0% : fill 30min 21% · séance 39% (68/159) · gap 6% · délai 15.4min · rebond 72% (54/68) (MFE +1.92%)
   - −5.0% : fill 30min 14% · séance 30% (53/159) · gap 3% · délai 38.9min · rebond 66% (39/53) (MFE +2.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −3.17%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −3.07%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.7% (p90 −2.29%) → stop au-delà de −1.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1324 jambes) : jambe baissière méd −1.26% (p90 −3.04%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (59 séances) :
      · −1.0% : fill 95% (56/59) · rebond 52% (33/56)
      · −2.0% : fill 93% (54/59) · rebond 60% (37/54)
      · −3.0% : fill 80% (49/59) · rebond 64% (38/49)
      · −4.0% : fill 68% (42/59) · rebond 70% (35/42)
      · −5.0% : fill 59% (35/59) · rebond 68% (27/35)
   - **flat** (11 séances) :
      · −1.0% : fill 83% (10/11) · rebond 66% (7/10)
      · −2.0% : fill 74% (9/11) · rebond 65% (7/9)
      · −3.0% : fill 74% (9/11) · rebond 73% (7/9)
      · −4.0% : fill 68% (8/11) · rebond 85% (6/8)
      · −5.0% : fill 55% (7/11) · rebond 63% (5/7)
   - **gap-up** (89 séances) :
      · −1.0% : fill 58% (48/89) · rebond 74% (36/48)
      · −2.0% : fill 40% (35/89) · rebond 74% (28/35)
      · −3.0% : fill 22% (22/89) · rebond 92% (21/22)
      · −4.0% : fill 16% (18/89) · rebond 72% (13/18)
      · −5.0% : fill 8% (11/89) · rebond 60% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 62% si les 15 1res min sont vertes (75 cas) · 31% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **10min** → P(séance verte=clôture>ouverture) 63% si début vert vs 28% si rouge (base 44% · écart 34 pts) ; prédictivité sature ensuite (plafond brut 284min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **63%** · continue >prix actuel 51% ; creux résiduel méd -2.33% (q20 -4.61%) → **SL/trailing à −4.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.95% / q75 +5.39% → **scale +2.95% / runner +5.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **28%** (continue à baisser 61%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.99%** (au-delà de la MAE q10 -6.99%), cible rebond +2.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.33% .. +4.1%] · haut q95 +5.94% · bas q05 -5.72%
   - 60min (n=160) : retour [-4.39% .. +4.55%] · haut q95 +6.48% · bas q05 -5.91%
   - 2h (n=160) : retour [-5.15% .. +5.34%] · haut q95 +7.16% · bas q05 -6.63%
   - 4h (n=160) : retour [-5.33% .. +6.48%] · haut q95 +7.84% · bas q05 -7.2%
   - 6h (n=160) : retour [-6.3% .. +7.83%] · haut q95 +8.85% · bas q05 -7.75%
   - session (n=160) : retour [-7.87% .. +8.67%] · haut q95 +10.28% · bas q05 -9.9%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **38%**. Lecture précoce 30 min : signature présente → 16% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.4% / p90 1.99%) · ~5.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **90%** (reprise méd 24.99 min, n=53)
   - −1.0% → **91%** (reprise méd 44.55 min, n=28)
   - −1.5% → **80%** (reprise méd 50.92 min, n=16)
   - −2.0% → **85%** (reprise méd 52.07 min, n=12)
   - −3.0% → **100%** (reprise méd 60.96 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.99%** (p90, défaut prudent ; serré/agressif −1.4%) ; extension open→close méd +8.74% (q75 +9.27% / q95 +13.89%), MFE méd +9.37% / q90 +14.21%
   - Échelle scale-out : +9.37% (33%) / +10.06% (33%) / +14.21% (34%)
- **DÉSARMER** : repli > **−1.99%** depuis le plus-haut = décay → P(retournement) **15%** (préavis méd 36.46 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.21% : P(retournement après) 0% (mèche méd 2.71%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +1.29%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.54 · part idiosyncratique 0.46
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 29.6  _(survente)_
- **ADX** : 24.0  _(pas de tendance nette)_
- **MACD** : hist -1.455  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 53.2%
- **ATR** : 9.42 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.195  _(distribution)_
- **Vol ratio** : 1.06  _(volume normal)_
- **Choppiness** : 41.6  _(transition)_
- **MA** : MA20 136.37 · MA50 135.37 · MA200 103.91  _(prix < MA20)_
- **Dist MA** : MA20 -11.8% · MA50 -11.2% · MA200 +15.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (798115 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
