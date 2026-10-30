# SOI

**Generated** : 2026-10-30T01:12:11.182404+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · €133.80  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (4 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €133.80 (+1.1% vs entrée) · entrée €132.35 · stop €129.04 · T1 €136.04 · R/R 1.11  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-29 : 133.8 · ATR Wilder 9.24 (6.91 %)_
- **Swing** : plage **120.01 → 112.74** (-10.3 % a -15.74 % sous la cloture, 0.79 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 119.6-123.3 (B) ; 114.3-118.7 (B) ; 109.55-114.1 (A). stop INDICATIF 100.18 (-11.14 % sous le bas ; sous le support 104.8-109.4 (- 0,5 ATR)).
- **Deep** : plage **112.74 → 83.04** (-15.74 % a -37.93 % sous la cloture, 3.21 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 109.55-114.1 (A) ; 104.8-109.4 (A) ; 97.95-102.4 (B) ; 91.65-96.02 (A) ; 84.75-89.15 (B). stop INDICATIF 73.23 (-11.82 % sous le bas ; sous le support 77.85-82.4 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.3 ATR sous le plus haut 20 s., RSI(2) 95.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 125.2-128.0 (B, -4.33 %) ; 119.6-123.3 (B, -7.85 %) ; 114.3-118.7 (B, -11.29 %) ; 109.55-114.1 (A, -14.72 %) ; 104.8-109.4 (A, -18.24 %) ; 97.95-102.4 (B, -23.47 %)
- Resistances reelles au-dessus : 137.5-140.8 (A, 2.77 %) ; 142.9-146.0 (A, 6.8 %) ; 148.6-152.0 (A, 11.06 %) ; 154.8-159.4 (A, 15.7 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.14 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.05 %)** : le gap seul le franchit 0.391 % des séances (5 fois sur 1280).
   - exécution **7.306 pt plus bas** dans le cas TYPIQUE (médiane), 16.014 au p90, **20.244 au pire**
   - perte réelle **16.593 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 9.05 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0295 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.737 % | p01 -5.344 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4634** [0.3902 ; 0.5378] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4534** [0.4015 ; 0.5061] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4195** [0.3683 ; 0.472] _(largeur 10.4 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.64 %** | CVaR **-13.34 %** | vol 6.3 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.05 % contre 6.66 % aujourd'hui, rapport 0.46)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.89 % vs -11.79 % si l'on extrapolait par √5 _(rapport 1.093 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0801** (β de hausse 1.5829, asymétrie 0.6823) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.174× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 123.8459 sur support (0.65 ATR, 7.44 %) — p(stop avant cible) 0.568 [0.52 ; 0.62], R/R 3.247, perte reelle 7.824 % (gap inclus), CVaR 11.593 %, EV 1.5633 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5115 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.568, borne haute 0.620 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 11.59 % > budget 8.37 %
- Budget de queue : **8.37 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.202 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 19.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.65 ATR (stop 7.44 %) — p(stop avant cible) 0.568 [0.52 ; 0.62], R/R 3.247, perte reelle 7.824 % (gap inclus), EV 1.5633 % — **REFUSE**
      - refuse : p_stop_first 0.568, borne haute 0.620 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 11.59 % > budget 8.37 %
      - ⚠ support DETECTE a 0.65 ATR du spot — compartiment <1, mesure a 48.9 % de casse (IC clusterise [0.458 ; 0.522] sur 1149 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 9.994 %) — p(stop avant cible) 0.4668 [0.41 ; 0.52], R/R 2.453, perte reelle 10.356 % (gap inclus), EV 1.5973 % — **REFUSE**
      - refuse : R/R 2.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.31 % > budget 8.37 %
   - 🟢 support a 1.88 ATR (stop 15.661 %) — p(stop avant cible) 0.2799 [0.23 ; 0.33], R/R 1.579, perte reelle 16.085 % (gap inclus), EV 1.7936 % — **REFUSE**
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.03 % > budget 8.37 %
   - ⚪ swing_based a 2.92 ATR (stop 22.561 %) — p(stop avant cible) 0.1278 [0.10 ; 0.17], R/R 1.109, perte reelle 22.915 % (gap inclus), EV 2.3645 % — **REFUSE**
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.47 % > budget 8.37 %
   - 🟢 support a 3.17 ATR (stop 24.256 %) — p(stop avant cible) 0.0913 [0.06 ; 0.13], R/R 1.034, perte reelle 24.558 % (gap inclus), EV 2.425 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.81 % > budget 8.37 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.666 %) — p(stop avant cible) 0.8722 [0.83 ; 0.90], R/R 14.394, perte reelle 1.765 % (gap inclus), EV 0.7827 % — **REFUSE**
      - refuse : cible atteinte seulement 6.1 % du temps (< 15 %) meme a 10 seances : le R/R de 14.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.872, borne haute 0.904 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 grid_snapped a 0.65 ATR (stop 6.334 %) — p(stop avant cible) 0.6018 [0.55 ; 0.65], R/R 3.721, perte reelle 6.828 % (gap inclus), EV 1.9195 % — **REFUSE**
      - refuse : p_stop_first 0.602, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 11.49 % > budget 8.37 %
   - ⚪ atr_grid a 1.25 ATR (stop 8.328 %) — p(stop avant cible) 0.5347 [0.48 ; 0.59], R/R 2.923, perte reelle 8.693 % (gap inclus), EV 1.4148 % — **REFUSE**
      - refuse : p_stop_first 0.535, borne haute 0.587 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.03 % > budget 8.37 %
   - 🟢 grid_snapped a 1.88 ATR (stop 14.555 %) — p(stop avant cible) 0.3242 [0.28 ; 0.37], R/R 1.686, perte reelle 15.069 % (gap inclus), EV 1.3724 % — **REFUSE**
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.64 % > budget 8.37 %
   - ⚪ atr_grid a 2.5 ATR (stop 16.656 %) — p(stop avant cible) 0.2519 [0.21 ; 0.30], R/R 1.489, perte reelle 17.059 % (gap inclus), EV 2.0509 % — **REFUSE**
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.69 % > budget 8.37 %
   - ⚪ grid_snapped a 2.92 ATR (stop 21.455 %) — p(stop avant cible) 0.1406 [0.11 ; 0.18], R/R 1.164, perte reelle 21.835 % (gap inclus), EV 2.3672 % — **REFUSE**
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.52 % > budget 8.37 %
   - ⚪ atr_grid a 4.0 ATR (stop 26.65 %) — p(stop avant cible) 0.0675 [0.04 ; 0.10], R/R 0.943, perte reelle 26.944 % (gap inclus), EV 2.36 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.05 % > budget 8.37 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.981 %) — p(stop avant cible) 0.0313 [0.02 ; 0.05], R/R 0.844, perte reelle 30.106 % (gap inclus), EV 2.3552 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.64 % > budget 8.37 %
   - ⚪ atr_grid a 5.0 ATR (stop 33.312 %) — p(stop avant cible) 0.0257 [0.01 ; 0.05], R/R 0.763, perte reelle 33.312 % (gap inclus), EV 2.2703 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.29 % > budget 8.37 %
   - ⚪ atr_grid a 5.5 ATR (stop 36.643 %) — p(stop avant cible) 0.0146 [0.01 ; 0.03], R/R 0.691, perte reelle 36.771 % (gap inclus), EV 2.2876 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.07 % > budget 8.37 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.974 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.633, perte reelle 40.118 % (gap inclus), EV 2.3035 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.71 % > budget 8.37 %
   - ⚪ atr_grid a 6.5 ATR (stop 43.306 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.587, perte reelle 43.306 % (gap inclus), EV 2.3531 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.74 % > budget 8.37 %
   - ⚪ atr_grid a 7.0 ATR (stop 46.637 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.545, perte reelle 46.637 % (gap inclus), EV 2.3531 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.74 % > budget 8.37 %
   - ⚪ atr_grid a 7.5 ATR (stop 49.968 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.508, perte reelle 49.968 % (gap inclus), EV 2.3531 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.74 % > budget 8.37 %
   - ⚪ atr_grid a 8.0 ATR (stop 53.299 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.477, perte reelle 53.299 % (gap inclus), EV 2.3531 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.74 % > budget 8.37 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 133.8, ATR14 8.9143 (6.662 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 2.385 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.333 % | 133.3543 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.666 % | 132.9086 | 84.8 % | 89.89 % | 91.75 % | 94.29 % | 96.04 % | 97.2 % |
| 0.15 ATR | 0.999 % | 132.4629 | 77.84 % | 84.89 % | 87.52 % | 90.85 % | 93.57 % | 95.1 % |
| 0.2 ATR | 1.332 % | 132.0171 | 69.02 % | 79.59 % | 83.4 % | 87.7 % | 91.2 % | 93.11 % |
| 0.25 ATR | 1.666 % | 131.5714 | 62.55 % | 75.76 % | 79.96 % | 85.93 % | 89.81 % | 92.51 % |
| 0.35 ATR | 2.332 % | 130.68 | 50.78 % | 67.32 % | 73.08 % | 80.81 % | 85.56 % | 89.91 % |
| 0.5 ATR | 3.331 % | 129.3429 | 36.08 % | 55.54 % | 62.77 % | 73.03 % | 80.71 % | 87.01 % |
| 0.75 ATR | 4.997 % | 127.1143 | 16.86 % | 35.23 % | 46.56 % | 58.17 % | 72.21 % | 80.22 % |
| 1.0 ATR | 6.662 % | 124.8857 | 8.04 % | 23.55 % | 34.09 % | 47.34 % | 64.09 % | 74.83 % |
| 1.25 ATR | 8.328 % | 122.6571 | 4.02 % | 15.7 % | 25.34 % | 37.6 % | 56.48 % | 69.73 % |
| 1.5 ATR | 9.994 % | 120.4286 | 2.16 % | 10.6 % | 18.47 % | 30.02 % | 48.57 % | 63.44 % |
| 2.0 ATR | 13.325 % | 115.9714 | 0.59 % | 4.51 % | 9.14 % | 18.21 % | 35.11 % | 52.85 % |
| 2.5 ATR | 16.656 % | 111.5143 | 0.29 % | 2.45 % | 5.01 % | 11.91 % | 24.43 % | 45.05 % |
| 3.0 ATR | 19.987 % | 107.0572 | 0.2 % | 0.79 % | 2.55 % | 7.28 % | 17.21 % | 36.96 % |
| 4.0 ATR | 26.65 % | 98.1429 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 10.19 % | 23.38 % |
| 6.0 ATR | 39.974 % | 80.3143 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 11.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.19 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.63 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.55 ATR | 1.96 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.78 ATR | 1.03 ATR | 1.26 ATR | 1.44 ATR | 1.95 ATR | 2.50 ATR |
| **5 s.** | 0.46 ATR | 0.94 ATR | 1.06 ATR | 1.40 ATR | 1.71 ATR | 1.92 ATR | 2.71 ATR | 3.61 ATR |
| **10 s.** | 0.67 ATR | 1.46 ATR | 1.63 ATR | 2.10 ATR | 2.47 ATR | 2.81 ATR | 4.07 ATR | 5.81 ATR |
| **20 s.** | 0.99 ATR | 2.18 ATR | 2.50 ATR | 3.29 ATR | 3.88 ATR | 4.59 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (63.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.63–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.997 %, prix 127.114), p(touche) 35.23 % (en stress 82.35 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.781–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.662 %, prix 124.8862), p(touche) 34.09 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.06–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.328 %, prix 122.6571), p(touche) 37.6 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.633–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.503–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.006 | EV/share : €-0.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 59.2 | bear 5.3 | side 35.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 134.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.087% → cible +2.789% / stop −2.5%, p_fill 80%, n_eff≈85.4) : P(cible|rempli) **34%** · **EV/risk -0.179** (×p_fill ; si rempli -0.56% du capital)
  - **swing** (entrée dip −2.388% → cible +13.206% / stop −6.825%, p_fill 66%, n_eff≈76.5) : P(cible|rempli) **16%** · **EV/risk -0.205** (×p_fill ; si rempli -2.12% du capital)
  - **deep** (entrée dip −3.687% → cible +14.735% / stop −10.376%, p_fill 68%, n_eff≈78.0) : P(cible|rempli) **29%** · **EV/risk -0.163** (×p_fill ; si rempli -2.51% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 33.1  _(momentum baissier)_
- **ADX** : 25.2  _(tendance etablie)_
- **MACD** : hist -1.569  _(pas de croisement recent)_
- **BB** : %B 0.43 · largeur 55.4%
- **ATR** : 8.91 (55.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.098  _(distribution)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 34.4  _(marche directionnel)_
- **MA** : MA20 138.93 · MA50 135.17 · MA200 103.45  _(prix < MA20)_
- **Dist MA** : MA20 -3.7% · MA50 -1.0% · MA200 +29.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (802991 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
