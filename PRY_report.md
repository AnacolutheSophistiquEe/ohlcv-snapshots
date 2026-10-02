# PRY

**Generated** : 2026-10-02T00:13:57.652910+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €125.05  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €125.05 (+1.6% vs entrée) · entrée €123.13 · stop €118.56 · T1 €128.25 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 244 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €122.32–€123.94 (mid €123.13)
- Spot actuel : €125.05 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : €118.56 (plancher anti-bruit (R/R<2) ; -3.71 % depuis l'entree)
- Targets : T1 €128.25 · R/R 1.12 | T2 €133.36 · R/R 2.24 | T3 €138.48 · R/R 3.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €118.56


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.57 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.19 %)** : le gap seul le franchit 0.315 % des séances (4 fois sur 1270).
   - exécution **1.675 pt plus bas** dans le cas TYPIQUE (médiane), 3.961 au p90, **4.808 au pire**
   - perte réelle **7.321 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 5.19 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0067 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.86 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0003** [0.0 ; 0.0152] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.4438** [0.3921 ; 0.4965] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4045** [0.3537 ; 0.4568] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 82.4 observations effectives », dont la borne haute a 95 % vaut environ 3.6 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.24 %** | CVaR **-5.74 %** | vol 2.59 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.41 % contre 2.78 % aujourd'hui, rapport 0.50)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.46 % vs -7.52 % si l'on extrapolait par √5 _(rapport 0.86 ; < 1 = le √5 surestime)_
- **β de baisse : 1.033** (β de hausse 1.2244, asymétrie 0.8436) vs FTSEMIB — 566 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.353× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 122.7625 sur atr_grid (0.5 ATR, 1.829 %) — p(stop avant cible) 0.793 [0.75 ; 0.83], R/R 12.081, perte reelle 1.962 % (gap inclus), CVaR 3.742 %, EV 0.0207 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.5303 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 12.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.793, borne haute 0.833 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 3.74 % > budget 3.41 %
- Budget de queue : **3.41 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.206 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 43.2 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.86 ATR (stop 5.052 %) — p(stop avant cible) 0.4901 [0.44 ; 0.54], R/R 4.535, perte reelle 5.226 % (gap inclus), EV 0.2145 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 6.46 % > budget 3.41 %
   - ⚪ swing_based a 1.38 ATR (stop 6.945 %) — p(stop avant cible) 0.3242 [0.28 ; 0.37], R/R 3.348, perte reelle 7.081 % (gap inclus), EV 0.6983 % — **REFUSE**
      - refuse : cible atteinte seulement 2.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 7.79 % > budget 3.41 %
   - 🔴 support a 4.61 ATR (stop 18.748 %) — p(stop avant cible) 0.0107 [0.00 ; 0.03], R/R 1.197, perte reelle 19.809 % (gap inclus), EV 1.491 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.83 % > budget 3.41 %
      - ⚠ support DETECTE a 0.76 ATR du spot — compartiment <1, mesure a 46.7 % de casse (IC clusterise [0.436 ; 0.499] sur 1172 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 10.16 ATR (stop 39.061 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.607, perte reelle 39.061 % (gap inclus), EV 1.5015 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.63 % > budget 3.41 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.915 %) — p(stop avant cible) 0.8917 [0.86 ; 0.92], R/R 23.122, perte reelle 1.025 % (gap inclus), EV 0.023 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 23.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.892, borne haute 0.921 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.829 %) — p(stop avant cible) 0.793 [0.75 ; 0.83], R/R 12.081, perte reelle 1.962 % (gap inclus), EV 0.0207 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 12.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.793, borne haute 0.833 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 3.74 % > budget 3.41 %
   - ⚪ grid_snapped a 0.86 ATR (stop 4.254 %) — p(stop avant cible) 0.5548 [0.50 ; 0.61], R/R 5.353, perte reelle 4.428 % (gap inclus), EV 0.1412 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.555, borne haute 0.607 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.81 % > budget 3.41 %
   - ⚪ grid_snapped a 1.38 ATR (stop 6.148 %) — p(stop avant cible) 0.388 [0.34 ; 0.44], R/R 3.752, perte reelle 6.317 % (gap inclus), EV 0.4883 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 7.35 % > budget 3.41 %
   - ⚪ atr_grid a 2.25 ATR (stop 8.232 %) — p(stop avant cible) 0.253 [0.21 ; 0.30], R/R 2.841, perte reelle 8.344 % (gap inclus), EV 0.8785 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.80 % > budget 3.41 %
   - ⚪ atr_grid a 2.5 ATR (stop 9.146 %) — p(stop avant cible) 0.2129 [0.17 ; 0.26], R/R 2.561, perte reelle 9.255 % (gap inclus), EV 0.9211 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.61 % > budget 3.41 %
   - ⚪ atr_grid a 2.75 ATR (stop 10.061 %) — p(stop avant cible) 0.1665 [0.13 ; 0.21], R/R 2.343, perte reelle 10.116 % (gap inclus), EV 1.0651 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.24 % > budget 3.41 %
   - ⚪ atr_grid a 3.0 ATR (stop 10.976 %) — p(stop avant cible) 0.1107 [0.08 ; 0.15], R/R 2.129, perte reelle 11.131 % (gap inclus), EV 1.2255 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.32 % > budget 3.41 %
   - ⚪ atr_grid a 3.5 ATR (stop 12.805 %) — p(stop avant cible) 0.0725 [0.05 ; 0.10], R/R 1.821, perte reelle 13.016 % (gap inclus), EV 1.3042 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.11 % > budget 3.41 %
   - ⚪ atr_grid a 4.0 ATR (stop 14.634 %) — p(stop avant cible) 0.0342 [0.02 ; 0.06], R/R 1.602, perte reelle 14.794 % (gap inclus), EV 1.4659 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.68 % > budget 3.41 %
   - 🔴 grid_snapped a 4.61 ATR (stop 17.951 %) — p(stop avant cible) 0.0109 [0.00 ; 0.03], R/R 1.226, perte reelle 19.329 % (gap inclus), EV 1.4939 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.77 % > budget 3.41 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.122 %) — p(stop avant cible) 0.0089 [0.00 ; 0.02], R/R 1.114, perte reelle 21.269 % (gap inclus), EV 1.4833 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.00 % > budget 3.41 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.951 %) — p(stop avant cible) 0.0077 [0.00 ; 0.02], R/R 1.039, perte reelle 22.815 % (gap inclus), EV 1.4794 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.05 % > budget 3.41 %
   - ⚪ atr_grid a 6.5 ATR (stop 23.78 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 0.958, perte reelle 24.751 % (gap inclus), EV 1.4852 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.93 % > budget 3.41 %
   - ⚪ atr_grid a 7.0 ATR (stop 25.61 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.904, perte reelle 26.211 % (gap inclus), EV 1.4969 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.73 % > budget 3.41 %
   - ⚪ atr_grid a 7.5 ATR (stop 27.439 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.79, perte reelle 29.996 % (gap inclus), EV 1.487 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.89 % > budget 3.41 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.268 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.733, perte reelle 32.353 % (gap inclus), EV 1.4963 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.75 % > budget 3.41 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 125.05, ATR14 4.575 (3.659 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 1.259 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.183 % | 124.8213 | 91.88 % | 93.95 % | 94.74 % | 95.53 % | 97.2 % | 97.88 % |
| 0.1 ATR | 0.366 % | 124.5925 | 85.25 % | 88.9 % | 91.17 % | 92.94 % | 95.1 % | 96.27 % |
| 0.15 ATR | 0.549 % | 124.3638 | 77.82 % | 84.34 % | 87.5 % | 90.46 % | 92.91 % | 94.25 % |
| 0.2 ATR | 0.732 % | 124.135 | 69.8 % | 79.19 % | 82.74 % | 86.98 % | 90.71 % | 92.33 % |
| 0.25 ATR | 0.915 % | 123.9063 | 62.08 % | 74.33 % | 78.67 % | 83.2 % | 88.11 % | 90.31 % |
| 0.35 ATR | 1.28 % | 123.4488 | 49.21 % | 63.63 % | 70.83 % | 76.74 % | 83.82 % | 87.49 % |
| 0.5 ATR | 1.829 % | 122.7625 | 34.95 % | 51.83 % | 60.02 % | 67.89 % | 76.52 % | 81.94 % |
| 0.75 ATR | 2.744 % | 121.6188 | 19.21 % | 34.39 % | 43.25 % | 54.37 % | 64.74 % | 73.26 % |
| 1.0 ATR | 3.659 % | 120.475 | 9.8 % | 23.29 % | 31.55 % | 44.14 % | 55.34 % | 64.88 % |
| 1.25 ATR | 4.573 % | 119.3313 | 5.54 % | 15.76 % | 23.81 % | 34.29 % | 46.95 % | 57.21 % |
| 1.5 ATR | 5.488 % | 118.1875 | 2.48 % | 9.51 % | 15.97 % | 24.16 % | 36.36 % | 48.64 % |
| 2.0 ATR | 7.317 % | 115.9 | 0.4 % | 3.96 % | 7.54 % | 13.72 % | 24.18 % | 37.13 % |
| 2.5 ATR | 9.146 % | 113.6125 | 0.0 % | 1.59 % | 3.37 % | 7.95 % | 15.58 % | 26.54 % |
| 3.0 ATR | 10.976 % | 111.325 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 9.69 % | 18.97 % |
| 4.0 ATR | 14.634 % | 106.75 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.8 % | 11.1 % |
| 6.0 ATR | 21.951 % | 97.6 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.29 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.48 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 0.97 ATR | 1.21 ATR | 1.37 ATR | 1.85 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.86 ATR | 0.98 ATR | 1.28 ATR | 1.48 ATR | 1.70 ATR | 2.32 ATR | 2.89 ATR |
| **10 s.** | 0.53 ATR | 1.16 ATR | 1.30 ATR | 1.64 ATR | 1.97 ATR | 2.24 ATR | 2.97 ATR | 3.96 ATR |
| **20 s.** | 0.70 ATR | 1.46 ATR | 1.66 ATR | 2.19 ATR | 2.60 ATR | 2.93 ATR | 4.29 ATR | 5.63 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.598–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.744 %, prix 121.6186), p(touche) 34.39 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.724–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.744 %, prix 121.6186), p(touche) 43.25 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.979–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.659 %, prix 120.4744), p(touche) 44.14 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.296–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.488 %, prix 118.1873), p(touche) 36.36 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.658–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.317 %, prix 115.9001), p(touche) 37.13 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.07 | EV/share : €-0.322 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 10 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.0 | bear 5.0 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 500.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.696% → cible +2.436% / stop −8.0%, p_fill 77%, n_eff≈82.4) : P(cible|rempli) **23%** · **EV/risk -0.056** (×p_fill ; si rempli -0.58% du capital)
  - **swing** (entrée dip −1.531% → cible +4.154% / stop −3.716%, p_fill 66%, n_eff≈76.2) : P(cible|rempli) **33%** · **EV/risk -0.189** (×p_fill ; si rempli -1.06% du capital)
  - **deep** (entrée dip −2.372% → cible +5.925% / stop −5.621%, p_fill 68%, n_eff≈75.8) : P(cible|rempli) **33%** · **EV/risk -0.148** (×p_fill ; si rempli -1.22% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→38% · +3.0%→24% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.71% (p90 6.32%) · excursion haute méd. +1.4% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.214% vs midi 0.772% vs clôture 1.067% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr -0.006)_ ; drift intra méd. -0.527% ; recovery-V 23%
- **σ réalisé intraday** 2.43% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 67% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 126.1525 (VA 125.3125–126.7825 ; dernier close 124.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 24% · rebond 60% · **stop −2.81%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 36% (gap-down >1% 13% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.07%) · haut méd +0.45% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.95% (p90 −2.34%) · haut méd +0.57% · range méd 1.66%
- Excursion ouverture 30min (n=160) : bas méd −1.01% (p90 −2.42%) · haut méd +0.64% · range méd 1.85%
- Excursion ouverture 60min (n=160) : bas méd −1.09% (p90 −2.96%) · haut méd +0.78% · range méd 2.1%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 124.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 48% · séance 67% (110/159) · gap 20% · délai 0.4min · rebond 54% (62/110) (MFE +1.1%)
   - −1.0% : fill 30min 41% · séance 56% (91/159) · gap 13% · délai 1.3min · rebond 60% (55/91) (MFE +1.26%)
   - −1.5% : fill 30min 25% · séance 46% (73/159) · gap 7% · délai 21.5min · rebond 51% (40/73) (MFE +1.06%)
   - −2.0% : fill 30min 19% · séance 38% (61/159) · gap 3% · délai 41.0min · rebond 51% (35/61) (MFE +1.02%)
   - −3.0% : fill 30min 6% · séance 24% (41/159) · gap 1% · délai 97.2min · rebond 60% (27/41) (MFE +1.15%)
   - −4.0% : fill 30min 3% · séance 14% (25/159) · gap 0% · délai 282.0min · rebond 57% (15/25) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 10% (16/159) · gap 0% · délai 394.7min · rebond 66% (11/16) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.99%) → stop au-delà de −1.5% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −1.73%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.8%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=482 jambes) : jambe baissière méd −1.07% (p90 −2.61%) · ~7.0 jambes/séance
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
      · −1.0% : fill 41% (36/88) · rebond 65% (24/36)
      · −2.0% : fill 24% (21/88) · rebond 30% (9/21)
      · −3.0% : fill 15% (12/88) · rebond 80% (9/12)
      · −4.0% : fill 10% (8/88) · rebond 54% (5/8)
      · −5.0% : fill 4% (3/88) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 64% si les 15 1res min sont vertes (76 cas) · 28% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 81% si début vert vs 22% si rouge (base 46% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **81%** · continue >prix actuel 47% ; creux résiduel méd -1.03% (q20 -1.89%) → **SL/trailing à −1.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.02% → **scale +1.08% / runner +2.02%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **22%** (continue à baisser 65%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.82%** (au-delà de la MAE q10 -3.82%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.98% .. +2.19%] · haut q95 +3.14% · bas q05 -3.37%
   - 60min (n=160) : retour [-3.3% .. +2.18%] · haut q95 +3.36% · bas q05 -3.59%
   - 2h (n=160) : retour [-3.39% .. +2.64%] · haut q95 +3.41% · bas q05 -4.14%
   - 4h (n=160) : retour [-3.47% .. +2.77%] · haut q95 +3.43% · bas q05 -4.49%
   - 6h (n=160) : retour [-3.74% .. +3.57%] · haut q95 +4.18% · bas q05 -4.7%
   - session (n=160) : retour [-4.77% .. +3.42%] · haut q95 +4.54% · bas q05 -6.33%


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.6  _(neutre)_
- **ADX** : 12.8  _(pas de tendance nette)_
- **MACD** : hist 0.222  _(pas de croisement recent)_
- **BB** : %B 0.58 · largeur 9.8%
- **ATR** : 4.57 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.116  _(distribution)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 59.3  _(transition)_
- **MA** : MA20 124.03 · MA50 123.36 · MA200 118.89  _(prix > MA20)_
- **Dist MA** : MA20 +0.8% · MA50 +1.4% · MA200 +5.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (854889 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
