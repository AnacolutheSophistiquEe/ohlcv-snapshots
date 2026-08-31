# PRY

**Generated** : 2026-08-31T00:13:19.009397+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €122.50  

> 🟡 **WAIT-FOR-DIP** — spot +6.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €122.50 (+6.5% vs entrée) · entrée €115.07 · stop €110.49 · T1 €118.43 · R/R 0.73  
> ↳ P(T1 av. stop) 77 % · EV/risk 0.232 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €114.40–€115.74 (mid €115.07)
- Spot actuel : €122.50 (+6.5% au-dessus de la zone — repli à attendre)
- Stop : €110.49 (stop swing_plan-based (-9.8%))
- Targets : T1 €118.43 · R/R 0.73 | T2 €121.78 · R/R 1.47 | T3 €125.13 · R/R 2.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €110.49


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.50 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.8 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1270).
   - exécution **0.198 pt plus bas** dans le cas TYPIQUE (médiane), 0.198 au p90, **0.198 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 9.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0002 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.846 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.431** [0.3589 ; 0.5054] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3915** [0.3411 ; 0.4437] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3275** [0.2796 ; 0.3782] _(largeur 9.9 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 18.1 observations effectives », dont la borne haute a 95 % vaut environ 16.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (41.0 pt), swing (49.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.27 %** | CVaR **-5.76 %** | vol 2.64 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 1.77 % contre 2.91 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.48 % vs -7.48 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0273** (β de hausse 1.2241, asymétrie 0.8392) vs FTSEMIB — 562 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.409× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 109.9089 sur atr_grid (2.75 ATR, 10.278 %) — p(stop avant cible) 0.1693 [0.13 ; 0.21], R/R 2.557, perte reelle 10.278 % (gap inclus), CVaR 10.278 %, EV 1.3079 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.606 %) — p(stop avant cible) 0.429 [0.38 ; 0.48], R/R 3.322, perte reelle 7.909 % (gap inclus), EV -0.1609 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 1.4 % x 26.28 % + P(rien) 55.7 % x 5.15 % ne couvrent pas P(stop) 42.9 % x 7.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.38 ATR (stop 7.219 %) — p(stop avant cible) 0.3229 [0.28 ; 0.37], R/R 2.628, perte reelle 9.998 % (gap inclus), EV 0.1728 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 3.05 ATR (stop 13.46 %) — p(stop avant cible) 0.0705 [0.05 ; 0.10], R/R 1.952, perte reelle 13.46 % (gap inclus), EV 1.5156 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.46 % > budget 12.00 %
   - 🟢 support a 4.05 ATR (stop 17.186 %) — p(stop avant cible) 0.0152 [0.01 ; 0.03], R/R 1.529, perte reelle 17.186 % (gap inclus), EV 1.7247 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.19 % > budget 12.00 %
   - 🟢 support a 9.59 ATR (stop 37.921 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.693, perte reelle 37.921 % (gap inclus), EV 1.7215 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.92 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.934 %) — p(stop avant cible) 0.8871 [0.85 ; 0.92], R/R 13.786, perte reelle 1.906 % (gap inclus), EV -0.6558 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 13.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.887, borne haute 0.917 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 0.7 % x 26.28 % + P(rien) 10.6 % x 8.04 % ne couvrent pas P(stop) 88.7 % x 1.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.869 %) — p(stop avant cible) 0.7781 [0.73 ; 0.82], R/R 8.73, perte reelle 3.01 % (gap inclus), EV -0.5706 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.778, borne haute 0.820 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 1.0 % x 26.28 % + P(rien) 21.2 % x 7.08 % ne couvrent pas P(stop) 77.8 % x 3.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.803 %) — p(stop avant cible) 0.6638 [0.61 ; 0.71], R/R 5.992, perte reelle 4.385 % (gap inclus), EV -0.4239 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.664, borne haute 0.712 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 1.4 % x 26.28 % + P(rien) 32.2 % x 6.59 % ne couvrent pas P(stop) 66.4 % x 4.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.738 %) — p(stop avant cible) 0.5813 [0.53 ; 0.63], R/R 4.691, perte reelle 5.601 % (gap inclus), EV -0.4793 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.581, borne haute 0.632 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 1.4 % x 26.28 % + P(rien) 40.5 % x 5.97 % ne couvrent pas P(stop) 58.1 % x 5.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.38 ATR (stop 6.277 %) — p(stop avant cible) 0.3801 [0.33 ; 0.43], R/R 3.322, perte reelle 7.909 % (gap inclus), EV 0.3971 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 8.41 %) — p(stop avant cible) 0.2554 [0.21 ; 0.30], R/R 2.628, perte reelle 9.998 % (gap inclus), EV 0.7235 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 9.344 %) — p(stop avant cible) 0.2225 [0.18 ; 0.27], R/R 2.628, perte reelle 9.998 % (gap inclus), EV 1.0047 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 10.278 %) — p(stop avant cible) 0.1693 [0.13 ; 0.21], R/R 2.557, perte reelle 10.278 % (gap inclus), EV 1.3079 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.05 ATR (stop 12.518 %) — p(stop avant cible) 0.0837 [0.06 ; 0.12], R/R 2.099, perte reelle 12.518 % (gap inclus), EV 1.5343 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.52 % > budget 12.00 %
   - 🟢 grid_snapped a 4.05 ATR (stop 16.244 %) — p(stop avant cible) 0.0205 [0.01 ; 0.04], R/R 1.618, perte reelle 16.244 % (gap inclus), EV 1.7307 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.24 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.688 %) — p(stop avant cible) 0.0123 [0.00 ; 0.03], R/R 1.406, perte reelle 18.688 % (gap inclus), EV 1.7232 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.69 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.557 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 1.278, perte reelle 20.557 % (gap inclus), EV 1.7065 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.56 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.426 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 1.172, perte reelle 22.426 % (gap inclus), EV 1.702 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.43 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.294 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 1.082, perte reelle 24.294 % (gap inclus), EV 1.7159 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.163 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 1.004, perte reelle 26.163 % (gap inclus), EV 1.7163 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.16 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.032 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.937, perte reelle 28.032 % (gap inclus), EV 1.714 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.03 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.901 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.879, perte reelle 29.901 % (gap inclus), EV 1.7191 % — **REFUSE**
      - refuse : cible atteinte seulement 1.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.90 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 122.5, ATR14 4.5786 (3.738 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.342 ATR = 1.278 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.187 % | 122.2711 | 91.98 % | 93.95 % | 94.74 % | 95.63 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.374 % | 122.0421 | 85.35 % | 88.9 % | 91.27 % | 93.04 % | 95.2 % | 96.27 % |
| 0.15 ATR | 0.561 % | 121.8132 | 77.72 % | 84.14 % | 87.6 % | 90.56 % | 93.01 % | 94.25 % |
| 0.2 ATR | 0.748 % | 121.5843 | 69.5 % | 78.79 % | 82.74 % | 86.88 % | 90.71 % | 92.23 % |
| 0.25 ATR | 0.934 % | 121.3554 | 61.78 % | 74.03 % | 78.67 % | 83.1 % | 87.91 % | 90.31 % |
| 0.35 ATR | 1.308 % | 120.8975 | 49.01 % | 63.73 % | 71.03 % | 76.84 % | 83.62 % | 87.49 % |
| 0.5 ATR | 1.869 % | 120.2107 | 34.95 % | 52.13 % | 60.22 % | 68.19 % | 76.32 % | 81.84 % |
| 0.75 ATR | 2.803 % | 119.0661 | 19.11 % | 34.29 % | 43.35 % | 54.57 % | 64.64 % | 73.26 % |
| 1.0 ATR | 3.738 % | 117.9214 | 10.0 % | 23.19 % | 31.55 % | 44.23 % | 55.44 % | 65.19 % |
| 1.25 ATR | 4.672 % | 116.7768 | 5.74 % | 15.86 % | 23.91 % | 34.39 % | 47.15 % | 57.42 % |
| 1.5 ATR | 5.606 % | 115.6321 | 2.48 % | 9.71 % | 15.97 % | 24.25 % | 36.76 % | 49.04 % |
| 2.0 ATR | 7.475 % | 113.3429 | 0.4 % | 3.96 % | 7.44 % | 13.82 % | 24.78 % | 38.14 % |
| 2.5 ATR | 9.344 % | 111.0536 | 0.0 % | 1.59 % | 3.37 % | 7.75 % | 16.08 % | 27.75 % |
| 3.0 ATR | 11.213 % | 108.7643 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 10.19 % | 19.98 % |
| 4.0 ATR | 14.95 % | 104.1857 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.9 % | 11.5 % |
| 6.0 ATR | 22.426 % | 95.0286 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

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
- **2 seance(s)** : plage utile 0.6–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.803 %, prix 119.0663), p(touche) 34.29 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.726–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.803 %, prix 119.0663), p(touche) 43.35 % (en stress 94.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.981–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.738 %, prix 117.921), p(touche) 44.23 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.302–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.606 %, prix 115.6326), p(touche) 36.76 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.685–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.475 %, prix 113.3431), p(touche) 38.14 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : €-0.142 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 26 % | T3 10 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 14.5 | bear 10.5 | side 75.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 122.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.756% → cible +3.421% / stop −1.711%, p_fill 35%, n_eff≈18.1) : P(cible|rempli) **0%** · **EV/risk -0.169** (×p_fill ; si rempli -0.82% du capital)
  - **swing** (entrée dip −6.062% → cible +2.913% / stop −3.979%, p_fill 23%, n_eff≈9.7) : P(cible|rempli) **75%** · **EV/risk +0.073** (×p_fill ; si rempli +1.27% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=6))
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
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
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

- **RSI** : 45.3  _(neutre)_
- **ADX** : 26.5  _(tendance etablie)_
- **MACD** : hist 0.086  _(bullish_recent)_
- **BB** : %B 0.36 · largeur 11.9%
- **ATR** : 4.58 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.321  _(distribution)_
- **Vol ratio** : 0.23  _(volume atone)_
- **Choppiness** : 48.5  _(transition)_
- **MA** : MA20 124.56 · MA50 130.6 · MA200 114.14  _(prix < MA20)_
- **Dist MA** : MA20 -1.7% · MA50 -6.2% · MA200 +7.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (903988 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
