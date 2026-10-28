# SMCI

**Generated** : 2026-10-28T01:24:23.685921+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $35.08  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $35.08 (+2.2% vs entrée) · entrée $34.34 · stop $33.55 · T1 $35.65 · R/R 1.66  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.29% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +5.5 % ≠ (strike 34.5 − spot 35.08)/spot = -1.7 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-27 : 35.08 · ATR Wilder 2.44 (6.96 %)_
- **Swing** : plage **32.08 → 30.25** (-8.57 % a -13.77 % sous la cloture, 0.75 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 31.11-32.04 (B) ; 29.85-31.03 (A). stop INDICATIF 27.28 (-9.81 % sous le bas ; sous le support 28.5-29.68 (- 0,5 ATR)).
- **Deep** : plage **30.25 → 24.68** (-13.77 % a -29.67 % sous la cloture, 2.29 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 29.85-31.03 (A) ; 28.5-29.68 (B) ; 26.86-27.75 (B) ; 25.46-26.06 (A) ; 24.19-25.41 (A). stop INDICATIF 21.44 (-13.12 % sous le bas ; sous le support 22.66-23.38 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.38 ATR sous le plus haut 20 s., RSI(2) 81.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 32.59-33.64 (B, -4.12 %) ; 31.11-32.04 (B, -8.68 %) ; 29.85-31.03 (A, -11.56 %) ; 28.5-29.68 (B, -15.41 %) ; 26.86-27.75 (B, -20.91 %) ; 25.46-26.06 (A, -25.72 %)
- Resistances reelles au-dessus : 36.8-37.85 (A, 4.89 %) ; 38.28-39.47 (A, 9.11 %) ; 39.52-40.13 (A, 12.64 %) ; 40.74-41.53 (A, 16.12 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.06 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.14 %)** : le gap seul le franchit 0.798 % des séances (10 fois sur 1253).
   - exécution **3.765 pt plus bas** dans le cas TYPIQUE (médiane), 14.939 au p90, **16.911 au pire**
   - perte réelle **18.539 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 12.14 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0511 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.818 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5028** [0.4288 ; 0.5767] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3764** [0.3265 ; 0.4283] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3281** [0.2802 ; 0.3789] _(largeur 9.9 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (26.6 pt), deep (27.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.39 %** | vol 5.86 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.83 % contre 6.21 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.54 % vs -16.84 % si l'on extrapolait par √5 _(rapport 1.041 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5343** (β de hausse 1.216, asymétrie 1.2618) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.849× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 34.4289 sur atr_grid (0.25 ATR, 1.87 %) — p(stop avant cible) 0.8943 [0.86 ; 0.92], R/R 9.617, perte reelle 2.124 % (gap inclus), CVaR 6.391 %, EV -0.0957 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.5816 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 9.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.894, borne haute 0.923 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 6.39 % > budget 4.58 %
- Budget de queue : **4.58 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.155 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 21.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.23 ATR (stop 12.486 %) — p(stop avant cible) 0.3119 [0.26 ; 0.36], R/R 1.448, perte reelle 14.112 % (gap inclus), EV 1.0155 % — **REFUSE**
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.40 % > budget 4.58 %
   - ⚪ swing_based a 1.79 ATR (stop 16.636 %) — p(stop avant cible) 0.2132 [0.17 ; 0.26], R/R 1.097, perte reelle 18.631 % (gap inclus), EV 1.0352 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.48 % > budget 4.58 %
   - 🟢 support a 2.81 ATR (stop 24.289 %) — p(stop avant cible) 0.1259 [0.09 ; 0.16], R/R 0.806, perte reelle 25.353 % (gap inclus), EV 0.9294 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.97 % > budget 4.58 %
   - 🟢 support a 3.69 ATR (stop 30.845 %) — p(stop avant cible) 0.0665 [0.04 ; 0.10], R/R 0.66, perte reelle 30.954 % (gap inclus), EV 0.7235 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.99 % > budget 4.58 %
   - 🟢 support a 4.46 ATR (stop 36.63 %) — p(stop avant cible) 0.0478 [0.03 ; 0.07], R/R 0.557, perte reelle 36.67 % (gap inclus), EV 0.5225 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.53 % > budget 4.58 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.87 %) — p(stop avant cible) 0.8943 [0.86 ; 0.92], R/R 9.617, perte reelle 2.124 % (gap inclus), EV -0.0957 % — **REFUSE**
      - refuse : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 9.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.894, borne haute 0.923 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.39 % > budget 4.58 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 7.4 % x 20.43 % + P(rien) 3.2 % x 9.25 % ne couvrent pas P(stop) 89.4 % x 2.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.74 %) — p(stop avant cible) 0.7615 [0.71 ; 0.80], R/R 4.825, perte reelle 4.235 % (gap inclus), EV 0.129 % — **REFUSE**
      - refuse : cible atteinte seulement 13.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.761, borne haute 0.804 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 10.82 % > budget 4.58 %
   - ⚪ atr_grid a 0.75 ATR (stop 5.61 %) — p(stop avant cible) 0.6607 [0.61 ; 0.71], R/R 3.217, perte reelle 6.351 % (gap inclus), EV 0.219 % — **REFUSE**
      - refuse : p_stop_first 0.661, borne haute 0.709 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 15.11 % > budget 4.58 %
   - ⚪ grid_snapped a 1.23 ATR (stop 11.462 %) — p(stop avant cible) 0.3572 [0.31 ; 0.41], R/R 1.569, perte reelle 13.018 % (gap inclus), EV 0.7735 % — **REFUSE**
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.18 % > budget 4.58 %
   - ⚪ grid_snapped a 1.79 ATR (stop 15.611 %) — p(stop avant cible) 0.2313 [0.19 ; 0.28], R/R 1.165, perte reelle 17.539 % (gap inclus), EV 0.9454 % — **REFUSE**
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.19 % > budget 4.58 %
   - ⚪ atr_grid a 2.5 ATR (stop 18.699 %) — p(stop avant cible) 0.1733 [0.14 ; 0.22], R/R 0.984, perte reelle 20.771 % (gap inclus), EV 1.1834 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.99 % > budget 4.58 %
   - 🟢 grid_snapped a 2.81 ATR (stop 23.264 %) — p(stop avant cible) 0.1413 [0.11 ; 0.18], R/R 0.835, perte reelle 24.479 % (gap inclus), EV 0.9072 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.70 % > budget 4.58 %
   - 🟢 grid_snapped a 3.69 ATR (stop 29.82 %) — p(stop avant cible) 0.069 [0.05 ; 0.10], R/R 0.681, perte reelle 29.983 % (gap inclus), EV 0.7812 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.05 % > budget 4.58 %
   - 🟢 grid_snapped a 4.46 ATR (stop 35.606 %) — p(stop avant cible) 0.0544 [0.03 ; 0.08], R/R 0.572, perte reelle 35.686 % (gap inclus), EV 0.5296 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.69 % > budget 4.58 %
   - ⚪ atr_grid a 5.5 ATR (stop 41.139 %) — p(stop avant cible) 0.0109 [0.00 ; 0.03], R/R 0.497, perte reelle 41.139 % (gap inclus), EV 0.7254 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.92 % > budget 4.58 %
   - ⚪ atr_grid a 6.0 ATR (stop 44.879 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 0.454, perte reelle 45.017 % (gap inclus), EV 0.7373 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.66 % > budget 4.58 %
   - ⚪ atr_grid a 6.5 ATR (stop 48.619 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.411, perte reelle 49.75 % (gap inclus), EV 0.7327 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.78 % > budget 4.58 %
   - ⚪ atr_grid a 7.0 ATR (stop 52.359 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.368, perte reelle 55.543 % (gap inclus), EV 0.7245 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.91 % > budget 4.58 %
   - ⚪ atr_grid a 7.5 ATR (stop 56.098 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.363, perte reelle 56.219 % (gap inclus), EV 0.7293 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.89 % > budget 4.58 %
   - ⚪ atr_grid a 8.0 ATR (stop 59.838 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.341, perte reelle 59.838 % (gap inclus), EV 0.7357 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.73 % > budget 4.58 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 35.085, ATR14 2.6243 (7.48 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 2.603 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.374 % | 34.9538 | 90.94 % | 93.75 % | 95.06 % | 95.55 % | 96.75 % | 97.95 % |
| 0.1 ATR | 0.748 % | 34.8226 | 82.38 % | 87.7 % | 89.61 % | 91.51 % | 93.29 % | 95.28 % |
| 0.15 ATR | 1.122 % | 34.6914 | 75.33 % | 82.66 % | 85.47 % | 88.68 % | 91.06 % | 94.05 % |
| 0.2 ATR | 1.496 % | 34.5601 | 68.38 % | 77.92 % | 81.13 % | 86.25 % | 89.63 % | 92.81 % |
| 0.25 ATR | 1.87 % | 34.4289 | 62.24 % | 73.29 % | 76.89 % | 82.91 % | 87.7 % | 91.27 % |
| 0.35 ATR | 2.618 % | 34.1665 | 49.75 % | 64.01 % | 70.33 % | 77.86 % | 83.54 % | 88.81 % |
| 0.5 ATR | 3.74 % | 33.7729 | 35.05 % | 50.4 % | 59.23 % | 69.46 % | 77.85 % | 84.39 % |
| 0.75 ATR | 5.61 % | 33.1168 | 17.42 % | 33.77 % | 43.69 % | 55.92 % | 67.28 % | 76.18 % |
| 1.0 ATR | 7.48 % | 32.4607 | 7.85 % | 21.88 % | 30.88 % | 44.29 % | 57.93 % | 69.51 % |
| 1.25 ATR | 9.35 % | 31.8046 | 3.73 % | 15.22 % | 22.7 % | 33.77 % | 48.68 % | 61.81 % |
| 1.5 ATR | 11.22 % | 31.1486 | 1.51 % | 9.68 % | 16.55 % | 26.39 % | 42.38 % | 55.44 % |
| 2.0 ATR | 14.96 % | 29.8364 | 0.3 % | 3.63 % | 8.68 % | 16.48 % | 30.49 % | 44.25 % |
| 2.5 ATR | 18.699 % | 28.5243 | 0.2 % | 1.51 % | 4.44 % | 10.01 % | 20.12 % | 32.34 % |
| 3.0 ATR | 22.439 % | 27.2121 | 0.2 % | 1.21 % | 2.62 % | 5.97 % | 14.63 % | 24.54 % |
| 4.0 ATR | 29.919 % | 24.5879 | 0.0 % | 0.6 % | 1.51 % | 2.83 % | 8.13 % | 14.68 % |
| 6.0 ATR | 44.879 % | 19.3393 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.51 ATR | 0.58 ATR | 0.77 ATR | 0.93 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.28 ATR | 0.65 ATR | 0.73 ATR | 0.96 ATR | 1.18 ATR | 1.36 ATR | 1.92 ATR | 2.43 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.98 ATR | 1.28 ATR | 1.57 ATR | 1.82 ATR | 2.50 ATR | 3.31 ATR |
| **10 s.** | 0.57 ATR | 1.21 ATR | 1.40 ATR | 1.89 ATR | 2.27 ATR | 2.51 ATR | 3.71 ATR | 5.03 ATR |
| **20 s.** | 0.79 ATR | 1.74 ATR | 1.97 ATR | 2.47 ATR | 2.97 ATR | 3.46 ATR | 5.02 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.581–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.61 %, prix 33.1167), p(touche) 33.77 % (en stress 88.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.729–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.61 %, prix 33.1167), p(touche) 43.69 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.985–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.35 %, prix 31.8046), p(touche) 33.77 % (en stress 90.91 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.396–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.22 %, prix 31.1485), p(touche) 42.38 % (en stress 96.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.966–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (18.699 %, prix 28.5245), p(touche) 32.34 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.011 | EV/share : $-0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 69.2 | bear 5.0 | side 25.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 158.0 (= 5 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.116% → cible +3.821% / stop −2.293%, p_fill 56%, n_eff≈59.1) : P(cible|rempli) **16%** · **EV/risk -0.132** (×p_fill ; si rempli -0.55% du capital)
  - **swing** (entrée dip −4.66% → cible +8.771% / stop −7.845%, p_fill 44%, n_eff≈50.7) : P(cible|rempli) **42%** · **EV/risk -0.001** (×p_fill ; si rempli -0.02% du capital)
  - **deep** (entrée dip −7.201% → cible +20.42% / stop −12.09%, p_fill 38%, n_eff≈44.6) : P(cible|rempli) **28%** · **EV/risk +0.052** (×p_fill ; si rempli +1.62% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→57% · +3.0%→40% · +5.0%→22% · +8.0%→8%
- Range intraday médian 5.72% (p90 9.37%) · excursion haute méd. +2.42% / basse méd. −2.68%
- Profil de vol intra : ouverture 3.884% vs midi 1.151% vs clôture 1.47% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.077)_ ; drift intra méd. -0.659% ; recovery-V 28%
- **σ réalisé intraday** 3.524% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 33.7346 (VA 33.3821–34.0871 ; dernier close 32.95)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 74% · **stop −4.61%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 50% (gap-down >1% 38% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.11% (p90 −2.79%) · haut méd +0.93% · range méd 2.16%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.55%) · haut méd +1.01% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.65% (p90 −3.98%) · haut méd +1.23% · range méd 3.58%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −4.46%) · haut méd +1.48% · range méd 4.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (116/159) · gap 42% · délai 0.0min · rebond 49% (64/116) (MFE +0.98%)
   - −1.0% : fill 30min 58% · séance 70% (109/159) · gap 38% · délai 0.0min · rebond 51% (60/109) (MFE +1.09%)
   - −1.5% : fill 30min 52% · séance 66% (100/159) · gap 28% · délai 0.0min · rebond 56% (62/100) (MFE +1.13%)
   - −2.0% : fill 30min 47% · séance 59% (87/159) · gap 23% · délai 0.1min · rebond 56% (54/87) (MFE +1.2%)
   - −3.0% : fill 30min 34% · séance 48% (73/159) · gap 11% · délai 2.7min · rebond 62% (43/73) (MFE +1.34%)
   - −4.0% : fill 30min 21% · séance 35% (54/159) · gap 5% · délai 12.5min · rebond 72% (36/54) (MFE +1.72%)
   - −5.0% : fill 30min 15% · séance 29% (44/159) · gap 2% · délai 21.5min · rebond 74% (31/44) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.69% (p90 −2.8%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.84%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.25%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=876 jambes) : jambe baissière méd −1.19% (p90 −2.78%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 98% (68/70) · rebond 39% (32/68)
      · −2.0% : fill 96% (64/70) · rebond 57% (37/64)
      · −3.0% : fill 86% (58/70) · rebond 60% (33/58)
      · −4.0% : fill 64% (44/70) · rebond 70% (29/44)
      · −5.0% : fill 53% (36/70) · rebond 71% (24/36)
   - **flat** (14 séances) :
      · −1.0% : fill 90% (13/14) · rebond 84% (10/13)
      · −2.0% : fill 57% (6/14) · rebond 47% (4/6)
      · −3.0% : fill 20% (3/14) · rebond 43% (2/3)
      · −4.0% : fill 7% (1/14) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/14) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 36% (28/75) · rebond 66% (18/28)
      · −2.0% : fill 21% (17/75) · rebond 58% (13/17)
      · −3.0% : fill 13% (12/75) · rebond 78% (8/12)
      · −4.0% : fill 11% (9/75) · rebond 81% (6/9)
      · −5.0% : fill 10% (8/75) · rebond 91% (7/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 67% si les 15 1res min sont vertes (78 cas) · 24% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 83% si début vert vs 11% si rouge (base 43% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **83%** · continue >prix actuel 59% ; creux résiduel méd -1.33% (q20 -2.94%) → **SL/trailing à −2.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +2.72% → **scale +1.67% / runner +2.72%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **11%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.93%** (au-delà de la MAE q10 -3.93%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.17% .. +4.1%] · haut q95 +5.04% · bas q05 -5.27%
   - 60min (n=160) : retour [-4.12% .. +4.96%] · haut q95 +6.21% · bas q05 -5.43%
   - 2h (n=160) : retour [-4.55% .. +5.52%] · haut q95 +7.12% · bas q05 -5.93%
   - 4h (n=160) : retour [-4.91% .. +6.39%] · haut q95 +7.24% · bas q05 -6.41%
   - 6h (n=160) : retour [-5.14% .. +6.41%] · haut q95 +7.8% · bas q05 -6.61%
   - session (n=160) : retour [-6.33% .. +6.37%] · haut q95 +7.95% · bas q05 -6.95%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.59%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.57 · part idiosyncratique 0.43
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-29 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.1  _(survente)_
- **ADX** : 23.5  _(pas de tendance nette)_
- **MACD** : hist -0.543  _(pas de croisement recent)_
- **BB** : %B 0.35 · largeur 49.0%
- **ATR** : 2.62 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.161  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 38.2  _(marche directionnel)_
- **MA** : MA20 37.95 · MA50 38.38 · MA200 32.59  _(prix < MA20)_
- **Dist MA** : MA20 -7.6% · MA50 -8.6% · MA200 +7.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (775894 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
