# PRY

**Generated** : 2026-10-09T21:53:38.477946+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €123.20  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (5 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €123.20 (+0.3% vs entrée) · entrée €122.83 · stop €113.00 · T1 €127.18 · R/R 0.44  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.150 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-09 : 123.2 · ATR Wilder 4.56 (3.7 %)_
- **Swing** : plage **118.24 → 115.17** (-4.03 % a -6.52 % sous la cloture, 0.67 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 115.85-117.1 (A). stop INDICATIF 108.02 (-6.21 % sous le bas ; sous le support 110.3-110.3 (- 0,5 ATR)).
- **Deep** : plage **115.17 → 106.99** (-6.52 % a -13.15 % sous la cloture, 1.79 ATR) — touchee 39 % → 15 % du temps en 20 seances ; supports reels dans la plage : 110.3-110.3 (C) ; 103.98-110.08 (B). stop INDICATIF 102.43 (-4.26 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (1.75 ATR sous le plus haut 20 s., RSI(2) 34.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 115.85-117.1 (A, -4.95 %) ; 110.3-110.3 (C, -10.47 %) ; 103.98-110.08 (B, -10.65 %) ; 96.88-99.95 (B, -18.87 %) ; 94.5-95.09 (A, -22.82 %) ; 91.78-92.37 (A, -25.02 %)
- Resistances reelles au-dessus : 129.4-131.2 (A, 5.03 %) ; 134.3-134.9 (A, 9.01 %) ; 145.98-148.26 (B, 18.49 %) ; 154.2-155.8 (B, 25.16 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.57 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.3 %)** : le gap seul le franchit 0.866 % des séances (11 fois sur 1270).
   - exécution **0.5 pt plus bas** dans le cas TYPIQUE (médiane), 2.876 au p90, **5.698 au pire**
   - perte réelle **5.601 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 4.3 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0113 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.86 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0003** [0.0 ; 0.0152] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.4351** [0.3836 ; 0.4877] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4025** [0.3518 ; 0.4548] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 91.1 observations effectives », dont la borne haute a 95 % vaut environ 3.3 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.24 %** | CVaR **-5.71 %** | vol 2.58 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.76 % contre 2.85 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.46 % vs -7.53 % si l'on extrapolait par √5 _(rapport 0.858 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0378** (β de hausse 1.2191, asymétrie 0.8513) vs FTSEMIB — 565 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.367× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 114.0786 sur atr_grid (2.0 ATR, 7.404 %) — p(stop avant cible) 0.2749 [0.23 ; 0.32], R/R 3.382, perte reelle 7.558 % (gap inclus), CVaR 8.251 %, EV 0.894 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.882 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.35 ATR (stop 3.575 %) — p(stop avant cible) 0.6201 [0.57 ; 0.67], R/R 6.813, perte reelle 3.753 % (gap inclus), EV 0.0204 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.620, borne haute 0.670 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ swing_based a 0.98 ATR (stop 5.887 %) — p(stop avant cible) 0.3966 [0.35 ; 0.45], R/R 4.218, perte reelle 6.061 % (gap inclus), EV 0.4147 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - 🟢 support a 4.22 ATR (stop 17.87 %) — p(stop avant cible) 0.0106 [0.00 ; 0.03], R/R 1.325, perte reelle 19.294 % (gap inclus), EV 1.4723 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.62 % > budget 12.00 %
   - 🟢 support a 9.78 ATR (stop 38.488 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.664, perte reelle 38.488 % (gap inclus), EV 1.4806 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.48 % > budget 12.00 %
   - ⚪ grid_snapped a 0.35 ATR (stop 2.42 %) — p(stop avant cible) 0.7379 [0.69 ; 0.78], R/R 9.929, perte reelle 2.575 % (gap inclus), EV -0.0809 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 9.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.738, borne haute 0.782 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.9 % x 25.56 % + P(rien) 25.3 % x 6.30 % ne couvrent pas P(stop) 73.8 % x 2.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.98 ATR (stop 4.732 %) — p(stop avant cible) 0.5227 [0.47 ; 0.57], R/R 5.239, perte reelle 4.88 % (gap inclus), EV 0.0487 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.523, borne haute 0.575 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.75 ATR (stop 6.478 %) — p(stop avant cible) 0.3576 [0.31 ; 0.41], R/R 3.833, perte reelle 6.67 % (gap inclus), EV 0.6101 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 7.404 %) — p(stop avant cible) 0.2749 [0.23 ; 0.32], R/R 3.382, perte reelle 7.558 % (gap inclus), EV 0.894 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 8.329 %) — p(stop avant cible) 0.2396 [0.20 ; 0.29], R/R 3.032, perte reelle 8.432 % (gap inclus), EV 0.8642 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.5 ATR (stop 9.255 %) — p(stop avant cible) 0.1969 [0.16 ; 0.24], R/R 2.733, perte reelle 9.355 % (gap inclus), EV 0.9755 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 10.18 %) — p(stop avant cible) 0.1495 [0.11 ; 0.19], R/R 2.498, perte reelle 10.233 % (gap inclus), EV 1.1125 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 11.106 %) — p(stop avant cible) 0.1069 [0.08 ; 0.14], R/R 2.268, perte reelle 11.272 % (gap inclus), EV 1.1991 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 12.957 %) — p(stop avant cible) 0.0677 [0.04 ; 0.10], R/R 1.945, perte reelle 13.146 % (gap inclus), EV 1.2897 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.21 % > budget 12.00 %
   - 🟢 grid_snapped a 4.22 ATR (stop 16.715 %) — p(stop avant cible) 0.0127 [0.00 ; 0.03], R/R 1.495, perte reelle 17.104 % (gap inclus), EV 1.4855 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.31 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.509 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 1.299, perte reelle 19.676 % (gap inclus), EV 1.4725 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.65 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.36 %) — p(stop avant cible) 0.0086 [0.00 ; 0.02], R/R 1.196, perte reelle 21.373 % (gap inclus), EV 1.4621 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.86 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.211 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 1.113, perte reelle 22.963 % (gap inclus), EV 1.4592 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.91 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.062 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 1.02, perte reelle 25.053 % (gap inclus), EV 1.4738 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.63 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 25.913 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 0.969, perte reelle 26.391 % (gap inclus), EV 1.4753 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.60 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 27.764 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.85, perte reelle 30.076 % (gap inclus), EV 1.4666 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.74 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.615 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.79, perte reelle 32.353 % (gap inclus), EV 1.4742 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.60 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 123.2, ATR14 4.5607 (3.702 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.277 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.185 % | 122.972 | 91.88 % | 94.05 % | 94.74 % | 95.53 % | 97.2 % | 97.88 % |
| 0.1 ATR | 0.37 % | 122.7439 | 85.25 % | 89.0 % | 91.17 % | 92.94 % | 95.1 % | 96.27 % |
| 0.15 ATR | 0.555 % | 122.5159 | 77.92 % | 84.44 % | 87.5 % | 90.46 % | 92.91 % | 94.25 % |
| 0.2 ATR | 0.74 % | 122.2879 | 70.0 % | 79.29 % | 82.74 % | 86.98 % | 90.71 % | 92.33 % |
| 0.25 ATR | 0.925 % | 122.0598 | 62.28 % | 74.33 % | 78.57 % | 83.2 % | 88.11 % | 90.31 % |
| 0.35 ATR | 1.296 % | 121.6037 | 49.41 % | 63.73 % | 70.73 % | 76.54 % | 83.82 % | 87.49 % |
| 0.5 ATR | 1.851 % | 120.9196 | 35.05 % | 51.83 % | 59.82 % | 67.59 % | 76.52 % | 81.94 % |
| 0.75 ATR | 2.776 % | 119.7795 | 19.41 % | 34.49 % | 43.25 % | 54.17 % | 64.74 % | 73.36 % |
| 1.0 ATR | 3.702 % | 118.6393 | 9.9 % | 23.29 % | 31.55 % | 44.04 % | 55.54 % | 65.19 % |
| 1.25 ATR | 4.627 % | 117.4991 | 5.54 % | 15.86 % | 23.91 % | 34.29 % | 47.15 % | 57.52 % |
| 1.5 ATR | 5.553 % | 116.3589 | 2.48 % | 9.61 % | 16.07 % | 24.16 % | 36.56 % | 49.04 % |
| 2.0 ATR | 7.404 % | 114.0786 | 0.4 % | 3.96 % | 7.54 % | 13.72 % | 24.28 % | 37.34 % |
| 2.5 ATR | 9.255 % | 111.7982 | 0.0 % | 1.59 % | 3.37 % | 7.95 % | 15.58 % | 26.74 % |
| 3.0 ATR | 11.106 % | 109.5179 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 9.69 % | 18.97 % |
| 4.0 ATR | 14.808 % | 104.9571 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.8 % | 11.1 % |
| 6.0 ATR | 22.211 % | 95.8357 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.29 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.48 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 0.97 ATR | 1.21 ATR | 1.38 ATR | 1.86 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.85 ATR | 0.98 ATR | 1.28 ATR | 1.48 ATR | 1.70 ATR | 2.32 ATR | 2.89 ATR |
| **10 s.** | 0.53 ATR | 1.17 ATR | 1.30 ATR | 1.65 ATR | 1.97 ATR | 2.25 ATR | 2.97 ATR | 3.96 ATR |
| **20 s.** | 0.70 ATR | 1.47 ATR | 1.67 ATR | 2.21 ATR | 2.61 ATR | 2.93 ATR | 4.29 ATR | 5.63 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.598–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.776 %, prix 119.78), p(touche) 34.49 % (en stress 88.12 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.724–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.776 %, prix 119.78), p(touche) 43.25 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.976–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.702 %, prix 118.6391), p(touche) 44.04 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.301–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.553 %, prix 116.3587), p(touche) 36.56 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.673–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.404 %, prix 114.0783), p(touche) 37.34 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.019 | EV/share : €-0.186 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 7.5 | side 7.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 370.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.304% → cible +3.541% / stop −8.0%, p_fill 85%, n_eff≈91.1) : P(cible|rempli) **8%** · **EV/risk -0.070** (×p_fill ; si rempli -0.66% du capital)
  - **swing** (entrée dip −0.598% → cible +3.85% / stop −3.724%, p_fill 81%, n_eff≈94.3) : P(cible|rempli) **37%** · **EV/risk -0.176** (×p_fill ; si rempli -0.81% du capital)
  - **deep** (entrée dip −0.877% → cible +5.905% / stop −5.602%, p_fill 88%, n_eff≈98.6) : P(cible|rempli) **38%** · **EV/risk -0.179** (×p_fill ; si rempli -1.14% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→40% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.71% (p90 6.32%) · excursion haute méd. +1.5% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.21% vs midi 0.779% vs clôture 1.066% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr 0.003)_ ; drift intra méd. -0.354% ; recovery-V 21%
- **σ réalisé intraday** 2.479% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 65% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 129.9327 (VA 129.5263–130.8813 ; dernier close 130.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 23% · rebond 60% · **stop −2.81%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.51% · baisse 35% (gap-down >1% 13% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.71% (p90 −2.05%) · haut méd +0.51% · range méd 1.3%
- Excursion ouverture 15min (n=160) : bas méd −0.93% (p90 −2.32%) · haut méd +0.61% · range méd 1.71%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.41%) · haut méd +0.74% · range méd 1.88%
- Excursion ouverture 60min (n=160) : bas méd −1.05% (p90 −2.93%) · haut méd +0.83% · range méd 2.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 129.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 65% (109/159) · gap 19% · délai 0.4min · rebond 54% (61/109) (MFE +1.1%)
   - −1.0% : fill 30min 39% · séance 54% (90/159) · gap 13% · délai 1.3min · rebond 60% (54/90) (MFE +1.25%)
   - −1.5% : fill 30min 24% · séance 45% (72/159) · gap 7% · délai 21.4min · rebond 51% (39/72) (MFE +1.06%)
   - −2.0% : fill 30min 18% · séance 37% (60/159) · gap 3% · délai 42.5min · rebond 51% (34/60) (MFE +1.01%)
   - −3.0% : fill 30min 6% · séance 23% (40/159) · gap 1% · délai 93.7min · rebond 60% (26/40) (MFE +1.15%)
   - −4.0% : fill 30min 2% · séance 14% (25/159) · gap 0% · délai 282.0min · rebond 57% (15/25) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 9% (16/159) · gap 0% · délai 394.7min · rebond 66% (11/16) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.89%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.31% (p90 −1.63%) → stop au-delà de −1.12% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.76%) → stop au-delà de −1.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=487 jambes) : jambe baissière méd −1.06% (p90 −2.48%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 94% (39/43) · rebond 49% (19/39)
      · −2.0% : fill 77% (31/43) · rebond 58% (18/31)
      · −3.0% : fill 47% (23/43) · rebond 50% (14/23)
      · −4.0% : fill 30% (15/43) · rebond 57% (9/15)
      · −5.0% : fill 26% (12/43) · rebond 57% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 48% (15/27) · rebond 74% (11/15)
      · −2.0% : fill 27% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 16% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 6% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 38% (36/89) · rebond 65% (24/36)
      · −2.0% : fill 23% (21/89) · rebond 30% (9/21)
      · −3.0% : fill 14% (12/89) · rebond 80% (9/12)
      · −4.0% : fill 9% (8/89) · rebond 54% (5/8)
      · −5.0% : fill 4% (3/89) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 63% si les 15 1res min sont vertes (77 cas) · 28% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 82% si début vert vs 21% si rouge (base 46% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **82%** · continue >prix actuel 45% ; creux résiduel méd -1.18% (q20 -1.89%) → **SL/trailing à −1.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +2.01% → **scale +1.07% / runner +2.01%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **21%** (continue à baisser 66%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.77%** (au-delà de la MAE q10 -3.77%), cible rebond +1.33% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.93% .. +2.17%] · haut q95 +3.13% · bas q05 -3.36%
   - 60min (n=160) : retour [-3.28% .. +2.31%] · haut q95 +3.46% · bas q05 -3.58%
   - 2h (n=160) : retour [-3.32% .. +2.69%] · haut q95 +3.52% · bas q05 -4.05%
   - 4h (n=160) : retour [-3.46% .. +3.2%] · haut q95 +4.0% · bas q05 -4.46%
   - 6h (n=160) : retour [-3.73% .. +3.5%] · haut q95 +4.42% · bas q05 -4.65%
   - session (n=160) : retour [-4.58% .. +3.44%] · haut q95 +4.53% · bas q05 -6.29%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.72 · part idiosyncratique 0.28
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 45.5  _(neutre)_
- **ADX** : 12.4  _(pas de tendance nette)_
- **MACD** : hist -0.115  _(bearish_recent)_
- **BB** : %B 0.43 · largeur 11.0%
- **ATR** : 4.56 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.154  _(distribution)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 64.8  _(marche en range (choppy))_
- **MA** : MA20 124.22 · MA50 124.11 · MA200 120.16  _(prix < MA20)_
- **Dist MA** : MA20 -0.8% · MA50 -0.7% · MA200 +2.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (899973 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
