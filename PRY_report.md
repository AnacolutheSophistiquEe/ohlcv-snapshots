# PRY

**Generated** : 2026-10-01T00:13:54.708871+00:00  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €124.25  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €124.25 (+1.2% vs entrée) · entrée €122.77 · stop €118.11 · T1 €130.68 · R/R 1.7  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 161 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €121.97–€123.58 (mid €122.77)
- Spot actuel : €124.25 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €118.11 (plancher anti-bruit (R/R<2) ; -3.80 % depuis l'entree)
- Targets : T1 €130.68 · R/R 1.7 | T2 €135.89 · R/R 2.82 | T3 €141.10 · R/R 3.93
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €118.11


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.57 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.94 %)** : le gap seul le franchit 0.394 % des séances (5 fois sur 1270).
   - exécution **1.614 pt plus bas** dans le cas TYPIQUE (médiane), 3.929 au p90, **5.058 au pire**
   - perte réelle **6.853 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 4.94 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0075 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.86 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0003** [0.0 ; 0.0152] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.4742** [0.422 ; 0.5269] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4087** [0.3578 ; 0.4611] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 82.4 observations effectives », dont la borne haute a 95 % vaut environ 3.6 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.24 %** | CVaR **-5.74 %** | vol 2.58 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.41 % contre 2.78 % aujourd'hui, rapport 0.51)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.46 % vs -7.52 % si l'on extrapolait par √5 _(rapport 0.86 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0398** (β de hausse 1.2244, asymétrie 0.8492) vs FTSEMIB — 566 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.48× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 123.0857 sur atr_grid (0.25 ATR, 0.937 %) — p(stop avant cible) 0.8899 [0.85 ; 0.92], R/R 23.398, perte reelle 1.046 % (gap inclus), CVaR 2.676 %, EV -0.0037 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.6307 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 23.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.890, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.171 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 44.7 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 2.93 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.68 ATR (stop 4.913 %) — p(stop avant cible) 0.5112 [0.46 ; 0.56], R/R 4.794, perte reelle 5.107 % (gap inclus), EV 0.1008 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.511, borne haute 0.564 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.46 % > budget 3.00 %
   - ⚪ swing_based a 1.76 ATR (stop 8.957 %) — p(stop avant cible) 0.222 [0.18 ; 0.27], R/R 2.702, perte reelle 9.06 % (gap inclus), EV 0.9069 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.41 % > budget 3.00 %
   - 🔴 support a 4.35 ATR (stop 18.691 %) — p(stop avant cible) 0.0108 [0.00 ; 0.03], R/R 1.238, perte reelle 19.775 % (gap inclus), EV 1.4887 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.84 % > budget 3.00 %
      - ⚠ support DETECTE a 0.58 ATR du spot — compartiment <1, mesure a 45.4 % de casse (IC clusterise [0.423 ; 0.484] sur 1130 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 9.81 ATR (stop 39.134 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.626, perte reelle 39.134 % (gap inclus), EV 1.4996 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.65 % > budget 3.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.937 %) — p(stop avant cible) 0.8899 [0.85 ; 0.92], R/R 23.398, perte reelle 1.046 % (gap inclus), EV -0.0037 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 23.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.890, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 0.6 % x 24.48 % + P(rien) 10.4 % x 7.46 % ne couvrent pas P(stop) 89.0 % x 1.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.68 ATR (stop 3.664 %) — p(stop avant cible) 0.6094 [0.56 ; 0.66], R/R 6.378, perte reelle 3.838 % (gap inclus), EV 0.1543 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.609, borne haute 0.660 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.37 % > budget 3.00 %
   - ⚪ atr_grid a 1.5 ATR (stop 5.622 %) — p(stop avant cible) 0.4284 [0.38 ; 0.48], R/R 4.222, perte reelle 5.798 % (gap inclus), EV 0.4395 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 6.96 % > budget 3.00 %
   - ⚪ grid_snapped a 1.76 ATR (stop 7.709 %) — p(stop avant cible) 0.2657 [0.22 ; 0.31], R/R 3.124, perte reelle 7.837 % (gap inclus), EV 0.9096 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 8.39 % > budget 3.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 8.433 %) — p(stop avant cible) 0.245 [0.20 ; 0.29], R/R 2.862, perte reelle 8.554 % (gap inclus), EV 0.8391 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.02 % > budget 3.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 10.308 %) — p(stop avant cible) 0.1533 [0.12 ; 0.19], R/R 2.351, perte reelle 10.41 % (gap inclus), EV 1.1005 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.62 % > budget 3.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 11.245 %) — p(stop avant cible) 0.1052 [0.08 ; 0.14], R/R 2.147, perte reelle 11.404 % (gap inclus), EV 1.2158 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.58 % > budget 3.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 13.119 %) — p(stop avant cible) 0.0662 [0.04 ; 0.10], R/R 1.842, perte reelle 13.289 % (gap inclus), EV 1.297 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.34 % > budget 3.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 14.993 %) — p(stop avant cible) 0.0296 [0.02 ; 0.05], R/R 1.609, perte reelle 15.213 % (gap inclus), EV 1.4637 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.77 % > budget 3.00 %
   - 🔴 grid_snapped a 4.35 ATR (stop 17.442 %) — p(stop avant cible) 0.0126 [0.00 ; 0.03], R/R 1.333, perte reelle 18.358 % (gap inclus), EV 1.4898 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.76 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.615 %) — p(stop avant cible) 0.009 [0.00 ; 0.02], R/R 1.139, perte reelle 21.493 % (gap inclus), EV 1.4784 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.07 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.489 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 1.034, perte reelle 23.681 % (gap inclus), EV 1.4754 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.15 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.363 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.971, perte reelle 25.222 % (gap inclus), EV 1.4912 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.82 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.237 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.921, perte reelle 26.585 % (gap inclus), EV 1.4943 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.78 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.112 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.81, perte reelle 30.229 % (gap inclus), EV 1.485 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.93 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.986 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.757, perte reelle 32.353 % (gap inclus), EV 1.4947 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.77 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 124.25, ATR14 4.6571 (3.748 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 1.289 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.187 % | 124.0171 | 91.88 % | 93.95 % | 94.74 % | 95.53 % | 97.2 % | 97.88 % |
| 0.1 ATR | 0.375 % | 123.7843 | 85.25 % | 88.9 % | 91.17 % | 92.94 % | 95.1 % | 96.27 % |
| 0.15 ATR | 0.562 % | 123.5514 | 77.82 % | 84.34 % | 87.5 % | 90.46 % | 92.91 % | 94.25 % |
| 0.2 ATR | 0.75 % | 123.3186 | 69.8 % | 79.19 % | 82.74 % | 86.98 % | 90.71 % | 92.33 % |
| 0.25 ATR | 0.937 % | 123.0857 | 62.08 % | 74.33 % | 78.67 % | 83.2 % | 88.11 % | 90.31 % |
| 0.35 ATR | 1.312 % | 122.62 | 49.21 % | 63.73 % | 70.93 % | 76.74 % | 83.82 % | 87.49 % |
| 0.5 ATR | 1.874 % | 121.9214 | 34.95 % | 51.83 % | 60.12 % | 67.89 % | 76.52 % | 81.94 % |
| 0.75 ATR | 2.811 % | 120.7571 | 19.21 % | 34.39 % | 43.25 % | 54.27 % | 64.84 % | 73.36 % |
| 1.0 ATR | 3.748 % | 119.5929 | 9.8 % | 23.29 % | 31.55 % | 44.04 % | 55.44 % | 64.98 % |
| 1.25 ATR | 4.685 % | 118.4286 | 5.54 % | 15.76 % | 23.81 % | 34.19 % | 46.95 % | 57.21 % |
| 1.5 ATR | 5.622 % | 117.2643 | 2.48 % | 9.51 % | 15.97 % | 24.16 % | 36.36 % | 48.64 % |
| 2.0 ATR | 7.496 % | 114.9357 | 0.4 % | 3.96 % | 7.54 % | 13.72 % | 24.18 % | 37.13 % |
| 2.5 ATR | 9.371 % | 112.6071 | 0.0 % | 1.59 % | 3.37 % | 7.95 % | 15.58 % | 26.54 % |
| 3.0 ATR | 11.245 % | 110.2786 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 9.69 % | 18.97 % |
| 4.0 ATR | 14.993 % | 105.6214 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.8 % | 11.1 % |
| 6.0 ATR | 22.489 % | 96.3071 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.29 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.48 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 0.97 ATR | 1.21 ATR | 1.37 ATR | 1.85 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.85 ATR | 0.98 ATR | 1.28 ATR | 1.48 ATR | 1.70 ATR | 2.32 ATR | 2.89 ATR |
| **10 s.** | 0.53 ATR | 1.16 ATR | 1.30 ATR | 1.64 ATR | 1.97 ATR | 2.24 ATR | 2.97 ATR | 3.96 ATR |
| **20 s.** | 0.70 ATR | 1.46 ATR | 1.66 ATR | 2.19 ATR | 2.60 ATR | 2.93 ATR | 4.29 ATR | 5.63 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.598–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.811 %, prix 120.7573), p(touche) 34.39 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.724–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.811 %, prix 120.7573), p(touche) 43.25 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.977–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.748 %, prix 119.5931), p(touche) 44.04 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.296–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.622 %, prix 117.2647), p(touche) 36.36 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.658–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.496 %, prix 114.9362), p(touche) 37.13 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.066 | EV/share : €-0.306 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 4 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 9.9 | bear 5.1 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 497.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.544% → cible +1.884% / stop −8.0%, p_fill 77%, n_eff≈82.4) : P(cible|rempli) **29%** · **EV/risk -0.072** (×p_fill ; si rempli -0.75% du capital)
  - **swing** (entrée dip −1.192% → cible +6.445% / stop −3.793%, p_fill 69%, n_eff≈80.0) : P(cible|rempli) **23%** · **EV/risk -0.144** (×p_fill ; si rempli -0.79% du capital)
  - **deep** (entrée dip −1.838% → cible +7.149% / stop −5.728%, p_fill 74%, n_eff≈82.4) : P(cible|rempli) **25%** · **EV/risk -0.218** (×p_fill ; si rempli -1.68% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→39% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.71% (p90 6.32%) · excursion haute méd. +1.5% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.215% vs midi 0.772% vs clôture 1.067% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.013)_ ; drift intra méd. -0.488% ; recovery-V 24%
- **σ réalisé intraday** 2.424% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 65% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 126.05 (VA 124.65–126.25 ; dernier close 124.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 24% · rebond 60% · **stop −2.81%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.46% · baisse 37% (gap-down >1% 14% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −2.08%) · haut méd +0.47% · range méd 1.27%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −2.34%) · haut méd +0.58% · range méd 1.68%
- Excursion ouverture 30min (n=160) : bas méd −1.03% (p90 −2.43%) · haut méd +0.68% · range méd 1.87%
- Excursion ouverture 60min (n=160) : bas méd −1.13% (p90 −2.98%) · haut méd +0.79% · range méd 2.11%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 124.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 48% · séance 67% (109/159) · gap 20% · délai 0.4min · rebond 53% (61/109) (MFE +1.06%)
   - −1.0% : fill 30min 42% · séance 55% (90/159) · gap 14% · délai 1.0min · rebond 58% (54/90) (MFE +1.22%)
   - −1.5% : fill 30min 26% · séance 47% (73/159) · gap 8% · délai 21.5min · rebond 51% (40/73) (MFE +1.06%)
   - −2.0% : fill 30min 19% · séance 39% (61/159) · gap 4% · délai 41.0min · rebond 51% (35/61) (MFE +1.02%)
   - −3.0% : fill 30min 6% · séance 24% (41/159) · gap 1% · délai 97.2min · rebond 60% (27/41) (MFE +1.15%)
   - −4.0% : fill 30min 3% · séance 14% (25/159) · gap 0% · délai 282.0min · rebond 57% (15/25) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 10% (16/159) · gap 0% · délai 394.7min · rebond 66% (11/16) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.06%) → stop au-delà de −1.52% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −1.73%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.8%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=489 jambes) : jambe baissière méd −1.07% (p90 −2.62%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 94% (40/44) · rebond 49% (20/40)
      · −2.0% : fill 77% (32/44) · rebond 58% (19/32)
      · −3.0% : fill 48% (24/44) · rebond 51% (15/24)
      · −4.0% : fill 30% (15/44) · rebond 57% (9/15)
      · −5.0% : fill 26% (12/44) · rebond 57% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 48% (15/27) · rebond 74% (11/15)
      · −2.0% : fill 27% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 16% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 6% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (88 séances) :
      · −1.0% : fill 39% (35/88) · rebond 62% (23/35)
      · −2.0% : fill 25% (21/88) · rebond 30% (9/21)
      · −3.0% : fill 16% (12/88) · rebond 80% (9/12)
      · −4.0% : fill 10% (8/88) · rebond 54% (5/8)
      · −5.0% : fill 5% (3/88) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 67% si les 15 1res min sont vertes (75 cas) · 28% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 81% si début vert vs 22% si rouge (base 47% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **81%** · continue >prix actuel 57% ; creux résiduel méd -0.89% (q20 -1.87%) → **SL/trailing à −1.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.35% / q75 +2.4% → **scale +1.35% / runner +2.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **22%** (continue à baisser 64%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.96%** (au-delà de la MAE q10 -3.96%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.07% .. +2.19%] · haut q95 +3.15% · bas q05 -3.38%
   - 60min (n=160) : retour [-3.33% .. +2.19%] · haut q95 +3.37% · bas q05 -3.59%
   - 2h (n=160) : retour [-3.46% .. +2.64%] · haut q95 +3.41% · bas q05 -4.23%
   - 4h (n=160) : retour [-3.48% .. +2.8%] · haut q95 +3.44% · bas q05 -4.53%
   - 6h (n=160) : retour [-3.75% .. +3.61%] · haut q95 +4.19% · bas q05 -4.74%
   - session (n=160) : retour [-4.85% .. +3.47%] · haut q95 +4.55% · bas q05 -6.36%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.63 · part idiosyncratique 0.37
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.9  _(neutre)_
- **ADX** : 13.2  _(pas de tendance nette)_
- **MACD** : hist 0.195  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 10.2%
- **ATR** : 4.66 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.081  _(distribution)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 60.0  _(transition)_
- **MA** : MA20 123.78 · MA50 123.39 · MA200 118.69  _(prix > MA20)_
- **Dist MA** : MA20 +0.4% · MA50 +0.7% · MA200 +4.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (855363 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
