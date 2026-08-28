# PRY

**Generated** : 2026-08-28T21:48:32.557675+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €122.05  

> 🟡 **WAIT-FOR-DIP** — spot +6.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €122.05 (+6.3% vs entrée) · entrée €114.87 · stop €110.29 · T1 €118.23 · R/R 0.73  
> ↳ P(T1 av. stop) 76 % · EV/risk 0.242 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €114.20–€115.54 (mid €114.87)
- Spot actuel : €122.05 (+6.3% au-dessus de la zone — repli à attendre)
- Stop : €110.29 (stop swing_plan-based (-9.63%))
- Targets : T1 €118.23 · R/R 0.73 | T2 €121.59 · R/R 1.47 | T3 €124.95 · R/R 2.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €110.29


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.50 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.63 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1270).
   - exécution **0.368 pt plus bas** dans le cas TYPIQUE (médiane), 0.368 au p90, **0.368 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 9.63 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0003 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.846 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3991** [0.3283 ; 0.4732] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.3914** [0.341 ; 0.4436] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3224** [0.2748 ; 0.373] _(largeur 9.8 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 18.1 observations effectives », dont la borne haute a 95 % vaut environ 16.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.7 pt), swing (48.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.27 %** | CVaR **-5.76 %** | vol 2.64 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 1.77 % contre 2.91 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.48 % vs -7.48 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0273** (β de hausse 1.2243, asymétrie 0.8391) vs FTSEMIB — 562 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.409× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 110.6036 sur atr_grid (2.5 ATR, 9.378 %) — p(stop avant cible) 0.2225 [0.18 ; 0.27], R/R 2.675, perte reelle 9.998 % (gap inclus), CVaR 9.378 %, EV 1.0128 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.627 %) — p(stop avant cible) 0.4285 [0.38 ; 0.48], R/R 3.381, perte reelle 7.909 % (gap inclus), EV -0.1528 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 1.4 % x 26.74 % + P(rien) 55.8 % x 5.14 % ne couvrent pas P(stop) 42.9 % x 7.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.28 ATR (stop 6.877 %) — p(stop avant cible) 0.3449 [0.30 ; 0.40], R/R 3.114, perte reelle 8.587 % (gap inclus), EV 0.3767 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ sr_based a 2.95 ATR (stop 13.141 %) — p(stop avant cible) 0.0757 [0.05 ; 0.11], R/R 2.035, perte reelle 13.141 % (gap inclus), EV 1.5084 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.14 % > budget 12.00 %
   - 🟢 support a 3.95 ATR (stop 16.88 %) — p(stop avant cible) 0.0152 [0.01 ; 0.03], R/R 1.584, perte reelle 16.88 % (gap inclus), EV 1.7375 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.88 % > budget 12.00 %
   - 🟢 support a 9.5 ATR (stop 37.692 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.709, perte reelle 37.692 % (gap inclus), EV 1.7296 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.69 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.938 %) — p(stop avant cible) 0.8871 [0.85 ; 0.92], R/R 14.03, perte reelle 1.906 % (gap inclus), EV -0.6525 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 14.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.887, borne haute 0.917 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 0.7 % x 26.74 % + P(rien) 10.6 % x 8.04 % ne couvrent pas P(stop) 88.7 % x 1.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.876 %) — p(stop avant cible) 0.778 [0.73 ; 0.82], R/R 8.832, perte reelle 3.028 % (gap inclus), EV -0.5795 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.778, borne haute 0.819 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 1.0 % x 26.74 % + P(rien) 21.2 % x 7.08 % ne couvrent pas P(stop) 77.8 % x 3.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.814 %) — p(stop avant cible) 0.6629 [0.61 ; 0.71], R/R 6.099, perte reelle 4.385 % (gap inclus), EV -0.4031 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.663, borne haute 0.711 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 1.4 % x 26.74 % + P(rien) 32.3 % x 6.61 % ne couvrent pas P(stop) 66.3 % x 4.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.751 %) — p(stop avant cible) 0.5813 [0.53 ; 0.63], R/R 4.775, perte reelle 5.601 % (gap inclus), EV -0.473 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.581, borne haute 0.632 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 1.4 % x 26.74 % + P(rien) 40.5 % x 5.97 % ne couvrent pas P(stop) 58.1 % x 5.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.503 %) — p(stop avant cible) 0.2891 [0.24 ; 0.34], R/R 2.675, perte reelle 9.998 % (gap inclus), EV 0.5169 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 8.441 %) — p(stop avant cible) 0.2553 [0.21 ; 0.30], R/R 2.675, perte reelle 9.998 % (gap inclus), EV 0.7325 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 9.378 %) — p(stop avant cible) 0.2225 [0.18 ; 0.27], R/R 2.675, perte reelle 9.998 % (gap inclus), EV 1.0128 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.95 ATR (stop 12.196 %) — p(stop avant cible) 0.0837 [0.06 ; 0.12], R/R 2.193, perte reelle 12.196 % (gap inclus), EV 1.5696 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.20 % > budget 12.00 %
   - 🟢 grid_snapped a 3.95 ATR (stop 15.935 %) — p(stop avant cible) 0.0205 [0.01 ; 0.04], R/R 1.678, perte reelle 15.935 % (gap inclus), EV 1.7452 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.93 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.757 %) — p(stop avant cible) 0.0123 [0.00 ; 0.03], R/R 1.426, perte reelle 18.757 % (gap inclus), EV 1.7304 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.76 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.633 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 1.296, perte reelle 20.633 % (gap inclus), EV 1.7138 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.63 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.508 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 1.188, perte reelle 22.508 % (gap inclus), EV 1.7095 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.51 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.384 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 1.097, perte reelle 24.384 % (gap inclus), EV 1.7235 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.38 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.26 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 1.018, perte reelle 26.26 % (gap inclus), EV 1.724 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.26 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.135 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.95, perte reelle 28.135 % (gap inclus), EV 1.7218 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.13 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.011 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.891, perte reelle 30.011 % (gap inclus), EV 1.727 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.01 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 122.05, ATR14 4.5786 (3.751 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.342 ATR = 1.283 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.188 % | 121.8211 | 91.98 % | 93.95 % | 94.74 % | 95.63 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.375 % | 121.5921 | 85.35 % | 88.9 % | 91.27 % | 93.04 % | 95.2 % | 96.27 % |
| 0.15 ATR | 0.563 % | 121.3632 | 77.72 % | 84.14 % | 87.6 % | 90.56 % | 93.01 % | 94.25 % |
| 0.2 ATR | 0.75 % | 121.1343 | 69.5 % | 78.79 % | 82.74 % | 86.88 % | 90.71 % | 92.23 % |
| 0.25 ATR | 0.938 % | 120.9054 | 61.78 % | 74.03 % | 78.67 % | 83.1 % | 87.91 % | 90.31 % |
| 0.35 ATR | 1.313 % | 120.4475 | 49.01 % | 63.73 % | 71.03 % | 76.84 % | 83.62 % | 87.49 % |
| 0.5 ATR | 1.876 % | 119.7607 | 34.95 % | 52.13 % | 60.22 % | 68.19 % | 76.32 % | 81.84 % |
| 0.75 ATR | 2.814 % | 118.6161 | 19.11 % | 34.29 % | 43.35 % | 54.57 % | 64.64 % | 73.26 % |
| 1.0 ATR | 3.751 % | 117.4714 | 10.0 % | 23.19 % | 31.55 % | 44.23 % | 55.44 % | 65.19 % |
| 1.25 ATR | 4.689 % | 116.3268 | 5.74 % | 15.86 % | 23.91 % | 34.39 % | 47.15 % | 57.42 % |
| 1.5 ATR | 5.627 % | 115.1821 | 2.48 % | 9.71 % | 15.97 % | 24.25 % | 36.76 % | 49.04 % |
| 2.0 ATR | 7.503 % | 112.8929 | 0.4 % | 3.96 % | 7.44 % | 13.82 % | 24.78 % | 38.14 % |
| 2.5 ATR | 9.378 % | 110.6036 | 0.0 % | 1.59 % | 3.37 % | 7.75 % | 16.08 % | 27.75 % |
| 3.0 ATR | 11.254 % | 108.3143 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 10.19 % | 19.98 % |
| 4.0 ATR | 15.006 % | 103.7357 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.9 % | 11.5 % |
| 6.0 ATR | 22.508 % | 94.5786 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.31 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.49 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.73 ATR | 0.97 ATR | 1.21 ATR | 1.37 ATR | 1.85 ATR | 2.30 ATR |
| **5 s.** | 0.38 ATR | 0.86 ATR | 0.98 ATR | 1.28 ATR | 1.48 ATR | 1.70 ATR | 2.31 ATR | 2.88 ATR |
| **10 s.** | 0.53 ATR | 1.16 ATR | 1.30 ATR | 1.66 ATR | 1.99 ATR | 2.27 ATR | 3.04 ATR | 3.98 ATR |
| **20 s.** | 0.70 ATR | 1.47 ATR | 1.69 ATR | 2.25 ATR | 2.68 ATR | 3.00 ATR | 4.38 ATR | 5.65 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.393–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.6–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.814 %, prix 118.6155), p(touche) 34.29 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.726–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.814 %, prix 118.6155), p(touche) 43.35 % (en stress 94.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.981–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.751 %, prix 117.4719), p(touche) 44.23 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.302–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.627 %, prix 115.1822), p(touche) 36.76 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.685–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.503 %, prix 112.8926), p(touche) 38.14 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.034 | EV/share : €-0.156 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 26 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 14.5 | bear 10.5 | side 75.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 122.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.672% → cible +3.715% / stop −1.858%, p_fill 37%, n_eff≈18.1) : P(cible|rempli) **0%** · **EV/risk -0.182** (×p_fill ; si rempli -0.91% du capital)
  - **swing** (entrée dip −5.878% → cible +2.925% / stop −3.986%, p_fill 23%, n_eff≈10.4) : P(cible|rempli) **74%** · **EV/risk +0.070** (×p_fill ; si rempli +1.23% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→66% · +2.0%→40% · +3.0%→26% · +5.0%→6% · +8.0%→0%
- Range intraday médian 4.04% (p90 6.33%) · excursion haute méd. +1.37% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.379% vs midi 0.788% vs clôture 1.146% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.002)_ ; drift intra méd. -0.749% ; recovery-V 19%
- **σ réalisé intraday** 2.566% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 62% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 125.0613 (VA 124.4282–125.7997 ; dernier close 123.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 29% · rebond 73% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.73% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.42% · baisse 34% (gap-down >1% 15% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.25%) · haut méd +0.47% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −1.02% (p90 −2.41%) · haut méd +0.58% · range méd 1.77%
- Excursion ouverture 30min (n=160) : bas méd −1.03% (p90 −3.07%) · haut méd +0.74% · range méd 2.04%
- Excursion ouverture 60min (n=160) : bas méd −1.18% (p90 −3.24%) · haut méd +0.86% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 123.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 68% (110/159) · gap 20% · délai 0.4min · rebond 53% (65/110) (MFE +1.31%)
   - −1.0% : fill 30min 45% · séance 58% (92/159) · gap 15% · délai 1.0min · rebond 59% (57/92) (MFE +1.17%)
   - −1.5% : fill 30min 33% · séance 48% (72/159) · gap 10% · délai 5.3min · rebond 55% (43/72) (MFE +1.12%)
   - −2.0% : fill 30min 22% · séance 41% (61/159) · gap 6% · délai 26.3min · rebond 59% (40/61) (MFE +1.12%)
   - −3.0% : fill 30min 8% · séance 29% (42/159) · gap 2% · délai 78.6min · rebond 73% (31/42) (MFE +1.73%)
   - −4.0% : fill 30min 2% · séance 20% (26/159) · gap 1% · délai 337.0min · rebond 54% (16/26) (MFE +1.15%)
   - −5.0% : fill 30min 1% · séance 13% (17/159) · gap 1% · délai 395.2min · rebond 62% (12/17) (MFE +1.17%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −1.75%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −1.99%) → stop au-delà de −1.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.77%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=493 jambes) : jambe baissière méd −1.07% (p90 −2.63%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 90% (39/43) · rebond 46% (21/39)
      · −2.0% : fill 80% (33/43) · rebond 61% (22/33)
      · −3.0% : fill 60% (26/43) · rebond 71% (19/26)
      · −4.0% : fill 40% (15/43) · rebond 50% (9/15)
      · −5.0% : fill 33% (12/43) · rebond 48% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 59% (16/27) · rebond 70% (12/16)
      · −2.0% : fill 29% (7/27) · rebond 100% (7/7)
      · −3.0% : fill 14% (4/27) · rebond 68% (3/4)
      · −4.0% : fill 8% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 43% (37/89) · rebond 64% (24/37)
      · −2.0% : fill 29% (21/89) · rebond 40% (11/21)
      · −3.0% : fill 20% (12/89) · rebond 77% (9/12)
      · −4.0% : fill 15% (9/89) · rebond 55% (6/9)
      · −5.0% : fill 7% (4/89) · rebond 100% (4/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 68% si les 15 1res min sont vertes (76 cas) · 28% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 78% si début vert vs 24% si rouge (base 47% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -0.97% (q20 -2.16%) → **SL/trailing à −2.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.4% / q75 +2.51% → **scale +1.4% / runner +2.51%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **24%** (continue à baisser 63%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +1.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.08% .. +2.86%] · haut q95 +3.24% · bas q05 -3.39%
   - 60min (n=160) : retour [-3.34% .. +2.25%] · haut q95 +3.6% · bas q05 -3.64%
   - 2h (n=160) : retour [-3.51% .. +2.64%] · haut q95 +3.77% · bas q05 -4.29%
   - 4h (n=160) : retour [-3.48% .. +3.24%] · haut q95 +4.08% · bas q05 -4.55%
   - 6h (n=160) : retour [-3.76% .. +3.74%] · haut q95 +4.52% · bas q05 -4.75%
   - session (n=160) : retour [-4.92% .. +3.84%] · haut q95 +5.14% · bas q05 -6.39%


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

- **RSI** : 44.7  _(momentum baissier)_
- **ADX** : 26.5  _(tendance etablie)_
- **MACD** : hist 0.058  _(bullish_recent)_
- **BB** : %B 0.33 · largeur 12.0%
- **ATR** : 4.58 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.332  _(distribution)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 48.5  _(transition)_
- **MA** : MA20 124.54 · MA50 130.59 · MA200 114.14  _(prix < MA20)_
- **Dist MA** : MA20 -2.0% · MA50 -6.5% · MA200 +6.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (902575 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
