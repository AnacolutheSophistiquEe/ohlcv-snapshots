# PRY

**Generated** : 2026-09-25T21:56:08.621525+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €122.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)  
> ↳ spot €122.40 (+0.7% vs entrée) · entrée €121.56 · stop €116.79 · T1 €125.67 · R/R 0.86  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.315 _(réel 5 s)_ (GBM -0.004) · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.110 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €120.74–€122.39 (mid €121.56)
- Spot actuel : €122.40 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €116.79 (stop swing_plan-based (-4.58%))
- Targets : T1 €125.67 · R/R 0.86 | T2 €129.78 · R/R 1.72 | T3 €133.89 · R/R 2.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €116.79


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.57 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.58 %)** : le gap seul le franchit 0.63 % des séances (8 fois sur 1270).
   - exécution **0.689 pt plus bas** dans le cas TYPIQUE (médiane), 3.442 au p90, **5.418 au pire**
   - perte réelle **6.062 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 4.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0093 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.86 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0003** [0.0 ; 0.0152] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.4022** [0.3515 ; 0.4545] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3631** [0.3137 ; 0.4148] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 35.1 observations effectives », dont la borne haute a 95 % vaut environ 8.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.8 pt), swing (30.9 pt), deep (30.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.24 %** | CVaR **-5.74 %** | vol 2.58 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.47 % contre 2.80 % aujourd'hui, rapport 0.52)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.49 % vs -7.52 % si l'on extrapolait par √5 _(rapport 0.864 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0377** (β de hausse 1.2286, asymétrie 0.8446) vs FTSEMIB — 566 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.502× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 108.0857 sur atr_grid (3.0 ATR, 11.695 %) — p(stop avant cible) 0.08 [0.05 ; 0.11], R/R 2.252, perte reelle 11.695 % (gap inclus), CVaR 11.695 %, EV 1.3559 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 22 des 22 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 49.8 % de la queue et il ne reste que -1061.59 EUR a partager. Prix du risque -0.364 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.42 ATR (stop 3.807 %) — p(stop avant cible) 0.6034 [0.55 ; 0.65], R/R 4.701, perte reelle 5.601 % (gap inclus), EV -0.866 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.603, borne haute 0.654 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 1.2 % x 26.33 % + P(rien) 38.4 % x 5.70 % ne couvrent pas P(stop) 60.3 % x 5.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.847 %) — p(stop avant cible) 0.4186 [0.37 ; 0.47], R/R 3.329, perte reelle 7.909 % (gap inclus), EV -0.3758 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 1.2 % x 26.33 % + P(rien) 56.9 % x 4.59 % ne couvrent pas P(stop) 41.9 % x 7.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.33 ATR (stop 7.367 %) — p(stop avant cible) 0.2922 [0.25 ; 0.34], R/R 2.634, perte reelle 9.998 % (gap inclus), EV 0.1322 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 support a 3.86 ATR (stop 17.228 %) — p(stop avant cible) 0.0128 [0.00 ; 0.03], R/R 1.529, perte reelle 17.228 % (gap inclus), EV 1.5003 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.23 % > budget 12.00 %
      - ⚠ support DETECTE a 0.32 ATR du spot — compartiment <1, mesure a 48.0 % de casse (IC clusterise [0.451 ; 0.508] sur 1182 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 9.19 ATR (stop 37.98 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.693, perte reelle 37.98 % (gap inclus), EV 1.4953 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.98 % > budget 12.00 %
   - ⚪ grid_snapped a 0.42 ATR (stop 2.801 %) — p(stop avant cible) 0.6894 [0.64 ; 0.74], R/R 6.083, perte reelle 4.329 % (gap inclus), EV -0.7538 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.689, borne haute 0.736 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 1.2 % x 26.33 % + P(rien) 29.8 % x 6.40 % ne couvrent pas P(stop) 68.9 % x 4.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.33 ATR (stop 6.361 %) — p(stop avant cible) 0.3848 [0.33 ; 0.44], R/R 3.329, perte reelle 7.909 % (gap inclus), EV 0.0628 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 8.771 %) — p(stop avant cible) 0.235 [0.19 ; 0.28], R/R 2.634, perte reelle 9.998 % (gap inclus), EV 0.6547 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 9.746 %) — p(stop avant cible) 0.1901 [0.15 ; 0.23], R/R 2.634, perte reelle 9.998 % (gap inclus), EV 0.936 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 10.72 %) — p(stop avant cible) 0.1398 [0.11 ; 0.18], R/R 2.456, perte reelle 10.72 % (gap inclus), EV 1.1509 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 11.695 %) — p(stop avant cible) 0.08 [0.05 ; 0.11], R/R 2.252, perte reelle 11.695 % (gap inclus), EV 1.3559 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 13.644 %) — p(stop avant cible) 0.0496 [0.03 ; 0.08], R/R 1.93, perte reelle 13.644 % (gap inclus), EV 1.3948 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.64 % > budget 12.00 %
   - 🔴 grid_snapped a 3.86 ATR (stop 16.223 %) — p(stop avant cible) 0.0183 [0.01 ; 0.04], R/R 1.623, perte reelle 16.223 % (gap inclus), EV 1.5032 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.22 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 19.491 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 1.351, perte reelle 19.491 % (gap inclus), EV 1.4895 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.49 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 21.44 %) — p(stop avant cible) 0.0086 [0.00 ; 0.02], R/R 1.228, perte reelle 21.44 % (gap inclus), EV 1.4748 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.44 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 23.389 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 1.126, perte reelle 23.389 % (gap inclus), EV 1.4866 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.39 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 25.338 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 1.039, perte reelle 25.338 % (gap inclus), EV 1.4865 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.34 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 27.288 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 0.965, perte reelle 27.288 % (gap inclus), EV 1.4898 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 29.237 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.901, perte reelle 29.237 % (gap inclus), EV 1.4922 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.24 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 31.186 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.844, perte reelle 31.186 % (gap inclus), EV 1.4895 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.19 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 122.4, ATR14 4.7714 (3.898 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.345 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.195 % | 122.1614 | 91.88 % | 93.95 % | 94.74 % | 95.53 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.39 % | 121.9229 | 85.25 % | 88.9 % | 91.17 % | 92.94 % | 95.2 % | 96.27 % |
| 0.15 ATR | 0.585 % | 121.6843 | 77.82 % | 84.34 % | 87.5 % | 90.46 % | 93.01 % | 94.25 % |
| 0.2 ATR | 0.78 % | 121.4457 | 69.7 % | 79.09 % | 82.64 % | 86.88 % | 90.81 % | 92.33 % |
| 0.25 ATR | 0.975 % | 121.2071 | 61.98 % | 74.23 % | 78.57 % | 83.1 % | 88.21 % | 90.41 % |
| 0.35 ATR | 1.364 % | 120.73 | 49.31 % | 63.73 % | 70.83 % | 76.64 % | 83.92 % | 87.59 % |
| 0.5 ATR | 1.949 % | 120.0143 | 34.95 % | 51.73 % | 59.92 % | 67.69 % | 76.62 % | 81.94 % |
| 0.75 ATR | 2.924 % | 118.8214 | 19.11 % | 34.19 % | 42.96 % | 54.17 % | 64.84 % | 73.26 % |
| 1.0 ATR | 3.898 % | 117.6286 | 9.8 % | 23.09 % | 31.25 % | 43.84 % | 55.44 % | 64.98 % |
| 1.25 ATR | 4.873 % | 116.4357 | 5.54 % | 15.76 % | 23.61 % | 34.0 % | 46.95 % | 57.21 % |
| 1.5 ATR | 5.847 % | 115.2429 | 2.48 % | 9.51 % | 15.87 % | 23.96 % | 36.36 % | 48.64 % |
| 2.0 ATR | 7.796 % | 112.8571 | 0.4 % | 3.96 % | 7.54 % | 13.62 % | 24.18 % | 37.13 % |
| 2.5 ATR | 9.746 % | 110.4714 | 0.0 % | 1.59 % | 3.37 % | 7.95 % | 15.58 % | 26.54 % |
| 3.0 ATR | 11.695 % | 108.0857 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 9.69 % | 18.97 % |
| 4.0 ATR | 15.593 % | 103.3143 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.8 % | 11.1 % |
| 6.0 ATR | 23.389 % | 93.7714 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.29 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.10 ATR | 1.48 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 0.96 ATR | 1.21 ATR | 1.37 ATR | 1.85 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.85 ATR | 0.97 ATR | 1.27 ATR | 1.47 ATR | 1.69 ATR | 2.32 ATR | 2.89 ATR |
| **10 s.** | 0.53 ATR | 1.16 ATR | 1.30 ATR | 1.64 ATR | 1.97 ATR | 2.24 ATR | 2.97 ATR | 3.96 ATR |
| **20 s.** | 0.70 ATR | 1.46 ATR | 1.66 ATR | 2.19 ATR | 2.60 ATR | 2.93 ATR | 4.29 ATR | 5.63 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.395–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.596–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.924 %, prix 118.821), p(touche) 34.19 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.72–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.924 %, prix 118.821), p(touche) 42.96 % (en stress 94.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.972–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.898 %, prix 117.6288), p(touche) 43.84 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.296–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.847 %, prix 115.2433), p(touche) 36.36 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.658–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.796 %, prix 112.8577), p(touche) 37.13 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.004 | EV/share : €-0.017 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 24 % | T3 6 %
- Kelly (position) : f* 0.016 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.2 | bear 7.2 | side 7.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 245.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.315% → cible +1.512% / stop −8.0%, p_fill 84%, n_eff≈35.1) : P(cible|rempli) **45%** · **EV/risk -0.065** (×p_fill ; si rempli -0.61% du capital)
  - **swing** (entrée dip −0.682% → cible +3.38% / stop −3.925%, p_fill 88%, n_eff≈35.2) : P(cible|rempli) **36%** · **EV/risk -0.315** (×p_fill ; si rempli -1.40% du capital)
  - **deep** (entrée dip −1.053% → cible +4.781% / stop −5.91%, p_fill 93%, n_eff≈37.2) : P(cible|rempli) **28%** · **EV/risk -0.413** (×p_fill ; si rempli -2.64% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→65% · +2.0%→39% · +3.0%→25% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.87% (p90 6.32%) · excursion haute méd. +1.25% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.336% vs midi 0.768% vs clôture 1.076% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr -0.012)_ ; drift intra méd. -0.636% ; recovery-V 15%
- **σ réalisé intraday** 2.481% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 66% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 121.41 (VA 121.11–121.91 ; dernier close 122.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 27% · rebond 68% · **stop −2.77%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 38% (gap-down >1% 13% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.04%) · haut méd +0.45% · range méd 1.37%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −2.37%) · haut méd +0.59% · range méd 1.71%
- Excursion ouverture 30min (n=160) : bas méd −1.02% (p90 −2.92%) · haut méd +0.74% · range méd 1.89%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −3.14%) · haut méd +0.86% · range méd 2.21%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.25 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 70% (110/159) · gap 20% · délai 0.4min · rebond 51% (63/110) (MFE +1.04%)
   - −1.0% : fill 30min 42% · séance 57% (92/159) · gap 13% · délai 1.2min · rebond 56% (56/92) (MFE +1.11%)
   - −1.5% : fill 30min 29% · séance 48% (73/159) · gap 9% · délai 10.9min · rebond 52% (42/73) (MFE +1.06%)
   - −2.0% : fill 30min 20% · séance 39% (60/159) · gap 6% · délai 28.6min · rebond 56% (38/60) (MFE +1.1%)
   - −3.0% : fill 30min 7% · séance 27% (42/159) · gap 2% · délai 91.4min · rebond 68% (30/42) (MFE +1.69%)
   - −4.0% : fill 30min 2% · séance 18% (26/159) · gap 1% · délai 337.0min · rebond 54% (16/26) (MFE +1.15%)
   - −5.0% : fill 30min 1% · séance 11% (17/159) · gap 1% · délai 395.2min · rebond 62% (12/17) (MFE +1.17%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −1.74%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −1.67%) → stop au-delà de −1.11% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.65%) → stop au-delà de −1.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=496 jambes) : jambe baissière méd −1.06% (p90 −2.62%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 91% (38/42) · rebond 42% (20/38)
      · −2.0% : fill 74% (31/42) · rebond 60% (20/31)
      · −3.0% : fill 56% (25/42) · rebond 70% (18/25)
      · −4.0% : fill 38% (15/42) · rebond 50% (9/15)
      · −5.0% : fill 31% (12/42) · rebond 48% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 54% (16/27) · rebond 74% (12/16)
      · −2.0% : fill 30% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 18% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 6% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (90 séances) :
      · −1.0% : fill 43% (38/90) · rebond 60% (24/38)
      · −2.0% : fill 27% (21/90) · rebond 40% (11/21)
      · −3.0% : fill 19% (12/90) · rebond 77% (9/12)
      · −4.0% : fill 14% (9/90) · rebond 55% (6/9)
      · −5.0% : fill 7% (4/90) · rebond 100% (4/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 66% si les 15 1res min sont vertes (77 cas) · 26% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 76% si début vert vs 21% si rouge (base 45% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **76%** · continue >prix actuel 50% ; creux résiduel méd -0.89% (q20 -1.92%) → **SL/trailing à −1.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.62% → **scale +1.34% / runner +2.62%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **21%** (continue à baisser 63%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.06%** (au-delà de la MAE q10 -4.06%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.97% .. +2.76%] · haut q95 +3.15% · bas q05 -3.36%
   - 60min (n=160) : retour [-3.3% .. +2.2%] · haut q95 +3.46% · bas q05 -3.59%
   - 2h (n=160) : retour [-3.37% .. +2.64%] · haut q95 +3.48% · bas q05 -4.12%
   - 4h (n=160) : retour [-3.47% .. +3.18%] · haut q95 +3.96% · bas q05 -4.48%
   - 6h (n=160) : retour [-3.73% .. +3.63%] · haut q95 +4.47% · bas q05 -4.69%
   - session (n=160) : retour [-4.61% .. +3.54%] · haut q95 +4.96% · bas q05 -6.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.1  _(neutre)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist 0.29  _(pas de croisement recent)_
- **BB** : %B 0.46 · largeur 11.9%
- **ATR** : 4.77 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.114  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 60.9  _(transition)_
- **MA** : MA20 123.02 · MA50 123.63 · MA200 118.08  _(prix < MA20)_
- **Dist MA** : MA20 -0.5% · MA50 -1.0% · MA200 +3.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (876553 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
