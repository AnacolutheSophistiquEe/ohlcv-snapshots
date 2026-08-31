# PRY

**Generated** : 2026-08-31T21:48:22.122272+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €120.20  

> 🟡 **WAIT-FOR-DIP** — spot +4.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €120.20 (+4.6% vs entrée) · entrée €114.93 · stop €110.51 · T1 €118.32 · R/R 0.77  
> ↳ P(T1 av. stop) 68 % _(réel 5 s)_ · EV/risk 0.07 _(réel 5 s)_ (GBM -0.043) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.390 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €114.25–€115.61 (mid €114.93)
- Spot actuel : €120.20 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : €110.51 (stop swing_plan-based (-8.06%))
- Targets : T1 €118.32 · R/R 0.77 | T2 €121.72 · R/R 1.54 | T3 €125.11 · R/R 2.3
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €110.51


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.50 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.06 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1270).
   - exécution **1.938 pt plus bas** dans le cas TYPIQUE (médiane), 1.938 au p90, **1.938 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 8.06 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0015 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.846 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0004** [0.0 ; 0.0154] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.4039** [0.3532 ; 0.4562] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3439** [0.2953 ; 0.3951] _(largeur 10.0 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 20.0 observations effectives », dont la borne haute a 95 % vaut environ 15.0 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 15.6 observations effectives », dont la borne haute a 95 % vaut environ 19.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.1 pt), swing (42.7 pt), deep (45.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.27 %** | CVaR **-5.76 %** | vol 2.64 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 1.79 % contre 2.91 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.48 % vs -7.48 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0247** (β de hausse 1.2243, asymétrie 0.837) vs FTSEMIB — 562 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.39× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 107.487 sur sr_based (2.27 ATR, 10.577 %) — p(stop avant cible) 0.1639 [0.13 ; 0.21], R/R 2.716, perte reelle 10.577 % (gap inclus), CVaR 10.577 %, EV 1.298 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 19 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 61.4 % de la queue et il ne reste que 29.65 EUR a partager. Prix du risque 0.019 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.9 ATR (stop 5.551 %) — p(stop avant cible) 0.4377 [0.39 ; 0.49], R/R 3.925, perte reelle 7.321 % (gap inclus), EV 0.0168 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ sr_based a 2.27 ATR (stop 10.577 %) — p(stop avant cible) 0.1639 [0.13 ; 0.21], R/R 2.716, perte reelle 10.577 % (gap inclus), EV 1.298 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 3.67 ATR (stop 15.735 %) — p(stop avant cible) 0.0204 [0.01 ; 0.04], R/R 1.826, perte reelle 15.735 % (gap inclus), EV 1.7096 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.74 % > budget 12.00 %
   - 🟢 support a 9.41 ATR (stop 36.867 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.779, perte reelle 36.867 % (gap inclus), EV 1.6904 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.87 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.92 %) — p(stop avant cible) 0.889 [0.85 ; 0.92], R/R 15.218, perte reelle 1.888 % (gap inclus), EV -0.6341 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 15.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.889, borne haute 0.919 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 0.7 % x 28.73 % + P(rien) 10.4 % x 8.11 % ne couvrent pas P(stop) 88.9 % x 1.89 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.839 %) — p(stop avant cible) 0.7828 [0.74 ; 0.82], R/R 9.72, perte reelle 2.956 % (gap inclus), EV -0.5417 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.783, borne haute 0.824 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 1.0 % x 28.73 % + P(rien) 20.7 % x 7.14 % ne couvrent pas P(stop) 78.3 % x 2.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.9 ATR (stop 4.418 %) — p(stop avant cible) 0.5339 [0.48 ; 0.59], R/R 4.883, perte reelle 5.884 % (gap inclus), EV -0.1767 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.534, borne haute 0.586 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 1.0 % x 28.73 % + P(rien) 45.6 % x 5.86 % ne couvrent pas P(stop) 53.4 % x 5.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.437 %) — p(stop avant cible) 0.3798 [0.33 ; 0.43], R/R 3.633, perte reelle 7.909 % (gap inclus), EV 0.3942 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 7.357 %) — p(stop avant cible) 0.3076 [0.26 ; 0.36], R/R 2.874, perte reelle 9.998 % (gap inclus), EV 0.3109 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.27 ATR (stop 9.444 %) — p(stop avant cible) 0.227 [0.19 ; 0.27], R/R 2.874, perte reelle 9.998 % (gap inclus), EV 0.9601 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 10.116 %) — p(stop avant cible) 0.181 [0.14 ; 0.22], R/R 2.84, perte reelle 10.116 % (gap inclus), EV 1.2486 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 3.67 ATR (stop 14.602 %) — p(stop avant cible) 0.0391 [0.02 ; 0.06], R/R 1.968, perte reelle 14.602 % (gap inclus), EV 1.6566 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.60 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.553 %) — p(stop avant cible) 0.0201 [0.01 ; 0.04], R/R 1.736, perte reelle 16.553 % (gap inclus), EV 1.6947 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.55 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.392 %) — p(stop avant cible) 0.0122 [0.00 ; 0.03], R/R 1.562, perte reelle 18.392 % (gap inclus), EV 1.6963 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.39 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.231 %) — p(stop avant cible) 0.0102 [0.00 ; 0.03], R/R 1.42, perte reelle 20.231 % (gap inclus), EV 1.6797 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.23 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.07 %) — p(stop avant cible) 0.0088 [0.00 ; 0.02], R/R 1.302, perte reelle 22.07 % (gap inclus), EV 1.6717 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.07 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 23.91 %) — p(stop avant cible) 0.0052 [0.00 ; 0.02], R/R 1.202, perte reelle 23.91 % (gap inclus), EV 1.6884 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.91 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 25.749 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 1.116, perte reelle 25.749 % (gap inclus), EV 1.6861 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.75 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 27.588 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 1.041, perte reelle 27.588 % (gap inclus), EV 1.6838 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.59 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.427 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.976, perte reelle 29.427 % (gap inclus), EV 1.6884 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.43 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 120.2, ATR14 4.4214 (3.678 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.343 ATR = 1.262 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.184 % | 119.9789 | 91.98 % | 93.95 % | 94.74 % | 95.63 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.368 % | 119.7579 | 85.35 % | 88.9 % | 91.17 % | 93.04 % | 95.2 % | 96.27 % |
| 0.15 ATR | 0.552 % | 119.5368 | 77.72 % | 84.14 % | 87.5 % | 90.56 % | 93.01 % | 94.25 % |
| 0.2 ATR | 0.736 % | 119.3157 | 69.5 % | 78.79 % | 82.64 % | 86.88 % | 90.71 % | 92.23 % |
| 0.25 ATR | 0.92 % | 119.0946 | 61.88 % | 74.13 % | 78.67 % | 83.2 % | 88.01 % | 90.31 % |
| 0.35 ATR | 1.287 % | 118.6525 | 49.11 % | 63.83 % | 71.03 % | 76.94 % | 83.72 % | 87.49 % |
| 0.5 ATR | 1.839 % | 117.9893 | 35.05 % | 52.13 % | 60.22 % | 68.29 % | 76.42 % | 81.84 % |
| 0.75 ATR | 2.759 % | 116.8839 | 19.11 % | 34.29 % | 43.35 % | 54.67 % | 64.74 % | 73.26 % |
| 1.0 ATR | 3.678 % | 115.7786 | 10.0 % | 23.19 % | 31.55 % | 44.33 % | 55.54 % | 65.19 % |
| 1.25 ATR | 4.598 % | 114.6732 | 5.74 % | 15.86 % | 23.91 % | 34.39 % | 47.25 % | 57.42 % |
| 1.5 ATR | 5.518 % | 113.5679 | 2.48 % | 9.71 % | 15.97 % | 24.25 % | 36.86 % | 48.94 % |
| 2.0 ATR | 7.357 % | 111.3571 | 0.4 % | 3.96 % | 7.44 % | 13.82 % | 24.88 % | 38.04 % |
| 2.5 ATR | 9.196 % | 109.1464 | 0.0 % | 1.59 % | 3.37 % | 7.75 % | 16.08 % | 27.65 % |
| 3.0 ATR | 11.035 % | 106.9357 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 10.19 % | 19.98 % |
| 4.0 ATR | 14.714 % | 102.5143 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.9 % | 11.5 % |
| 6.0 ATR | 22.07 % | 93.6714 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.31 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.49 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.73 ATR | 0.97 ATR | 1.21 ATR | 1.37 ATR | 1.85 ATR | 2.30 ATR |
| **5 s.** | 0.38 ATR | 0.86 ATR | 0.98 ATR | 1.28 ATR | 1.48 ATR | 1.70 ATR | 2.31 ATR | 2.88 ATR |
| **10 s.** | 0.53 ATR | 1.17 ATR | 1.30 ATR | 1.66 ATR | 2.00 ATR | 2.28 ATR | 3.04 ATR | 3.98 ATR |
| **20 s.** | 0.70 ATR | 1.47 ATR | 1.68 ATR | 2.24 ATR | 2.67 ATR | 3.00 ATR | 4.38 ATR | 5.65 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.6–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.759 %, prix 116.8837), p(touche) 34.29 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.726–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.759 %, prix 116.8837), p(touche) 43.35 % (en stress 94.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.984–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.678 %, prix 115.779), p(touche) 44.33 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.304–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.518 %, prix 113.5674), p(touche) 36.86 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.681–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.357 %, prix 111.3569), p(touche) 38.04 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.043 | EV/share : €-0.189 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 26 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 8.3 | bear 6.7 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.989% → cible +1.32% / stop −8.0%, p_fill 46%, n_eff≈20.0) : P(cible|rempli) **25%** · **EV/risk -0.039** (×p_fill ; si rempli -0.68% du capital)
  - **swing** (entrée dip −4.382% → cible +2.952% / stop −3.847%, p_fill 40%, n_eff≈16.1) : P(cible|rempli) **68%** · **EV/risk +0.070** (×p_fill ; si rempli +0.68% du capital)
  - **deep** (entrée dip −6.772% → cible +4.175% / stop −5.919%, p_fill 30%, n_eff≈15.6) : P(cible|rempli) **55%** · **EV/risk -0.019** (×p_fill ; si rempli -0.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→65% · +2.0%→39% · +3.0%→25% · +5.0%→5% · +8.0%→0%
- Range intraday médian 4.02% (p90 6.32%) · excursion haute méd. +1.3% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.369% vs midi 0.771% vs clôture 1.139% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.011)_ ; drift intra méd. -0.812% ; recovery-V 18%
- **σ réalisé intraday** 2.536% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 64% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 124.1225 (VA 123.2725–124.6325 ; dernier close 122.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 28% · rebond 73% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.73% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.45% · baisse 34% (gap-down >1% 14% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.23%) · haut méd +0.38% · range méd 1.41%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −2.4%) · haut méd +0.56% · range méd 1.75%
- Excursion ouverture 30min (n=160) : bas méd −1.04% (p90 −3.0%) · haut méd +0.69% · range méd 2.03%
- Excursion ouverture 60min (n=160) : bas méd −1.17% (p90 −3.22%) · haut méd +0.86% · range méd 2.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.05 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 69% (110/159) · gap 20% · délai 0.4min · rebond 52% (65/110) (MFE +1.07%)
   - −1.0% : fill 30min 44% · séance 59% (92/159) · gap 14% · délai 1.2min · rebond 57% (57/92) (MFE +1.11%)
   - −1.5% : fill 30min 32% · séance 48% (72/159) · gap 10% · délai 8.1min · rebond 56% (43/72) (MFE +1.15%)
   - −2.0% : fill 30min 22% · séance 40% (60/159) · gap 6% · délai 26.4min · rebond 58% (39/60) (MFE +1.11%)
   - −3.0% : fill 30min 7% · séance 28% (42/159) · gap 2% · délai 78.6min · rebond 73% (31/42) (MFE +1.73%)
   - −4.0% : fill 30min 2% · séance 19% (26/159) · gap 1% · délai 337.0min · rebond 54% (16/26) (MFE +1.15%)
   - −5.0% : fill 30min 1% · séance 12% (17/159) · gap 1% · délai 395.2min · rebond 62% (12/17) (MFE +1.17%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.5% (p90 −1.75%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −1.99%) → stop au-delà de −1.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.77%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=494 jambes) : jambe baissière méd −1.07% (p90 −2.63%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 90% (38/42) · rebond 46% (21/38)
      · −2.0% : fill 80% (32/42) · rebond 60% (21/32)
      · −3.0% : fill 61% (26/42) · rebond 71% (19/26)
      · −4.0% : fill 40% (15/42) · rebond 50% (9/15)
      · −5.0% : fill 34% (12/42) · rebond 48% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 59% (16/27) · rebond 70% (12/16)
      · −2.0% : fill 29% (7/27) · rebond 100% (7/7)
      · −3.0% : fill 14% (4/27) · rebond 68% (3/4)
      · −4.0% : fill 8% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (90 séances) :
      · −1.0% : fill 45% (38/90) · rebond 60% (24/38)
      · −2.0% : fill 28% (21/90) · rebond 40% (11/21)
      · −3.0% : fill 19% (12/90) · rebond 77% (9/12)
      · −4.0% : fill 14% (9/90) · rebond 55% (6/9)
      · −5.0% : fill 7% (4/90) · rebond 100% (4/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 68% si les 15 1res min sont vertes (75 cas) · 28% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 78% si début vert vs 23% si rouge (base 46% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -0.97% (q20 -2.16%) → **SL/trailing à −2.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.4% / q75 +2.51% → **scale +1.4% / runner +2.51%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **23%** (continue à baisser 64%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.07%** (au-delà de la MAE q10 -4.07%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.08% .. +2.84%] · haut q95 +3.2% · bas q05 -3.39%
   - 60min (n=160) : retour [-3.34% .. +2.24%] · haut q95 +3.54% · bas q05 -3.59%
   - 2h (n=160) : retour [-3.48% .. +2.64%] · haut q95 +3.73% · bas q05 -4.26%
   - 4h (n=160) : retour [-3.48% .. +3.23%] · haut q95 +4.06% · bas q05 -4.54%
   - 6h (n=160) : retour [-3.76% .. +3.73%] · haut q95 +4.51% · bas q05 -4.74%
   - session (n=160) : retour [-4.89% .. +3.78%] · haut q95 +5.11% · bas q05 -6.38%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 39.8  _(momentum baissier)_
- **ADX** : 26.5  _(tendance etablie)_
- **MACD** : hist -0.029  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 11.8%
- **ATR** : 4.42 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.386  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 47.2  _(transition)_
- **MA** : MA20 124.58 · MA50 129.9 · MA200 114.31  _(prix < MA20)_
- **Dist MA** : MA20 -3.5% · MA50 -7.5% · MA200 +5.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (788442 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
