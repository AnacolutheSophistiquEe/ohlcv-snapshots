# IONQ

**Generated** : 2026-10-05T00:27:17.944355+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $43.77  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (usable=false (intervalle le plus large 25.0 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $43.77 (+4.5% vs entrée) · entrée $41.89 · stop $39.15 · T1 $45.32 · R/R 1.25  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.260 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 72.9 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $41.54–$42.23 (mid $41.89)
- Spot actuel : $43.77 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : $39.15 (plancher anti-bruit (R/R<2) ; -6.54 % depuis l'entree)
- Targets : T1 $45.32 · R/R 1.25 | T2 $48.37 · R/R 2.36 | T3 $51.43 · R/R 3.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $39.15


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.01 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.54 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1254).
   - exécution **1.153 pt plus bas** dans le cas TYPIQUE (médiane), 8.345 au p90, **11.319 au pire**
   - perte réelle **13.966 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 10.54 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0109 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.068 % | p01 -6.63 % | pire -21.859 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5247** [0.4504 ; 0.5982] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5228** [0.4701 ; 0.5751] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5063** [0.4537 ; 0.5588] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.0 pt), deep (25.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.53 %** | CVaR **-10.49 %** | vol 6.1 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 11.48 % contre 5.94 % aujourd'hui, rapport 1.93)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.6 % vs -19.55 % si l'on extrapolait par √5 _(rapport 0.9 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2211** (β de hausse 1.9986, asymétrie 1.1113) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 39.2533 sur grid_snapped (1.35 ATR, 10.319 %) — p(stop avant cible) 0.5473 [0.49 ; 0.60], R/R 2.1, perte reelle 10.416 % (gap inclus), CVaR 11.385 %, EV 0.2628 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3896 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.547, borne haute 0.599 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.364 %) — p(stop avant cible) 0.5894 [0.54 ; 0.64], R/R 2.307, perte reelle 9.482 % (gap inclus), EV 0.2299 % — **REFUSE**
      - refuse : p_stop_first 0.589, borne haute 0.640 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 1.35 ATR (stop 11.368 %) — p(stop avant cible) 0.4896 [0.44 ; 0.54], R/R 1.907, perte reelle 11.468 % (gap inclus), EV 0.1972 % — **REFUSE**
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.34 % > budget 12.00 %
   - 🟢 support a 3.51 ATR (stop 24.831 %) — p(stop avant cible) 0.093 [0.07 ; 0.13], R/R 0.88, perte reelle 24.867 % (gap inclus), EV 0.7627 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.90 % > budget 12.00 %
   - 🟢 support a 5.04 ATR (stop 34.404 %) — p(stop avant cible) 0.0214 [0.01 ; 0.04], R/R 0.635, perte reelle 34.438 % (gap inclus), EV 0.6754 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.92 % > budget 12.00 %
   - 🟢 support a 6.54 ATR (stop 43.771 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.5, perte reelle 43.771 % (gap inclus), EV 0.7443 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.81 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.561 %) — p(stop avant cible) 0.9107 [0.88 ; 0.94], R/R 13.676, perte reelle 1.599 % (gap inclus), EV 0.31 % — **REFUSE**
      - refuse : cible atteinte seulement 7.2 % du temps (< 15 %) meme a 10 seances : le R/R de 13.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.911, borne haute 0.937 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.121 %) — p(stop avant cible) 0.8488 [0.81 ; 0.88], R/R 6.743, perte reelle 3.243 % (gap inclus), EV 0.1702 % — **REFUSE**
      - refuse : cible atteinte seulement 12.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.849, borne haute 0.884 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 4.682 %) — p(stop avant cible) 0.7895 [0.74 ; 0.83], R/R 4.571, perte reelle 4.785 % (gap inclus), EV -0.1091 % — **REFUSE**
      - refuse : cible atteinte seulement 14.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.789, borne haute 0.830 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 14.6 % x 21.87 % + P(rien) 6.5 % x 7.44 % ne couvrent pas P(stop) 79.0 % x 4.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 6.243 %) — p(stop avant cible) 0.7361 [0.69 ; 0.78], R/R 3.462, perte reelle 6.317 % (gap inclus), EV -0.1607 % — **REFUSE**
      - refuse : p_stop_first 0.736, borne haute 0.780 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 17.9 % x 21.87 % + P(rien) 8.5 % x 6.71 % ne couvrent pas P(stop) 73.6 % x 6.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.35 ATR (stop 10.319 %) — p(stop avant cible) 0.5473 [0.49 ; 0.60], R/R 2.1, perte reelle 10.416 % (gap inclus), EV 0.2628 % — **REFUSE**
      - refuse : p_stop_first 0.547, borne haute 0.599 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 12.485 %) — p(stop avant cible) 0.4363 [0.38 ; 0.49], R/R 1.742, perte reelle 12.555 % (gap inclus), EV 0.3082 % — **REFUSE**
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.10 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 14.046 %) — p(stop avant cible) 0.3591 [0.31 ; 0.41], R/R 1.55, perte reelle 14.111 % (gap inclus), EV 0.2072 % — **REFUSE**
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.52 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 15.606 %) — p(stop avant cible) 0.2992 [0.25 ; 0.35], R/R 1.393, perte reelle 15.699 % (gap inclus), EV 0.2315 % — **REFUSE**
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.16 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 17.167 %) — p(stop avant cible) 0.2502 [0.21 ; 0.30], R/R 1.269, perte reelle 17.24 % (gap inclus), EV 0.4015 % — **REFUSE**
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.53 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 18.728 %) — p(stop avant cible) 0.2053 [0.17 ; 0.25], R/R 1.164, perte reelle 18.795 % (gap inclus), EV 0.6025 % — **REFUSE**
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.00 % > budget 12.00 %
   - 🟢 grid_snapped a 3.51 ATR (stop 23.783 %) — p(stop avant cible) 0.1011 [0.07 ; 0.14], R/R 0.918, perte reelle 23.815 % (gap inclus), EV 0.8254 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.85 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 28.091 %) — p(stop avant cible) 0.0617 [0.04 ; 0.09], R/R 0.776, perte reelle 28.173 % (gap inclus), EV 0.6683 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.19 % > budget 12.00 %
   - 🟢 grid_snapped a 5.04 ATR (stop 33.356 %) — p(stop avant cible) 0.0216 [0.01 ; 0.04], R/R 0.654, perte reelle 33.418 % (gap inclus), EV 0.6964 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.49 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 37.455 %) — p(stop avant cible) 0.0096 [0.00 ; 0.02], R/R 0.581, perte reelle 37.656 % (gap inclus), EV 0.7298 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.05 % > budget 12.00 %
   - 🟢 grid_snapped a 6.54 ATR (stop 42.723 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.512, perte reelle 42.723 % (gap inclus), EV 0.746 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.78 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 46.819 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.467, perte reelle 46.819 % (gap inclus), EV 0.7632 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.63 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 49.94 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.438, perte reelle 49.94 % (gap inclus), EV 0.776 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.41 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 43.77, ATR14 2.7324 (6.243 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.377 ATR = 2.353 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.312 % | 43.6334 | 93.56 % | 95.37 % | 96.07 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.624 % | 43.4968 | 85.81 % | 91.04 % | 92.14 % | 94.44 % | 95.84 % | 96.92 % |
| 0.15 ATR | 0.936 % | 43.3601 | 78.57 % | 86.0 % | 88.21 % | 91.41 % | 93.6 % | 95.69 % |
| 0.2 ATR | 1.249 % | 43.2235 | 71.03 % | 80.26 % | 84.17 % | 88.28 % | 90.86 % | 93.64 % |
| 0.25 ATR | 1.561 % | 43.0869 | 65.09 % | 76.13 % | 80.54 % | 85.66 % | 88.73 % | 92.1 % |
| 0.35 ATR | 2.185 % | 42.8137 | 52.72 % | 67.17 % | 73.79 % | 78.99 % | 84.06 % | 88.51 % |
| 0.5 ATR | 3.121 % | 42.4038 | 37.83 % | 54.18 % | 61.9 % | 70.61 % | 78.48 % | 84.62 % |
| 0.75 ATR | 4.682 % | 41.7207 | 22.43 % | 38.97 % | 48.08 % | 58.48 % | 69.04 % | 77.03 % |
| 1.0 ATR | 6.243 % | 41.0376 | 10.06 % | 24.27 % | 34.38 % | 45.45 % | 57.77 % | 68.31 % |
| 1.25 ATR | 7.803 % | 40.3546 | 3.82 % | 14.3 % | 23.89 % | 34.44 % | 49.95 % | 61.95 % |
| 1.5 ATR | 9.364 % | 39.6715 | 1.11 % | 7.05 % | 15.52 % | 25.25 % | 40.91 % | 56.21 % |
| 2.0 ATR | 12.485 % | 38.3053 | 0.1 % | 1.91 % | 4.94 % | 14.04 % | 28.02 % | 45.13 % |
| 2.5 ATR | 15.606 % | 36.9391 | 0.0 % | 0.2 % | 1.21 % | 5.66 % | 17.97 % | 34.15 % |
| 3.0 ATR | 18.728 % | 35.5729 | 0.0 % | 0.1 % | 0.4 % | 2.53 % | 11.27 % | 25.85 % |
| 4.0 ATR | 24.97 % | 32.8406 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.94 % | 10.56 % |
| 6.0 ATR | 37.455 % | 27.3759 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.03 ATR | 1.22 ATR | 1.37 ATR | 1.76 ATR | 2.00 ATR |
| **5 s.** | 0.42 ATR | 0.91 ATR | 1.01 ATR | 1.29 ATR | 1.51 ATR | 1.73 ATR | 2.24 ATR | 2.60 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.39 ATR | 1.81 ATR | 2.15 ATR | 2.40 ATR | 3.15 ATR | 3.75 ATR |
| **20 s.** | 0.81 ATR | 1.78 ATR | 2.01 ATR | 2.57 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.428–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.651–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.682 %, prix 41.7207), p(touche) 38.97 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.806–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.243 %, prix 41.0374), p(touche) 34.38 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.01–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.803 %, prix 40.3546), p(touche) 34.44 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.387–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.364 %, prix 39.6714), p(touche) 40.91 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.006–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.606 %, prix 36.9393), p(touche) 34.15 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (66.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.012 | EV/share : $-0.032 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 18 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 74.7 | bear 8.2 | side 17.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 583.0 (= 15 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.957% → cible +3.183% / stop −1.91%, p_fill 56%, n_eff≈63.4) : P(cible|rempli) **21%** · **EV/risk -0.169** (×p_fill ; si rempli -0.58% du capital)
  - **swing** (entrée dip −4.297% → cible +8.193% / stop −6.523%, p_fill 49%, n_eff≈59.0) : P(cible|rempli) **40%** · **EV/risk -0.049** (×p_fill ; si rempli -0.66% du capital)
  - **deep** (entrée dip −6.646% → cible +10.913% / stop −10.031%, p_fill 49%, n_eff≈56.4) : P(cible|rempli) **42%** · **EV/risk -0.072** (×p_fill ; si rempli -1.47% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→80% · +2.0%→64% · +3.0%→54% · +5.0%→28% · +8.0%→13%
- Range intraday médian 7.05% (p90 11.57%) · excursion haute méd. +3.57% / basse méd. −2.49%
- Profil de vol intra : ouverture 4.841% vs midi 1.378% vs clôture 1.552% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 62% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr 0.011)_ ; drift intra méd. -0.232% ; recovery-V 26%
- **σ réalisé intraday** 4.05% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 57% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 44.6406 (VA 44.2714–45.1154 ; dernier close 43.77)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 78% · **stop −4.38%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 49% (gap-down >1% 34% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.73%) · haut méd +1.28% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −3.76%) · haut méd +1.47% · range méd 3.38%
- Excursion ouverture 30min (n=160) : bas méd −1.31% (p90 −4.62%) · haut méd +1.81% · range méd 4.16%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −5.28%) · haut méd +1.87% · range méd 4.67%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (126/159) · gap 43% · délai 0.0min · rebond 61% (83/126) (MFE +1.81%)
   - −1.0% : fill 30min 60% · séance 70% (119/159) · gap 34% · délai 0.0min · rebond 67% (85/119) (MFE +1.91%)
   - −1.5% : fill 30min 53% · séance 65% (112/159) · gap 30% · délai 0.0min · rebond 70% (78/112) (MFE +2.06%)
   - −2.0% : fill 30min 46% · séance 54% (100/159) · gap 21% · délai 0.0min · rebond 69% (70/100) (MFE +2.17%)
   - −3.0% : fill 30min 37% · séance 43% (81/159) · gap 10% · délai 4.1min · rebond 70% (59/81) (MFE +2.38%)
   - −4.0% : fill 30min 22% · séance 33% (64/159) · gap 4% · délai 15.3min · rebond 69% (48/64) (MFE +2.23%)
   - −5.0% : fill 30min 11% · séance 25% (50/159) · gap 1% · délai 32.0min · rebond 78% (41/50) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.62%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −2.65%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.35%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1047 jambes) : jambe baissière méd −1.26% (p90 −2.97%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (80 séances) :
      · −1.0% : fill 100% (80/80) · rebond 69% (56/80)
      · −2.0% : fill 87% (73/80) · rebond 75% (54/73)
      · −3.0% : fill 72% (61/80) · rebond 72% (44/61)
      · −4.0% : fill 54% (47/80) · rebond 67% (34/47)
      · −5.0% : fill 38% (37/80) · rebond 70% (28/37)
   - **flat** (15 séances) :
      · −1.0% : fill 62% (10/15) · rebond 84% (9/10)
      · −2.0% : fill 43% (8/15) · rebond 90% (6/8)
      · −3.0% : fill 27% (5/15) · rebond 64% (4/5)
      · −4.0% : fill 23% (4/15) · rebond 57% (3/4)
      · −5.0% : fill 16% (3/15) · rebond 100% (3/3)
   - **gap-up** (64 séances) :
      · −1.0% : fill 41% (29/64) · rebond 55% (20/29)
      · −2.0% : fill 22% (19/64) · rebond 31% (10/19)
      · −3.0% : fill 15% (15/64) · rebond 60% (11/15)
      · −4.0% : fill 14% (13/64) · rebond 84% (11/13)
      · −5.0% : fill 12% (10/64) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 59% si les 15 1res min sont vertes (90 cas) · 26% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **56min** → P(séance verte=clôture>ouverture) 66% si début vert vs 19% si rouge (base 46% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=86) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.76% (q20 -4.14%) → **SL/trailing à −4.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.64% / q75 +3.31% → **scale +1.64% / runner +3.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **19%** (continue à baisser 59%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.23%** (au-delà de la MAE q10 -4.23%), cible rebond +1.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +5.46%] · haut q95 +7.35% · bas q05 -5.49%
   - 60min (n=160) : retour [-5.25% .. +5.86%] · haut q95 +7.69% · bas q05 -6.74%
   - 2h (n=160) : retour [-6.37% .. +5.93%] · haut q95 +8.07% · bas q05 -7.06%
   - 4h (n=160) : retour [-6.75% .. +6.86%] · haut q95 +8.75% · bas q05 -7.93%
   - 6h (n=160) : retour [-6.62% .. +7.19%] · haut q95 +9.75% · bas q05 -7.92%
   - session (n=160) : retour [-6.36% .. +8.14%] · haut q95 +9.8% · bas q05 -8.19%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0% / strong 7.5%) · base = 12 séances trend-up (n_eff 7.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **35%**. Lecture précoce 30 min : signature présente → 13% vs absente 5% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.3% (p75 2.44% / p90 3.18%) · ~4.0 replis/séance, durée méd 70.31 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 30.0 min, n=48)
   - −1.0% → **77%** (reprise méd 34.75 min, n=35)
   - −1.5% → **67%** (reprise méd 44.94 min, n=18)
   - −2.0% → **61%** (reprise méd 64.1 min, n=13)
   - −3.0% → **74%** (reprise méd 175.76 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.18%** (p90, défaut prudent ; serré/agressif −2.44%) ; extension open→close méd +8.16% (q75 +8.39% / q95 +13.57%), MFE méd +9.48% / q90 +12.4%
   - Échelle scale-out : +9.48% (33%) / +10.45% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−3.18%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 167.77 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 2.07%)
- **CONTEXTE** : la dernière heure tient les gains 70% du temps (retour médian dernière heure +0.1%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 72.9  _(surachat)_
- **ADX** : 22.0  _(pas de tendance nette)_
- **MACD** : hist 0.495  _(pas de croisement recent)_
- **BB** : %B 0.74 · largeur 30.1%
- **ATR** : 2.73 (19.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.261  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 44.4  _(transition)_
- **MA** : MA20 40.85 · MA50 40.6 · MA200 43.46  _(prix > MA20)_
- **Dist MA** : MA20 +7.2% · MA50 +7.8% · MA200 +0.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (843216 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
