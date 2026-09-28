# HOOD

**Generated** : 2026-09-28T00:46:38.037928+00:00  
**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $119.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $119.40 (+3.0% vs entrée) · entrée $115.91 · stop $109.70 · T1 $122.90 · R/R 1.13  
> ↳ P(T1 av. stop) 60 % _(réel 5 s)_ · EV/risk 0.158 _(réel 5 s)_ (GBM 0.002) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $114.52–$117.31 (mid $115.91)
- Spot actuel : $119.40 (+3.0% au-dessus de la zone — repli à attendre)
- Stop : $109.70 (stop swing_plan-based (-8.12%))
- Targets : T1 $122.90 · R/R 1.13 | T2 $129.89 · R/R 2.25 | T3 $136.87 · R/R 3.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $109.70


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.12 %)** : le gap seul le franchit 0.797 % des séances (10 fois sur 1254).
   - exécution **2.546 pt plus bas** dans le cas TYPIQUE (médiane), 6.372 au p90, **9.665 au pire**
   - perte réelle **11.287 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 8.12 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0253 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.415 % | p01 -7.299 % | pire -17.785 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3504** [0.2823 ; 0.4235] _(largeur 14.1 pt, n_eff 173.1)_
   - swing : **0.4822** [0.4299 ; 0.5348] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.2968** [0.2505 ; 0.3465] _(largeur 9.6 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.4 pt), swing (38.7 pt), deep (41.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.16 %** | CVaR **-8.88 %** | vol 4.37 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.73 % contre 4.70 % aujourd'hui, rapport 0.58)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.53 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.012 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7606** (β de hausse 1.6058, asymétrie 1.0964) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.419× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 105.4259 sur atr_grid (2.25 ATR, 11.704 %) — p(stop avant cible) 0.2974 [0.25 ; 0.35], R/R 1.772, perte reelle 14.605 % (gap inclus), CVaR 11.711 %, EV 1.7796 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 22 des 22 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 49.8 % de la queue et il ne reste que -1061.59 EUR a partager. Prix du risque -0.364 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.12 ATR (stop 8.658 %) — p(stop avant cible) 0.4384 [0.39 ; 0.49], R/R 2.232, perte reelle 11.595 % (gap inclus), EV 0.7282 % — **REFUSE**
      - refuse : cible atteinte seulement 8.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 3.01 ATR (stop 18.508 %) — p(stop avant cible) 0.1118 [0.08 ; 0.15], R/R 1.398, perte reelle 18.508 % (gap inclus), EV 2.8521 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.51 % > budget 12.00 %
   - 🟢 support a 4.5 ATR (stop 26.247 %) — p(stop avant cible) 0.0318 [0.02 ; 0.05], R/R 0.986, perte reelle 26.247 % (gap inclus), EV 2.9862 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.25 % > budget 12.00 %
   - 🟢 support a 9.0 ATR (stop 49.635 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.521, perte reelle 49.635 % (gap inclus), EV 3.1414 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.63 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.3 %) — p(stop avant cible) 0.9095 [0.88 ; 0.94], R/R 8.691, perte reelle 2.978 % (gap inclus), EV -1.306 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 8.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.909, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 2.6 % x 25.88 % + P(rien) 6.5 % x 11.40 % ne couvrent pas P(stop) 91.0 % x 2.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.601 %) — p(stop avant cible) 0.7945 [0.75 ; 0.83], R/R 5.66, perte reelle 4.573 % (gap inclus), EV -0.5222 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.794, borne haute 0.835 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 5.6 % x 25.88 % + P(rien) 14.9 % x 11.11 % ne couvrent pas P(stop) 79.5 % x 4.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.901 %) — p(stop avant cible) 0.7016 [0.65 ; 0.75], R/R 3.982, perte reelle 6.5 % (gap inclus), EV -0.3686 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.702, borne haute 0.748 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 6.6 % x 25.88 % + P(rien) 23.3 % x 10.71 % ne couvrent pas P(stop) 70.2 % x 6.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.12 ATR (stop 7.389 %) — p(stop avant cible) 0.5059 [0.45 ; 0.56], R/R 2.466, perte reelle 10.494 % (gap inclus), EV 0.2323 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.506, borne haute 0.558 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 10.403 %) — p(stop avant cible) 0.3582 [0.31 ; 0.41], R/R 1.962, perte reelle 13.192 % (gap inclus), EV 1.4279 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 11.704 %) — p(stop avant cible) 0.2974 [0.25 ; 0.35], R/R 1.772, perte reelle 14.605 % (gap inclus), EV 1.7796 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 13.004 %) — p(stop avant cible) 0.259 [0.21 ; 0.31], R/R 1.622, perte reelle 15.955 % (gap inclus), EV 1.9212 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.01 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 14.304 %) — p(stop avant cible) 0.2169 [0.18 ; 0.26], R/R 1.455, perte reelle 17.785 % (gap inclus), EV 2.0086 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.31 % > budget 12.00 %
   - 🟢 grid_snapped a 3.01 ATR (stop 17.239 %) — p(stop avant cible) 0.1314 [0.10 ; 0.17], R/R 1.455, perte reelle 17.785 % (gap inclus), EV 2.7828 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.24 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 20.806 %) — p(stop avant cible) 0.0744 [0.05 ; 0.11], R/R 1.244, perte reelle 20.806 % (gap inclus), EV 2.959 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.81 % > budget 12.00 %
   - 🟢 grid_snapped a 4.5 ATR (stop 24.978 %) — p(stop avant cible) 0.0338 [0.02 ; 0.06], R/R 1.036, perte reelle 24.978 % (gap inclus), EV 3.0016 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.98 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 28.609 %) — p(stop avant cible) 0.0248 [0.01 ; 0.05], R/R 0.905, perte reelle 28.609 % (gap inclus), EV 2.9802 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.61 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 31.21 %) — p(stop avant cible) 0.0185 [0.01 ; 0.04], R/R 0.829, perte reelle 31.21 % (gap inclus), EV 2.9999 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.21 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 33.81 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.765, perte reelle 33.81 % (gap inclus), EV 3.1079 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.81 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 36.411 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.711, perte reelle 36.411 % (gap inclus), EV 3.1249 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.41 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 39.012 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.663, perte reelle 39.012 % (gap inclus), EV 3.1327 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.01 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 41.613 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.622, perte reelle 41.613 % (gap inclus), EV 3.1414 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.61 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 119.4, ATR14 6.2107 (5.202 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.375 ATR = 1.951 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.26 % | 119.0895 | 93.06 % | 95.17 % | 96.07 % | 96.57 % | 97.06 % | 98.05 % |
| 0.1 ATR | 0.52 % | 118.7789 | 85.51 % | 90.53 % | 92.24 % | 93.74 % | 94.72 % | 96.41 % |
| 0.15 ATR | 0.78 % | 118.4684 | 77.57 % | 85.2 % | 88.0 % | 90.3 % | 92.59 % | 95.08 % |
| 0.2 ATR | 1.04 % | 118.1579 | 71.53 % | 80.16 % | 83.77 % | 86.97 % | 90.36 % | 93.23 % |
| 0.25 ATR | 1.3 % | 117.8473 | 64.69 % | 74.52 % | 79.23 % | 83.43 % | 87.72 % | 90.87 % |
| 0.35 ATR | 1.821 % | 117.2263 | 52.52 % | 65.46 % | 71.98 % | 77.58 % | 83.45 % | 88.0 % |
| 0.5 ATR | 2.601 % | 116.2946 | 37.22 % | 53.58 % | 61.19 % | 68.28 % | 76.55 % | 82.36 % |
| 0.75 ATR | 3.901 % | 114.742 | 19.62 % | 36.25 % | 45.97 % | 55.56 % | 65.69 % | 73.23 % |
| 1.0 ATR | 5.202 % | 113.1893 | 9.26 % | 23.06 % | 32.76 % | 43.74 % | 55.03 % | 65.64 % |
| 1.25 ATR | 6.502 % | 111.6366 | 4.83 % | 14.6 % | 22.48 % | 33.54 % | 47.01 % | 59.08 % |
| 1.5 ATR | 7.802 % | 110.0839 | 2.41 % | 9.87 % | 16.33 % | 27.07 % | 40.1 % | 53.44 % |
| 2.0 ATR | 10.403 % | 106.9786 | 0.5 % | 3.83 % | 7.26 % | 15.35 % | 29.64 % | 44.0 % |
| 2.5 ATR | 13.004 % | 103.8732 | 0.1 % | 1.51 % | 3.83 % | 8.18 % | 21.42 % | 34.56 % |
| 3.0 ATR | 15.605 % | 100.7679 | 0.0 % | 0.7 % | 2.32 % | 5.25 % | 15.43 % | 26.56 % |
| 4.0 ATR | 20.806 % | 94.5571 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.9 % | 14.87 % |
| 6.0 ATR | 31.21 % | 82.1357 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.68 ATR | 0.77 ATR | 0.99 ATR | 1.19 ATR | 1.35 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.97 ATR | 1.27 ATR | 1.59 ATR | 1.80 ATR | 2.37 ATR | 3.08 ATR |
| **10 s.** | 0.54 ATR | 1.16 ATR | 1.32 ATR | 1.84 ATR | 2.28 ATR | 2.62 ATR | 3.64 ATR | 4.68 ATR |
| **20 s.** | 0.70 ATR | 1.68 ATR | 1.95 ATR | 2.60 ATR | 3.13 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.424–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.901 %, prix 114.7422), p(touche) 36.25 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.768–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.202 %, prix 113.1888), p(touche) 32.76 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (62.1 % des re-echantillons)
- **5 seance(s)** : plage utile 0.973–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.202 %, prix 113.1888), p(touche) 43.74 % (en stress 98.99 %)  ✅ optimum identifie (62.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.323–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.802 %, prix 110.0844), p(touche) 40.1 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.947–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.403 %, prix 106.9788), p(touche) 44.0 % (en stress 97.96 %)  ✅ optimum identifie (64.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : $0.015 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 20 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 53.4 | bear 33.7 | side 12.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 597.0 (= 5 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.329% → cible +5.617% / stop −2.808%, p_fill 71%, n_eff≈30.5) : P(cible|rempli) **7%** · **EV/risk +0.081** (×p_fill ; si rempli +0.32% du capital)
  - **swing** (entrée dip −2.918% → cible +6.027% / stop −5.358%, p_fill 51%, n_eff≈22.3) : P(cible|rempli) **60%** · **EV/risk +0.158** (×p_fill ; si rempli +1.65% du capital)
  - **deep** (entrée dip −4.51% → cible +23.395% / stop −11.698%, p_fill 39%, n_eff≈19.1) : P(cible|rempli) **8%** · **EV/risk +0.114** (×p_fill ; si rempli +3.38% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→84% · +2.0%→57% · +3.0%→38% · +5.0%→22% · +8.0%→10%
- Range intraday médian 5.24% (p90 9.08%) · excursion haute méd. +2.18% / basse méd. −2.24%
- Profil de vol intra : ouverture 3.95% vs midi 1.007% vs clôture 1.167% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; neutre — autocorr -0.028)_ ; drift intra méd. 0.571% ; recovery-V 34%
- **σ réalisé intraday** 3.51% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 42% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 123.065 (VA 122.039–123.635 ; dernier close 122.07)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 40% · rebond 80% · **stop −3.83%** sous le fill (sous le bruit) · cible +2.2% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. 0.01% · baisse 50% (gap-down >1% 32% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.94% (p90 −2.68%) · haut méd +1.04% · range méd 2.28%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −3.52%) · haut méd +1.41% · range méd 2.91%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −3.84%) · haut méd +1.64% · range méd 3.42%
- Excursion ouverture 60min (n=160) : bas méd −1.84% (p90 −3.9%) · haut méd +1.69% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.11 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (124/159) · gap 42% · délai 0.0min · rebond 61% (68/124) (MFE +1.5%)
   - −1.0% : fill 30min 61% · séance 69% (110/159) · gap 32% · délai 0.0min · rebond 64% (65/110) (MFE +1.69%)
   - −1.5% : fill 30min 51% · séance 61% (101/159) · gap 24% · délai 0.6min · rebond 65% (59/101) (MFE +1.44%)
   - −2.0% : fill 30min 39% · séance 51% (89/159) · gap 15% · délai 1.5min · rebond 71% (56/89) (MFE +1.45%)
   - −3.0% : fill 30min 28% · séance 40% (69/159) · gap 7% · délai 10.8min · rebond 80% (49/69) (MFE +2.2%)
   - −4.0% : fill 30min 16% · séance 27% (51/159) · gap 3% · délai 11.9min · rebond 72% (34/51) (MFE +2.29%)
   - −5.0% : fill 30min 8% · séance 16% (33/159) · gap 2% · délai 28.3min · rebond 67% (24/33) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.64% (p90 −2.62%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.65% (p90 −2.3%) → stop au-delà de −1.8% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −2.37%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=786 jambes) : jambe baissière méd −1.12% (p90 −2.73%) · ~9.7 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 95% (73/76) · rebond 52% (38/73)
      · −2.0% : fill 82% (63/76) · rebond 66% (38/63)
      · −3.0% : fill 72% (54/76) · rebond 79% (38/54)
      · −4.0% : fill 49% (41/76) · rebond 71% (29/41)
      · −5.0% : fill 29% (28/76) · rebond 62% (19/28)
   - **flat** (17 séances) :
      · −1.0% : fill 69% (12/17) · rebond 85% (8/12)
      · −2.0% : fill 33% (9/17) · rebond 61% (6/9)
      · −3.0% : fill 10% (4/17) · rebond 18% (1/4)
      · −4.0% : fill 10% (4/17) · rebond 18% (1/4)
      · −5.0% : fill 4% (2/17) · rebond 100% (2/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 42% (25/66) · rebond 84% (19/25)
      · −2.0% : fill 23% (17/66) · rebond 92% (12/17)
      · −3.0% : fill 13% (11/66) · rebond 97% (10/11)
      · −4.0% : fill 9% (6/66) · rebond 91% (4/6)
      · −5.0% : fill 4% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 67% si les 15 1res min sont vertes (75 cas) · 34% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **21min** → P(séance verte=clôture>ouverture) 70% si début vert vs 27% si rouge (base 49% · écart 43 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **70%** · continue >prix actuel 53% ; creux résiduel méd -1.6% (q20 -3.49%) → **SL/trailing à −3.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.96% / q75 +3.54% → **scale +1.96% / runner +3.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **27%** (continue à baisser 58%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.71%** (au-delà de la MAE q10 -3.71%), cible rebond +1.67% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.1% .. +4.84%] · haut q95 +5.45% · bas q05 -4.99%
   - 60min (n=160) : retour [-3.67% .. +5.05%] · haut q95 +6.42% · bas q05 -5.48%
   - 2h (n=160) : retour [-4.69% .. +6.51%] · haut q95 +7.7% · bas q05 -5.97%
   - 4h (n=160) : retour [-4.7% .. +7.65%] · haut q95 +8.51% · bas q05 -6.61%
   - 6h (n=160) : retour [-5.74% .. +7.98%] · haut q95 +8.8% · bas q05 -7.09%
   - session (n=160) : retour [-5.29% .. +8.24%] · haut q95 +8.88% · bas q05 -7.11%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 8.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 22% vs absente 2% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.5% / p90 2.5%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **77%** (reprise méd 20.0 min, n=51)
   - −1.0% → **65%** (reprise méd 38.77 min, n=23)
   - −1.5% → **47%** (reprise méd 41.95 min, n=13)
   - −2.0% → **14%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.5%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +6.95% (q75 +9.04% / q95 +12.46%), MFE méd +8.52% / q90 +13.87%
   - Échelle scale-out : +8.52% (33%) / +9.47% (33%) / +13.87% (34%)
- **DÉSARMER** : repli > **−2.5%** depuis le plus-haut = décay → P(retournement) **81%** (préavis méd 286.42 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.87% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.38%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.0  _(neutre)_
- **ADX** : 18.6  _(pas de tendance nette)_
- **MACD** : hist 0.32  _(pas de croisement recent)_
- **BB** : %B 0.66 · largeur 25.6%
- **ATR** : 6.21 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.013  _(neutre)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 47.2  _(transition)_
- **MA** : MA20 114.71 · MA50 104.25 · MA200 94.63  _(prix > MA20)_
- **Dist MA** : MA20 +4.1% · MA50 +14.5% · MA200 +26.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (874928 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
