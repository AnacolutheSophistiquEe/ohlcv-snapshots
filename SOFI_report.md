# SOFI

**Generated** : 2026-09-03T00:35:01.412081+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $17.83  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $17.83 (+2.5% vs entrée) · entrée $17.40 · stop $16.71 · T1 $17.71 · R/R 0.45  
> ↳ P(T1 av. stop) 26 % _(réel 5 s)_ · EV/risk -0.06 _(réel 5 s)_ (GBM 0.001) · ¼-Kelly 0.051 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +5.6 % ≠ (strike 18.0 − spot 17.83)/spot = +0.9 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.34–$17.46 (mid $17.40)
- Spot actuel : $17.83 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : $16.71 (stop swing_plan-based (-10.3%))
- Targets : T1 $17.71 · R/R 0.45 | T2 $18.01 · R/R 0.88 | T3 $18.32 · R/R 1.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.71


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.99 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.3 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **0.805 pt plus bas** dans le cas TYPIQUE (médiane), 0.805 au p90, **0.805 au pire**
   - perte réelle **11.105 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 10.3 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0006 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.268 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1507** [0.1034 ; 0.2096] _(largeur 10.6 pt, n_eff 173.1)_
   - swing : **0.3834** [0.3333 ; 0.4355] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3724** [0.3227 ; 0.4243] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-5.88 %** | CVaR **-8.45 %** | vol 3.87 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 6.08 % contre 3.53 % aujourd'hui, rapport 1.72)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8253** (β de hausse 1.7107, asymétrie 1.067) vs IWM — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.326× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 15.7486 sur grid_snapped (2.06 ATR, 11.698 %) — p(stop avant cible) 0.2727 [0.23 ; 0.32], R/R 3.519, perte reelle 11.698 % (gap inclus), CVaR 11.698 %, EV -0.1598 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.42 ATR (stop 4.525 %) — p(stop avant cible) 0.6628 [0.61 ; 0.71], R/R 5.827, perte reelle 7.064 % (gap inclus), EV -1.6755 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.663, borne haute 0.711 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.68 %) : P(cible) 0.1 % x 41.16 % + P(rien) 33.6 % x 8.84 % ne couvrent pas P(stop) 66.3 % x 7.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 7.437 %) — p(stop avant cible) 0.4542 [0.40 ; 0.51], R/R 4.483, perte reelle 9.182 % (gap inclus), EV -0.7942 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.79 %) : P(cible) 0.1 % x 41.16 % + P(rien) 54.5 % x 6.13 % ne couvrent pas P(stop) 45.4 % x 9.18 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.06 ATR (stop 12.65 %) — p(stop avant cible) 0.2296 [0.19 ; 0.28], R/R 3.254, perte reelle 12.65 % (gap inclus), EV 0.0655 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.65 % > budget 12.00 %
   - 🟢 support a 3.34 ATR (stop 19.008 %) — p(stop avant cible) 0.0621 [0.04 ; 0.09], R/R 2.166, perte reelle 19.008 % (gap inclus), EV 0.4645 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.01 % > budget 12.00 %
   - ⚪ grid_snapped a 0.42 ATR (stop 3.573 %) — p(stop avant cible) 0.7376 [0.69 ; 0.78], R/R 7.539, perte reelle 5.46 % (gap inclus), EV -1.654 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.738, borne haute 0.782 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.65 %) : P(cible) 0.1 % x 41.16 % + P(rien) 26.2 % x 8.96 % ne couvrent pas P(stop) 73.8 % x 5.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 6.198 %) — p(stop avant cible) 0.5304 [0.48 ; 0.58], R/R 5.183, perte reelle 7.942 % (gap inclus), EV -0.8596 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.530, borne haute 0.583 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 0.1 % x 41.16 % + P(rien) 46.9 % x 7.08 % ne couvrent pas P(stop) 53.0 % x 7.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.677 %) — p(stop avant cible) 0.3956 [0.35 ; 0.45], R/R 4.153, perte reelle 9.913 % (gap inclus), EV -0.6303 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 0.1 % x 41.16 % + P(rien) 60.3 % x 5.39 % ne couvrent pas P(stop) 39.6 % x 9.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.06 ATR (stop 11.698 %) — p(stop avant cible) 0.2727 [0.23 ; 0.32], R/R 3.519, perte reelle 11.698 % (gap inclus), EV -0.1598 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.1 % x 41.16 % + P(rien) 72.6 % x 4.12 % ne couvrent pas P(stop) 27.3 % x 11.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 13.635 %) — p(stop avant cible) 0.1874 [0.15 ; 0.23], R/R 3.019, perte reelle 13.635 % (gap inclus), EV 0.2445 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.64 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 14.874 %) — p(stop avant cible) 0.1345 [0.10 ; 0.17], R/R 2.768, perte reelle 14.874 % (gap inclus), EV 0.4137 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.87 % > budget 12.00 %
   - 🟢 grid_snapped a 3.34 ATR (stop 18.056 %) — p(stop avant cible) 0.0659 [0.04 ; 0.10], R/R 2.28, perte reelle 18.056 % (gap inclus), EV 0.489 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.06 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 19.833 %) — p(stop avant cible) 0.051 [0.03 ; 0.08], R/R 2.076, perte reelle 19.833 % (gap inclus), EV 0.4659 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.83 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 22.312 %) — p(stop avant cible) 0.0339 [0.02 ; 0.06], R/R 1.845, perte reelle 22.312 % (gap inclus), EV 0.4312 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.31 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 24.791 %) — p(stop avant cible) 0.02 [0.01 ; 0.04], R/R 1.66, perte reelle 24.791 % (gap inclus), EV 0.4743 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.79 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.27 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 1.51, perte reelle 27.27 % (gap inclus), EV 0.5685 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.27 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 29.749 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.384, perte reelle 29.749 % (gap inclus), EV 0.5723 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.75 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 32.228 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 1.277, perte reelle 32.228 % (gap inclus), EV 0.5825 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.23 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 34.707 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 1.186, perte reelle 34.707 % (gap inclus), EV 0.5833 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 37.186 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 1.107, perte reelle 37.186 % (gap inclus), EV 0.5827 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.19 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 39.665 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.038, perte reelle 39.665 % (gap inclus), EV 0.5911 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.66 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 17.835, ATR14 0.8843 (4.958 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.376 ATR = 1.864 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.248 % | 17.7908 | 92.85 % | 95.77 % | 96.97 % | 97.37 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.496 % | 17.7466 | 85.2 % | 89.52 % | 91.93 % | 93.23 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.744 % | 17.7024 | 79.15 % | 84.98 % | 88.19 % | 90.39 % | 92.78 % | 94.76 % |
| 0.2 ATR | 0.992 % | 17.6581 | 71.7 % | 79.74 % | 83.55 % | 86.86 % | 90.45 % | 93.22 % |
| 0.25 ATR | 1.24 % | 17.6139 | 66.36 % | 75.2 % | 80.12 % | 84.13 % | 88.82 % | 91.79 % |
| 0.35 ATR | 1.735 % | 17.5255 | 52.57 % | 65.52 % | 72.15 % | 78.26 % | 85.26 % | 88.5 % |
| 0.5 ATR | 2.479 % | 17.3929 | 37.76 % | 53.53 % | 61.65 % | 68.96 % | 79.17 % | 84.29 % |
| 0.75 ATR | 3.719 % | 17.1718 | 20.24 % | 36.9 % | 47.02 % | 56.93 % | 69.61 % | 77.41 % |
| 1.0 ATR | 4.958 % | 16.9507 | 8.86 % | 24.4 % | 33.91 % | 44.99 % | 59.25 % | 68.58 % |
| 1.25 ATR | 6.198 % | 16.7296 | 4.13 % | 14.92 % | 23.71 % | 35.49 % | 49.9 % | 61.91 % |
| 1.5 ATR | 7.437 % | 16.5086 | 2.01 % | 9.48 % | 16.75 % | 27.5 % | 41.77 % | 55.34 % |
| 2.0 ATR | 9.916 % | 16.0664 | 0.7 % | 4.33 % | 8.38 % | 15.37 % | 28.96 % | 44.97 % |
| 2.5 ATR | 12.395 % | 15.6243 | 0.3 % | 1.92 % | 3.83 % | 9.5 % | 19.61 % | 35.63 % |
| 3.0 ATR | 14.874 % | 15.1821 | 0.1 % | 0.91 % | 2.83 % | 6.07 % | 14.02 % | 28.23 % |
| 4.0 ATR | 19.833 % | 14.2979 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.52 % | 14.78 % |
| 6.0 ATR | 29.749 % | 12.5293 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.94 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.90 ATR | 2.37 ATR |
| **5 s.** | 0.40 ATR | 0.90 ATR | 1.00 ATR | 1.33 ATR | 1.60 ATR | 1.81 ATR | 2.46 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.25 ATR | 1.40 ATR | 1.84 ATR | 2.21 ATR | 2.48 ATR | 3.62 ATR | 4.76 ATR |
| **20 s.** | 0.82 ATR | 1.76 ATR | 2.00 ATR | 2.68 ATR | 3.24 ATR | 3.61 ATR | 4.82 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.427–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.479 %, prix 17.3929), p(touche) 37.76 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.628–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.719 %, prix 17.1717), p(touche) 36.9 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.789–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.958 %, prix 16.9507), p(touche) 33.91 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.0–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.958 %, prix 16.9507), p(touche) 44.99 % (en stress 97.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.401–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.437 %, prix 16.5086), p(touche) 41.77 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.999–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.916 %, prix 16.0665), p(touche) 44.97 % (en stress 98.98 %)  ✅ optimum identifie (73.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.001 | EV/share : $0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 26 % | T3 12 %
- Kelly (position) : f* 0.202 | ¼-Kelly 0.051 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 64.3 | bear 9.8 | side 25.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.428% → cible +1.753% / stop −4.0%, p_fill 40%, n_eff≈16.9) : P(cible|rempli) **26%** · **EV/risk -0.060** (×p_fill ; si rempli -0.60% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→69% · +2.0%→49% · +3.0%→36% · +5.0%→12% · +8.0%→1%
- Range intraday médian 4.39% (p90 7.54%) · excursion haute méd. +1.83% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.045% vs midi 0.853% vs clôture 0.992% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑2%/↓0% ; spike-down 63% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.147 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -0.255% ; recovery-V 26%
- **σ réalisé intraday** 2.625% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 60% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 17.1559 (VA 17.0219–17.3066 ; dernier close 17.06)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 66% · **stop −3.09%** sous le fill (sous le bruit) · cible +1.78% · R/R 0.58 (high win-rate)
- Gaps overnight (n=159) : méd. 0.24% · baisse 44% (gap-down >1% 24% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.76%) · haut méd +0.71% · range méd 1.64%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −2.75%) · haut méd +0.99% · range méd 2.29%
- Excursion ouverture 30min (n=160) : bas méd −1.12% (p90 −3.2%) · haut méd +1.11% · range méd 2.66%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.7%) · haut méd +1.3% · range méd 3.29%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.05 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (120/159) · gap 31% · délai 0.0min · rebond 51% (63/120) (MFE +1.13%)
   - −1.0% : fill 30min 53% · séance 66% (109/159) · gap 24% · délai 1.4min · rebond 55% (63/109) (MFE +1.01%)
   - −1.5% : fill 30min 42% · séance 62% (100/159) · gap 20% · délai 9.8min · rebond 64% (66/100) (MFE +1.39%)
   - −2.0% : fill 30min 35% · séance 48% (79/159) · gap 10% · délai 9.8min · rebond 66% (54/79) (MFE +1.78%)
   - −3.0% : fill 30min 12% · séance 34% (57/159) · gap 3% · délai 50.3min · rebond 54% (37/57) (MFE +1.08%)
   - −4.0% : fill 30min 8% · séance 18% (36/159) · gap 2% · délai 48.8min · rebond 52% (23/36) (MFE +1.2%)
   - −5.0% : fill 30min 3% · séance 10% (20/159) · gap 2% · délai 192.2min · rebond 44% (10/20) (MFE +0.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.91%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −2.07%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.46%) → stop au-delà de −1.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=673 jambes) : jambe baissière méd −1.08% (p90 −2.77%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 98% (65/66) · rebond 54% (39/65)
      · −2.0% : fill 85% (55/66) · rebond 71% (39/55)
      · −3.0% : fill 66% (42/66) · rebond 57% (28/42)
      · −4.0% : fill 37% (28/66) · rebond 60% (20/28)
      · −5.0% : fill 22% (16/66) · rebond 54% (9/16)
   - **flat** (21 séances) :
      · −1.0% : fill 66% (12/21) · rebond 42% (5/12)
      · −2.0% : fill 45% (7/21) · rebond 55% (4/7)
      · −3.0% : fill 35% (6/21) · rebond 38% (3/6)
      · −4.0% : fill 22% (3/21) · rebond 30% (1/3)
      · −5.0% : fill 13% (1/21) · rebond 0% (0/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 42% (32/72) · rebond 62% (19/32)
      · −2.0% : fill 21% (17/72) · rebond 58% (11/17)
      · −3.0% : fill 11% (9/72) · rebond 60% (6/9)
      · −4.0% : fill 3% (5/72) · rebond 22% (2/5)
      · −5.0% : fill 1% (3/72) · rebond 44% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 61% si les 15 1res min sont vertes (74 cas) · 25% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **52min** → P(séance verte=clôture>ouverture) 79% si début vert vs 12% si rouge (base 41% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **79%** · continue >prix actuel 56% ; creux résiduel méd -1.09% (q20 -2.26%) → **SL/trailing à −2.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.38% / q75 +2.95% → **scale +1.38% / runner +2.95%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **12%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.24%** (au-delà de la MAE q10 -3.24%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.89% .. +3.71%] · haut q95 +4.01% · bas q05 -3.39%
   - 60min (n=160) : retour [-3.13% .. +3.69%] · haut q95 +4.52% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +3.9%] · haut q95 +5.22% · bas q05 -4.62%
   - 4h (n=160) : retour [-4.48% .. +4.59%] · haut q95 +5.68% · bas q05 -5.14%
   - 6h (n=160) : retour [-4.76% .. +4.07%] · haut q95 +5.7% · bas q05 -5.75%
   - session (n=160) : retour [-4.69% .. +5.05%] · haut q95 +5.7% · bas q05 -5.97%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.2  _(neutre)_
- **ADX** : 14.3  _(pas de tendance nette)_
- **MACD** : hist -0.125  _(bearish_recent)_
- **BB** : %B 0.3 · largeur 11.0%
- **ATR** : 0.88 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.148  _(distribution)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 59.5  _(transition)_
- **MA** : MA20 18.23 · MA50 17.84 · MA200 20.06  _(prix < MA20)_
- **Dist MA** : MA20 -2.2% · MA50 -0.0% · MA200 -11.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (486386 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
