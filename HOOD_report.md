# HOOD

**Generated** : 2026-09-21T00:45:51.893154+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $119.82  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $119.82 (+1.1% vs entrée) · entrée $118.49 · stop $114.94 · T1 $122.37 · R/R 1.09  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.0 _(réel 5 s)_ (GBM 0.044) · ¼-Kelly 0.02 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $117.71–$119.27 (mid $118.49)
- Spot actuel : $119.82 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : $114.94 (stop swing_plan-based (-11.98%))
- Targets : T1 $122.37 · R/R 1.09 | T2 $126.25 · R/R 2.19 | T3 $130.14 · R/R 3.28
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $114.94


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.98 %)** : le gap seul le franchit 0.159 % des séances (2 fois sur 1254).
   - exécution **3.975 pt plus bas** dans le cas TYPIQUE (médiane), 5.439 au p90, **5.805 au pire**
   - perte réelle **15.955 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 11.98 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0063 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.415 % | p01 -7.299 % | pire -17.785 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3185** [0.2525 ; 0.3905] _(largeur 13.8 pt, n_eff 173.1)_
   - swing : **0.2179** [0.1768 ; 0.2637] _(largeur 8.7 pt, n_eff 345.7)_
   - deep : **0.3655** [0.316 ; 0.4172] _(largeur 10.1 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.3 pt), swing (33.2 pt), deep (38.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.41 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 1.92 % contre 4.72 % aujourd'hui, rapport 0.41)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.53 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.012 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7649** (β de hausse 1.5962, asymétrie 1.1057) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.472× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 107.1974 sur atr_grid (1.75 ATR, 10.535 %) — p(stop avant cible) 0.3493 [0.30 ; 0.40], R/R 1.909, perte reelle 13.192 % (gap inclus), CVaR 10.546 %, EV 1.6096 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 22 des 22 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 42.1 % de la queue et il ne reste que -112.43 EUR a partager. Prix du risque -0.036 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.84 ATR (stop 8.343 %) — p(stop avant cible) 0.436 [0.38 ; 0.49], R/R 2.232, perte reelle 11.287 % (gap inclus), EV 1.0179 % — **REFUSE**
      - refuse : cible atteinte seulement 9.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 support a 2.65 ATR (stop 19.279 %) — p(stop avant cible) 0.0961 [0.07 ; 0.13], R/R 1.307, perte reelle 19.279 % (gap inclus), EV 2.9169 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.28 % > budget 12.00 %
      - ⚠ support DETECTE a 0.74 ATR du spot — compartiment <1, mesure a 50.1 % de casse (IC clusterise [0.466 ; 0.537] sur 1177 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 3.93 ATR (stop 26.99 %) — p(stop avant cible) 0.0296 [0.02 ; 0.05], R/R 0.933, perte reelle 26.99 % (gap inclus), EV 2.9364 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.99 % > budget 12.00 %
   - 🟢 support a 7.81 ATR (stop 50.296 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.501, perte reelle 50.296 % (gap inclus), EV 3.1035 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.30 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.505 %) — p(stop avant cible) 0.8996 [0.86 ; 0.93], R/R 7.724, perte reelle 3.261 % (gap inclus), EV -1.3354 % — **REFUSE**
      - refuse : cible atteinte seulement 3.5 % du temps (< 15 %) meme a 10 seances : le R/R de 7.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.900, borne haute 0.928 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.34 %) : P(cible) 3.5 % x 25.19 % + P(rien) 6.6 % x 11.02 % ne couvrent pas P(stop) 90.0 % x 3.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.01 %) — p(stop avant cible) 0.7607 [0.71 ; 0.80], R/R 4.994, perte reelle 5.044 % (gap inclus), EV -0.3513 % — **REFUSE**
      - refuse : cible atteinte seulement 6.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.761, borne haute 0.803 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 6.2 % x 25.19 % + P(rien) 17.8 % x 10.87 % ne couvrent pas P(stop) 76.1 % x 5.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.84 ATR (stop 6.844 %) — p(stop avant cible) 0.528 [0.48 ; 0.58], R/R 2.461, perte reelle 10.236 % (gap inclus), EV 0.1456 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.528, borne haute 0.580 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 10.535 %) — p(stop avant cible) 0.3493 [0.30 ; 0.40], R/R 1.909, perte reelle 13.192 % (gap inclus), EV 1.6096 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 12.04 %) — p(stop avant cible) 0.28 [0.23 ; 0.33], R/R 1.579, perte reelle 15.955 % (gap inclus), EV 1.767 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.05 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 13.545 %) — p(stop avant cible) 0.2384 [0.20 ; 0.29], R/R 1.579, perte reelle 15.955 % (gap inclus), EV 2.2105 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.55 % > budget 12.00 %
   - 🔴 grid_snapped a 2.65 ATR (stop 17.78 %) — p(stop avant cible) 0.1216 [0.09 ; 0.16], R/R 1.416, perte reelle 17.785 % (gap inclus), EV 2.9143 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.78 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 21.069 %) — p(stop avant cible) 0.0766 [0.05 ; 0.11], R/R 1.196, perte reelle 21.069 % (gap inclus), EV 2.8954 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.07 % > budget 12.00 %
   - 🟢 grid_snapped a 3.93 ATR (stop 25.491 %) — p(stop avant cible) 0.034 [0.02 ; 0.06], R/R 0.988, perte reelle 25.491 % (gap inclus), EV 2.9678 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.49 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 30.099 %) — p(stop avant cible) 0.0234 [0.01 ; 0.04], R/R 0.837, perte reelle 30.099 % (gap inclus), EV 2.9406 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.10 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 33.109 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 0.761, perte reelle 33.109 % (gap inclus), EV 3.0374 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.11 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 36.119 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.697, perte reelle 36.119 % (gap inclus), EV 3.0856 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.12 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 39.129 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.644, perte reelle 39.129 % (gap inclus), EV 3.0918 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.13 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 42.139 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.598, perte reelle 42.139 % (gap inclus), EV 3.1035 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.14 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 45.149 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.558, perte reelle 45.149 % (gap inclus), EV 3.1035 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.15 % > budget 12.00 %
   - 🟢 grid_snapped a 7.81 ATR (stop 48.797 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.516, perte reelle 48.797 % (gap inclus), EV 3.1035 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.80 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 119.82, ATR14 7.2129 (6.02 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.375 ATR = 2.257 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.301 % | 119.4594 | 92.96 % | 95.07 % | 95.97 % | 96.46 % | 97.06 % | 98.05 % |
| 0.1 ATR | 0.602 % | 119.0987 | 85.51 % | 90.33 % | 92.04 % | 93.54 % | 94.62 % | 96.41 % |
| 0.15 ATR | 0.903 % | 118.7381 | 77.57 % | 85.1 % | 87.8 % | 90.1 % | 92.49 % | 95.08 % |
| 0.2 ATR | 1.204 % | 118.3774 | 71.53 % | 79.96 % | 83.57 % | 86.77 % | 90.25 % | 93.23 % |
| 0.25 ATR | 1.505 % | 118.0168 | 64.59 % | 74.22 % | 78.93 % | 83.23 % | 87.61 % | 90.87 % |
| 0.35 ATR | 2.107 % | 117.2955 | 52.52 % | 65.26 % | 71.77 % | 77.47 % | 83.35 % | 87.9 % |
| 0.5 ATR | 3.01 % | 116.2135 | 37.22 % | 53.37 % | 60.99 % | 68.08 % | 76.35 % | 82.46 % |
| 0.75 ATR | 4.515 % | 114.4103 | 19.62 % | 36.25 % | 45.87 % | 55.45 % | 65.48 % | 73.23 % |
| 1.0 ATR | 6.02 % | 112.6071 | 9.26 % | 23.06 % | 32.66 % | 43.64 % | 54.72 % | 65.64 % |
| 1.25 ATR | 7.525 % | 110.8038 | 4.83 % | 14.6 % | 22.38 % | 33.33 % | 46.6 % | 59.08 % |
| 1.5 ATR | 9.03 % | 109.0006 | 2.41 % | 9.87 % | 16.33 % | 26.87 % | 39.59 % | 53.44 % |
| 2.0 ATR | 12.04 % | 105.3941 | 0.5 % | 3.83 % | 7.26 % | 15.35 % | 29.34 % | 44.0 % |
| 2.5 ATR | 15.05 % | 101.7877 | 0.1 % | 1.51 % | 3.83 % | 8.18 % | 21.12 % | 34.56 % |
| 3.0 ATR | 18.059 % | 98.1812 | 0.0 % | 0.7 % | 2.32 % | 5.25 % | 15.33 % | 26.56 % |
| 4.0 ATR | 24.079 % | 90.9683 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.9 % | 14.87 % |
| 6.0 ATR | 36.119 % | 76.5424 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.77 ATR | 0.99 ATR | 1.19 ATR | 1.35 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.26 ATR | 1.58 ATR | 1.80 ATR | 2.37 ATR | 3.08 ATR |
| **10 s.** | 0.53 ATR | 1.15 ATR | 1.31 ATR | 1.82 ATR | 2.26 ATR | 2.60 ATR | 3.63 ATR | 4.68 ATR |
| **20 s.** | 0.70 ATR | 1.68 ATR | 1.95 ATR | 2.60 ATR | 3.13 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.424–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.622–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.515 %, prix 114.4101), p(touche) 36.25 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.766–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.02 %, prix 112.6068), p(touche) 32.66 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (63.1 % des re-echantillons)
- **5 seance(s)** : plage utile 0.971–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.02 %, prix 112.6068), p(touche) 43.64 % (en stress 98.99 %)  ✅ optimum identifie (60.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.307–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.03 %, prix 109.0003), p(touche) 39.59 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.947–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.04 %, prix 105.3937), p(touche) 44.0 % (en stress 97.96 %)  ✅ optimum identifie (64.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.044 | EV/share : $0.156 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 22 % | T3 22 %
- Kelly (position) : f* 0.079 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 21.3 | bear 47.2 | side 31.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 479.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.113% → cible +3.276% / stop −3.0%, p_fill 71%, n_eff≈30.8) : P(cible|rempli) **20%** · **EV/risk -0.000** (×p_fill ; si rempli -0.00% du capital)
  - **swing** (entrée dip −2.444% → cible +19.55% / stop −9.775%, p_fill 59%, n_eff≈24.0) : P(cible|rempli) **10%** · **EV/risk +0.234** (×p_fill ; si rempli +3.90% du capital)
  - **deep** (entrée dip −3.77% → cible +10.359% / stop −9.384%, p_fill 55%, n_eff≈23.3) : P(cible|rempli) **58%** · **EV/risk +0.162** (×p_fill ; si rempli +2.77% du capital)
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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 62.5  _(momentum haussier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist -0.277  _(bearish_recent)_
- **BB** : %B 0.84 · largeur 22.4%
- **ATR** : 7.21 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.128  _(accumulation)_
- **Vol ratio** : 1.59  _(volume au-dessus de la moyenne)_
- **Choppiness** : 53.6  _(transition)_
- **MA** : MA20 111.29 · MA50 103.17 · MA200 94.9  _(prix > MA20)_
- **Dist MA** : MA20 +7.7% · MA50 +16.1% · MA200 +26.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (814938 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
