# SOI

**Generated** : 2026-10-28T01:11:52.247150+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · €122.55  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €122.55 (+0.8% vs entrée) · entrée €121.56 · stop €118.78 · T1 €127.07 · R/R 1.98  
> ↳ ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.29% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-27 : 122.55 · ATR Wilder 9.13 (7.45 %)_
- **Swing** : plage **108.93 → 101.99** (-11.11 % a -16.77 % sous la cloture, 0.76 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 104.8-109.2 (A) ; 97.95-102.4 (B). stop INDICATIF 87.08 (-14.62 % sous le bas ; sous le support 91.65-96.02 (- 0,5 ATR)).
- **Deep** : plage **101.99 → 72.38** (-16.77 % a -40.94 % sous la cloture, 3.24 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 97.95-102.4 (B) ; 91.65-96.02 (A) ; 84.75-89.15 (B) ; 77.85-82.4 (A) ; 68.5-72.9 (B). stop INDICATIF 58.93 (-18.58 % sous le bas ; sous le support 63.5-65.16 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.58 ATR sous le plus haut 20 s., RSI(2) 76.5. Limite **117.98** (seance suivante), stop catastrophe 81.45, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 114.1-118.5 (B, -3.3 %) ; 109.4-111.2 (B, -9.26 %) ; 104.8-109.2 (A, -10.89 %) ; 97.95-102.4 (B, -16.44 %) ; 91.65-96.02 (A, -21.65 %) ; 84.75-89.15 (B, -27.25 %)
- Resistances reelles au-dessus : 128.0-132.5 (A, 4.45 %) ; 132.6-136.1 (A, 8.2 %) ; 137.5-140.8 (A, 12.2 %) ; 142.9-146.0 (A, 16.61 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.14 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.34 %)** : le gap seul le franchit 0.312 % des séances (4 fois sur 1280).
   - exécution **8.198 pt plus bas** dans le cas TYPIQUE (médiane), 16.781 au p90, **19.954 au pire**
   - perte réelle **18.446 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 9.34 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0285 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.737 % | p01 -5.344 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5125** [0.4383 ; 0.5862] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4157** [0.3646 ; 0.4682] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3806** [0.3306 ; 0.4326] _(largeur 10.2 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.64 %** | CVaR **-13.34 %** | vol 6.3 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.12 % contre 6.66 % aujourd'hui, rapport 0.47)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.89 % vs -11.79 % si l'on extrapolait par √5 _(rapport 1.093 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0775** (β de hausse 1.5856, asymétrie 0.6795) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.158× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 114.2218 sur grid_snapped (0.6 ATR, 6.796 %) — p(stop avant cible) 0.5842 [0.53 ; 0.64], R/R 3.868, perte reelle 7.207 % (gap inclus), CVaR 11.289 %, EV 2.1438 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9916 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 14.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.584, borne haute 0.635 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 11.29 % > budget 6.34 %
- Budget de queue : **6.34 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.155 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 21.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.6 ATR (stop 7.831 %) — p(stop avant cible) 0.548 [0.50 ; 0.60], R/R 3.395, perte reelle 8.212 % (gap inclus), EV 1.7979 % — **REFUSE**
      - refuse : cible atteinte seulement 14.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.548, borne haute 0.600 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 11.80 % > budget 6.34 %
      - ⚠ support DETECTE a 0.43 ATR du spot — compartiment <1, mesure a 49.7 % de casse (IC clusterise [0.467 ; 0.529] sur 1189 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 11.335 %) — p(stop avant cible) 0.4104 [0.36 ; 0.46], R/R 2.366, perte reelle 11.782 % (gap inclus), EV 2.0563 % — **REFUSE**
      - refuse : R/R 2.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.98 % > budget 6.34 %
   - 🟢 support a 1.84 ATR (stop 17.215 %) — p(stop avant cible) 0.238 [0.20 ; 0.28], R/R 1.576, perte reelle 17.686 % (gap inclus), EV 2.4734 % — **REFUSE**
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.46 % > budget 6.34 %
   - 🟢 support a 4.42 ATR (stop 36.668 %) — p(stop avant cible) 0.0148 [0.01 ; 0.03], R/R 0.758, perte reelle 36.791 % (gap inclus), EV 2.7485 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.15 % > budget 6.34 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.889 %) — p(stop avant cible) 0.842 [0.80 ; 0.88], R/R 14.029, perte reelle 1.987 % (gap inclus), EV 1.3464 % — **REFUSE**
      - refuse : cible atteinte seulement 6.4 % du temps (< 15 %) meme a 10 seances : le R/R de 14.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.842, borne haute 0.877 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 grid_snapped a 0.6 ATR (stop 6.796 %) — p(stop avant cible) 0.5842 [0.53 ; 0.64], R/R 3.868, perte reelle 7.207 % (gap inclus), EV 2.1438 % — **REFUSE**
      - refuse : cible atteinte seulement 14.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.584, borne haute 0.635 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 11.29 % > budget 6.34 %
   - ⚪ atr_grid a 1.25 ATR (stop 9.446 %) — p(stop avant cible) 0.4784 [0.43 ; 0.53], R/R 2.844, perte reelle 9.801 % (gap inclus), EV 2.044 % — **REFUSE**
      - refuse : R/R 2.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.79 % > budget 6.34 %
   - 🟢 grid_snapped a 1.84 ATR (stop 16.18 %) — p(stop avant cible) 0.2578 [0.21 ; 0.31], R/R 1.681, perte reelle 16.581 % (gap inclus), EV 2.5288 % — **REFUSE**
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.25 % > budget 6.34 %
   - ⚪ atr_grid a 2.5 ATR (stop 18.892 %) — p(stop avant cible) 0.2017 [0.16 ; 0.25], R/R 1.436, perte reelle 19.41 % (gap inclus), EV 2.69 % — **REFUSE**
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.98 % > budget 6.34 %
   - ⚪ atr_grid a 2.75 ATR (stop 20.781 %) — p(stop avant cible) 0.14 [0.11 ; 0.18], R/R 1.311, perte reelle 21.262 % (gap inclus), EV 2.9156 % — **REFUSE**
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.13 % > budget 6.34 %
   - ⚪ atr_grid a 3.0 ATR (stop 22.67 %) — p(stop avant cible) 0.1235 [0.09 ; 0.16], R/R 1.211, perte reelle 23.024 % (gap inclus), EV 2.8459 % — **REFUSE**
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.54 % > budget 6.34 %
   - ⚪ atr_grid a 3.5 ATR (stop 26.448 %) — p(stop avant cible) 0.0741 [0.05 ; 0.11], R/R 1.043, perte reelle 26.739 % (gap inclus), EV 2.8043 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.88 % > budget 6.34 %
   - ⚪ atr_grid a 4.0 ATR (stop 30.227 %) — p(stop avant cible) 0.0317 [0.02 ; 0.05], R/R 0.919, perte reelle 30.33 % (gap inclus), EV 2.8101 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.83 % > budget 6.34 %
   - 🟢 grid_snapped a 4.42 ATR (stop 35.633 %) — p(stop avant cible) 0.0177 [0.01 ; 0.04], R/R 0.782, perte reelle 35.633 % (gap inclus), EV 2.755 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.01 % > budget 6.34 %
   - ⚪ atr_grid a 5.0 ATR (stop 37.783 %) — p(stop avant cible) 0.0123 [0.00 ; 0.03], R/R 0.735, perte reelle 37.922 % (gap inclus), EV 2.7574 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.98 % > budget 6.34 %
   - ⚪ atr_grid a 5.5 ATR (stop 41.562 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.671, perte reelle 41.562 % (gap inclus), EV 2.8035 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.06 % > budget 6.34 %
   - ⚪ atr_grid a 6.0 ATR (stop 45.34 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.615, perte reelle 45.34 % (gap inclus), EV 2.8164 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.79 % > budget 6.34 %
   - ⚪ atr_grid a 6.5 ATR (stop 49.118 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.568, perte reelle 49.118 % (gap inclus), EV 2.8164 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.79 % > budget 6.34 %
   - ⚪ atr_grid a 7.0 ATR (stop 52.897 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.527, perte reelle 52.897 % (gap inclus), EV 2.8164 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.79 % > budget 6.34 %
   - ⚪ atr_grid a 7.5 ATR (stop 56.675 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.492, perte reelle 56.675 % (gap inclus), EV 2.8164 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.79 % > budget 6.34 %
   - ⚪ atr_grid a 8.0 ATR (stop 60.453 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.461, perte reelle 60.453 % (gap inclus), EV 2.8164 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.79 % > budget 6.34 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 122.55, ATR14 9.2607 (7.557 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.359 ATR = 2.713 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.378 % | 122.087 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.756 % | 121.6239 | 84.8 % | 89.89 % | 91.75 % | 94.29 % | 96.04 % | 97.2 % |
| 0.15 ATR | 1.134 % | 121.1609 | 77.84 % | 84.99 % | 87.62 % | 90.85 % | 93.57 % | 95.1 % |
| 0.2 ATR | 1.511 % | 120.6979 | 69.02 % | 79.69 % | 83.5 % | 87.7 % | 91.2 % | 93.11 % |
| 0.25 ATR | 1.889 % | 120.2348 | 62.55 % | 75.86 % | 80.06 % | 85.93 % | 89.81 % | 92.51 % |
| 0.35 ATR | 2.645 % | 119.3088 | 50.88 % | 67.52 % | 73.18 % | 80.81 % | 85.56 % | 89.91 % |
| 0.5 ATR | 3.778 % | 117.9196 | 36.08 % | 55.64 % | 62.77 % | 73.03 % | 80.71 % | 87.01 % |
| 0.75 ATR | 5.668 % | 115.6045 | 16.96 % | 35.33 % | 46.66 % | 58.17 % | 72.21 % | 80.22 % |
| 1.0 ATR | 7.557 % | 113.2893 | 8.04 % | 23.55 % | 34.09 % | 47.34 % | 64.09 % | 74.83 % |
| 1.25 ATR | 9.446 % | 110.9741 | 4.02 % | 15.7 % | 25.34 % | 37.6 % | 56.38 % | 69.63 % |
| 1.5 ATR | 11.335 % | 108.6589 | 2.16 % | 10.6 % | 18.47 % | 29.92 % | 48.37 % | 63.24 % |
| 2.0 ATR | 15.113 % | 104.0286 | 0.59 % | 4.51 % | 9.14 % | 18.21 % | 34.92 % | 52.65 % |
| 2.5 ATR | 18.892 % | 99.3982 | 0.29 % | 2.45 % | 5.01 % | 11.91 % | 24.33 % | 44.86 % |
| 3.0 ATR | 22.67 % | 94.7679 | 0.2 % | 0.79 % | 2.55 % | 7.28 % | 17.11 % | 36.76 % |
| 4.0 ATR | 30.227 % | 85.5072 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 10.09 % | 23.18 % |
| 6.0 ATR | 45.34 % | 66.9857 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 11.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.94 ATR | 1.19 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.63 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.55 ATR | 1.96 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.78 ATR | 1.03 ATR | 1.26 ATR | 1.44 ATR | 1.95 ATR | 2.50 ATR |
| **5 s.** | 0.46 ATR | 0.94 ATR | 1.06 ATR | 1.40 ATR | 1.71 ATR | 1.92 ATR | 2.71 ATR | 3.61 ATR |
| **10 s.** | 0.67 ATR | 1.45 ATR | 1.62 ATR | 2.09 ATR | 2.47 ATR | 2.80 ATR | 4.03 ATR | 5.80 ATR |
| **20 s.** | 0.99 ATR | 2.17 ATR | 2.49 ATR | 3.28 ATR | 3.87 ATR | 4.57 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.41–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (63.8 % des re-echantillons)
- **2 seance(s)** : plage utile 0.631–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.783–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.557 %, prix 113.2889), p(touche) 34.09 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.06–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.625–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.491–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.008 | EV/share : €0.023 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 — | T3 —
- Kelly (position) : f* 0.01 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 54.8 | bear 29.8 | side 15.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 123.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.813% → cible +4.537% / stop −2.285%, p_fill 85%, n_eff≈90.3) : P(cible|rempli) **16%** · **EV/risk -0.246** (×p_fill ; si rempli -0.66% du capital)
  - **swing** (entrée dip −1.784% → cible +12.993% / stop −7.694%, p_fill 77%, n_eff≈90.3) : P(cible|rempli) **23%** · **EV/risk -0.122** (×p_fill ; si rempli -1.22% du capital)
  - **deep** (entrée dip −2.755% → cible +14.121% / stop −11.656%, p_fill 73%, n_eff≈83.7) : P(cible|rempli) **36%** · **EV/risk -0.115** (×p_fill ; si rempli -1.85% du capital)
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.54 · part idiosyncratique 0.46
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.0  _(survente)_
- **ADX** : 26.8  _(tendance etablie)_
- **MACD** : hist -3.819  _(pas de croisement recent)_
- **BB** : %B 0.25 · largeur 55.0%
- **ATR** : 9.26 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.145  _(distribution)_
- **Vol ratio** : 0.44  _(volume atone)_
- **Choppiness** : 30.8  _(marche directionnel)_
- **MA** : MA20 141.84 · MA50 134.43 · MA200 102.45  _(prix < MA20)_
- **Dist MA** : MA20 -13.6% · MA50 -8.8% · MA200 +19.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (784718 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
