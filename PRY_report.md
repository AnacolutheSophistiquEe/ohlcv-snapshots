# PRY

**Generated** : 2026-09-03T21:48:51.685048+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €119.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €119.80 (+2.0% vs entrée) · entrée €117.50 · stop €108.10 · T1 €119.00 · R/R 0.16  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk -0.044 _(réel 5 s)_ (GBM -0.068) · ¼-Kelly 0.098 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.440 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €117.20–€117.80 (mid €117.50)
- Spot actuel : €119.80 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : €108.10 (stop swing_plan-based (-7.8%))
- Targets : T1 €119.00 · R/R 0.16 | T2 €120.50 · R/R 0.32 | T3 €121.99 · R/R 0.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €108.10


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.50 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.8 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1270).
   - exécution **2.198 pt plus bas** dans le cas TYPIQUE (médiane), 2.198 au p90, **2.198 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 7.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0017 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.846 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0004** [0.0 ; 0.0154] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.3958** [0.3453 ; 0.448] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.358** [0.3088 ; 0.4095] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 20.6 observations effectives », dont la borne haute a 95 % vaut environ 14.5 %.
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.7 observations effectives », dont la borne haute a 95 % vaut environ 17.9 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.1 pt), swing (42.9 pt), deep (45.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.19 %** | CVaR **-4.89 %** | vol 2.54 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.79 % contre 2.91 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.48 % vs -7.48 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0284** (β de hausse 1.225, asymétrie 0.8395) vs FTSEMIB — 563 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.414× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 106.9107 sur atr_grid (3.0 ATR, 10.759 %) — p(stop avant cible) 0.1476 [0.11 ; 0.19], R/R 2.713, perte reelle 10.759 % (gap inclus), CVaR 10.759 %, EV 1.2037 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.4 % de la queue et il ne reste que -955.87 EUR a partager. Prix du risque -0.692 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.83 ATR (stop 5.058 %) — p(stop avant cible) 0.4894 [0.44 ; 0.54], R/R 3.988, perte reelle 7.321 % (gap inclus), EV -0.5632 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 1.0 % x 29.19 % + P(rien) 50.0 % x 5.44 % ne couvrent pas P(stop) 48.9 % x 7.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.24 ATR (stop 10.111 %) — p(stop avant cible) 0.1779 [0.14 ; 0.22], R/R 2.887, perte reelle 10.111 % (gap inclus), EV 1.1319 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 3.68 ATR (stop 15.297 %) — p(stop avant cible) 0.0265 [0.01 ; 0.05], R/R 1.908, perte reelle 15.297 % (gap inclus), EV 1.5816 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.30 % > budget 12.00 %
   - 🟢 support a 9.6 ATR (stop 36.499 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.8, perte reelle 36.499 % (gap inclus), EV 1.5652 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.50 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.897 %) — p(stop avant cible) 0.8924 [0.86 ; 0.92], R/R 15.595, perte reelle 1.872 % (gap inclus), EV -0.6439 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 15.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.892, borne haute 0.922 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 0.7 % x 29.19 % + P(rien) 10.1 % x 8.19 % ne couvrent pas P(stop) 89.2 % x 1.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.793 %) — p(stop avant cible) 0.7908 [0.75 ; 0.83], R/R 10.161, perte reelle 2.873 % (gap inclus), EV -0.55 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.791, borne haute 0.831 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 1.0 % x 29.19 % + P(rien) 19.9 % x 7.17 % ne couvrent pas P(stop) 79.1 % x 2.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.83 ATR (stop 4.047 %) — p(stop avant cible) 0.575 [0.52 ; 0.63], R/R 5.212, perte reelle 5.601 % (gap inclus), EV -0.4039 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.575, borne haute 0.626 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 1.0 % x 29.19 % + P(rien) 41.5 % x 6.08 % ne couvrent pas P(stop) 57.5 % x 5.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.276 %) — p(stop avant cible) 0.3943 [0.34 ; 0.45], R/R 3.691, perte reelle 7.909 % (gap inclus), EV 0.2293 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ grid_snapped a 2.24 ATR (stop 9.1 %) — p(stop avant cible) 0.2327 [0.19 ; 0.28], R/R 2.92, perte reelle 9.998 % (gap inclus), EV 0.8009 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 10.759 %) — p(stop avant cible) 0.1476 [0.11 ; 0.19], R/R 2.713, perte reelle 10.759 % (gap inclus), EV 1.2037 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 3.68 ATR (stop 14.285 %) — p(stop avant cible) 0.0485 [0.03 ; 0.07], R/R 2.044, perte reelle 14.285 % (gap inclus), EV 1.4714 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.28 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.139 %) — p(stop avant cible) 0.02 [0.01 ; 0.04], R/R 1.809, perte reelle 16.139 % (gap inclus), EV 1.5767 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.14 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.932 %) — p(stop avant cible) 0.0123 [0.00 ; 0.03], R/R 1.628, perte reelle 17.932 % (gap inclus), EV 1.5728 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.93 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.725 %) — p(stop avant cible) 0.0107 [0.00 ; 0.03], R/R 1.48, perte reelle 19.725 % (gap inclus), EV 1.5558 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.72 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.518 %) — p(stop avant cible) 0.0094 [0.00 ; 0.02], R/R 1.357, perte reelle 21.518 % (gap inclus), EV 1.5426 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.52 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 23.311 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 1.252, perte reelle 23.311 % (gap inclus), EV 1.545 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.31 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 25.104 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 1.163, perte reelle 25.104 % (gap inclus), EV 1.5566 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.10 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 26.898 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 1.085, perte reelle 26.898 % (gap inclus), EV 1.5576 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.90 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 28.691 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 1.017, perte reelle 28.691 % (gap inclus), EV 1.5636 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.69 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 119.8, ATR14 4.2964 (3.586 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 1.234 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.179 % | 119.5852 | 92.08 % | 94.05 % | 94.84 % | 95.63 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.359 % | 119.3704 | 85.45 % | 89.0 % | 91.27 % | 93.04 % | 95.2 % | 96.27 % |
| 0.15 ATR | 0.538 % | 119.1555 | 77.82 % | 84.24 % | 87.6 % | 90.56 % | 93.01 % | 94.25 % |
| 0.2 ATR | 0.717 % | 118.9407 | 69.6 % | 78.89 % | 82.74 % | 86.88 % | 90.71 % | 92.23 % |
| 0.25 ATR | 0.897 % | 118.7259 | 61.98 % | 74.33 % | 78.87 % | 83.3 % | 88.21 % | 90.31 % |
| 0.35 ATR | 1.255 % | 118.2963 | 49.21 % | 64.02 % | 71.23 % | 77.04 % | 83.92 % | 87.49 % |
| 0.5 ATR | 1.793 % | 117.6518 | 35.05 % | 52.33 % | 60.42 % | 68.39 % | 76.62 % | 81.84 % |
| 0.75 ATR | 2.69 % | 116.5777 | 19.11 % | 34.49 % | 43.55 % | 54.77 % | 64.94 % | 73.16 % |
| 1.0 ATR | 3.586 % | 115.5036 | 10.0 % | 23.29 % | 31.75 % | 44.53 % | 55.74 % | 64.98 % |
| 1.25 ATR | 4.483 % | 114.4295 | 5.74 % | 15.96 % | 24.11 % | 34.49 % | 47.45 % | 57.21 % |
| 1.5 ATR | 5.38 % | 113.3554 | 2.48 % | 9.71 % | 16.07 % | 24.35 % | 37.06 % | 48.74 % |
| 2.0 ATR | 7.173 % | 111.2071 | 0.4 % | 3.96 % | 7.44 % | 13.82 % | 24.98 % | 37.74 % |
| 2.5 ATR | 8.966 % | 109.0589 | 0.0 % | 1.59 % | 3.37 % | 7.75 % | 16.08 % | 27.35 % |
| 3.0 ATR | 10.759 % | 106.9107 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 10.19 % | 19.78 % |
| 4.0 ATR | 14.345 % | 102.6143 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.9 % | 11.4 % |
| 6.0 ATR | 21.518 % | 94.0214 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.31 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.49 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.73 ATR | 0.97 ATR | 1.22 ATR | 1.38 ATR | 1.85 ATR | 2.30 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.99 ATR | 1.29 ATR | 1.48 ATR | 1.71 ATR | 2.31 ATR | 2.88 ATR |
| **10 s.** | 0.54 ATR | 1.17 ATR | 1.31 ATR | 1.67 ATR | 2.00 ATR | 2.28 ATR | 3.04 ATR | 3.98 ATR |
| **20 s.** | 0.70 ATR | 1.46 ATR | 1.67 ATR | 2.23 ATR | 2.65 ATR | 2.98 ATR | 4.36 ATR | 5.65 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.395–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.69 %, prix 116.5774), p(touche) 34.49 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.729–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.69 %, prix 116.5774), p(touche) 43.55 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.989–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.586 %, prix 115.504), p(touche) 44.53 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.309–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.38 %, prix 113.3548), p(touche) 37.06 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.67–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.173 %, prix 111.2067), p(touche) 37.74 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.068 | EV/share : €-0.639 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 31 % | T3 14 %
- Kelly (position) : f* 0.391 | ¼-Kelly 0.098 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.4 | bear 7.1 | side 85.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.913% → cible +1.274% / stop −8.0%, p_fill 49%, n_eff≈20.6) : P(cible|rempli) **22%** · **EV/risk -0.044** (×p_fill ; si rempli -0.71% du capital)
  - **swing** (entrée dip −4.214% → cible +2.848% / stop −3.744%, p_fill 37%, n_eff≈16.7) : P(cible|rempli) **65%** · **EV/risk +0.038** (×p_fill ; si rempli +0.38% du capital)
  - **deep** (entrée dip −6.51% → cible +4.028% / stop −5.754%, p_fill 36%, n_eff≈15.7) : P(cible|rempli) **40%** · **EV/risk -0.029** (×p_fill ; si rempli -0.46% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→65% · +2.0%→38% · +3.0%→25% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.96% (p90 6.32%) · excursion haute méd. +1.25% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.359% vs midi 0.759% vs clôture 1.106% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr -0.02)_ ; drift intra méd. -0.859% ; recovery-V 17%
- **σ réalisé intraday** 2.472% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 67% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 118.2512 (VA 117.0762–118.6037 ; dernier close 117.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 29% · rebond 68% · **stop −2.77%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.4% · baisse 36% (gap-down >1% 14% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.12%) · haut méd +0.38% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −2.37%) · haut méd +0.58% · range méd 1.71%
- Excursion ouverture 30min (n=160) : bas méd −1.03% (p90 −2.96%) · haut méd +0.69% · range méd 1.97%
- Excursion ouverture 60min (n=160) : bas méd −1.13% (p90 −3.19%) · haut méd +0.86% · range méd 2.21%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 117.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 70% (110/159) · gap 21% · délai 0.3min · rebond 49% (63/110) (MFE +0.99%)
   - −1.0% : fill 30min 44% · séance 60% (93/159) · gap 14% · délai 1.3min · rebond 56% (57/93) (MFE +1.11%)
   - −1.5% : fill 30min 31% · séance 50% (73/159) · gap 10% · délai 10.9min · rebond 52% (42/73) (MFE +1.06%)
   - −2.0% : fill 30min 21% · séance 41% (60/159) · gap 6% · délai 28.6min · rebond 56% (38/60) (MFE +1.1%)
   - −3.0% : fill 30min 7% · séance 29% (42/159) · gap 2% · délai 91.4min · rebond 68% (30/42) (MFE +1.69%)
   - −4.0% : fill 30min 2% · séance 19% (26/159) · gap 1% · délai 337.0min · rebond 54% (16/26) (MFE +1.15%)
   - −5.0% : fill 30min 1% · séance 12% (17/159) · gap 1% · délai 395.2min · rebond 62% (12/17) (MFE +1.17%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.75%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −2.0%) → stop au-delà de −1.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.77%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=496 jambes) : jambe baissière méd −1.07% (p90 −2.63%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 91% (38/42) · rebond 42% (20/38)
      · −2.0% : fill 74% (31/42) · rebond 60% (20/31)
      · −3.0% : fill 56% (25/42) · rebond 70% (18/25)
      · −4.0% : fill 38% (15/42) · rebond 50% (9/15)
      · −5.0% : fill 31% (12/42) · rebond 48% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 63% (17/27) · rebond 74% (13/17)
      · −2.0% : fill 35% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 21% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 8% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (90 séances) :
      · −1.0% : fill 45% (38/90) · rebond 60% (24/38)
      · −2.0% : fill 28% (21/90) · rebond 40% (11/21)
      · −3.0% : fill 19% (12/90) · rebond 77% (9/12)
      · −4.0% : fill 14% (9/90) · rebond 55% (6/9)
      · −5.0% : fill 7% (4/90) · rebond 100% (4/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 63% si les 15 1res min sont vertes (76 cas) · 27% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 73% si début vert vs 20% si rouge (base 44% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **73%** · continue >prix actuel 51% ; creux résiduel méd -1.14% (q20 -2.22%) → **SL/trailing à −2.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.26% / q75 +2.27% → **scale +1.26% / runner +2.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **20%** (continue à baisser 66%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.05% .. +2.8%] · haut q95 +3.17% · bas q05 -3.38%
   - 60min (n=160) : retour [-3.32% .. +2.22%] · haut q95 +3.47% · bas q05 -3.59%
   - 2h (n=160) : retour [-3.44% .. +2.64%] · haut q95 +3.6% · bas q05 -4.21%
   - 4h (n=160) : retour [-3.47% .. +3.21%] · haut q95 +4.02% · bas q05 -4.52%
   - 6h (n=160) : retour [-3.75% .. +3.7%] · haut q95 +4.49% · bas q05 -4.73%
   - session (n=160) : retour [-4.81% .. +3.64%] · haut q95 +5.05% · bas q05 -6.35%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.2  _(momentum baissier)_
- **ADX** : 27.9  _(tendance etablie)_
- **MACD** : hist -0.157  _(bearish_recent)_
- **BB** : %B 0.26 · largeur 13.8%
- **ATR** : 4.3 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.435  _(distribution)_
- **Vol ratio** : 0.91  _(volume normal)_
- **Choppiness** : 49.0  _(transition)_
- **MA** : MA20 123.87 · MA50 128.13 · MA200 114.84  _(prix < MA20)_
- **Dist MA** : MA20 -3.3% · MA50 -6.5% · MA200 +4.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (760953 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
