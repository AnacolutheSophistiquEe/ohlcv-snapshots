# PRY

**Generated** : 2026-09-21T00:17:55.089905+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €121.95  

> 🟡 **WAIT-FOR-DIP** — spot +4.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €121.95 (+4.9% vs entrée) · entrée €116.20 · stop €111.61 · T1 €120.22 · R/R 0.88  
> ↳ P(T1 av. stop) 59 % _(réel 5 s)_ · EV/risk 0.024 _(réel 5 s)_ (GBM -0.056) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €115.39–€117.00 (mid €116.20)
- Spot actuel : €121.95 (+4.9% au-dessus de la zone — repli à attendre)
- Stop : €111.61 (stop swing_plan-based (-8.48%))
- Targets : T1 €120.22 · R/R 0.88 | T2 €124.24 · R/R 1.75 | T3 €128.26 · R/R 2.63
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €111.61


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.57 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.48 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1270).
   - exécution **1.518 pt plus bas** dans le cas TYPIQUE (médiane), 1.518 au p90, **1.518 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 8.48 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0012 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.86 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0003** [0.0 ; 0.0152] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.4087** [0.3578 ; 0.4611] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.352** [0.3031 ; 0.4034] _(largeur 10.0 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 19.3 observations effectives », dont la borne haute a 95 % vaut environ 15.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.3 pt), swing (45.4 pt), deep (49.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.24 %** | CVaR **-5.74 %** | vol 2.58 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.82 % contre 2.94 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.49 % vs -7.5 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0378** (β de hausse 1.2273, asymétrie 0.8456) vs FTSEMIB — 564 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.494× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 108.041 sur sr_based (2.38 ATR, 11.405 %) — p(stop avant cible) 0.1063 [0.08 ; 0.14], R/R 2.354, perte reelle 11.405 % (gap inclus), CVaR 11.405 %, EV 1.2763 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 22 des 22 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 42.1 % de la queue et il ne reste que -112.43 EUR a partager. Prix du risque -0.036 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.641 %) — p(stop avant cible) 0.431 [0.38 ; 0.48], R/R 3.394, perte reelle 7.909 % (gap inclus), EV -0.3597 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 1.2 % x 26.84 % + P(rien) 55.6 % x 4.88 % ne couvrent pas P(stop) 43.1 % x 7.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.28 ATR (stop 7.263 %) — p(stop avant cible) 0.2989 [0.25 ; 0.35], R/R 2.685, perte reelle 9.998 % (gap inclus), EV 0.1526 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 2.38 ATR (stop 11.405 %) — p(stop avant cible) 0.1063 [0.08 ; 0.14], R/R 2.354, perte reelle 11.405 % (gap inclus), EV 1.2763 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 3.92 ATR (stop 17.191 %) — p(stop avant cible) 0.0132 [0.00 ; 0.03], R/R 1.562, perte reelle 17.191 % (gap inclus), EV 1.5495 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.19 % > budget 12.00 %
   - 🟢 support a 9.46 ATR (stop 38.02 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.706, perte reelle 38.02 % (gap inclus), EV 1.5446 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.02 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.94 %) — p(stop avant cible) 0.8908 [0.85 ; 0.92], R/R 13.974, perte reelle 1.921 % (gap inclus), EV -0.7522 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 13.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.891, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 0.7 % x 26.84 % + P(rien) 10.3 % x 7.63 % ne couvrent pas P(stop) 89.1 % x 1.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.88 %) — p(stop avant cible) 0.7907 [0.75 ; 0.83], R/R 8.804, perte reelle 3.049 % (gap inclus), EV -0.7776 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 8.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.791, borne haute 0.831 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 0.9 % x 26.84 % + P(rien) 20.0 % x 6.90 % ne couvrent pas P(stop) 79.1 % x 3.05 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.82 %) — p(stop avant cible) 0.6782 [0.63 ; 0.73], R/R 6.201, perte reelle 4.329 % (gap inclus), EV -0.621 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.678, borne haute 0.726 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 1.2 % x 26.84 % + P(rien) 30.9 % x 6.40 % ne couvrent pas P(stop) 67.8 % x 4.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.76 %) — p(stop avant cible) 0.5934 [0.54 ; 0.64], R/R 4.793, perte reelle 5.601 % (gap inclus), EV -0.7359 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.593, borne haute 0.644 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 1.2 % x 26.84 % + P(rien) 39.4 % x 5.71 % ne couvrent pas P(stop) 59.3 % x 5.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.581 %) — p(stop avant cible) 0.3708 [0.32 ; 0.42], R/R 3.126, perte reelle 8.587 % (gap inclus), EV 0.0265 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ grid_snapped a 2.38 ATR (stop 10.082 %) — p(stop avant cible) 0.1709 [0.13 ; 0.21], R/R 2.663, perte reelle 10.082 % (gap inclus), EV 1.1071 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 13.161 %) — p(stop avant cible) 0.0694 [0.05 ; 0.10], R/R 2.04, perte reelle 13.161 % (gap inclus), EV 1.3404 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.16 % > budget 12.00 %
   - 🟢 grid_snapped a 3.92 ATR (stop 15.868 %) — p(stop avant cible) 0.0188 [0.01 ; 0.04], R/R 1.692, perte reelle 15.868 % (gap inclus), EV 1.5598 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.802 %) — p(stop avant cible) 0.0113 [0.00 ; 0.03], R/R 1.428, perte reelle 18.802 % (gap inclus), EV 1.5443 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.80 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.682 %) — p(stop avant cible) 0.0094 [0.00 ; 0.02], R/R 1.298, perte reelle 20.682 % (gap inclus), EV 1.5304 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.68 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.562 %) — p(stop avant cible) 0.0075 [0.00 ; 0.02], R/R 1.19, perte reelle 22.562 % (gap inclus), EV 1.526 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.56 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.442 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 1.098, perte reelle 24.442 % (gap inclus), EV 1.5399 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.44 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.322 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 1.02, perte reelle 26.322 % (gap inclus), EV 1.5387 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.32 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.202 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.952, perte reelle 28.202 % (gap inclus), EV 1.5376 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.20 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.083 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.892, perte reelle 30.083 % (gap inclus), EV 1.5413 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.08 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 121.95, ATR14 4.5857 (3.76 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.297 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.188 % | 121.7207 | 91.78 % | 93.86 % | 94.74 % | 95.63 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.376 % | 121.4914 | 85.15 % | 88.8 % | 91.17 % | 93.04 % | 95.2 % | 96.27 % |
| 0.15 ATR | 0.564 % | 121.2621 | 77.72 % | 84.24 % | 87.5 % | 90.56 % | 93.01 % | 94.25 % |
| 0.2 ATR | 0.752 % | 121.0329 | 69.6 % | 78.99 % | 82.64 % | 86.88 % | 90.71 % | 92.23 % |
| 0.25 ATR | 0.94 % | 120.8036 | 62.08 % | 74.33 % | 78.67 % | 83.2 % | 88.11 % | 90.31 % |
| 0.35 ATR | 1.316 % | 120.345 | 49.41 % | 63.92 % | 71.03 % | 76.84 % | 83.82 % | 87.49 % |
| 0.5 ATR | 1.88 % | 119.6571 | 34.95 % | 51.93 % | 60.12 % | 67.99 % | 76.52 % | 81.84 % |
| 0.75 ATR | 2.82 % | 118.5107 | 19.01 % | 34.39 % | 43.15 % | 54.47 % | 64.74 % | 73.16 % |
| 1.0 ATR | 3.76 % | 117.3643 | 9.9 % | 23.19 % | 31.55 % | 44.14 % | 55.34 % | 64.98 % |
| 1.25 ATR | 4.7 % | 116.2179 | 5.64 % | 15.86 % | 23.91 % | 34.19 % | 46.85 % | 57.21 % |
| 1.5 ATR | 5.64 % | 115.0714 | 2.48 % | 9.51 % | 16.07 % | 24.16 % | 36.16 % | 48.64 % |
| 2.0 ATR | 7.521 % | 112.7786 | 0.4 % | 3.96 % | 7.54 % | 13.62 % | 23.98 % | 37.13 % |
| 2.5 ATR | 9.401 % | 110.4857 | 0.0 % | 1.59 % | 3.37 % | 7.95 % | 15.38 % | 26.54 % |
| 3.0 ATR | 11.281 % | 108.1929 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 9.69 % | 18.97 % |
| 4.0 ATR | 15.041 % | 103.6071 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.8 % | 11.1 % |
| 6.0 ATR | 22.562 % | 94.4357 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.73 ATR | 1.00 ATR | 1.30 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.48 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 0.97 ATR | 1.21 ATR | 1.38 ATR | 1.86 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.86 ATR | 0.98 ATR | 1.28 ATR | 1.48 ATR | 1.70 ATR | 2.32 ATR | 2.89 ATR |
| **10 s.** | 0.53 ATR | 1.16 ATR | 1.29 ATR | 1.63 ATR | 1.96 ATR | 2.23 ATR | 2.97 ATR | 3.96 ATR |
| **20 s.** | 0.70 ATR | 1.46 ATR | 1.66 ATR | 2.19 ATR | 2.60 ATR | 2.93 ATR | 4.29 ATR | 5.63 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.599–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.82 %, prix 118.511), p(touche) 34.39 % (en stress 87.13 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.723–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.82 %, prix 118.511), p(touche) 43.15 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.979–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.76 %, prix 117.3647), p(touche) 44.14 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.293–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.64 %, prix 115.072), p(touche) 36.16 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.658–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.521 %, prix 112.7781), p(touche) 37.13 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.056 | EV/share : €-0.256 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 21 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 75.5 | bear 10.7 | side 13.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 366.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.141% → cible +1.548% / stop −8.0%, p_fill 45%, n_eff≈19.3) : P(cible|rempli) **22%** · **EV/risk -0.024** (×p_fill ; si rempli -0.44% du capital)
  - **swing** (entrée dip −4.72% → cible +3.461% / stop −3.946%, p_fill 28%, n_eff≈15.6) : P(cible|rempli) **59%** · **EV/risk +0.024** (×p_fill ; si rempli +0.34% du capital)
  - **deep** (entrée dip −7.289% → cible +4.895% / stop −6.084%, p_fill 25%, n_eff≈12.9) : P(cible|rempli) **46%** · **EV/risk -0.004** (×p_fill ; si rempli -0.10% du capital)
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

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 52.4  _(neutre)_
- **ADX** : 19.5  _(pas de tendance nette)_
- **MACD** : hist 0.1  _(pas de croisement recent)_
- **BB** : %B 0.5 · largeur 10.7%
- **ATR** : 4.59 (57.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.194  _(distribution)_
- **Vol ratio** : 0.42  _(volume atone)_
- **Choppiness** : 58.9  _(transition)_
- **MA** : MA20 121.93 · MA50 124.32 · MA200 117.04  _(prix > MA20)_
- **Dist MA** : MA20 +0.0% · MA50 -1.9% · MA200 +4.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (819276 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
