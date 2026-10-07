# PRY

**Generated** : 2026-10-07T00:14:25.119688+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €130.15  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)  
> ↳ spot €130.15 (+3.8% vs entrée) · entrée €125.36 · stop €121.13 · T1 €130.08 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €124.52–€126.19 (mid €125.36)
- Spot actuel : €130.15 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : €121.13 (plancher anti-bruit (R/R<2) ; -3.37 % depuis l'entree)
- Targets : T1 €130.08 · R/R 1.12 | T2 €134.81 · R/R 2.23 | T3 €139.54 · R/R 3.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €121.13


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.57 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.93 %)** : le gap seul le franchit 0.157 % des séances (2 fois sur 1270).
   - exécution **1.657 pt plus bas** dans le cas TYPIQUE (médiane), 2.785 au p90, **3.068 au pire**
   - perte réelle **8.587 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 6.93 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0026 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.86 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0003** [0.0 ; 0.0152] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.4528** [0.4009 ; 0.5055] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4196** [0.3684 ; 0.4721] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 51.7 observations effectives », dont la borne haute a 95 % vaut environ 5.8 %.
- ⚠ **5 s — échantillon insuffisant sur : swing (28.8 pt), deep (29.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.24 %** | CVaR **-5.74 %** | vol 2.58 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.51 % contre 2.81 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.46 % vs -7.52 % si l'on extrapolait par √5 _(rapport 0.86 ; < 1 = le √5 surestime)_
- **β de baisse : 1.031** (β de hausse 1.2225, asymétrie 0.8433) vs FTSEMIB — 564 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.325× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 122.75 sur atr_grid (1.75 ATR, 5.686 %) — p(stop avant cible) 0.4133 [0.36 ; 0.47], R/R 3.234, perte reelle 5.855 % (gap inclus), CVaR 6.953 %, EV 0.4118 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.712 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.874 %) — p(stop avant cible) 0.5093 [0.46 ; 0.56], R/R 3.734, perte reelle 5.072 % (gap inclus), EV 0.0609 % — **REFUSE**
      - refuse : cible atteinte seulement 3.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.509, borne haute 0.562 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ sr_based a 2.16 ATR (stop 9.203 %) — p(stop avant cible) 0.2092 [0.17 ; 0.25], R/R 2.035, perte reelle 9.305 % (gap inclus), EV 0.8054 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 2.68 ATR (stop 10.897 %) — p(stop avant cible) 0.1138 [0.08 ; 0.15], R/R 1.717, perte reelle 11.026 % (gap inclus), EV 1.091 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 6.19 ATR (stop 22.292 %) — p(stop avant cible) 0.0075 [0.00 ; 0.02], R/R 0.823, perte reelle 23.01 % (gap inclus), EV 1.3644 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.00 % > budget 12.00 %
   - 🟢 support a 12.2 ATR (stop 41.808 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.453, perte reelle 41.808 % (gap inclus), EV 1.3859 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.56 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.812 %) — p(stop avant cible) 0.9156 [0.88 ; 0.94], R/R 20.699, perte reelle 0.915 % (gap inclus), EV -0.1143 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 20.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.916, borne haute 0.942 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 1.1 % x 18.93 % + P(rien) 7.4 % x 7.06 % ne couvrent pas P(stop) 91.6 % x 0.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.624 %) — p(stop avant cible) 0.8189 [0.78 ; 0.86], R/R 10.797, perte reelle 1.754 % (gap inclus), EV -0.0727 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 10.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.819, borne haute 0.857 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 1.8 % x 18.93 % + P(rien) 16.3 % x 6.29 % ne couvrent pas P(stop) 81.9 % x 1.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.437 %) — p(stop avant cible) 0.7311 [0.68 ; 0.78], R/R 7.3, perte reelle 2.594 % (gap inclus), EV -0.0512 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 7.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.731, borne haute 0.776 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 2.5 % x 18.93 % + P(rien) 24.4 % x 5.61 % ne couvrent pas P(stop) 73.1 % x 2.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.249 %) — p(stop avant cible) 0.639 [0.59 ; 0.69], R/R 5.481, perte reelle 3.454 % (gap inclus), EV 0.0255 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.639, borne haute 0.688 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 4.061 %) — p(stop avant cible) 0.5634 [0.51 ; 0.61], R/R 4.509, perte reelle 4.199 % (gap inclus), EV 0.1439 % — **REFUSE**
      - refuse : cible atteinte seulement 3.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.563, borne haute 0.615 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.75 ATR (stop 5.686 %) — p(stop avant cible) 0.4133 [0.36 ; 0.47], R/R 3.234, perte reelle 5.855 % (gap inclus), EV 0.4118 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ grid_snapped a 2.16 ATR (stop 7.998 %) — p(stop avant cible) 0.2518 [0.21 ; 0.30], R/R 2.334, perte reelle 8.111 % (gap inclus), EV 0.8215 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.68 ATR (stop 9.692 %) — p(stop avant cible) 0.1852 [0.15 ; 0.23], R/R 1.937, perte reelle 9.778 % (gap inclus), EV 0.873 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 11.371 %) — p(stop avant cible) 0.0992 [0.07 ; 0.13], R/R 1.637, perte reelle 11.567 % (gap inclus), EV 1.1194 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 12.996 %) — p(stop avant cible) 0.0689 [0.05 ; 0.10], R/R 1.437, perte reelle 13.178 % (gap inclus), EV 1.1893 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.25 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 14.62 %) — p(stop avant cible) 0.0336 [0.02 ; 0.06], R/R 1.281, perte reelle 14.781 % (gap inclus), EV 1.3515 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.60 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 16.245 %) — p(stop avant cible) 0.0176 [0.01 ; 0.04], R/R 1.141, perte reelle 16.599 % (gap inclus), EV 1.3864 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.44 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.869 %) — p(stop avant cible) 0.0108 [0.00 ; 0.03], R/R 0.981, perte reelle 19.294 % (gap inclus), EV 1.3772 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.69 % > budget 12.00 %
   - 🟢 grid_snapped a 6.19 ATR (stop 21.086 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 0.852, perte reelle 22.218 % (gap inclus), EV 1.361 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.05 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 22.743 %) — p(stop avant cible) 0.007 [0.00 ; 0.02], R/R 0.795, perte reelle 23.804 % (gap inclus), EV 1.3598 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.06 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.367 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 0.751, perte reelle 25.224 % (gap inclus), EV 1.3776 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.72 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 25.992 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.716, perte reelle 26.438 % (gap inclus), EV 1.3792 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.67 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 130.15, ATR14 4.2286 (3.249 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.121 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.162 % | 129.9386 | 91.88 % | 94.05 % | 94.74 % | 95.53 % | 97.2 % | 97.88 % |
| 0.1 ATR | 0.325 % | 129.7271 | 85.25 % | 89.0 % | 91.17 % | 92.94 % | 95.1 % | 96.27 % |
| 0.15 ATR | 0.487 % | 129.5157 | 77.92 % | 84.44 % | 87.5 % | 90.46 % | 92.91 % | 94.25 % |
| 0.2 ATR | 0.65 % | 129.3043 | 70.0 % | 79.29 % | 82.74 % | 86.98 % | 90.71 % | 92.33 % |
| 0.25 ATR | 0.812 % | 129.0929 | 62.28 % | 74.33 % | 78.67 % | 83.2 % | 88.11 % | 90.31 % |
| 0.35 ATR | 1.137 % | 128.67 | 49.41 % | 63.73 % | 70.83 % | 76.54 % | 83.82 % | 87.49 % |
| 0.5 ATR | 1.624 % | 128.0357 | 35.15 % | 51.83 % | 59.92 % | 67.69 % | 76.52 % | 81.94 % |
| 0.75 ATR | 2.437 % | 126.9786 | 19.41 % | 34.49 % | 43.35 % | 54.27 % | 64.74 % | 73.36 % |
| 1.0 ATR | 3.249 % | 125.9214 | 9.8 % | 23.29 % | 31.55 % | 44.14 % | 55.44 % | 65.09 % |
| 1.25 ATR | 4.061 % | 124.8643 | 5.54 % | 15.76 % | 23.81 % | 34.29 % | 47.05 % | 57.42 % |
| 1.5 ATR | 4.873 % | 123.8071 | 2.48 % | 9.51 % | 15.97 % | 24.16 % | 36.46 % | 48.84 % |
| 2.0 ATR | 6.498 % | 121.6929 | 0.4 % | 3.96 % | 7.54 % | 13.72 % | 24.18 % | 37.13 % |
| 2.5 ATR | 8.122 % | 119.5786 | 0.0 % | 1.59 % | 3.37 % | 7.95 % | 15.58 % | 26.54 % |
| 3.0 ATR | 9.747 % | 117.4643 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 9.69 % | 18.97 % |
| 4.0 ATR | 12.996 % | 113.2357 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.8 % | 11.1 % |
| 6.0 ATR | 19.494 % | 104.7786 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.29 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.48 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 0.97 ATR | 1.21 ATR | 1.37 ATR | 1.85 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.85 ATR | 0.98 ATR | 1.28 ATR | 1.48 ATR | 1.70 ATR | 2.32 ATR | 2.89 ATR |
| **10 s.** | 0.53 ATR | 1.16 ATR | 1.30 ATR | 1.64 ATR | 1.97 ATR | 2.24 ATR | 2.97 ATR | 3.96 ATR |
| **20 s.** | 0.70 ATR | 1.47 ATR | 1.66 ATR | 2.19 ATR | 2.60 ATR | 2.93 ATR | 4.29 ATR | 5.63 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.598–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.437 %, prix 126.9782), p(touche) 34.49 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.725–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.437 %, prix 126.9782), p(touche) 43.35 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.979–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.249 %, prix 125.9214), p(touche) 44.14 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.298–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.873 %, prix 123.8078), p(touche) 36.46 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.664–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.498 %, prix 121.6928), p(touche) 37.13 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.045 | EV/share : €-0.191 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 12 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.0 | bear 5.0 | side 10.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 521.0 (= 4 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.674% → cible +1.652% / stop −8.0%, p_fill 49%, n_eff≈51.7) : P(cible|rempli) **33%** · **EV/risk -0.023** (×p_fill ; si rempli -0.37% du capital)
  - **swing** (entrée dip −3.681% → cible +3.771% / stop −3.373%, p_fill 38%, n_eff≈43.7) : P(cible|rempli) **42%** · **EV/risk -0.035** (×p_fill ; si rempli -0.31% du capital)
  - **deep** (entrée dip −5.697% → cible +5.447% / stop −5.168%, p_fill 36%, n_eff≈40.0) : P(cible|rempli) **58%** · **EV/risk +0.092** (×p_fill ; si rempli +1.31% du capital)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.65 · part idiosyncratique 0.35
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 64.2  _(momentum haussier)_
- **ADX** : 13.0  _(pas de tendance nette)_
- **MACD** : hist 0.741  _(pas de croisement recent)_
- **BB** : %B 0.9 · largeur 11.2%
- **ATR** : 4.23 (41.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.139  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 61.9  _(marche en range (choppy))_
- **MA** : MA20 124.61 · MA50 123.8 · MA200 119.59  _(prix > MA20)_
- **Dist MA** : MA20 +4.4% · MA50 +5.1% · MA200 +8.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (536707 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
